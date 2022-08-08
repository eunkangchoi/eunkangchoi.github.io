---
layout: default
title: (Java) 변수와 자료형
parent: Java 와 Spring-Boot
tags:
    - java
    - 변수
    - 자료형
    - java 10
comments: true
---


작성완료
{: .label .label-green }


## Table of contents
{: .no_toc .text-delta}

1. TOC
{:toc}

---

## 변수 (Variable) 와 자료형

Java에서 **변수**는 '변하는 자료'를 저장하는 공간 입니다.

**자료형**은 표현하려는 자료에 맞는 데이터 타입을을 의미합니다.

표현하려는 자료형을 이용하여 변수를 선언해야합니다.


```java
//(변수 age 선언) [타입] [변수명] = [값]
int age = 20 ;

// (선언 이후, 변수 age 값 변경)
age = 21;
```

- 변수이름을 설정할 때 주의사항

> - 변수 이름은 영문자(대문자, 소문자) + 숫자를 사용할 수  있습니다. 
> - 특수문자 중에서는 `$` 와 `_` 만 가능합니다. (예: _countResources)
> - 다만 변수이름의 시작을 숫자로 할 수 없습니다. (예: 30days)
> - 예약어 를 변수명으로 사용할 수 없습니다.

> 자바에서의 예약어들
> 
|abstract|assert|boolean|break|byte|case|
|catch|char|class|const|continue|default|
|double|do|else|enum|extends|false|
|final|finally|float|for|goto|if|
|implements|import|instanceof|int|interface|long|
|native|new|null|package|private|protected|
|public|return|short|static|strictfp|super|
|switch|synchronized|this|throw|throws|transient|
|true|try|void|volatile|while|yield|


> - camelCase를 사용하여 변수명을 만들고, 이 변수가 *어떤 기능을 나타내는지를 짐작할 수 있도록* (변수명이 길더라도) 가독성 좋게 하는 게 좋습니다. (예: numberOfProducts )


- 자료형에 대한 참고 다큐먼트
  - [05. 변수는 변하는 수 입니다.](https://gitlab.com/easyspubjava/javacoursework/-/tree/master/Chapter1/01-05)
  - [06. 자료형 - 정수는 어떻게 표현하나요?](https://gitlab.com/easyspubjava/javacoursework/-/tree/master/Chapter1/01-06)
  - [07. 자료형 - 실수는 어떻게 표현하나요?](https://gitlab.com/easyspubjava/javacoursework/-/blob/master/Chapter1/01-07/README.md)
  - [08. 자료형 - 문자는 프로그램에서 어떻게 표현하여 사용하나요?](https://gitlab.com/easyspubjava/javacoursework/-/blob/master/Chapter1/01-08/README.md)

---

## 지역변수 자료형 없이 사용하기 (java.10ver)

- Java 10 이후에서 사용하능합니다.

- 지역변수만 사용가능합니다.
- 변수를 초기화 할 때, 자동으로 타입을 추론합니다.
- 다만, 초기화 이후에는 해당변수의 타입의 변경이 불가능합니다.



```java
public class TestLocalVarialbeType {
    public static void main(String [] args) {
        var integerType = 10 ;
        integerType = 12; // (가능)
        // integerType = "StringType"; (에러발생: Type mismatch: cannot convert from String to int)
    }
}
```
