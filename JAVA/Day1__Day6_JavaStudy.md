# Day1

## 1. Installation(설치)

(1) 크롬 브라우저 설치 : https://www.google.com/chrome
(2) Java SE(JDK) 설치 : http://java.sun.com/ -> https://www.oracle.com/technetwork/java/index.html
     설치후 환경변수 설정 : JAVA_HOME, PATH
                                  JAVA_HOME - C:\Program Files\Java\jdk1.8.0_231
                                  PATH - %JAVA_HOME%\bin
(3) Eclipse 설치 : http://www.eclipse.org/
                        C:\unico\eclipse-workspace
                        프로젝트라는 폴더를 생성해야 한다.
                        Java Project   javaexam
                        Dynamic Web Project
                        Spring MVC Project
                                 :

 맛보기용 자바 프로그램 : FirstApp

## 1. JAVA 구문

JAVA의 정석 책 참고

### 개요

1. 데이터 타입: 2장
2. 변수 활용: 2장
3. 연산자: 3장
4. 제어문: 4장
5. 배열: 5장

----------------------------- 기본 구문

6. 클래스 정의와 객체 생성
7. 상속, 다형성, 추상클래스, 인터페이스
8. 예외처리

----------------------------- OOP  구문 객체지향 구문

9. API - Application Programming Interface

   자주 필요로하는 기능을 미리 만들어 놓은 프로그램
   클래스(Math, Date, Calendar, ...) - 패키지(java.io, java.net,java.sql, java.lang...) 패키지들
   IO 패키지 - 파일 입출력 패키지. 
   패키지 - 클래스 묶음. JAVA.LANG - OBJECT, STRING, STIRNGbUFFER 등등 클래스들.
   패키지화 학습 소스들을 패키지화 : DAY1, DAY2 ..... 클래스 묶어 놓고, 그룹화

### LiteralTest

1. 데이터 타입
   숫자데이터 - 정수(byte(1바이트 -128~+127), short(2), int(4), long(8)), 실수(float(4), double(8))
   논리데이터 - True and False (Boolean)
   문자데이터 - 문자의 코드값 처리할 수 있는 타입, 2바이트, '1' ->0031, 'a' -> 0061, '가' - AC00
   문자열데이터 - 객체로 취급, "ABC", "가나다", "123". "###". ""

1(정수)   1.0(실수)   '1'(문자)   "1"(문자열형)

abSW
ST009
ASCII Code

리터럴(Literal) : 프로그램 소스 코드에서 사용되는 데이터 값을 리터럴이라고 한다.
                    		1, 1.0, '1', "1", "가",  리터럴이라고 부른다.
	        				true, false, "java"
                    		!!!! 문자데이터 안에는 문자가 반드시 한!! 개!! 만 있어야 한다! 

변수 : 데이터 값을 저장하는 메모리의 방
       데이터 값을 저장하기 위해 메모리의 일정 공간에 붙여진 이름
        저장된 데이터 값을 계속해서 변경 가능
        반드시 만들어서 써야 한다
        필요시 생성해서 사용한다.

​        변수의 생성을 변수 선언이라고 한다. 

​		타입 변수명;
​        타입 변수명 = 초기값; // 초기값 : 최초로 넣어지는 값

​		정수 데이터 -> byte, short, int, long 중에서 선택 어지간하면 int

​		실수 데이터 -> float, double                          		어지간하면 float

​		문자 데이터 -> char

​    	논리 데이터 -> boolean

​		문자열 -> string

[대입연산자] 의 오른쪽에는 다양하게 올 수 있다! 
		오늘쪽에 있는 것에 먼저 연산이 된다.
	변수 =    식;
  	          변수, 리터럴,연산식, 리턴값이 있는 메서드의 호출식

```java
//방         값
L-value   R-value

10 = 20;		 it is impossible
data1 = data2;	 it is possible
data1 = 100; 	 it is possible

data1 = Math.random();  0.0 <= x < 1.0
```



### 연산자

```java
//- 기능
//  산술연산자, 비교연산자, 논리연산자, 조건연산자, 대입연산자
//	     ㄴ(조건문, 제어문하고 같이 쓰임)

//- 사용되는 항 (피연산자, 연산에 사용되는 데이터)의 갯수
//  단항 연산자 : ++num (num = num+1)
//  이항 연산자 : 항1 연산자 항2; it has variety of kinds maybe countless 
//  삼항 연산자 : 항1 ? 항2 : 항3
	       int bigNumber = num1> num2 ? num1 : num2;

	       int bigNumber;
	       if(num1>num2)
		bigNumber = num1;
	       else
		bigNumber = num2;

(우선순위 순)
. 
++. --. +, -, !, ~,(타입명) {부호 연산자} <-단항 연산자
*, /, %
+, -
==, !=, >, <, >=, <=, instanceof (7장 공부할때) <- 연산결과가 boolean 값으로 나온다
>>, >>>, <<, <<<
&, |, ^
&&
||
항1 ? 항2 : 항3
=, +=, -=, *=, /=

int su=10;
su = su + 3;
++su;
su += 1;
```
```java
//실습1 LiteralTest
public class LiteralTest {
	public static void main(String[] args) {
		System.out.println(1 + 1);		// 2
		System.out.println(1.0 + 1);	// 2.0 	1.0 + 1 -> 1.0 + 1.0 -> 2.0
		System.out.println('1' + 1);	// 50 	1이라는 문자의 값
		System.out.println("123" + 4);	// 11	"123" + 4 -> "123" + "4" -> "11"
		
		System.out.println(7777777777777777777777777777777D);
	}
}
```

```java
//실습2 VariableTest
public class VariableTest {

	public static void main(String[] args) {
		System.out.println(1+2+3+4+5+10); // 25
		System.out.println(1+2+3+4+5-10); // 5
		System.out.println(1+2+3+4+5*10); // 60
		System.out.println(1+2+3+4+5/10); // 10 10.5X
		
		
		char munja = 'A'; // 0x41, 65
		System.out.println(munja + munja); // 130
		System.out.println("" + munja + munja); // "" : NULL문자열
		System.out.println(munja + munja + ""); // 이미 계산 됐으니 숫자 값이 출력이 된다.
	}

}
```

- **실습3 문제**

다음에 제시된 세 개의 정수데이터(리터럴)를 변수를 선언하여 저장하고 합계와 평균을 
구하여 제시된 출력 형식과 같이 출력하는 프로그램을 작성하시오. 
(평균의 소수 이하는 고려하지 않는다.)
작성 클래스명 : Exercise1

10, 25, 33

[ 출력 형식 ]
합계 : 68
평균 : 22

```java
//실습3 Exercise1
public class Exercise1 {
	public static void main(String[] args) {
		int a = 10, b = 25, c = 33;
		int sum = 0, avg = 0;
		sum = a + b + c;
		avg = sum / 3;
		System.out.println("합계 : " + sum);
		System.out.println("합계 : " + avg);
	}
}
```

- **실습4 문제**

다음에 제시된 두 개의 정수데이터(리터럴)를 
변수를 선언하여 저장하고 
나눈 몫과 나머지를 구하여 제시된 출력 형식과 같이 
출력하는 프로그램을 작성하시오. 

