---
layout: default
title: module 과 require
parent: Node.JS
---

작성중
{: .label .label-yellow }

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

exports 특정 키워드로 명시된 객체에 정의된 함수나 객체를 정의할 수 있다.

<br>

_Variables local to the module will be private, because the module is wrapped in a function by Node.js._
{: .fs-3 }

_In this example, the variable `PI` is private to `circle.js`_
{: .fs-3 }

함수모듈에 있는 로컬변수는 private 타입을 갖는다.

<br>


---
