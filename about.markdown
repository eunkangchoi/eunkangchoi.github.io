---
layout: page
title: Resume
permalink: /about
nav_order: 2
---

# 안녕하세요. 주니어 백엔드 개발자 **최은강** 입니다.
{: .no_toc }

![]( {{ site.photo | absolute_url }}/about/cek_emoji.jpg){:width="200px" height="200px" .mt-3 }
{: .d-flex .flex-justify-around .mb-2}


<br>
<h4>연봉 보다는 <b>성장</b> / 안정 보다는 <b>도전</b> / 기억 보다는 <b>기록</b> / 혼자 보다는 <b>같이</b></h4>
<br><b>"낙숫물도 끊임없이 떨어지면 바위도 뚫는다"</b> 라는 신념을 갖고 더 나은 개발자가 되기 위해 꾸준히 노력하고 있습니다.<br><b>"우물안 개구리가 되지말자"</b> 라는 마인드로 항상 초심을 잃지 않고 겸손함을 갖고 개발에 임하고 있습니다.<br>
<br>개발하면서 겪은 고민사항과 그 고민에 대한 해결과정을 블로그에 기록하고 스스로 배우고, 스스로 문제를 해결하여 공유하는 것을 목표로 하고있습니다.<br>


<br>


### Contacts
{: .no_toc}