작성 클래스명 : Exercise2
35, 10
[ 출력 결과 ]
35 를 10 으로 나눈 결과 몫은 3 이고 나머지는 5 입니다.  

```java
//실습4 Exercise2
public class Exercise2 {
	public static void main(String[] args) {
		int a, b;
		a = 35;
		b = 10;
		System.out.println("35를 10으로 나눈 결과 몫은 " + 35 / 10 + " 이고 " + "나머지는 " + 35 % 10 + " 입니다.");
	}
}
```

- **실습5 문제**

1. char 타입의 변수 name1, name2, name3 를 선언하고 본인 
  이름의 각 문자들을 문자 리터럴로 만들어 각각 저장한다.
2. 이름을 하나의 행에 출력한다.  
  작성 클래스명 : Exercise3

```java
//실습5 Exercise3
public class Exercise3 {

	public static void main(String[] args) {
		char name1, name2, name3;
		name1 = '유';
		name2 = '성';
		name3 = '진';
		System.out.println("" + name1 + name2 + name3); 
	}
}
```

-  **실습6 문제**

(문제에서 요구되는 변수들외에는 추가로 선언하지 않는다.)

1. int 타입의 변수 number 를 선언하고 100 이라는 값을 저장한다.
2. int 타입의 변수 result 를 선언한다.
3. number 변수의 값에 10을 더하고 결과를 result 에 담아 
   결과를 출력한다.    출력형식 : 덧셈 연산의 결과 - 110
4. number 변수의 값에 10을 빼고 결과를 result 에 담아 
   결과를 출력한다.    출력형식 : 뺄셈 연산의 결과 - 90
5. number 변수의 값에 10을 곱하고 결과를 result 에 담아 
   결과를 출력한다.    출력형식 : 곱셈 연산의 결과 - 1000
6. number 변수의 값에 10을 나누고 결과를 result 에 담아 
   결과를 출력한다.	  출력형식 : 나눗셈 연산의 결과 - 10

작성 클래스명 : Exercise4

```java
//실습6 Exercise4
public class Exercise4 {
	public static void main(String[] args) {
		int number = 100;
		int result = 0;
		result = number + 10;
		System.out.println("덧셈 연산의 결과 - " + result);
		
		result = number - 10;
		System.out.println("뺄셈 연산의 결과 - " + result);
		
		result = number * 10;
		System.out.println("곱셈 연산의 결과 - " + result);
		
		result = number / 10;
		System.out.println("나눗셈 연산의 결과 - " + result);
	}
}
```

# Day2

연산자 피연산자(항)

++su, --su, -su, !true

++su, su++ <- 요 2개는 다른고얌

I-value: 방: 변수
r-value: 값: 식(변수, 리터럴, 연산식, 리턴값이 있는 메서드의 호출식)

= 연산을 처리할 때
I-value의 타입과 r-value의 타입은 동일해야 한다.
그런데 만일 다른 타입이 사용되면 r-value의 값이 손실되지 않는 범위에서 I-value의 타입으로 자동 변환한다.

int = char
(4)    (2)

int = double
(4)   (8)
ㄴ 이런 경우에는 형태를 변환해줘야 한다. e.g. ivalue=(int)dvalue

Boolean은 형태 변환 못해~~


```java
[조건문 Swtich]

	switch(식) {
	    ㄴ! 중괄호 셋트가반드시 필요
	    ㄴ! boolean 사용 못함. 
	    ㄴ! int(byte, short, char)랑 string만 사용할 수 있음!

	    case 비교값1 : 수행문장1;
		          수행문장2;
		          break;

	    case 비교값2 : 수행문장3;
		          수행문장4;
		          break;

	    case 비교값3 : 수행문장5;
		          수행문장6;			          
		          break;

	    case 비교값4 : 수행문장7;
		          수행문장8;	
		          break;

	    default: 수행문장 9; <- 그 외의 모든 경우 라는 뜻.
		
	}
```

```java
byte < short < int < long < float < double
(1)      (2)       (4)    (8)
char < int < long < float < double


short = char
char = short
char = byte
```

### 제어문

정의된 수행 문장들을 한번씩 순차적으로 수행하면서 진행하는 것이 기본이지만
조건에 따라 수행문장들을 선택하여 수행하거나 
반복해서 여러번 수행도록 하고자 할때 제어문을 사용한다.

- (선택) 조건 제어문 - if , else, = they are friend. they are not single exisintg
- 반복 제어문 - for, while, do ~ while
- 분기 제어문 - break, continue 

```java
case1)	if(조건식)
	     수행문장1:

case2)	if(조건식){
	    수행문장1:
	    수행문장2:
	}

case3)	if(조건식){
	    수행문장1:
	    수행문장2:
	}else
	    수행문장3:
	    수행문장4:
	}

int month = (int)(Math.random()*12)+1;
int month = (int)(Math.random()*12)+1;
int month = (int)(Math.random()*12)+1
```

```java
if(조건식1)
     수행문장1;
else if(조건식2)
     수행문장2;
else if(조건식3)
     수행문장3;
        ;
else
     수행문장n;
     
switch(식) {
      case 비교값1 : 수행문장1;
                          수행문장2;
      case 비교값2 : 수행문장3;
                          수행문장4;
      case 비교값3 : 수행문장5;
                          수행문장6;
      case 비교값4 : 수행문장7;
                          수행문장8;
      default : 수행문장9;
   }

switch(식) {
      case 비교값1 : 수행문장1;
                          수행문장2;
                          break;
      case 비교값2 : 수행문장3;
                          수행문장4;
                          break;
      case 비교값3 : 수행문장5;
                          수행문장6;
      case 비교값4 : 수행문장7;
                          수행문장8;
		break;
      default : 수행문장9;                    
   }
  
   식 : int(byte,short,char), String


       

```
### 반복 구문

```java
while : 조건이 만족되는 동안 반복하려는 경우

for(초기식:조건식:증감식)
    반복문장
while(조건식)
    반복문장

for(변수의 선언 및 초기화;반복횟수를 결정할 조건식;변수의 값을 변화시키는 식)
ㄴ 반드시 세미콜론을 사용해줘야 한다!!!!!!!!!!!
ㄴ e.g. for(;;)  -> infinite loof!!!
ㄴ for(int i=1; i<10;i++)
ㄴ for(int i=1;i <= 10;i+=2)
ㄴ for(int num=1; num <= 9; num++)
	System.out.print(5*num + "     ")
ㄴ for(int n=5; n>0;n--)
	System.out.print(n)
ㄴ 식은 생략될 수 있지만 세미콜론은 생략될 수 없다!
```

```java
// 실습1 OperTest1
public class OperTest1 {
	public static void main(String[] args) {
		int num1 = 100, num2 = 50;
	
		System.out.println(num1 + num2);
		System.out.println(num1 - num2);
		System.out.println(num1 * num2);
		System.out.println(num1 / num2);
		System.out.println(num1 % num2);
		System.out.println(num1 > num2);
		System.out.println(num1 <= num2);
		System.out.println(num1 == num2);
		System.out.println(num1 != num2);
	}
}
```

