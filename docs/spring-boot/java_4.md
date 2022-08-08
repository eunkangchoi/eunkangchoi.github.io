---
layout: default
title: (Java) Java 14.ver 에서만 지원되는 코드 표현
parent: Java 와 Spring-Boot
tags:
    - java
    - java 14
    - 조건문

comments: true
---

작성완료
{: .label .label-green }


## Table of contents
{: .no_toc .text-delta}

1. TOC
{:toc}

---

## Java 14부터 지원되는 Switch Expression

### 기본 switch-case문
{: no_toc}

```java
public static void main(String [] args) {
    Scanner sc = new Scanner(System.in);

    System.out.print("숫자를 입력해주세요: \n");
    int inputMonth = sc.nextInt();
    
    int resultDays = 0;
    switch(inputMonth) {
        case 1: case 3: case 5: case 7: case 8: case 10: case 12:
            resultDays = 31;
            break;
        
        case 4: case 6: case 9: case 11:
            resultDays = 30;
            break;

        case 2:
            resultDays = 28;
            break;

        default:
            System.out.println("Not Month Data - Retry...");
    }

    if (resultDays > 0) {
        System.out.println("resultDays: " + resultDays);
    }
}
```

<br>

### Java 14 부터 지원되는 switch-case문
{: no_toc}

- `yield` 키워드를 사용합니다 : return 과 같은 역할 입니다.

```java
public static void main (String [] args) {
    Scanner sc = new Scanner(System.in);
		System.out.println("숫자를 입력해주세요: ");
	    int inputMonth = sc.nextInt();
	    
	    int resultDays = switch(inputMonth) {
	        case 1, 3, 5, 7, 8, 10, 12 -> {
		         yield 31;
	        }
	        case 4, 6, 9, 11 -> {	        	
	        	yield 30;
	        }
	        
	        case 2 -> {
	        	yield 28;
	        }
	        
	        default -> {
	            System.out.println("Not Month Data - Retry...");
	            yield 0;
	        }
	    };

	    if(resultDays > 0 ) {
	        System.out.println("resultDays: " + resultDays);
	    }
}
```
