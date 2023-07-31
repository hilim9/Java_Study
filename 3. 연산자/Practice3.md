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
numOfApples/sizeOfBucket + (numOfApples%sizeOfBucket > 0 ? 1 : 0) ;

---
