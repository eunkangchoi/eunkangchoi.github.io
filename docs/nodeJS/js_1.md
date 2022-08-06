---
layout: default
title: (JS)
parent: Node.JS
tags:
    - javascript
    - document
    - window

comments: true
---

작성완료
{: .label .label-green }

---

## Table of contents
{: .no_toc .text-delta}

1. TOC
{:toc}

---

## window 가 document 보다 더 넓은 개념입니다.


`window` 객체는 브라우저를 열 때 맨처음에 나옵니다. javascrpit 객체의 핵심 객체들의 뿌리입니다.

`window.document`(`document`) 는 `DOM객체`의 최상단을 의미합니다. 렌더링을 위한 객체입니다.

`window.screen`(`screen`)는 display의 화면 폭(width)과 높이(height)와 같은 물리적인 화면에 대해 다룹니다.

- `alert()`, `confirm()`, `resize()` 등 함수나, javascript 시작할때 자주사용하는 함수인 `console.log`의 `console`도 Window 객체에 내장되어 있습니다.


## DOM 객체는 무엇인가요?

문서 객체 모델(DOM: Document Object Model) 은 HTML, XML 문서의 프로그래밍 인터페이스 입니다.

DOM은 **문서의 구조화된 표현을 제공**하며 **프로그래밍 언어가 DOM 구조에 접근할 수 있는 방법을 제공하여 문서구조, 스타일, 내용등을 변경**할 수 있도록 합니다.

DOM은 노드(node)와 objects 로 문서를 표현합니다. 둘의 공통점은 웹페이지를 스크립트 또는 프로그래밍 언어들에서 사용될 수 있도록 연결시켜주는 역할을 합니다.


웹페이지는 일종의 문서(document) 입니다.
문서는 웹브라우저를 통해 그 내용이 해석되어 웹브라우저 화면에 나타나거나 HTML 소스 자체를 나타나기도 합니다.


자바스크립트와 같은 스크립팅 언어를 이용하여 DOM을 수정할 수 있습니다.

---

[참고자료]

- [stackoverflow - What is the difference between window, screen, and document in javascript?](https://stackoverflow.com/questions/9895202/what-is-the-difference-between-window-screen-and-document-in-javascript)


- [자바스크립트 Window / Document 무슨차이일까?](https://nookpi.tistory.com/56)

- [MDN - DOM 객체](https://developer.mozilla.org/ko/docs/Web/API/Document_Object_Model/Introduction)