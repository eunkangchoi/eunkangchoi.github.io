---
layout: default
title: Node.JS 시작하기
parent: Node.JS
tags:
    - Node.js

comments: true
---

작성완료
{: .label .label-green }

* 수강강좌: 한번에 끝내는 Node.js 웹프로그래밍 초격차 패키지 온라인

코드는 도구와 패키지들을 잘활용해서 내코드가 올바른지, 개발환경을 더 잘꾸려놓는게 중요하다.
실수를 하더라도 빨리 알아챌 수 있다. 미연의 실수를 방지하기위해서 자신의 툴셋을 키워놓고
자신의 툴셋에서 무엇이 부족하고, 어느부분을 보완해야될 지를 파악하고
개발환경을 더 잘 꾸릴 수 있는 위한 고민을 하며 신경쓰는게 좋다.
코드는 도구를 잘 쓸수록 더 좋다.
{: .fs-3 .fw-300 }

---

1. TOC
{:toc}


## 1) Node.js 특징과 강점과 약점
### 1.1 (강점) 비동기성
이벤트 루프의 비동기성(Asynchronized)으로 
요청하고 기다리기 방식(동기, synchronized) 에서 발생하는 문제를 해결한다.
동기에서 발생하는 문제는 네트워크를 경유하여 요청이 계속 쌓이게되면 많은 CPU 클럭수를 발생하여 응답데이터를 갖고오기까지 시간이 많이 소요된다.
비동기는 동기와 반대로 앞의 코드가 끝날 때까지 기다릴 필요없이 다음코드를 실행할 수 있다.
자바스크립트의 비동기 처리방식은 '콜백'을 활용한다.
 
- 동기화(synchronus)
    - 한 자원에 동시에 접근하는 것을 제한한다.
    - 순차적으로 접근하여 작업을 진행한다.
    - 다음에 실행될 명령은 현재 실행중인 명령이 종료할때까지 대기한다.
    - 메소드, 블록 단위로 적용이 가능하다.

 
- 비동기화(Asynchronus)
    - 현재 실행중인 명령이 종료되지 않아도 다음 명령이 실행 가능하다.
    - 콜백함수를 통해 결과를 확인한다.
    - 스레드

 
 
### 1.2 (강점) Offloading
Offloading 은 저수준의 오래걸리는 일은 node에게 맡기고, 고수준의 로직은 메인스레드에서 맡긴다.
이러한 이유로 Node가 빠른 속도와 매우 높은 확장성을 갖는다.
Node가 복잡하고 오래걸리는 일을 하고, 프로그래머는 비즈니스로직을 작성한다.
비동기에서는 싱글스레드로만 있기때문에, 비동기로인한 동시성 문제가 없다.
 
### 1.3 (약점) 저수준 처리의 개선
자바스크립트 한계가 있다.
이미지파일중 특정한 파일을 찾거나, 오디오파일들을 합치는 등 노드만으로는 저수준처리로는 느릴 수 밖에 없다.
Node.js는 C와 Web Assembly 모듈을 바인딩해서 저수준처리를 해결할 수 있다.
 
### 1.4 (강점) npm - 방대한 오픈소스 생태계
npm : Node Package Manager 의 줄임말 이다.
오픈소스 생태계로부터 많은 정보들을 얻을 수 있다.

---

## 2) Node.js 개발환경

* 필자 컴퓨터 os: mac OS
nvm (node version manager) - 노드버젼을 관리하는 도구
tj/n - 간단하고 쓸모가 높은 바이너리 CLI 이다.
nvm, tj/n을 왜 사용하는가?
서버에서의 node 버젼과 로컬에서의 버젼이 달라서 동작에 오류가 생길 경우를 대비하기 위해서이다. Node의 버젼을 관리가 필요하다.



### 2.1 npm과 package.json

npm (Node Package Manager) 은 Node.js 의 기본 패키지 관리자이다.
Node.js 에서 사용할 수 있는 모듈들을 패키지화 하여 모아둔 저장소 역할과 패키지 설치 및 관리를 위한 CLI(Command Line Interface)를 제공한다.


Node.js 프로젝트가 의존하고 있는 패키지의 업데이트되므로, package.json 파일을 통해서 프로젝트 정보와 패키지 의존성(dependency)을 관리한다. 또한 여러컴퓨터에서 같은 코드로 작업할 때 동일한 개발환경으로 빠르게 구축할 수 있다.


package.json 은 해당 프로그램을 실행시키기 위해서 필요한 모듈, 프로그램 실행방법, 테스트 방법 등 이 표기 되어있다.
package.json은 Maven의 pom.xml 과 비슷한 역할을 한다. 
 

실제 로컬환경에서 설치된 버젼을 확인하고 싶다면 package-lock.json 에서 볼 수 있다. 
여러사람들과 함께 작업하는 경우에는 package-lock.json 을 커밋해야한다. 그 이유는 서로간에 패키지 버젼이 안맞는 문제를 방지 할 수 있기 때문이다.
 

실제 모듈들은 node_modules 라는 폴더에 저장되어있다.
node_modules 폴더안에 있는 .bin 은 실행할 수 있는 바이너리 파일이다.
 
작업하고 있는 node.js 프로젝트가 npm 이 관리하고 있는 패키지임을 알려줘야하는데, package.json이 필요하다.

```shell
$ npm init -y
```


* [추가] npm install 할 때 패키지 명령어와 플래그들 의미

- `-D`, `--save-dev` : 패키지를 설치하고, 프로젝트의 devDependencies 목록(개발단계에서만 필요)에 추가.

- `-g` , `--global` :  시스템 폴더에 패키지를 설치. package.json 의 의존성 목록에 기록되지 않음.



### 2.2 Prettier 와 ESLint 와 TypeScript
여러사람들과 프로젝트를 함께 작업할 때 코드에 오타가 있거나, 코드라인이 엉망인 것과 같은 가독성이 좋지 않을 경우에는 시간낭비가 크다. 코드의 품질과 쓸데없는 시간을 단축시키기 위해서 IDE의 코드포맷팅 도구가 있다. 
 

2.2.1 Prettier - Formatting 패키지. 세미콜론이 붙어있는지, 스페이스와 같은 문자그대로를 검토해준다.
Prettier 설치
vscode의 extensions에서 prettier을 설치할 수 있다


```shell
$ npm install --save-dev prettier
```


prettier에서 설정파일인 `.prettierrc.json` 이 필요하다.

```json
// 파일명: .prettierrc.json
{
	"semi": false,
    	"signleQuote": false
}
```


vscode에서 프리티어가 동작하려면 `setting.json` 파일이 필요하다.
.vscode 폴더를 만든 후에, .vscode 폴더 안에 `setting.json` 파일을 생성한다.

```json
// 파일명:  setting.json
{
    "[javascript]": {
        "editor.formatOnSave": true,
        "editor.defaultFormatter": "esbenp.prettier-vscode"
    }
}
```