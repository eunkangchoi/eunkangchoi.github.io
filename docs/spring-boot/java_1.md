---
layout: default
title: Java 설치 & Eclipse IDE 설치 & Java 프로그래밍 시작
parent: spring-boot
tags:
    - java
    - eclipse
    - 프로그래밍
    - 패스트캠퍼스 국비교육
---

### **환경 설치**


#### 1\. JDK 설치 - Java SE Development Kit

-   필자 OS 환경: **MacOS** / **Intel 칩**
-   설치링크: [https://www.oracle.com/java/technologies/downloads/#jdk18-mac](https://www.oracle.com/java/technologies/downloads/#jdk18-mac)
-   설치항목: `x64 DMG Installer`

<br><br>

#### 2\. Eclipse 설치

-   Download from: Korea, Republic Of - Kakao Corp. (https)
-   File: eclipse-inst-jre-mac64.dmg
-   설치링크: [https://www.eclipse.org/downloads/download.php?file=/oomph/epp/2022-06/R/eclipse-inst-jre-mac64.dmg](https://www.eclipse.org/downloads/download.php?file=/oomph/epp/2022-06/R/eclipse-inst-jre-mac64.dmg) 


![](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FbVlgOA%2FbtrIT8mJtpi%2Fk6VqBwEHuzecrymLyxtB01%2Fimg.png)


Eclipse Installer 를 더블클릭합니다.

<br><br>

![](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2Fwt1Lu%2FbtrINvw9Ihe%2F2a5P7t4YKFvN2VsJYAnc2k%2Fimg.png)

맨위의 Eclipse IDE for Java Developers 를 클릭합니다.

<br><br>


![](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2Fbr0MFT%2FbtrIT9lF3hJ%2FBbCIhO5Aoz9dNKC2Ku7491%2Fimg.png)

자동으로 java vm 과 설치될 이클립스 ide 저장 경로를 나타냅니다.

<br><br>

설치 완료가 되면 Launch 버튼을 누르면 아래와 같이 "**Select a directory as workspace** 경로 팝업창"이 나옵니다.

macOS에서 eclipse ide 경로의 기본값으로는 **`/Users/유저명/eclipse-workspace`** 값으로 합니다.


**프로그래머 자신이 쉽게 알 수 있는 위치로 eclipse workspace 경로값을 설정**합니다.

그리고 **Use this as the default and do not ask again 체크박스는 표시하지 말고 놔두는게** 좋을거 같습니다.

이클립스를 실행시킬때마다 IDE 위치를 확인하여 조회할 수 있도록 합니다.

왜냐하면 다른 위치에서도 프로젝트를 조회할 수 있도록 하기 위해서입니다.

![](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FegnHlz%2FbtrISO3kMhD%2F4LKE7svrK8vVaFwTTkvUc0%2Fimg.png)


<br>

---

### **첫 Java 프로젝트 만들기**

![](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FPkIJz%2FbtrIO13srRL%2FszGVslmhVFNO3CYKwkhjik%2Fimg.png)

프로젝트를 생성할 때, **프로젝트명**(Project Name)**의 맨앞은 대문자**로 합니다.

또한 주의사항은, **Module 영역의 "Create module-info.java file" 의 체크박스를 해제**시킵니다.

![](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FbIfDER%2FbtrISARtJE0%2FCaEfAHPf6JKVgfBdmF1QA1%2Fimg.png)

<br><br>

---

[추가항목]

현재 이클립스에 설치된 jre를 확인할 수 있습니다.


![](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2Fct57OR%2FbtrIPWgb4wp%2FoCloOARV7MkDmkt3ki21f1%2Fimg.png)


![](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2Fbr2JF1%2FbtrIUllY4gu%2F59gNsgX4Oki8PpA9JDjT1k%2Fimg.png)

jre는 여러개 설치가 가능하며, 설치된 jre가 여러개일 때 하나를 선택할 수 있습니다.

<br>

---

<br><br>


그러면 아래 화면과 같이 Chapter1 프로젝트안에 src 가 생깁니다.

하지만 아직 이 상태에서는 코드를 작성할 수 있는 단계가 아닙니다.

여기서 클래스 파일을 추가해야 됩니다.

**프로젝트명**(Chapter1) **의 src 디렉토리를 오른쪽 마우스 클릭하고 Class 파일을 새로 생성**합니다.

![](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FOL68Y%2FbtrINuZo2ta%2FVVLtUy5KYa8k9cstFYZEW1%2Fimg.png)


![](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FcACYXp%2FbtrIUmLYd08%2F5ZKvOHeLk8HTZIztqcEPFk%2Fimg.png)

---

\[ 추가항목 \] 패키지없이 프로젝트 생성하기 

![](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FIWAMx%2FbtrIRFS8ei3%2F1j5McCYshOhKKJlIM2KZBK%2Fimg.png)

패키지(Package)를  입력하지 않으면,  **(default package)** 라는 곳에 HelloDefaultPackage.java (클래스 파일)이  생성됩니다.

<br>

![](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FohEr4%2FbtrITpCgaeg%2FCTMGWKlKfcGZBhy5Kw4yWK%2Fimg.png)


<br><br>

실제 파일탐색기에서 **`(default package)`** 에 저장된 HelloDefaultPackage.java 파일이 저장된 위치는

`Chapter1(프로젝트이름)/src` 에 저장되어 있음을 알 수 있습니다.

![](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FbWD24e%2FbtrINuE75PQ%2FRIyJ9PM644TM5UPe0WZNVK%2Fimg.png)

---

<br><br>

![](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2Fb8NG69%2FbtrIVhDKsjD%2FGq8fiElkhC2gumXDcyhfJK%2Fimg.png)

**패키지**는 **일종의 소스의 묶음** 입니다.

**패키지 이름을 설정할 때, 알파벳 소문자와 숫자 조합으로 하는게 좋습니다.**

이는 반드시는 아니지만, 패키지명에 대한 convention 규칙입니다.

실제 이클립스에서도 컨벤션 규칙에 벗어나면 생성되지 못하도록 했습니다.

<br><br>

마찬가지로 **클래스 이름을 설정할 때는 반드시 영어로 해야하며, camel case 로 합니다**.

즉 클래스이름을 HelloWorld, ClassName, MyTodoList 과 같은 형식으로 해야합니다.

- camel case : 'CamelCase' 와 같이 맨앞에 대문자 로 해야합니다.

<br><br>

Main() 함수는 함수를 구동하기 위한 함수 입니다.

웹서버에서 자바를 실행하기 때문에 Main()이 반드시 필요한 경우는 아닙니다. 

패키지 명을 'study.java.basic.chapter01' 를 설정하면 HelloWorld.java 클래스 파일은

`Chapter > src > study > java > basic > chapter01` 에 저장되어 있습니다.

![](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FWJyuq%2FbtrIO2gZ56G%2Fd1DvUF9CK7QW5NH9z4o5G0%2Fimg.png)