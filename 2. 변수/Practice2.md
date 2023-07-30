## 2-1
**기본형(primitive type)**
* 논리형
  - boolean (1 byte)
* 문자형
  - char (2 byte)
* 정수형
  - byte (1 byte)
  - short (2 byte)
  - int (4 byte)
  - long (8 byte)
* 실수형
  - float (4 byte)
  - double (8 byte)

---
## 2-2
```
long regNo = 1212123434343L;
```
int형의 범위(-2,147,483,648 ~ 2,147,483,647)를 벗어나기 때문에 long타입을 사용해야한다

---
## 2-3
* 리터럴: 100, 100L, 3.14f
* 변수: i, l
* 키워드: int, long, final, float
* 상수: PI

---
## 2-4
Byte  
ㄴ 기본형인 byte와 헷갈리지 말것!

---
## 2-5
```
1 System.out.println("1" + "2")   → (12 )   // 문자열 + 문자열 = 문자열
2 System.out.println(true + "")   → (true ) // 예약어 + 문자열 = 문자열
3 System.out.println('A' + 'B')   → (131 )  // 65 + 66
4 System.out.println('1' + 2)     → (51 )   // 49 + 2
5 System.out.println('1' + '2')   → (99 )   // 49 + 50
6 System.out.println('J' + "ava") → (Java ) // 문자 + 문자열 = 문자열 
7 System.out.println(true + null) → (오류 )
```
1, 2, 6<br>
문자열과 덧셈연산을 하면 그 결과는 항상 문자열이 된다<br>
```
문자열 + any type = 문자열
```
3, 4, 5<br>
문자와 문자의 연산은 int형으로 변환된 후에 연산이 진행되기 때문에<br>
문자코드(아스키코드)값으로 변환 후 연산이 된다 (예: A = 65)

---
## 2-6
```
b. True
c. NULL
d. Class
e. System
```

---
## 2-7
```
a. $ystem
d. lf
g. $MAX_NUM
```
특수문자 '_' , '$'만 허용한다

---
## 2-8
참조형 변수의 크기는 **4byte** 이므로 기본형 int, float와 같다

---
## 2-9
형변환  
d, e
```
byte b = 10;
char ch = 'A';
int i = 100;
long l = 1000L;
-------------------------
a. b = (byte)i;
b. ch = (char)b;
c. short s = (short)ch;
d. float f = (float)l;
e. i = (int)ch;
```
a. int(4byte) → byte(1byte)이므로 반드시 형변환이 필요하다<br>
b. byte(1byte) → char(2byte)이지만 범위가 달라서 형변환이 필요하다<br>
c. char,short은 2byte이지만 범위가 달라서 형변환이 필요하다<br>
d. float(4byte)의 범위가 long(8byte)보다 커서 생략가능하다<br>
e. char(2 byte) → int(4byte)이므로 생략가능하다

---
## 2-10
char타입이 자정할 수 있는 값의 범위 ( 0 ~ 65535 = 65536개)

---
## 2-11
a, b, c, d
```
a. byte b = 256;
b. char c = '';
c. char answer = 'no';
d. float f = 3.14
e. double d = 1.4e3f;
```
a. byte의 범위(-128~127)를 넘는 값으로 초기화 할 수 없다  
b. char는 반드시 한 개의 문자를 지정해야한다  
c. char는 두 개 이상의 문자를 저장할 수 없다 (문자 '', 문자열 "")  
d. 3.14는 3.14d의 생략된 형태이므로 접미사f를 붙이거나 형변환이 필요하다  
e. double(8byte)에 float값(4byte)을 넣는 것이므로 가능하다  

---
## 2-12
main메서드의 선언부
```
a. public static void main(String[] args)
b. public static void main(String args[])
c. public static void main(String[] arv)  // 매개변수 args의 이름은 달라도 된다
d. public void static main(String[] args) // void는 반드시 main앞에 와야 한다
e. static public void main(String[] args) // public과 static은 위치가 바뀌어도 된다
```
a, b, c, e

---
## 2-13
타입의 기본값
```
a. boolean - false
b. char - '\u0000'
c. float - 0.0
d. int - 0
e. long - 0
f. String - ""
```
c. float - 0.0f  
e. long - 0L  
f. String은 참조형 타입. 모든 참조형 타입의 기본값은 null  