```java
// 실습2 OperTest2
public class OperTest2 {
	public static void main(String[] args) {
		// 증감연산자 : 증가연산자(++), 감소연산자(--)
		int su1, su2, su3, su4;
		su1 = 10;
		System.out.println(su1);
		System.out.println(++su1);
		System.out.println(++su1);
		System.out.println(++su1);
		System.out.println(--su1);
		
		su2 = 10;
		System.out.println(su2);
		System.out.println(su2++);
		System.out.println(su2++);
		System.out.println(su2++);
		System.out.println(su2--);
		
		su3 = 10;
		System.out.println(su3);	//10
		System.out.println(su3++);	//10
		System.out.println(++su3);	//12
		System.out.println(su3++);	//12
		System.out.println(--su3);	//12
		System.out.println(--su3);	//11
		
		su4 = 10;
		System.out.println(su4);	//10
		++su4;
		System.out.println(su4);	//10
		su4++;
		System.out.println(++su4);	//12
		System.out.println(su4++);	//12
		System.out.println(--su4);	//12
		System.out.println(--su4);	//11
	}
}
```

```java
// 실습3 OperTest3
public class OperTest3 {
	public static void main(String[] args) {
		int ivalue;
		char cvalue;
		double dvalue;
		boolean bvalue;
		
		ivalue = 100;
		cvalue = 'A';
		dvalue = 3.14;
		bvalue = true;
		
		System.out.println(ivalue);
		System.out.println(cvalue);
		System.out.println(dvalue);
		System.out.println(bvalue);
		
		ivalue = cvalue;
		System.out.println(ivalue);
		
		ivalue = (int)dvalue; 			// 강제 형변환 연산자
		System.out.println(ivalue);
		
	}
}
```

- **실습4 문제**

[if 문 사용 실습 ]

1. OperAndLab(&&연산자사용), OperOrLab(||연산자사용) 
   이라는 클래스를 각각 하나씩 생성한다.
2. grade 라는 변수를 int 타입으로 선언하고 1 부터 6 사이의 숫자를 
   추출하고 저장한다.
3. grade 의 값이 1 또는 2 또는 3이면 다음 결과를 출력한다.
   "x 학년은 저학년입니다."
   grade 의 값이 4 또는 5 또는 6이면 다음 결과를 출력한다.
   "x 학년은 고학년입니다."

```java
//실습4 OperAndLab & OperOrLab
public class OperAndLab {
	public static void main(String[] args) {
		int grade = 0;
		grade = (int)(Math.random() * 6) + 1;
		
		if(grade >= 1 && grade <= 3) {
			System.out.println(grade + "학년은 저학년입니다.");
		}
		else{
			System.out.println(grade + "학년은 고학년입니다.");
		}
	}
}

public class OperOrLab {
	public static void main(String[] args) {
		int grade = 0;
		grade = (int)(Math.random() * 6) + 1;
		
		if(grade == 1 || grade == 2 || grade == 3) {
			System.out.println(grade + "학년은 저학년입니다.");
		}
		else {
			System.out.println(grade + "학년은 고학년입니다.");
		}
	}
}
```

- 실습5 문제**

[if 문 사용 실습]

1. ConditionOperLab 이라는 클래스를 생성한다.
2. 1부터 5사이의 랜덤값을 추출한다.
3. 추출된 값이 1이면 300 과 50 의 덧셈 연산을 처리한다.
   추출된 값이 2이면 300 과 50 의 뺄셈 연산을 처리한다.
   추출된 값이 3이면 300 과 50 의 곱센 연산을 처리한다.
   추출된 값이 4이면 300 과 50 의 나눗셈 연산을 처리한다.
   추출된 값이 5이면 300 과 50 의 나머지 연산을 처리한다.
4. 출력 형식(단, 결과를 출력하는 수행문장은 한 번만 구현한다.)
   결과값 : XX

```java
// 실습5 ConditionOperLab
public class ConditionOperLab {

	public static void main(String[] args) {
		int num = 300;
		int num2 = 50;
		int rand = (int)(Math.random() * 6) + 1;
		
		if(rand == 1) {
			System.out.println("결과값 : " + num + num2);
		}
		else if(rand == 2) {
			System.out.println("결과값 : " + (num - num2));
		}
		else if(rand == 3) {
			System.out.println("결과값 : " + num * num2);
		}
		else if(rand == 4) {
			System.out.println("결과값 : " + num / num2);
		}
		else if(rand == 5) {
			System.out.println("결과값 : " + num % num2);
		}
	}
}
```

- **실습6 문제**

[연산자 실습]

1. TimeTest 라는 클래스를 생성한다.
2. time 이라는 변수를 선언하여 32150(초) 이라는 값을 초기화 한다.   
3. time 변수의 값으로 "XX시간 XX분 XX초" 형식으로 변환하여 출력한다.

```java
// 실습6 TimeTest
public class TimeTest {

	public static void main(String[] args) {
		int time = 32150;
		int hour, minute, second;

		minute = time/60;
		hour = minute/60;
		second = time%60;
		minute = minute % 60;
				
		System.out.println(hour + "시간" + minute + "분" + second + "초");

	}

}
```

```java
//실습7 RandomTest
public class RandomTest {

	public static void main(String[] args) {
//		System.out.println(Math.random()); // 0.0 <= n < 1.0
		double rand1 = Math.random();
		System.out.println(rand1);
		double rand2 = rand1 * 100;
		System.out.println(rand2);
		int rand3 = (int)rand2;
		System.out.println(rand3); // 0 ~ 99
		
		// rand1을 가지고 1부터 6사이의 난수를 만드는 식을 구현하고
		// sixNum 변수에 담아서 출력해 보기
		int sixNum = (int)(rand1 * 6) + 1;
		System.out.println(sixNum);
		
		// rand1을 가지고 1부터 45사이의 난수를 만드는 식을 구현하고
		// lottoNum 변수에 담아서 출력해 보기
		int lottoNum = (int)(rand1 * 45) + 1;
		System.out.println(lottoNum);
	}

}
```

```java
//실습8 IfTest1
public class IfTest1 {

	public static void main(String[] args) {
		int num = (int)(Math.random()*10) + 1;
		if(num % 2 == 0) {
			System.out.println(num + " : 짝수");
		}
		else {
			System.out.println(num + " : 홀수");
		}
	}
}

```

```java
// 실습9 IfTest2
public class IfTest2 {

	public static void main(String[] args) {
		System.out.println("문장1");
		System.out.println("문장2");
		
		if((int)(Math.random()*10) + 1 > 5) {
			System.out.println("문장3");
		}
		else {
			System.out.println("문장4");
			System.out.println("문장5");
		}
		System.out.println("문장6");
		
	}
}
```

```java
// 실습10 IfTest3
public class IfTest3 {

	public static void main(String[] args) {
		int month = (int)(Math.random()*12) + 1;

		if(month == 12 || month == 1 || month == 2) {
			System.out.println(month + " : 겨울");
		}
		else if(month == 3 || month == 4 || month == 5) {
			System.out.println(month + " : 봄");
		}
		else if(month == 6 || month == 7 || month == 8) {
			System.out.println(month + " : 여름");
		}
		else if(month == 9 || month == 10 || month == 11) {
			System.out.println(month + " : 가을");
		}
		
	}
}
```

