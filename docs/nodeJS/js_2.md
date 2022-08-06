---
layout: default
title: (JS) className vs classList
parent: Node.JS
tags:
    - javascript
    - className
    - classList

comments: true
---

작성완료
{: .label .label-green }

## [Javascript] className 과 classList 

---

## Table of contents
{: .no_toc .text-delta}

1. TOC
{:toc}

---

## className

- 특정 element의 클래스 속성 값을 가져오거나 설정할 수 있습니다.

```js
<button>sample Btn</button>
```

sample Btn의 클래스의 속성값을 설정하거나 바꿀 수 있습니다.

```js
let btn = document.querySelector("button :first-child")

btn.className = "btn btn2"
```


<br><br>

## classList

- 공백문자를 기준으로 분리된 여러개의 클래스 요소들의 집합이자, 동적인 DomTokenList 를 리턴합니다.

```js
<button class="btn btn2">sample Btn</button>
```

위의 예시의 버튼 태그가 갖는 클래스는 2개 이며, ` ` 문자로 구분하여 `btn` 과 `btn2`를 가집니다.


![]( {{ site.photo | absolute_url}}/nodejs/js_1/js1.png)

<br>

- 클래스를 추가(add) 하거나 제거(remove) 할 수 있습니다.


<br>

- `classList.toggle` 을 이용하여 해당 클래스를 추가 제거할 수 있습니다.

[Click me if you want to show sample code](https://codesandbox.io/s/vigilant-lehmann-4yrbbj?file=/src/sample_js01.js){: .btn .btn-green .mr-4}

```js
const btn = document.querySelector(".btn");

let btnClassList = btn.classList;

function clickHandler() {
  if (btnClassList.contains("btn")) {
    alert("클래스 'btn'이 들어있습니다.");
    // <button>에 class 'btn'이 있습니다.
  } else {
    alert("No class-tag");
    // <button>에 class 'btn'이 없습니다.
  }
  console.log(btnClassList); 

  btnClassList.toggle("btn");
  // 'btn'이 있으면, 토글함수는  btnClassList.remove("btn")으로 해당 클래스요소를 제거하여 처리합니다.
  // 반대로 'btn'이 없다면, 토글함수는 btnClassList.add("btn")으로 해당 클래스 요소를 추가하여 처리합니다.
}
```

---

[참고자료]

- [mdn web docs - Element.classList](https://developer.mozilla.org/en-US/docs/Web/API/Element/classList)
- [mdn web docs - Element.className](https://developer.mozilla.org/en-US/docs/Web/API/Element/className)
- [stackoverflow - className vs classList](https://stackoverflow.com/questions/69361432/difference-between-classname-and-classlist)
