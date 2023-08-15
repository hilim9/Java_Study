## 4-1
조건식을 기입
```
1. int형 변수 x가 10보다 크고 20보다 작을 때 true인 조건식  // 10 < x && x < 20
2. char형 변수 ch가 공백이나 탭이 아닐 때 true인 조건식  // !(ch == ' ' || ch =='\t') 또는 ch!=' ' && ch !='\t'
3. char형 변수 ch가 ‘x' 또는 ’X'일 때 true인 조건식  // ch == 'x' || ch == 'X'
4. char형 변수 ch가 숫자(‘0’~‘9’)일 때 true인 조건식  // '0' <= ch && ch <='9'
5. char형 변수 ch가 영문자(대문자 또는 소문자)일 때 true인 조건식 // ('a' <= ch && ch <= 'z') || ('A' <= ch && ch <= 'Z')
6. int형 변수 year가 400으로 나눠떨어지거나 또는 4로 나눠떨어지고 100으로 나눠떨어지지 않을 때 true인 조건식
// year%400==0 || year%4==0 && year%100!=
7. boolean형 변수 powerOn가 false일 때 true인 조건식  // !powerOn 또는 powerOn==false
8. 문자열 참조변수 str이 “yes”일 때 true인 조건식  // str.equals("yes") 또는 "yes".equals(str)
```

---
## 4-2
1부터 20까지의 정수 중에서 2 또는 3의 배수가 아닌 수의 총합을 구하는 코드
```
public static void main(String[] args) {
    int sum = 0;
    for(int i=1; i <=20; i++) {
        if(i%2!=0 && i%3!=0) // i가 2또는 3의 배수가 아닐 때만 sum에 i를 더한다.
            sum +=i;
    }
    System.out.println("sum="+sum);  // 73
}
```

--- 
## 4-3
1+(1+2)+(1+2+3)+(1+2+3+4)+...+(1+2+3+4+5+6+7+8+9+10) 총합을 계산하는 코드
```
public static void main(String[] args) {
    int sum = 0;
    int totalSum = 0;
    for(int i=1; i <=10; i++) {
        sum += i;
        totalSum += sum;
    }
    System.out.println("totalSum="+totalSum); // 220
}
```

---
## 4-4
1+(-2)+3+(-4)+... 과 같은 식으로 계속 더해나갔을 때, 총합이
100이상이 되는지 구하시오.
```
public static void main(String[] args) {
    int sum = 0; // 총합을 저장할 변수
    int s = 1; // 값의 부호를 바꿔주는데 사용할 변수
    int num = 0;

    // 조건식의 값이 true이므로 무한반복문이 된다.
    for(int i=1; true; i++, s=-s) { // 매 반복마다 s의 값은 1, -1, 1, -1...
        num = s * i; // i와 부호(s)를 곱해서 더할 값을 구한다.
        sum += num;
        if(sum >= 100) // 총합이 100보다 같거나 크면 반복문을 빠져 나간다.
            break;
    }

    // 위의 for문을 간략화
    /* for(int i=1; sum < 100; i++, s=-s) {
        num = i * s;
        sum += num;
    } */
    System.out.println("num="+num);
    System.out.println("sum="+sum); // 199
}
```

---
## 4-5
for문을 while문으로 변경

+ for문
```
public static void main(String[] args) {
    for(int i=0; i<=10; i++) {
        for(int j=0; j<=i; j++)
            System.out.print("*");
        System.out.println();
    }
}
```
+ while문
```
public static void main(String[] args) {
    int i=0;
    while( i<=10) {
        int j=0;
        while(j<=i) {
            System.out.print("*");
            j++;
        }
        System.out.println();
        i++;
    }
}
```

---