```java
// 실습11 IfTest4
public class IfTest4 {

	public static void main(String[] args) {
		int score = (int)(Math.random()*101);
		
		if(score >= 90) {
			System.out.print(score + " : A");
			if(score >= 97) {
				System.out.println("+등급");
			}
			else if(score >= 94) {
				System.out.println("0등급");
			}
			else {
				System.out.println("-등급");
			}
		}
		else if(score >= 80) {
			System.out.print(score + " : B");
			if(score >= 87) {
				System.out.println("+등급");
			}
			else if(score >= 84) {
				System.out.println("0등급");
			}
			else {
				System.out.println("-등급");
			}
		}
		else if(score >= 70) {
			System.out.print(score + " : C");
			if(score >= 77) {
				System.out.println("+등급");
			}
			else if(score >= 74) {
				System.out.println("0등급");
			}
			else {
				System.out.println("-등급");
			}
		}
		else if(score >= 60) {
			System.out.print(score + " : D");
			if(score >= 67) {
				System.out.println("+등급");
			}
			else if(score >= 64) {
				System.out.println("0등급");
			}
			else {
				System.out.println("-등급");
			}
		}
		else {
			System.out.println(score + " : F등급");
		}
		System.out.println("수행종료!!");		
	}
}
```

- **실습12 문제**

[switch 문 사용 실습 ]

1. OperAndLab.java를 복사해서 SwitchLab1.java를 생성한다.
2. 다음 기능을 if 문이 아닌 switch 문으로 변경하여 구현한다.
   grade 의 값이 1 또는 2 또는 3이면 다음 결과를 출력한다.
   "x 학년은 저학년입니다."
   grade 의 값이 4 또는 5 또는 6이면 다음 결과를 출력한다.
   "x 학년은 고학년입니다."

```java
// 실습12 SwitchLab1
public class SwitchLab1 {

	public static void main(String[] args) {
		int grade = 0;
		grade = (int)(Math.random() * 6) + 1;
		
//		if(grade >= 1 && grade <= 3) {
//			System.out.println(grade + "학년은 저학년입니다.");
//		}
//		else{
//			System.out.println(grade + "학년은 고학년입니다.");
//		}
		
		switch (grade) {
		case 1:
		case 2:
		case 3:
			System.out.println(grade + "학년은 저학년입니다.");
			break;
		case 4:
		case 5:
		case 6:
			System.out.println(grade + "학년은 고학년입니다.");
			break;
		}
			
	}

}
```

- **실습13 문제**

[switch 문 사용 실습 ]

1. ConditionOperLab.java를 복사해서 SwitchLab2.java를 생성한다.
2. 다음 기능을 if 문이 아닌 switch 문으로 변경하여 구현한다.
    추출된 값이 1이면 300 과 50 의 덧셈 연산을 처리한다.
    추출된 값이 2이면 300 과 50 의 뺄셈 연산을 처리한다.
    추출된 값이 3이면 300 과 50 의 곱센 연산을 처리한다.
    추출된 값이 4이면 300 과 50 의 나눗셈 연산을 처리한다.
    추출된 값이 5이면 300 과 50 의 나머지 연산을 처리한다.
3. 출력 형식(단, 결과를 출력하는 수행문장은 한 번만 구현한다.)
    결과값 : XX

```java
// 실습13 SwitchLab2
public class SwitchLab2 {

	public static void main(String[] args) {
		int num = 300;
		int num2 = 50;
		int rand = (int)(Math.random() * 5) + 1;
		int result = 0;

		switch(rand) {
			case 1:
				result = num + num2;
				break;
			case 2:
				result = num - num2;
				break;
			case 3:
				result = num * num2;
				break;
			case 4:
				result = num / num2;
				break;
			default:
				result = num % num2;
		}
		System.out.println(result);
	}
}
```

```java
// 실습14 SwitchTest1
public class SwitchTest1 {

   public static void main(String[] args) {
      int num=(int)(Math.random()*10)+1;
      switch(num%2) {
      case 0 : System.out.println(num +" : 짝수");
               break;
      case 1 : System.out.println(num +" : 홀수");
      }
   }
}
```

```java
// 실습15 SwitchTest2
public class SwitchTest2 {

   public static void main(String[] args) {
      int month = (int)(Math.random()*12)+1;
      
      switch(month) { //식:변수, 연산식, 리턴값이 있는 메서드의 호출식(int,String)
                           // 반드시 하나의 값만 지정 가능 in case 
      case 12 :
      case 1 :
      case 2 : System.out.println(month + "월은 겨울");
               break;
      case 3: 
      case 4:
      case 5: System.out.println(month + "월은 봄");
               break;
      case 6: 
      case 7:
      case 8: System.out.println(month + "월은 여름");
               break;
      default: System.out.println(month+ "월은 가을");
      }
   }
}
```

```java
// 실습16 SwitchTest3
public class SwitchTest3 {

	public static void main(String[] args) {
		int score = (int)(Math.random()*101);
		
		switch(score / 10) {
			case 10:
			case 9:System.out.println(score + " : A등급");
				break;
			case 8:System.out.println(score + " : B등급");
				break;
			case 7: System.out.println(score + " : C등급");
				break;
			case 6: System.out.println(score + " : D등급");
				break;
			default:
				System.out.println(score + " : F등급");
		}
		System.out.println("수행종료!!");
	}

}
```

# Day 3

``` java
L - value = r-value
(변수)        (식)

double    int
long       char
int         (int)double   
char       (char)int
```

l-value는 변수만 온다.
r-value는 식만 올 수 있다.
BUT 이 둘은 반드시 타입이 똑같아야한다.

둘이 타입이 다르면 형태를 반드시 변환해줘야한다.



l-value=r-value
변수      식
실수      정수
(자동으로 형이 변환된다)

- 자동 형 변환규칙.
   .without order, they are automaticallly chaning the type.
	rule 1. 정수에서 실수
	rule 2. 사이즉 적은 타입에서 큰 타입으로 !!!!


{see below for the size}
	byte                1
	short               2
	float int           4 
	double long      8

```java
   [e.g. 대입 연산]
double       ->         int
long          ->         char
int            ->    (int)double <= 이 친구는 강제로 형 변환 필요
char          ->    (char)int    

    c.f. boolean은 그 어떤 형태로 변환 할 수 없다!!

   [e.g. 식]
v1    +     v2
int          int         => int
long       long       => long
        float       float       => float
int         double    => doubl
int         char       => int
int         long       => long
long      float        => float

   c.f. char       char        => int
```

- 중첩된 for문 : 구구단

```java
상수; 초기화된 값이 고정되는 변수


for: 횟수에 반복, 값의 변화에 따른 반복
while: 조건에 따른 반복


for(초기식:조건식:증감식)
	반복문장

초기식:
while (조건식) {
	반복문장;
	증감식;
}
```

```java
// 실습 1 ForTest1
public class ForTest1 {

	public static void main(String[] args) {
		for(int num = 1; num <= 20; num++) {
			System.out.print(num +" ");
		}
		System.out.println();
		for(int num = 20; num >= 1; num--) {
			System.out.print(num + " ");
		}
		System.out.println();
		for(int num = 20; num >= 1; num-=3) {
			System.out.print(num + " ");
		}
		System.out.println();
		int num;
		for(num = 10; num >= 1; num-=3) {
			System.out.print(num + " ");
		}
		System.out.println();
		System.out.println(num);

	}
}
```

