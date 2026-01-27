# 변수 Variable

자료를 저장하기 위한 메모리 공간

자바의 변수는 데이터 형태 즉 타입으로 구분

타입에 따라 메모리 공간의 크기가 달라지며 크게 2가지로 분류

## 기본형 Primitive Type

| 구분   | Type    | bit 수 | 값                                                            |
| ------ | ------- | ------ | ------------------------------------------------------------- |
| 논리형 | boolean | -      | true / false                                                  |
| 정수형 | byte    | 8      | -2^7 ~ 2^7-1 (-128 ~ 127)                                     |
| 정수형 | short   | 16     | -2^15 ~ 2^15-1 (-32768 ~ 32767)                               |
| 정수형 | int     | 32     | -2^31 ~ 2^31-1 (-2147483648 ~ 2147483647)                     |
| 정수형 | long    | 32     | -2^63 ~ 2^63-1 (-9223372036854775808L ~ 9223372036854775807L) |
| 실수형 | float   | 32     | float f=0.123...789F;                                         |
| 실수형 | double  | 64     | double d=0.123...789;                                         |
| 문자형 | char    | 16     | /u0000 ~ /uffff ( 0~2^16-1) - Unicode 지원                    |

## 참조형

### String

문자열을 저장할 수 있는 참조형 변수

#### 생성

- literal 할당

문자열 풀(String Pool)에 저장

```java
String str1 = "Hello";
String str2 = "Hello";

str1 == str2 // true
```

#### String 생성자 메서드 사용

- 힙 (Heap)에 저장

```java
String str3 = new String("Hello");
String str4 = new String("Hello");

str3 == str4 // false
```

#### Text Block

```java
String str = """
내 이름은 %s.
나이는 %d살이고, 사는 곳은 %s.
""".formatted("홍길동", 20, "서울");

System.out.println(str);

// 내 이름은 홍길동.
// 나이는 20살이고, 사는 곳은 서울.
```
