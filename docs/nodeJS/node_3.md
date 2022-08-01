---
layout: default
title: npm 과 yarn 패키지
parent: Node.JS
comments: true
---

작성중
{: .label .label-yellow }

* 수강강좌: 한번에 끝내는 Node.js 웹프로그래밍 초격차 패키지 온라인

---

## Table of contents
{: .no_toc .text-delta}

1. TOC
{:toc}

---

## npm
{: .d-inline-block }

npm(Node Package Manager)

### npm 설치

```shell
$ npm install decamelize
```

### package.json vs package-lock.json


```json
{
    "dependencies":{
        "decamelize": "^5.0.0"
    }
}
```

`^` 기호들을 사용해서 비슷한 버전을 추적하고 확인한다. package.json 에서 설정된 node 버젼과 실제 로컬 컴퓨터에서 설치된 Node 버젼은 서로 일치하지 않다.


package-lock.json 은 설치된 패키지의 실제 정보들을 담고있다. 협업할때 패키지의 버젼을 일치시켜야하며, 푸시할때 package-lock.json 도 같이 푸시해야한다.