```java
// 실습2 ForTest2
public class ForTest2 {
   public static void main(String[] args) {

      for(int i=1;i<=50;i++) {
         System.out.println(Math.random()*10);
      }
   }
}
```

```java
//실습 3 ForTest3
public class ForTest3 {
   public static void main(String[] args) {
      for(int i=1;i<=50;i++) {
         System.out.println(Math.random()*10);
      }

   }
}
```

```java
// 실습4 ForTest4
public class ForTest4 {

	public static void main(String[] args) {
		// 10부터 1까지의 숫자에 대하여 숫자값과 해당 숫자의 제곱값을
		// 행단위로 출력해 보자

		for (int n = 10; n >= 1; n--) {
			System.out.println(n + " : " + n * n);
		}
		System.out.println("-----------------");
		// 10부터 20까지의 숫자에 대하여 3씩 증가시키면서 숫자값과
		// 해당 숫자의 제곱값을 행단위로 출력해 보자
		for (int n = 10; n <= 20; n+=3) {
			System.out.println(n + " : " + n * n);
		}
		System.out.println("-----------------");

	}
}
```

```java
// 실습5 ForTest5
public class ForTest5 {

	public static void main(String[] args) {
		// 1부터 10까지의 합을 출력
		int sum = 0;
	
		 for(int n = 1; n <= 10; n++) { sum = sum + n; } 
		 System.out.println("sum = " + sum);
		 
		 for(int n = 1; n <= 10; n++) { 
			 sum = sum + n;
			 System.out.println("sum = " + sum);
		 } 
	}
}
```

```java
// 실습6 ForTest6
public class ForTest6 {
	public static void main(String[] args) {
		// A ~ Z 까지 출력해 보자
		char munja = 'A';
		for (int i = 1; i <= 26; i++) {
			System.out.print(munja++ + " ");
		}
		System.out.println("\n------------------------");
		for (munja = 'A'; munja <= 'Z'; munja++) {
			System.out.print(munja + " ");
		}
		System.out.println("\n------------------------");
		munja = 'A';
		for (int i = 1; i <= 26; i++) {
			System.out.print(munja + " ");
			munja += 1;
		}
		System.out.println("\n------------------------");
		munja = 'A';
		for (int i = 1; i <= 26; i++) {
			System.out.print(munja + " ");
			munja = (char)(munja + 1); // 괄호로 묶어 주지 않으면 연산자 우선 순위 때문에 error난다.
		}
		System.out.println("\n------------------------");
	}
}
```

```java
// 실습7 ForTest7
public class ForTest7 {

	public static void main(String[] args) {
		for(int dan = 1; dan <= 9; dan++) {
			for(int num = 1; num <= 9; num++) {
				System.out.print(dan + "x" + num + "="+dan*num +'\t');
			}
			System.out.println();
		}
	}
}

```

```java
// 실습8 ForTest8
public class ForTest8 {

	public static void main(String[] args) {
		for(int dan = 1; dan <= 9; dan++) {
			for(int num = 1; num <= 9; num++) {
				System.out.print(dan+"x"+num+"="+dan*num+"\t");
			}
			System.out.println();
		}
	}
}
```

```java
// 실습9 ForTest9
public class ForTest9 {

	public static void main(String[] args) {
		final char DECO = '&';
		int rand = (int)(Math.random()*6 + 5);
		
		for(int i = 1; i <= rand; i++) {
			for(int j = 1; j <= i; j++) {
				System.out.print(DECO);
			}
			System.out.println();
		}
	}
}
```

```java
// 실습10 WhileTest1
public class WhileTest1 {

	public static void main(String[] args) {
		int sum = 0;
		int i = 0;
		while(sum < 100) {
			i = (int)(Math.random()*50) + 1;
			sum += i;
			System.out.println("sum = " + sum);
		}
	}
}
```

```java
// 실습11 WhileTest2
public class WhileTest2 {

	public static void main(String[] args) {
		System.out.println("main() 수행 시작");
		char munja = '가';
		while(munja <= '나') {
			System.out.println(munja);
			munja++;
		}
		System.out.println("main() 수행 종료");
	}
}
```

```java
// 실습12 WhileTest3
public class WhileTest3 {
	public static void main(String[] args) {
		int lottoNum;
		while(true) {
			lottoNum = (int)(Math.random() * 6) + 1;
			if(lottoNum == 3) {
				System.out.println("당첨!! ㅋㅋㅋ : " + lottoNum);
				break;
			}
			else {
				System.out.println("재시도!! ㅠㅠㅠ : " + lottoNum);
			}
		}
		System.out.println("수행 종료..." + lottoNum);
	}
}
```

- ****

  **실습13 문제**

1. ForLab1 이라는 클래스를 만든다.

2. 다음과 같은 결과가 출력되도록 구현한다.

   1 2 3 4 5 6 7 8 9 10

```java
// 실습13 ForLab1
public class ForLab1 {
	public static void main(String[] args) {
		for(int i = 1; i <= 10; i++) {
			System.out.print(i + " ");
		}
		System.out.println();

	}
}
```

- **실습14 문제**

1. ForLab2 이라는 클래스를 만든다.
2. 다음과 같은 결과가 출력되도록 구현한다.

    9 : 홀수
    8 : 짝수
    7 : 홀수
    6 : 짝수
    5 : 홀수
    4 : 짝수

```java
// 실습14 ForLab2
public class ForLab2 {
	public static void main(String[] args) {
		for(int i = 9; i >= 4; i--) {
			if(i % 2 == 0) {
				System.out.print(i + " : 짝수");				
			}
			else {
				System.out.print(i + " : 홀수");
			}
		}
		System.out.println();
	}
}
```

- **실습15 문제**

1. ForLab3 이라는 클래스를 만든다.
2. 1부터 10사이의 난수를 하나 추출한다.
3. 30부터 40사이의 난수를 하나 추출한다.
4. 첫번째 난수부터 두번째 난수 까지의 숫자들 중에서 짝수의 합을 구해
    다음 형식으로 출력한다.

    X 부터 Y 까지의 짝수의 합 : XX

```java
// 실습15 ForLab3
public class ForLab3 {
	public static void main(String[] args) {
		// rand 범위 설정
		// 곱셈의 수는 최댓값 - 최솟값 + 1
		// 덧셈의 수는 최솟값
		int randValue1 = (int)(Math.random() * 10 + 1); 
		int randValue2 = ((int)(Math.random() * 11) + 30); // 30 ~ 40
		int sum = 0;
		

		for(int i = randValue1; i <= randValue2; i++) {
			if(i % 2 == 0) {
				sum += i;
			}
		}
		System.out.println("X 부터 Y 까지의 짝수의 합 :" + sum);
	}
}
```

- **실습16 문제**

1. ForLab4 이라는 클래스를 만든다.
2. 3부터 10사이의 난수를 추출한다.(첫 번째 난수)
3. 1부터 3사이의 난수를 추출한다.(두 번째 난수)
4. 두 번째 난수값이 1이면 "*"을 첫 번째 난수값의 갯수로 하나의 행에 출력한다.
    두 번째 난수값이 2이면 "$"을 첫 번째 난수값의 갯수로 하나의 행에 출력한다.
    두 번째 난수값이 3이면 "#"을 첫 번째 난수값의 갯수로 하나의 행에 출력한다.

