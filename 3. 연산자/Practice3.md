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