- :email: <dmsrkd1216@gmail.com>
- :link: [LinkedIn](https://www.linkedin.com/in/%EC%9D%80%EA%B0%95-%EC%B5%9C-8b0378191/)
- :pencil: [Tistory Blog](https://ek12mv2.tistory.com/)

<br>

### Hobbies
{: .no_toc .mb-3}

**스포츠** : 수영, 요가, 자전거, 스키

**취미** : 웹툰보기, 독서, 신문읽기, 개발 블로그 포스팅

<br>

### Interested Techs
{: .no_toc .mb-3}

- Environments & Languages: **NodeJS**, **Javascript**, **Typescript**
- Frameworks: **Express.js**, **Nest.js**
- Databases: **MySQL**, **Redis**, **MongoDB**
- Clouds:  **AWS**, **GCP**
- CI & CD:  **Docker**, **Kubernetes**
- Etcs: gRPC , WebSocket, REST API, GraphQL


---

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}


---

## NodeJS Project Experiences

## 원티드 프리온보딩 5기

<small>[✨ TIP ] 아래 링크를 클릭하면 래포지토리로 이동할 수 있습니다!</small>


{: .no_toc}
### [1. 원티드 프리온보딩 선발과제 - 채용을 위한 웹서비스 Restful API](https://github.com/loveAlakazam/wanted-pre-onboarding-backend-2022-10)

- 개인작업(1인)
- 활용기술스택
    - Environment: NodeJS
    - Framework: ExpressJS
    - Language: TypeScript
    - Database: MySQL
- 진행기간: 2022.10.16 ~ 2022.10.19    

<br>

{: .no_toc}
### [2. 회원 등급에 따른 게시판 서비스와 통계 Restful API 웹서비스](https://github.com/loveAlakazam/1_statistics) 

- 팀작업 (4인)
- 활용 기술스택
    - Environment: NodeJS
    - Language: TypeScript
    - Framework: NestJS
    - Database: AWS RDS (MySQL 8.0)
    - ORM: TypeORM
    - Etc: Github Action & Workflow

- 담당역할
    - [PUT] 게시글 수정 API 작성
    - [GET] 금일 접속자 연령별 조회

- 진행기간: 2022.10.26 ~ 2022.10.31

- 블로그 포스팅
    - [AWS RDS 인스턴스 만들기 & NestJS 에 AWS RDS 연결하기](https://ek12mv2.tistory.com/303)
    - [Type ORM Group by 로직 짜다가 발생한 에러 해결하기 + 팀원 코드리뷰](https://ek12mv2.tistory.com/310)
        


<br>

{: .no_toc}
### [3. 해외 배송 쇼핑몰 Restful API 웹서비스](https://github.com/loveAlakazam/2_shopping_mall_management) 

- 팀작업 (4인)
- 활용 기술스택
    - Environment: NodeJS
    - Language: TypeScript
    - Framework: NestJS
    - Database: AWS RDS (MySQL 8.0)
    - ORM: TypeORM
    - Etc: Github Action & Workflow


- 담당역할
    - 쿠폰 API 담당
        - 운영자만 사용가능 쿠폰 API
            - [POST] 쿠폰생성
            - [GET] 모든 쿠폰 목록 조회 및 검색
            - [GET] 사용자 id를 검색하면, 사용자가 보유한 모든 쿠폰 조회 (기간 지난 쿠폰도 포함)
            
        - 일반유저만 사용가능 쿠폰 API
            - [GET] 사용가능한 보유 쿠폰 조회 & 쿠폰 타입별로 보유쿠폰 검색
            - [POST] 운영자가 생성한 쿠폰을 받아서 보유 쿠폰으로 등록
            - [PATCH] 보유쿠폰 기간 연장
            - [PATCH] 보유쿠폰 사용
            - [PATCH] 주문취소시 사용했던 보유쿠폰 다시 사용가능한 보유쿠폰으로 복원
        - ( [:: TODO 👊 ::] 고도화 예정) Scheduler와 axios를 이용하여 달러환율 구하기

    - Github Action & Workflow 세팅
        - 이슈 생성시 자동으로 브랜치 생성
        - develop/feature 브랜치에서 푸시할 때, Node.JS 자동 빌드 워크플로우 생성

- 진행기간: 2022.10.31 ~ 2022.11.06        

- 블로그 포스팅
    - [쿠폰모듈 어떻게 개발할지 고민했던 흔적](https://ek12mv2.tistory.com/313)
    - [Type number trivaially inferred from a number literal, remove type annotation 에러 해결하기](https://ek12mv2.tistory.com/315)
    - [Git Rebase](https://ek12mv2.tistory.com/307)
    - [npm ci 명령어로 협업중 package-lock.json 패키기 동기화 시키기](https://ek12mv2.tistory.com/308)
    - [날짜 데이터 insert 하기](https://ek12mv2.tistory.com/316)

<br>

```md  
[팀과제 후기]

팀원의 코드리뷰 너무 좋았습니다! 
배울점이 많고 실력좋은 동료들과 같이 고민하고, 피드백 받고 개발관련 이야기했던게 너무 아련한 추억이 됐네요...ㅎㅎ
개인적인 생각이지만, 솔직히 개인과제비중보다는 팀과제의 비중을 늘렸으면 좋겠어요 🥹
팀과제를 같이하면서 팀원들의 코드를 보는 것마저도 NestJS를 몰랐던 저에겐 너무 도움됐어요..!
```

<br>


{: .no_toc}
### [4. 비밀글 기능이 포함된 게시판 Restful API 웹서비스](https://github.com/loveAlakazam/3_Posts) 

- 개인작업(1인)
- 활용기술 스택
    - Environment: NodeJS
    - Language: TypeScript
    - Framework: NestJS
    - Database: AWS RDS (MySQL 8.0)
    - ORM: TypeORM
    - Test: Jest
    - Etc
        - Github Action & Workflow
        - Axios & OpenAPI

- 진행 기간: 2022.11.04 ~ 2022.11.07

- 블로그 포스팅
    - [Jest를 이용한 테스트 환경만들기](https://ek12mv2.tistory.com/325)
    - [Joi를 validation schema를 사용해보기](https://ek12mv2.tistory.com/342)
    - [스키마중 소수넘버 컬럼 정의하기](https://ek12mv2.tistory.com/322)
    - [정규표현식에 맞는 데이터인지 확인하는 방법 & 선택적으로 입력데이터를 받기: class-validator 활용하기 ](https://ek12mv2.tistory.com/323)
    - [raw query에서는 take()와 limit()이 적용안되는 오류 해결하여 pagination 구현하기](https://ek12mv2.tistory.com/329)
    - [(고도화) Axios를 활용하여 OpenAPI 로부터 현재 날씨 데이터를 파싱하기](https://ek12mv2.tistory.com/328)

- 진행기간 이후에도 고도화 작업 내역
    - Axios와 OpenAPI를 활용하여 게시글을 등록할 때 날씨데이터도 같이 등록할 수 있도록 변경했습니다.

<br>

{: .no_toc}
### [5. MongoDB를 활용한 벤치마킹 쇼핑몰 Restful API 웹서비스](https://github.com/loveAlakazam/4_MarketService) 

- 개인작업(1인)
- 활용기술 스택
    - Environment: NodeJS
    - Language: TypeScript
    - Framework: NestJS
    - Database: MongoDB (MongoDB Atlas 5.0.13)
    - Test: Jest
    - Etc
        - Mongoose
        - Github Action & Workflow
        - Swagger

- 진행기간: 2022.11.07 ~ 2022.11.17

- 블로그 포스팅
    - [나만의 Custom Error Exception 와 Custom Exception Filter 만들기 (feat: NestJS 다큐먼트 읽기)](https://ek12mv2.tistory.com/331)
    - [서비스 로직에서 db를 호출하지 말고, Repository 레이어를 추가하기 ](https://ek12mv2.tistory.com/339)
    - [NestJS framework에 MongoDB 연결하기](https://ek12mv2.tistory.com/333)
    - [MongoDB+NestJS+Mongoose - 콜렉션의 외래키 컬럼 설정하는 방법](https://ek12mv2.tistory.com/336)
    - [Guard가 있는 컨트롤러 유닛 테스트하기 - 유저 controller 테스트](https://ek12mv2.tistory.com/343)
    - [Cast to date failed for value "[Function:now]" 에러 해결 - Soft Delete 구현하기](https://ek12mv2.tistory.com/344)
    - [MongoDB populate() 사용해보기](https://ek12mv2.tistory.com/345)
    - [MongoDB $cond, $exists, $nin, $gt 옵션들을 활용하여 쿼리문 만들기 : 판매자가 올린 다른 상품들 데이터 구하기 ](https://ek12mv2.tistory.com/347)
    - [MongoDB aggregation 활용하여 마켓리스트 나타내기](https://ek12mv2.tistory.com/348)

- 진행 기간 이후에도 고도화 작업 내역
    - 회원탈퇴 기능 고도화
        - 셀러회원이 탈퇴했을 경우 셀러회원이 등록한 상품데이터와 마켓데이터들도 모두 삭제처리되도록 변경했습니다.
    - 셀러등록 기능 고도화
        - 회원 모델에 `예금주명`, `은행`, `계좌번호` 컬럼을 추가하여 셀러의 계좌정보를 등록을 요청하도록 변경했습니다. 
    - Swagger 적용하기

<br>

[6. [:: TODO 👊 ::] Boss Raid 미니 게임 Restful API 웹서비스(진행중이라서 private 입니다 ^^)](https://github.com/loveAlakazam/5_Boss_Raid_API)

- 개인작업(1인)
- 활용기술 스택
    - Environment: NodeJS
    - Language: TypeScript
    - Framework: NestJS
    - Database: AWS RDS (MySQL 8.0), Redis
    - ORM: TypeORM
    - Test: Jest
    - Etc
        - Github Action & Workflow


<br>

[7. [:: TODO 👊 ::] gRPC + NestJS 를 활용한 나만의 SNS 감정노트 Web 서비스 (진행예정이라서 private 입니다 ^^)](https://github.com/loveAlakazam/My_SNS_Networking)

<br>


[8. [:: TODO 👊 ::] NestJS + GraphQL 을 활용한 나만의 가계부 만들기 Web 서비스(진행예정이라서 private 입니다 ^^)](https://github.com/loveAlakazam/My_AccountBooks)


<br>

---

# Work Experiences
{: .text-delta}



---



## 스윗코리아

{: .d-inline-block }

latest
{: .label .label-purple}

Backend Developer
{: .fs-4 }


> Period
>> 2021.04 - 2022.06
>
> Tech Stack
>> - **Programming Language** : Go, Javascript (AngularJS)
>>
>> - **Database**: MySQL, NoSQL(Redis)
>>
>> - **Cloud**: GCP(Google Cloud Platform) - Kubernetes Engine
>>
>> - **Messaging Queue Service**: Pub/Sub
>>
>> - **Etc** : gRPC, protobuff, Socket.io
>
> 주요업무
>> - Swit 웹서비스 및 모바일을 위한 API 개발
>> - 실시간 메시징, 알람, 업무협업을 위한 각종 기능 개발 및 Open API 지원
>> - Swit 시스템 운영과 버그픽스 및 성능 개선
>> - OAuth2.0, Access Token 기반의 Open API 활용한 개발
{: .fs-3 }


<br><br>

What Did I Do?
{: .fs-4 }

### 1. Multi Assignees of TaskPlus
{: .no_toc}
> 2022.05 - 2022.06
> - 기존 proto 모델에 Type이 단일 string 에서 array-string 으로 변경해서 해당 필드를 사용하는 API 조사와 API별로 테스트케이스를 만들어서 unit-test와 동시에 HTTP 로컬 통신테스트를 했습니다.
>
> - 건강상의 이유로 멀티어사이니를 끝까지 마무리하지 못했지만, 다른사람들이 만든 코드에서 필드 타입 하나를 찾아서 바꾸는 과정에서도 커뮤니케이션과 시간이 많이 필요했습니다. 필드타입이 바뀌면서 다른 API에서 오류가 없는지 꼼꼼한 테스트와 디버깅이 필요하다는 것을 배웠습니다.
{: .pb-3}

### 2. 워크스페이스 권한 분리 - Seperation of Channel & Project 
{: .no_toc}
> 2022.03 - 2022.04 
> - protocbuff 모델에서 필드를 추가하였습니다.
> - 권한/분리가 필요하는 API가 어떤 것인지 찾아봐야하고 해당 API 들을 단위테스트 와 통신테스트를 했습니다.
>
> - 서버의 url 라우터단은 Node.js이고, 실질적인 서비스를 제공하는 서버는 Go(Go-Gin)로 되어있었습니다. 프로젝트가 여러개이고 서로 다른 프레임워크를 사용하는 프로젝트일때 포트포워딩 설정으로 디버깅을 할 수 있게 되었습니다.
{: .pb-3}

### 3. Channel API Porting
{: .no_toc}
> 2022.01 - 2022.04
> - Node.js 로 된 채널 관련 API 들을 Go-Lang 으로된 API 로 porting 작업 및 리팩토링(Refactoring) 을 했습니다.
> - Port Forwarding 하여 각 API 로직별로 unit-test 를 했습니다.
{: .pb-3}

### 4. swit-support API 추가 및 페이지 개선
{: .no_toc}
> 2021.05 - 2022.04
> - 스탠다드 레벨의 워크스페이스를 구독한 클라이언트들의 정보를 뿌려주는 GET 방식의 API를 만들었습니다.
> - 스탠다드 레벨의 워크스페이스 유효기간을 늘리는 POST 방식의 API를 만들었습니다.
>
> - Billing id 를 구분자로 하여 스탠다드 레벨, Advanced 레벨의 워크스페이스를 구독한 클라이언트들의 정보를 나타내는 Modal UI를 만들었습니다.
>
> - JWT(Json Web Token)을 이용하여 json형태로 유저 토큰 데이터를 전달하도록하고, OAuth2.0 방식으로 된 Google Login API를 활용하여 로그인 API 생성 및 구글 계정으로 로그인할 수 있도록 로그인모듈을 개선시켰습니다.
>
> - GCP Scheduler와 Batch 서비스를 활용하여, Advanced 레벨의 워크스페이스를 구독한 클라이언트의 정보데이터를 하루단위로 자동갱신하는 스케줄러를 만들었습니다.

<br><br>

### 5. 내 기억에 남는 버그픽스들
{: .no_toc .mt-3}

> 1. OG 데이터 영역 내용이 공백으로 나오거나, 특수문자(`-`, `_`) 가 포함된 유튜브영상 id인 경우에는 재생이 안되는 문제를 발견하여 해결했습니다. 이는 QA(Quality Assurance) 팀이 찾지 못한 이슈였습니다.
>
> 2. 키워드 검색 이슈 개선 했습니다. 이전에는 키워드가 마크업 포멧안에 있으면 검색결과에 반영이 되지 않았는데, bullet-list, ordered-list 과 같은 마크업 포맷 안에 있는 키워드도 검색 결과에 나타낼 수 있도록 했습니다. 더나아가 검색키워드의 검색범위를 메시지 뿐만아니라 업무카드, 메시지의 코멘트, 업무카드 코멘트로 확장시켰습니다.
>
> 3. 리턴 타입을 `map[string]interface{}{}` 으로 바꿈으로써 각 업무카드에 연관된 메일들을 불러오는 API 를 개선하였고, 이로인해 업무카드 리스트를 보여주는데 걸리는 시간을 3m 에서 250ms 로 단축시켰습니다.
>

<br>

### 6. 자기주도적으로 문서화 및 공유하여 불편사항을 개선한 경험
{: .no_toc .mt-3 }

>신규입사자들의 입장을 생각하여 신규입사자들이 설치에 어려움없이 빠르게 환경셋팅을  조성할 수 있도록 IDE를 포함한 백엔드 **개발환경 셋팅 가이드라인** 과 **로컬호스트에서 Go-Land 디버깅하는 과정**을 Jira Confluence에 공유했습니다. <br><br>1년동안 사내 Confluence 다큐먼트 중 가장 많은 조회수를 유지했고, 선배동료가 신규입사자에게 제가 만든 다큐먼트를 공유하는 모습을 보며 뿌듯함을 느꼈습니다. 내가 아는 지식을 문서화시키고 공유하여 다른사람에게 작은 도움을 줄 수 있는 개발자가 되고 싶습니다.


---

# Associations
{: .text-delta}


---

# Educations
{: .text-delta}

## 원티드 프리온보딩 백엔드코스

> 기간: 2022.10.24 ~ 2022.11.28
>
> Tech Stack: **Node.js**, **Typescript**, **Nest.js**
>
> 2차례의 팀과제와 2차례의 개인과제 진행




<br>

## NomadCoders 온라인교육 수강

- [2주안에 Typescript 뽀개기 (2022.10.17 ~2022.11.07) ](https://nomadcoders.co/certs/90261e39-b762-47d0-bf29-8f7e29390744)

- [NestJS로 API 만들기(2022.10.06 ~ 2022.10.07)](https://nomadcoders.co/certs/e483b317-1562-4f5b-bb27-fd4c85d7a3db)

- [Vanilla JS 2주완성반 27기 수료 (2022.08.01 ~ 2022.08.15)](https://nomadcoders.co/certs/45634687-335c-442e-8d26-ffbcee21c174)

- [Youtube Clone Coding (진행중)]()


<br>

## KH 정보교육원 수료

- 수료기간: 2020.05 - 2020.12
- Tech Stack: Java, Spring, Apache Tomcat, Oracle, Ajax, jQuery, Javascript, HTML, JSP, CSS

- [파일확장자 페이지 만들기](https://github.com/loveAlakazam/Blocked_Files_Web_Project)
- [전국방방곡곡](https://www.notion.so/ek12mv2/2d3462b523534168bc1b1e8671c2eb36)
- [Good Ball](https://www.notion.so/ek12mv2/Good-Ball-75b549e4b9954f85abbdb358e49e06b4)
- [커피깡](https://www.notion.so/ek12mv2/8d7c2b4ece104c36a37931c0f2c1a4fb) 


## 스파르타 코딩클럽 웹개발 8기 수료

- 수료기간: 2020.05 - 2020.06
- Tech Stack: Python3, MongoDB, AWS EC2, Flask, HTML, CSS, jQuery, Javascript

- [오늘은 뭐먹지](https://www.notion.so/ek12mv2/c87702bb94ad4a7595eebc0b6ad5ed35)

<br>

## 상명대학교(제2캠퍼스) 졸업

- 재학기간: 2016.03 - 2021.02

- [전자제품을 제어하는 RPi 음성인식 스피커](https://www.notion.so/ek12mv2/RPi-ce29171715d44d1a89fbded3403a5f33)
- [Hey 천안역전](https://www.notion.so/ek12mv2/Hey-570a69bd44fa47f1933fe9c4c24b2ae4)
- [시각장애인을 위한 모자](https://www.notion.so/ek12mv2/6601bd9a629848f4adf65e635ef8441f)


---
# Certifications & Awards
{: .text-delta}


## Certifications

- **정보처리기사** (2020.12)
- **리눅스마스터 2급** (2020.07)

## Awards

- 대한전기학회 여성 캡스톤 경진대회 우수상 (2017.10)