```java
// 실습16 ForLab4
public class ForLab4 {
	public static void main(String[] args) {
		int randValue1 = (int)(Math.random() * 8 + 3);// + randTemp;
		int randValue2 = (int)(Math.random() * 3 + 1);
	
//		System.out.println(randValue1);
//		System.out.println(randValue2);
		if(randValue2 == 1) {
			for(int i = 0; i < randValue1; i++) {
				System.out.print("*");				
			}
			System.out.print("\n");
		}
		else if(randValue2 == 2) {
			for(int i = 0; i < randValue1; i++) {
				System.out.print("$");				
			}
			System.out.print("\n");
		}
		else if(randValue2 == 3) {
			for(int i = 0; i < randValue1; i++) {
				System.out.print("#");				
			}
			System.out.print("\n");
		}
	}
}
```

- **실습17 문제**

1. ForLab5 이라는 클래스를 만든다.
2. int 타입으로 evenNum 변수와 oddNum 변수를 선언한다.
3. 1 부터 100 까지의 값 중에서 
   짝수의 합은 evenNum 에 누적하고 
   홀수의 합은 oddNum 에 누적한다.
4. 수행 결과는 다음과 같이 출력한다.

    1부터 100까지의 숫자들 중에서 
    짝수의 합은 XXX 이고 
    홀수의 합은 YYY 이다.

```java
// 실습17 ForLab5
public class ForLab5 {
	public static void main(String[] args) {
		int evenNum = 0;
		int oddNum = 0;
		
		for(int i = 1; i <= 100; i++) {
			if(i % 2 == 0) {
				evenNum += i;
			}
			else {
				oddNum += i;
			}
		}
		System.out.println("1부터 100까지의 숫자들 중에서");
		System.out.println("짝수의 합은 " + evenNum + " 이고");
		System.out.println("홀수의 합은 " + oddNum + " 이고");
	}
}
```

- **실습18 문제**

[모양 출력(중첩 for)]

1. ForLab6 라는 클래스를 만든다.
2. char 타입으로 상수를 하나 만들어 '&'로 초기화 한다.
3. 5부터 10사이의 난수를 하나 추출한다.
4. 추출된 숫자가 5라면 반복문을 사용하여 다음과 같이 출력한다.

	&
	&&
	&&&
	&&&&
	&&&&&
   
     추출된 숫자가 7이라면 반복문을 사용하여 다음과 같이 출력한다.

	&
	&&
	&&&
	&&&&
	&&&&&
	&&&&&&
	&&&&&&&

```java
// 실습18 ForLab6
public class ForLab6 {

	public static void main(String[] args) {
		final char DECO = '&';
		int rand = (int)(Math.random()*6 + 5);
		
		for(int i = 1; i <= rand; i++) {
			for(int j = 1; j <= i; j++) {
				System.out.print(DECO);
			}
			System.out.println();
		}

	}

}

```

- **실습19 문제**

[모양 출력(중첩 for)]

1. ForLab7 라는 클래스를 생성한다.
2. STAR 라는 상수를 만든고 '*'으로 초기화 한다.
3. 다음과 같은 결과가 되도록 구현한다.

    *******
    ******
    *****
    ****
    ***
    **
    *
```java
// 실습19 ForLab7
public class ForLab7 {

	public static void main(String[] args) {
		final char STAR = '*';
		for(int i = 1; i <= 7; i++) {
			for(int j = 7; j >= i; j--) {
				System.out.print(STAR);
			}
			System.out.println();
		}
	}
}
```

- **실습20 문제**

[모양 출력(중첩 for)]

1. ForLab8 라는 클래스를 생성한다.
2. 다음과 같은 결과가 되도록 구현한다.

    	A
	BC
	DEF
	GHIJ
	KLMNO

```java
// 실습20 ForLab8
public class ForLab8 {
	public static void main(String[] args) {
		char STAR = 'A';
		for(int i = 1; i <= 5; i++) {
			for(int j = 1; j <= i; j++) {
				System.out.print(STAR++);
			}
			System.out.println();
		}
	}
}
```

- **실습21 문제**

1. WhileLab1 라는 클래스를 생성한다.
2. 5부터 10사이의 난수를 추출한다.
3. 1부터 추출된 숫자값까지의 각 숫자들의 제곱값을 행단위로 출력한다.
   (하나의 클래스안에 for 와 while 로 각각 구현한다.)
   ===>  7이 추출되면
    [ for 결과 ]
     1 -> 1
     2 -> 4
     3 -> 9
     4 -> 16
     5 -> 25
     6 -> 36
     7 -> 49
    [ while 결과 ]
     1 -> 1
     2 -> 4
     3 -> 9
     4 -> 16
     5 -> 25
     6 -> 36
     7 -> 49

```java
// 실습21 WhileLab1
public class WhileLab1 {
	public static void main(String[] args) {
		int rand = (int)(Math.random()* 6 + 5);
		System.out.println("[for 결과]");
		for(int i = 1; i <= rand; i++) {
			System.out.println(i + " -> " + i * i);
		}
		System.out.println("[while 결과]");
		int i = 1;
		while(i <= rand) {
			System.out.println(i + " -> " + i * i);
			i++;
		}	
	}
}
```

- **실습22 문제**

1. WhileLab2 이라는 클래스를 생성한다.
2. 다음 기능을 반복해서 수행하는 프로그램을 구현하며
    반복문으로 while 문을 사용한다.

    1부터 6사이의 두개 난수를 추출하여 각각 pairNum1, pairNum2 에 저장한다.

    추출된 두 개의 숫자가 서로 다르면 값의 크기를 비교하여 
    "pairNum1이 pairNum2 보다 크다." 또는 "pairNum1이 pairNum2 보다 작다." 
    출력한다.
    
    추출된 두 개의 숫자가 동일하면 "게임 끝"이라는 메시지를 출력하고 종료한다.

```java
// 실습22 WhileLab2
public class WhileLab2 {
	public static void main(String[] args) {
		while (true) {
			int pairNum1 = (int) (Math.random() * 6 + 1);
			int pairNum2 = (int) (Math.random() * 6 + 1);
			if (pairNum1 != pairNum2) {
				if (pairNum1 > pairNum2) {
					System.out.println("pairNum1이 pairNum2 보다 크다.");
				} else {
					System.out.println("pairNum1이 pairNum2 보다 작다.");
				}
			} else {
				System.out.println("게임끝");
				break;
			}
		}
	}
}
```

- **실습23 문제**

[while 문으로 무한루프 처리]

1. WhileLab3 라는 클래스를 생성한다.
2. 0부터 30사이의 난수를 추출한다.
    추출된 숫자가 1이면 'A', 2 이면 'B', ... 26이면 'Z' 를 출력하는데
    계속 난수 추출과 출력을 반복하다가 난수가 0이 추출되거나
    27~30이 추출되면 반복을 끝낸다.

    반복하는 동안 출력형식 :  	B(2)
    												 A(1)
													 D(4)
			  										  :
    마지막에는 "수행횟수는 x 번입니다"를 출력하고 종료한다.

