---
layout: page
title: Resume
permalink: /about/
---

# 안녕하세요. 주니어 백엔드 개발자 **최은강** 입니다.
{: .no_toc }

![]( {{ site.photo | absolute_url }}/about/cek_emoji.jpg){:width="200px" height="200px" .mt-3 }
{: .d-flex .flex-justify-around .mb-2}

<br><b>"낙숫물도 끊임없이 떨어지면 바위도 뚫는다"</b> 라는 신념을 갖고 더 나은 개발자가 되기 위해 꾸준히 노력하고 있습니다.<br><b>"우물안 개구리가 되지말자"</b> 라는 마인드로 항상 겸손함을 갖고 개발에 임하고 있습니다.
{: .fs-4 .flex-justify-between}


### Contacts
{: .no_toc}

- :email: <dmsrkd1216@gmail.com>
- :link: [LinkedIn](https://www.linkedin.com/in/%EC%9D%80%EA%B0%95-%EC%B5%9C-8b0378191/)
- :pencil: [Tistory Blog](https://ek12mv2.tistory.com/)

<br>

### Hobbies
{: .no_toc .mb-3}

**스포츠** : 수영, 요가, 자전거, 스키

**취미** : 웹툰보기, 독서, 신문읽기

<br>

---

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}


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
>> - **Database**: MySQL
>>
>> - **Cloud**: GCP(Google Cloud Platform) - Kubernetes Engine
>>
>> - **Messaging Queue Service**: Pub/Sub
>>
>> - **Etc** : gRPC, protobuff, Socket.io
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

# Educations
{: .text-delta}

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



