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