```java
// 실습23 WhileLab3
public class WhileTest3 {

	public static void main(String[] args) {
		int lottoNum;
		while(true) {
			lottoNum = (int)(Math.random() * 6) + 1;
			if(lottoNum == 3) {
				System.out.println("당첨!! ㅋㅋㅋ : " + lottoNum);
				break;
			}
			else {
				System.out.println("재시도!! ㅠㅠㅠ : " + lottoNum);
			}
		}
		System.out.println("수행 종료..." + lottoNum);
	}
}

```

# Day4

[자바의 산술 이항 연산의 특징] - 교재 92 페이지

   (1) int 타입보다 작은 타입들(byte, short, char)은 int 타입으로 변환하여 연산
   (2) 두 항의 타입이 다를 때 하나로 일치해서 연산(표현 범위가 적은 타입에서 큰타입으로)

```java
    표현 범위의 관계 : int < long < float < double
```

[배열: array]

- 동일한 타입의 데이터들의 집합

- 배열을 만드는 방법

- 배열을 사용하는 방법

- 여러개의 데이터들을 프로그램에서 다뤄야 할 때 변수를 여러개 선언하여 사용하는 것은 비효율적이다. (코딩, 수행)

- 배열을 만드는 방법
   - 배열로 구성하려는 데이터들의 타입
   - 배열로 구성하려는 데이터들의 최대 갯수

	new 데이타타입[크기]
	
	```java
	new int [10] --------- 0
	new char [26] ------- '\u0000'
	new double [5] ----- 0.0
	new long [1]    ----- 0L
new boolean[10] --- false
	
	{값1, 값2, 값3 ...}
	{10,20,30}, {4,1,5,7,8,1,3}, {'a', 'b', 'c'), {true}
	```

- 배열을 사용하는 방법
    배열을 사용하기 위해서는 배열을 만든 다음 변수에 담는다.
    배열변수가 필요하다.

```java
타입[] 변수명; 타입 변수명 [];
	int a1[]; int[] a2' char[] a3; boolean a4[];
	
	int a1[] = new int [10];
	int a2[] = {10, 20,30};

	a1[0], a1[1], a2[1].........a1[9]

	배열변수명 [인덱스] // 인덱스는 0부터 지정
	배열을 구성하는 데이터들 : " 엘리먼트(element)", 요수, 원소
	배열변수.length : 배열변수 대입된 배열의 요소갯수
	
	System.out.println(a1[0]);
	System.out.println(a1[1]);
	System.out.println(a1[2]);

	System.out.println(a1[9]);

	a1[0] = 1000;
	a1[1] = 999;
	a1[9] += 10;

	for (int i=0;i<a1.length: i++)
        System.out.println(a1[i]);
```
```java
// 실습1 CharacterTest1
public class CharacterTest1 {
	public static void main(String[] args) {
		char v1 = 65;
		char v2 = 'A';
		char v3 = 0x41; // 영(공)엑스
		char v4 = '\u0041'; // 유니코드
		System.out.println((char)(v1+1)); // 형변환 (타입명)
		System.out.println((char)(v2+1));
		System.out.println((char)(v3+1));
		System.out.println((char)(v4+1));
		
		System.out.println();
		System.out.println((++v1)); // 형변환 (타입명)
		System.out.println((++v2));
		System.out.println((++v3));
		System.out.println((++v4));
		
		System.out.println();
		System.out.println((v1+=1)); // 형변환 (타입명)
		System.out.println((v2+=1));
		System.out.println((v3+=1));
		System.out.println((v4+=1));
		
		System.out.println();
		int v5 = 65;
		int v6 = 'A';
		int v7 = 0x41;
		int v8 = '\u0041';
		System.out.println(v5);
		System.out.println(v6);
		System.out.println(v7);
		System.out.println(v8);
	}
}
```

```java
// 실습2 ArrayTest1_1
//foreach
public class ArrayTest1_1 {

	public static void main(String[] args) {
		int a1[] = new int[10];
		System.out.println(a1.length);
		int a2[] = {10, 20, 30};
		System.out.println(a2.length);
		
		//System.out.println();
		for(int i = 0; i < a1.length; i++) {
			System.out.print(a1[i] + " ");
		}
		System.out.println();
		for(int data : a1) {
			System.out.print(data + " ");
		}
		System.out.println();
		for(int i = 0; i < a2.length; i++) {
			System.out.print(a2[i] + " ");
		}
		System.out.println();
		for(int data : a2) {
			System.out.print(data + " ");
		}
		System.out.println();
		
		for(int i = 0; i < a1.length; i++) {
			a1[i] = (i + 1) * 100;
		}
		System.out.println();
		for(int i = 0; i < a1.length; i++) {
			System.out.print(a1[i] + " ");
		}
		System.out.println();
		for(int data : a1)
			System.out.print(data + " ");
		System.out.println();
//		a2[3] = 100;

	}
}
```

```java
// 실습3 ArrayTest1
public class ArrayTest1 {

	public static void main(String[] args) {
		int a1[] = new int[10];
		System.out.println(a1.length);
		int a2[] = {10, 20, 30};
		System.out.println(a2.length);
		
		//System.out.println();
		for(int i = 0; i < a1.length; i++) {
			System.out.print(a1[i] + " ");
		}
		System.out.println();
		for(int i = 0; i < a2.length; i++) {
			System.out.print(a2[i] + " ");
		}
		
		for(int i = 0; i < a1.length; i++) {
			a1[i] = (i + 1) * 100;
		}
		System.out.println();
		for(int i = 0; i < a1.length; i++) {
			System.out.print(a1[i] + " ");
		}
//		a2[3] = 100;
	}
}
```

```java
// 실습4 ArrayTest2
public class ArrayTest2 {

	public static void main(String[] args) {
		int a1[] = new int[5];
		a1[0] = 33;
		a1[1] = 20;
		a1[2] = 15;
		a1[3] = 40;
		a1[4] = 7;
		System.out.println(a1[0]);
		System.out.println(a1[a1.length - 1]);
		
		for(int i = a1.length-1; i>= 0; i--) {
			System.out.print(a1[i] + " ");
		}
		System.out.println();
		
		for(int i = 0; i < a1.length; i+=2) {
			System.out.print(a1[i] + " ");
		}
		System.out.println();
	}
}
```

```java
// 실습5 ArrayTest3
public class ArrayTest3 {

	public static void main(String[] args) {
		int a1[] = {3, 10, 2, 9, 5, 11, 12, 1};
		int max;
		// a1 배열변수에 할당된 배열의 요소중 최댓값
		max = a1[0];
		for(int i = 1; i < a1.length; i++) {
			if(a1[i] > max) {
				max = a1[i];
			}
		}
		System.out.println("최댓값 : " + max);
		int min;
		// a1 배열변수에 할당된 배열의 요소중 최솟값
		min = a1[0];
		for(int i = 1; i < a1.length; i++) {
			if(a1[i] < min) {
				min = a1[i];
			}
		}
		System.out.println("최솟값 : " + min);
	}
}
```

```java
// 실습6 ArrayTest4
public class ArrayTest4 {

	public static void main(String[] args) {
		int a1[] = {3, 10, 2, 9, 5, 11, 12, 1};
		
		// a1 배열변수에 할당된 배열의 요소중 최댓값
		
		for(int i = 0; i < a1.length; i+=2) {
			System.out.println(a1[i] + " ");
		}
			System.out.println();
	}
}
```

