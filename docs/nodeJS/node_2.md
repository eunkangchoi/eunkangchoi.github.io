---
layout: default
title: module 과 require
parent: Node.JS
---

작성중
{: .label .label-green }

* 수강강좌: 한번에 끝내는 Node.js 웹프로그래밍 초격차 패키지 온라인

* 공식문서를 읽는 습관을 들이자! 어렵겠지만, 최신정보도 공식문서로부터 얻을 수 있기 때문이다!

---

## Table of contents
{: .no_toc .text-delta}

1. TOC
{:toc}

---

## require 와 module, module의 resolution
{: .d-inline-block }

* 참고문서
- Node.js version: v18.6.0
- [Node.js Documents - Modules: CommonJS modules ](https://nodejs.org/api/modules.html#modules-commonjs-modules)
- [Node.js Documents - Modules ECMAScript modules](https://nodejs.org/api/esm.html#modules-ecmascript-modules)
- [Node.js Documents - require](https://nodejs.org/api/modules.html#requireid)

---

### Node.js에서의 module
{: .no-toc .text-delta }

Node.js 에서의 모듈은 파일이다.
파일의 상대경로 혹은 절대경로를 정의하여 불러온다. 해당 모듈안에 있는 변수와 상수 함수를 불러올 수 있다.


Node.js에서는 CommonJS 모듈과 ECMA-Script 모듈로 나눠져있다. 그러나 여기 강의에서는 ECMA-Script 모듈이 아닌 CommonJS 모듈을 중심으로 소개하고있다.

<br>

ECMA-Script의 경우에는 Node.js 공식문서를 확인하면된다.
그래도 CommonJS에서의 모듈과 ECMA-Script 모듈에 대한 간단한 차이점을 정리해본다.

<br>

- CommonJS module 과 ECMA-Script module의 차이점
{: .no-toc .fs-5 .fw-300 }

|| CommonJS    | ECMA-Script  |
|:--------:|:-------------|:------------------|
|모듈단위 파일 확장자      | `*.js`       | `*.mjs` |
|모듈을 불러오는 함수 및 시스템예약어| **require()** | **import**, **export**   |

<br>


공식문서를 확인해보면
CommonJS에서는 `require(id)` 함수를 통해서 모듈을 불러올 수 있다. 

require함수의 인자 `id`는 해당 모듈의 경로(상대경로 혹은 절대 경로)를 의미한다.

<br>

반면에 ECMAScript에서는 `export` 시스템 예약어로 다른모듈로부터 불러올 모듈을 정의하며 , `import 이름 from 경로` 형태로 모듈을 불러온다.  

<br>

##### ECMAScript Module
{: .no_toc .fs-5 }

- ECMAScript Modules 정의 - Node.js 공식문서에서 발췌
> ECMAScript modules are the official standard format to package Javascript code for reuse. Modules are defined using a variety of `import` and `export` statements.

<br><br>

ECMAScript Module 예시 1
{: .no-toc .fs-5 .fw-300 }

- addTwo.mjs
  
```js
function addTwo(num) {
    return num + 2;
}

// eslint-disable-next-line import/prefer-default-export
export { addTwo };
```

<br>

- main.mjs

```js
// eslint-disable-next-line import/extensions
import {addTwo} from './addTwo.mjs'

const twoAddTwo = addTwo(2);
console.log(twoAddTwo); // 4
```

<br><br>

ECMAScript Module 예시 2
{: .no_toc .fs-5 .fw-300 }

- animals.mjs

```js
const animals = ['dog', 'cat']
export default animals
```

<br>

- main.mjs

```js
// eslint-disable-next-line import/extensions
import animals from './animals.mjs'

console.log(animals) // ['dog', 'cat']
```

<br><br>

##### CommonJS Module
{: .no_toc .fs-5 }

- `require()` 함수로 모듈을 불러온다.
  - 프로젝트 내 모듈은 상대경로로 불러올 수 있다.
  - **node에 내장된 모듈**(node standard library에 있는 모듈)은 절대경로를 지정해서 불러올 수 있다.
  - 해당 모듈이 `node_modules` 디렉토리 안에 있거나, `node_modules` 내부의 폴더안에 있다면 절대경로로 지정해서 불러올 수 있다.
  - 절대경로(이름)을 지정하면, module.paths의 경로들을 순서대로 검사하여 해당 모듈이 있으면, 가장 먼저 발견한 모듈을 불러온다.


- 모듈 안에 정의된 변수는 `private` 타입을 갖는다.


- 같은 모듈을 여러번 불러와도 딱 한번만 호출된다. 즉 불러오는 모듈은 모두 같은 대상이다.(동일한 객체이다)

<br>

CommonJS Module 예시1
{: .fs-5 .fw-300 }

- circle.js

```js
const { PI } = Math;
exports.area = (r) => PI * r ** 2;
exports.circumference = (r) => 2 * PI * r;
```


<br>

- main.js

```js
const circle = require('../circle')

console.log(`반지름이 4인 원의 넓이: ${circle.area(4)}`)
// 반지름이 4인 원의 넓이: 50.26548245743669

console.log(`반지름이 4인 원의 둘레: ${circle.circumference(4)}`)
// 반지름이 4인 원의 둘레: 25.132741228718345

```

<br>

_Functions and objects are added to the root of a module by specifying additional properties on the special `exports` object._
{: .fs-3 }

**exports 특정 키워드로 명시된 객체에 정의된 함수나 객체를 정의할 수 있다.**

<br>

_Variables local to the module will be private, because the module is wrapped in a function by Node.js._
{: .fs-3 }

_In this example, the variable `PI` is private to `circle.js`_
{: .fs-3 }

**함수모듈에 있는 로컬변수는 private 타입을 갖는다.**

<br>

CommonJS Module 예시 2-1
{: .fs-5 .fw-300 }

- animals.js

```js
const animals = ['dog', 'cat']
console.log('::: animals.js loaded')
module.exports = animals
```

<br>

- main.js

```js
// 같은 경로에 있는 animals.js 를 불러온다.
const animalsA = require('./animals');
const animalsB = require('./animals');
const animalsC = require('./animals');

console.log(animalsA === animalsB) // true
console.log(animalsA === animalsC) // true
console.log(animalsC === animalsB) // true
```



- console.log result

```md
::: animals.js loaded
true
true
true
```

animalsA, animalsB, animalsC는 모두 같은 대상을 가리킨다.

<br>

CommonJS Module 예시 2-2
{: .fs-5 .fw-300}

animals.js 처럼 사용자가 직접 만든 모듈을 불러오는게 아닌
`http`와 같은 **node에 내장 되어있는 모듈**을 불러온다면 **해당 모듈이름(절대경로)**을 불러오면된다.

```js
/* eslint-disable */
const http = require('http');
```


<br>

CommonJS Module 예시 2-3
{: .fs-5 .fw-300 }

예시 2-1의 animals.js 모듈을 `node_modules` 디렉토리 안에 복사했다고 가정하자. 

또는 animals.js 모듈을 `node_modules` 디렉토리 안에 새로운폴더 `tmp`를 만들어서 복사했다고 하자.(즉, 경로가 node_modules/tmp 인 경우이다)


`node_modules` 디렉토리 안에 있는 모듈을 불러올 때는 위예시와 마찬가지로 **해당 모듈 이름(절대경로)**를 불러오면된다.

- main.js

```js
/* eslint-disable */
// file-path: node_modules/animals.js
const mAnimals = require('animals')
console.log(mAnimals)

// file-path: node_modules/tmp/animals.js
const tAnimals = require('tmp/animals')
console.log(tAnimals)
```



CommonJS Module 예시 3
{: .fs-5 .fw-300 }

- main.js

```js
const {path, paths, filename} = module
console.log({ path, paths, filename })
```


- console.log result

```md
{
  path: '/Users/seokangchoi/Documents/ek_projects/f01_simple_rest_api_nodejs/practices/common_js',
  paths: [
    '/Users/seokangchoi/Documents/ek_projects/f01_simple_rest_api_nodejs/practices/common_js/node_modules',
    '/Users/seokangchoi/Documents/ek_projects/f01_simple_rest_api_nodejs/practices/node_modules',
    '/Users/seokangchoi/Documents/ek_projects/f01_simple_rest_api_nodejs/node_modules',
    '/Users/seokangchoi/Documents/ek_projects/node_modules',
    '/Users/seokangchoi/Documents/node_modules',
    '/Users/seokangchoi/node_modules',
    '/Users/node_modules',
    '/node_modules'
  ],
  filename: '/Users/seokangchoi/Documents/ek_projects/f01_simple_rest_api_nodejs/practices/common_js/main.js'
}
```

<br>

- `path` 는 해당모듈이 속한 절대경로를 의미한다. (단, 해당모듈 이름은 제외된다.)


- `paths` 는 해당모듈을 탐색하여 거친 경로들을 의미한다. 루트 디렉토리(/)를 시작점으로 하여 해당모듈이 포함한 위치까지 구석구석 찾는다. 여기서 `node_modules` 는 위의 예시 2-3 과 node에 설치된 모듈들을 저장한 디렉토리인 node_modules 와 다르게 **경로의 끝**을 의미한다. 

Node.js will not append `node_modules` to a path already ending in `node_modules`


- `filename` 은 해당모듈명까지 포함된 절대경로이다.

- 참고자료 링크: [Loading from node_modules folders](https://nodejs.org/api/modules.html#loading-from-node_modules-folders)

---
