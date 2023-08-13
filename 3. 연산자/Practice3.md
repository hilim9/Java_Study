## 3-1
```
public static void main(String[] args) {
      int x = 2;
      int y = 5;
      char c = 'A';
      System.out.println(1 + x << 33);  // 6
      System.out.println(y >= 5 || x < 0 && x > 2); // true || false && false -> true || false = false
      System.out.println(y += 10 - x++); // 15 -2 = 13
      System.out.println(x+=2); // 5 = 3 + 2
      System.out.println( !('A' <= c && c <='Z') ); !(true && true) = false
      System.out.println('C'-c); // 67 - 65 = 2
      System.out.println('5'-'0'); // 53 - 48 = 5
      System.out.println(c+1); // 65 + 1 = 66
      System.out.println(++c); // B
      System.out.println(c++); // B
      System.out.println(c); // C
    }
}
```

---
## 3-2
사과를 담는데 필요한 바구니의 수를 구하는 코드
```
public static void main(String[] args) {
      int numOfApples = 123; // 사과의 개수
      int sizeOfBucket = 10; // 바구니의 크기(바구니에 담을 수 있는 사과의 개수)
      int numOfBucket = ( 빈칸에 들어갈 코드는? )
      
      System.out.println("필요한 바구니의 수 :"+numOfBucket);
      }
}
```
numOfApples / sizeOfBucket + (numOfApples % sizeOfBucket > 0 ? 1 : 0) ;

numOfApples / sizeOfBucket 연산을 했을 때 바구니의 수는 12가 나온다  
하지만 3개가 남기 때문에 13개가 필요하다  
그래서 나머지 연산자를 이용하여 나머지가 발생하는지 확인하고 1을 더해주어야 한다  

---
## 3-3
삼항연산자를 이용하여 num의 값에 따라 양수, 음수, 0을 출력하는 코드
```
public static void main(String[] args) {
      int num = 10;
      System.out.println( ??? );
}
```
num == 0 ? "0" : num > 0 ? "양수" : "음수";0

---
## 3-4
변수 num의 값 중 백의 자리 이하를 버리는 코드
```
public static void main(String[] args) {
      int num = 456;
      System.out.println( ??? );
}
```
num / 100 * 100

---
## 3-5
변수의 값 중 일의 자리를 1로 바꾸는 코드
```
public static void main(String[] args) {
      int num = 333;
      System.out.println( ??? );

      // 실행 결과 331
}
```
num / 10 * 10 + 1

---
## 3-6
변수의 값보다 크고 가장 가까운 10의 배수에서 변수의 값을 뺀 나머지를 구하는 코드
```
public static void main(String[] args) {
      int num = 24;
      System.out.println( ??? );
}
```
10 - num % 10 OR   
(num / 10 + 1) * 10 - num

---
## 3-7
화씨(Fahrenheit)를 섭씨(Celcius)로 변환하는 코드
```
public static void main(String[] args) {
      int fahrenheit = 100;
      float celcius = ( ??? );
      System.out.println("Fahrenheit:"+fahrenheit);
      System.out.println("Celcius:"+celcius);
}
```
(int)((5/9f * (fahrenheit - 32))*100 + 0.5) / 100f

---
## 3-8
실행결과를 얻기위한 코드 수정
```
public static void main(String[] args) {
      byte a = 10;
      byte b = 20;
      byte c = a + b;               // (byte) (a + b);
      char ch = 'A';
      ch = ch + 2;                  // (char) (ch + 2);
      float f = 3 / 2;              // 3 / 2f;
      long l = 3000 * 3000 * 3000;  // 3000 * 3000 * 3000L;
      float f2 = 0.1f;
      double d = 0.1;
      boolean result = d==f2;       // (float) d == f2;
      System.out.println("c="+c);
      System.out.println("ch="+ch);
      System.out.println("f="+f);
      System.out.println("l="+l);
      System.out.println("result="+result);

      // 실행 결과
      ch=C
      f=1.5
      l=27000000000
      result=true
}
```

---
## 3-9
변수가 영문자(대소포함) 이거나 숫자일 때만 true값을 출력하는 코드
```
public static void main(String[] args) {
      char ch = 'z';
      boolean b = ( ??? );
      System.out.println(b);
}
```
'a' <= ch && ch <= 'z' || 'A' <= ch && ch <= 'Z' || '0' <= ch && ch <= '9'

---
## 3-10
대문자를 소문자로 변경하는 코드   
(저장된 문자가 대문자인 경우에만 소문자로 변경)
```
public static void main(String[] args) {
      char ch = 'A';
      char lowerCase = ( 1 ) ? ( 2 ) : ch;
      System.out.println("ch:"+ch);
      System.out.println("ch to lowerCase:"+lowerCase);
}
```
('A' <= ch && ch <= 'Z') ? (char)(ch+32): ch