```java
// 실습7 BreakTest
public class BreakTest {

	public static void main(String[] args) {
		//boolean flag = false;
		done: for(int dan = 1; dan <= 9; dan++) {
			for(int num = 1; num <= 9; num++) {
				if(dan*num > 30) {
					//flag = true;
					break done;
				}
				System.out.print(dan+"x"+num+"="+dan*num+"\t");
			}
			System.out.println();
			//if(flag == true) break;
		}
	}
}
```

- **실습8 문제**

1. ArrayLab1 이라는 클래스를 하나 만든다.
2. ary 라는 int 타입의 배열 변수를 선언하고 10개의 엘리먼트를 갖는 배열을 생성하여 대입한다.
3. 배열의 값들을 하나의 행에 다음 형식으로 출력한다.
   0 0 0 0 0 0 0 0 0 0
4. 생성된 배열에 10, 20, 30, 40, 50, 60, 70, 80, 90, 100 을 각각의 element 로 저장한다.
5. 배열의 값들을 하나의 행에 다음 형식으로 출력한다.
   10 20 30 40 50 60 70 80 90 100
6. 배열의 값들을 하나의 행에 다음 형식으로 출력한다.
   100 90 80 70 60 50 40 30 20 10
7. 배열의 값들을 하나의 행에 다음 형식으로 출력한다.
   20 40 60 80 100

```java
// 실습8 ArrayLab1
public class ArrayLab1 {

	public static void main(String[] args) {
		int ary[] = new int[10];
		for(int i = 0; i < 10; i++) {
			System.out.print(ary[i] + " ");
		}
		System.out.println();
		for(int i = 0; i < 10; i++) {
			ary[i] = (i + 1) * 10;
		}
		for(int i = 0; i < 10; i++) {
			System.out.print(ary[i] + " ");
		}
		System.out.println();
		for(int i = 9; i >= 0; i--) {
			System.out.print(ary[i] + " ");
		}
		System.out.println();
		for(int i = 1; i < 10; i+=2) {
			System.out.print(ary[i] + " ");
		}
	}
}
```

- **실습8 문제**

1. ArrayLab2 라는 클래스를 하나 만든다.
2. 10개의 숫자(정수)를 저장할 수 있는 배열을 하나 만든다.
3. 각각의 원소에  4부터 20사이의 난수를 추출하여 저장한다.
4. 모든 원소의 합을 구한다.
5. 다음과 같은 형식으로 출력한다.

    모든 원소의 값 : x,x,x,x,x,x,x,x,x,x
    모든 원소의 합 : x

```java
// 실습9 ArrayLab2
public class ArrayLab2 {
	public static void main(String[] args) {
		int arr[] = new int[10];
		int rand;
		int sum = 0;
		System.out.print("모든 원소의 값  : ");
		for(int i = 0; i < 10; i++) {
			rand = (int)(Math.random()*17 + 4);
			arr[i] = rand; 
			System.out.print(arr[i]);
			if(i == 9) break;
			System.out.print(", ");
		}
		System.out.println();
		for(int i = 0; i < 10; i++) {
			sum += arr[i];
		}
		System.out.println("모든 원소의 합  : " + sum);
	}
}

```

- **실습10 문제**

1. ArrayLab3 라는 클래스를 하나 만든다.
2. 'J', 'a', 'v', 'a' 라는 원소들로 구성되는 char 타입의 배열을
   만든다.
3. 각 원소들의 값에서 대문자는 소문자로 소문자는 대문자로 
    변환한다.
4. 수행 결과 :

    변환된 배열 : j,A,V,A

```java
// 실습10 ArrayLab3
public class ArrayLab3 {

	public static void main(String[] args) {
		char arr[] = {'J', 'a', 'v', 'a'};
		
		for(int i = 0 ; i < arr.length; i++) {
			if(arr[i] >= 'a' && arr[i] <= 'z') {
				arr[i] -=32;
			}
			else if(arr[i] >= 'A' && arr[i] <= 'Z') {
				arr[i] +=32;
			}
		}
		
		System.out.print("변환된 배열 : ");
		for(int i = 0; i < arr.length; i++) {
			if(i != arr.length - 1) System.out.print(arr[i] + ", ");
			else System.out.println(arr[i]);
		}
	}
}
```

- **실습11 문제**

1. ArrayLab4 이라는 클래스를 하나 만든다.
2. 10 개의 원소를 갖는 int 타입의 배열을 생성한 후에 이 배열의 
   각각의 원소값으로 1부터 26 사이의 난수를 추출하여 저장한다.
3. 10개의 원소를 갖는 char 타입의 배열을 생성한다.
4. 2번에서 생성한 배열의 각각의 원소값의 3번에서 생성한 배열의
   원소값으로 저장하는데 이 때는 
   1이면 'A', 2 이면 'B', ... 26이면 'Z'를 저장한다.
5. 두 배열의 원소값을 다음과 같이 출력한다.

    10,1,3,21,6,8,11,26,22,19
    J,A,C,U,F,H,K,Z,V,S

```java
// 실습11 ArrayLab4
public class ArrayLab4 {
	public static void main(String[] args) {
		int arr[] = new int[10];
		char arrChar[] = new char[10];
		for(int i = 0; i < 10; i++) {
			arr[i] = (int)(Math.random()*26 + 1);
			if(i != 9) System.out.print(arr[i] + ", ");
			else System.out.print(arr[i]);
		}
		
		System.out.println();
		for(int i = 0; i < 10; i++) {
			arrChar[i] = (char)(arr[i] + '@');
			if(i != 9) System.out.print(arrChar[i] + ", ");
			else System.out.print(arrChar[i]);
		}
	}
}
```

# Day5

new 타입[행의크기][열의크기]

타입[][] 변수명;
타입 변수명[][];
타입[] 변수명[];

가변비율
행마다 열의 개수를 다르게 가져갈 수 있다.!!!

new 타입[행의크기][]

```java
int[][] emp = new int[5][];
emp[0] = new int[10];
emp[1] = new int[20];
emp[2] = new int[50];
```

가변배열!

### for each

for(Java 5) : for each 문

- 배열 또는 컬렉션 객체의 데이터들을 꺼내서 반복처리하려는 경우 사용하는 반복문이다.
- 앞에서부터 차례대로 하나하나 꺼내서 처리하려는 경우!

```java
for(변수선언 : 배열 또는 콜렉션 객체)]
     반복문장; 

for( int data : score)
     sum += data;
```

- **실습1 문제**

자바의 제어문 ~ 기본 배열

1. LottoMachine1 이라는 클래스를  생성한다.
2. 1부터 45 사이의 6개를 추출하여 다음 형식으로 출력한다.
    단, 6개 숫자는 중복을 허용하지 않는다.

    [ 출력형식 ]

    오늘의 로또 번호 - x, x, x, x, x, x

6개의 배열을 갖는 원소를 만들기
int a1[] = new int[6];

random[i] = (int)(Math.random()*46)+1;

1. 난수추출
2. 체크하기
3. 넣기 또는 넣지 않고 다음 반복으로 
-------------------------
