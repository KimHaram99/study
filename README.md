# study
# python
+ int(), str(), range()
+ 연산자 **, %, //
+ 문자 chr() <> 아스키코드 ord()
+ boolean : >=, <=, ==(이꼴?), !=, not(), and, &, or, |
+ AA.count("A")
+ AA.index("A")\
+ index = AA.index("A")\
index = AA.index("A",index+1)

입력 input(), split()

    a,b=map(int,input().split())

용량이 큰 경우 input 대신 sys.stdin.readline을 사용한다.
단, 이 경우 맨 끝의 개행문자까지 같이 입력됨>.rstrip() 추가

    import sys
    a, b = map(int,sys.stdin.readline().split())

python_출력 print(), format, join()

    print("{0:빈공간표시,정렬,부호,자리수,콤마}".format(입력))
    print("{0:^<+30,}".format(10000000000))
    +10,000,000,000^^^^^^^^^^^^^^^

    print(f"{0:.자릿수f}")
    print("{0:.2f}".format(5/3)) 둘째자리까지 반올림
    1.67

    print('\n'.join(map(str,[a+b, a-b, a*b, a//b, a%b])))

python_list[]

    출력
    print(*list)
    
    위치를 변경
    list[i], list[j] = list[j], list[i]
    list[i:j+1] = list[j:i-1:-1]

    추가
    list.append("0")
    
    a = [abc]
    a = [a]*2
    a = [[abc],[abc]]

    python_한줄 if문
    print(1 if i == i[::-1] else 0) 맞으면1, 틀리면0

python_반복 for, while

    while True:
        try:
            A, B = map(int,input().split())
        except:
            break

python_기타

    진법변환
    10>bin(2),oct(8),hex(16)
    print(bin(10)[2:])
    10<
    print(int('1010',2))

python_백준_분수찾기

    x = int(input())
    c = 1

    while x > c:
        x -= c
        c += 1

    if c % 2 == 0:
        a = x
        b = c-x+1

    else:
        b = x
        a = c-x+1
        
    print(f"{a}/{b}")

# Java 기초 (+intellij)
    New_package(폴더)_New_Class
    package chap_01;
    public class _01_HelloWorld {
        public static void main(String[] args) {
            System.out.println("Hello,World!");  출
        }
    }
+ println=printline 을 의미함
+ psvm 입력 또는 main 입력
+ sout 입력, fori 입력
+ shift+f10 실행
+ ctrl+d 복붙
+ shift+tab 탭 이전, ctrl+alt+l 탭 정렬
+ 주석\
// (ctrl+/)\
/* 주석 */ (ctrl+shift+/)

변수입력

    String name;
            name = "A";
    String name = "A";
    char grade = 'A'; 한글자 문자에 사용

    int hour =15; 자동double
    long l = 1000000000000L; 큰 숫자를 입력할 때 사용
    l = 1_000_000_000_000L
    
    int i = 1, j = 2;
    
실수값(double,float)

    double score = 10.1; 정밀함
    float score = 10.1F; 짧은

    boolean pass = true; or False;

변수이름조건

    _, 문자, 숫자 
    소문자로 시작
    공백 불가
    예약어 불가
    
+ '상수'는 대문자로 정의

      한 번 저장. 절대 변하지 않는다.
        final String CODE = "KR";

형 변환

    int score = 93;
    System.out.println(score);
    System.out.println((float) score);
    System.out.println((double) score);

    정수와 실수의 합은 자동 double

    변수에 형변화된 데이터 사용
    double convertedScoreDouble = score; // 191 > 191.0
    int > long > float > double(자동형변환)
    int convertedScoreDouble = (int) score; // 191.8 > 191
    double > float > long > int(수동형변환)

    숫자를 문자열로
    String s1 = String.valueof(93); (i:, d:...)
    s1 = Integer.toString(i: 93);
    s2 = Double.toString(d: 98,8);

    문자열을 숫자로
    int i = Integer.parseInt(s: "93");
    ...
    
연산자

    증감연산 ++, --
    System.out.print(++val) 1더한 후 계산
    System.out.print(val++) 계산 후 1더함

    대입연산 +=, -=, *=, /=, %=
    int num = 10;
    num = num + 2;
        num += 2;

    비교연산자 >, >=, <, <=, ==, !=
    (1 < 3 < 5) 사용 불가능

    논리 연산자 or, and
    boolean A = true;
    boolean B = false;
    System.out.println(A || B); 한개이상 true 조건.
    System.out.println(A && B); 모두 true 조건.

    논리 부정 연산자 ! = 반대값 출력
    System.out.println(!true); = false

삼항 연산자

    결과 = (조건) ? (참의 경우 결과) : (거짓의 경우 결과)
    int x = 5;
    int y = 3;
    int max = (x>y) ? x : y;
    System.out.println(max);

문자열

    println(s.length()); //글자수

    대소문자 변환
    println(s.toUpperCase());
    println(s.toLowerCase());

    포함 관계
    println(s.contains("Java")); 포함 true
    println(s.indexOf("java")); 위치정보(없으면 -1출력)
    println(s.lastIndexOf("java")); 마지막 위치정보
    println(s.startsWith("I like")); 이 문차열로 시작시 true
    println(s.endsWith(".")); 이 문자열로 끝나면 true

문자열 변환 및 출력

    println(s.replace("and",",")); 문자를 문자로 변환
    
    println(s.substring(0,7)); 이 위치 전까지 문장을 출력
    println(s.substring(7)); 이 위치부터 문장을 출력
    println(s.substring(s.indexOf("java"))); 이 문자부터 출력
    println(s.substring(s.indexOf("java"),s.indexOf("."))); 문자부터 문자까지 출력
    
    println(s.trim()); 공백제거

    println(s1.concat(",").concat(s2)); 문자열 결합

문자열 비교

    println(s1.equals("java")); 같으면 true
    대소문자 구분 없이 문자열 내용이 같은지 체크할 땐
    equalsIgnoreCase 사용

    s1, s2 같은경우 문자열 입력시 참조가 같지만,
    new String 으로 같은내용 입력시 참조가 바뀜
    
    즉, s1 == s2 // false 참조를 확인
    s1.equals(s2) // true 값을 확인

특수문자, 탈출 문자

    줄바꿈 \n
    탭 \t
    역슬래시입력 \\
    큰따움표입력 \"
    작은따움표입력 \'

IF (&& ||)

    if (조건 && 조건)
    내용 라인이 한줄이면 중괄호 생략가능
    
    if (조건 || 조건) {
    아래 라인이 두줄 이상인 경우{}사용 합니다.
    } 

    if (조건) {
    내용
    } else if {
    내용    
    } else {
    내용
    }

Switch Case

    switch(expression){
        case A: 명령 (A일 경우)
            break
        case B:
        case C: 명령 (B 또는 C일 경우)
            break
        default: 명령 (해당없는경우 실행)
    }


# Java 반복문

for

    for (int i = 0; i < 10; i++);
    System.out.println(i);
    0 부터 9까지 출력됨

배열의 순회, 입력 및 출력

    for (int i = 0; i < 배열. length ; i++ )
        System.out.println(변수배열[i] + "내용")

+ enhanced for (for-each) 반복문

        for (String 새로운변수 : 변수배열) {
            System.out.println(변수 + "내용")
        }
+ fori 자동입력 / ++ 1 증가 / += 2 짝수로 증가
+ Break 실행시 반복을 종료
+ Continue 현재 반복을 건너뜀, 다음 반복 실행

while

    while (조건) {
        내용
        탈출조건
    }

+ DoWhile

        do {
            내용
            탈출조건
        } while(조건);

이중 반복문

    for (int i = 0; i < 5; i++){
        for (int j = 0; j < 5; j++){
            System.out.print("*");
        } System.out.println();
    }

    for (int i = 0; i < 5; i++){
                for (int j = 0; j < i+1; j++){
                    System.out.print("*");
                } System.out.println();
    }

배열 Array (묶음)
: 같은 자료형의 값 여러 개를 저장하는 연속된 공간

    1. String[] coffees = new String[4];
    
    2. String coffees[] = new String[4];
    coffees[0] = "아메리카노"; 0위치에 입력 또는 변경

    3. String[] coffees = new String[] {"1","2"} 순서대로 입력
    
    4. String[] coffees = {"1","2"} 순서대로 입력


다차원 배열 (2차원 배열)

    String[][] seats = new String[][] {
        {"1","2"},
        {"3","4"}
    }   
다차원 배열의 순회

    for (int i = 0; i < seats.length; i++) { //세로
        for(int j = 0; j < seats[i].length; j++) { //가로
            System.out.print(seats[i][j] + " "); // A1 A2
        }
        System.out.println();
    }

아스키 코드 ASCII (ANSI) : 미국 표준 코드

    char c = 'A';
    System.out.println((int)c); // 65

+ 아스키코드를 사용한 배열입력

        String[][] seat = new string[5][5]
        char ch = 'A';
        for (int i = 0; i < seat.length; i++){
            for (int j = 0; j < seat[i].length; j++){
                seat[i][j] = String.valueOf(ch) + (j+1);
            }ch++;
        }

메소드(함수)
    
    public static void hello() {
        System.out.println("안녕하세요?")
    }
    pyblic static void main(Stringp[] args) { //메소드 호출
        System.out.println("메소드호출전");
        hello();
        System.out.println("메소드호출후");
    }

+ 전달값, Parameter
        
+ 거듭제곱
    
        public static void power(int number) {
            int result = number * number;
            System.out.println(number+"의2승은"+result);
        } public static void main(String[] args) {
            power(2);    
        }
+ 거듭제곱(2)
    
        public static void powerByExp(int number, int exponent) {
            int result = 1;
            for (int i = 0; i < exponent; i++) {
                result *= number;
            } System.out.println(number+"의"+exponent+"승은"+result)    
        }
+ 반환값, Return

        public static String getNumber() {
        String number = "010-1234-1234"
        return number;    
        }
        public static void main(String[] args) {
            String contactNumber = getNumber();
            System.out.println("호텔 전화번호:"+contactNumber)
        }

+ 전달값과 반환값

        public static int getPower(int number) {
            int result = number * number;
            return result;
        }

        public staric int getPowerByExp(int number, int exponent) {
            int result =1;
            for (int i = 0; i < exponent; i++) {
                result *= number;
            } return result;
        }

        public static void main(String[] args) {
            int reVal = getPower(2); // 2*2= 4
            System.out.pringln(retval);
            
            reVal = getPowerByExp(3,3); // 3*3*3= 27
            System.out.pringln(retval);

            System.out.println(getPowerByExp(2,4)) 2*2*2*2 = 16
        }

메소드 오버로딩

    public static int getPower(int number) {}
    public static int getpower(String strnum) {}
    public static int getpower(int number, int exponent) {}
    위처럼 자료형(type)이 다르거나 전달값 개수가 다른 여러개의 메소드의 이름을 같게 지정할 수 있다.
    단, 메소드를 정의하는 자료형은 다르게 할 수 없다.
    main {
    System.out.println(getPower(3)) //3*3= 9
    System.out.println(getPower("4")) //4*4= 16
    System.out.println(getPower(3,3)) //3*3*3= 27
    }
+ 메소드 안에서 아래의 메소드를 호출

        Public Static int getPower(int number){
            return getPower(number,2);
        } 
        public Static int getPower(int number,int exponent){
            int result = 1;
            for (int i = 0; i < exponent; i++){
                result *= number;
            } return result;
        }

변수의 범위 :
+ public 영역에서 만든 변수 = 다른 영역 X.
+ for 문에서 사용된 변수 =  for문 밖 X.
+ {중괄호} 내에서 사용된 변수 = 중괄호 밖X

main 메소드<유튜브참고>

# 자바의정석 (이클립스)
단축키
+ ctrl+shift+L 단축키 목록
+ ctrl+"+"."-" 화면크기
+ ctrl+d 한 줄 삭제
+ ctrl+alt+down 행 단위 복사
+ alt+shift+A 멀티컬럼 편집
+ alt+up, down 행단위 이동
+ tap, shift+tap, ctrl+i 들여쓰기
+ ctrl+/ 주석(토글)
+ ctrl+space 자동완성

변수(variable): 하나의 값을 저장하는 공간\
상수(constant): 값을 한 번 저장하는 공간\
리터럴(literal): 값
+ 변수(그릇)보다 리터럴이 큰 경우 에러

리터럴의 접두사와 접미사 조건
- 변수 기본형(Primitive type): 8개 고정
        + 실제 값을 저장

       (1) 논리 boolean: true or false
       
       (2) 문자형 ch: '' 한글자를 무조건 입력, 유니코드(2byte), 양수값 = 부호없는 정수범위.

       (1) 정수 byte: 127까지만 저장가능한 int 타입
       (2) 정수 short: 없음/C언어 호환용
       (4) 정수(integer): 없음
         int i = 100 10진수
         int i = 0b01 2진수(0b)
         int oct = 010 8진수(0)
         int hex = 0x10 16진수(0x)
       (8) 정수(Long): L
         long i = 100; L생략가능
         long i = 10_000_000_000L; L생략불가
         int값이 20억까지 저장가능.
      
       (4) 실수(float): f/부동소수점(떠다닌다는 뜻), 정밀도7자리
       (8) 실수(double): d 생략가능/정밀함, 정밀도15자리
        System.out.println(10.) 혹은 .10 사용가능
        System.out.println(1e3) = 10^3 = 1000.0
        System.out.println(10f) = 10.0

      정수 범위(8비트의 경우)
      0 ~ 2^n-1 = 0~255
      -2^(n-1) ~ 2^(n-1)-1 = -128~127
      
      부호비트S(Sign bit): 양수=0, 음수=1, 음수포함인경우 S표시
- 변수 참조형(Reference type): String, System 등 무한 추가 가능\
        + 메모리 주소를 저장 (4byte{32bit JVM}=40억 또는 8byte{64bit JVM}=40*40=1600)

       문자열 str: "" 빈 문자열 가능

# printf()
println() 단점
+ 출력형식 지정불가
+ 실수 자리수 조절 불가
+ 10진수로만 출력

# 지시자를 통한 출력형식
%n 지시자 뒤에 붙이면 줄바꿈\
지시자 앞에 숫자 = 자리수(오른쪽정렬/음수=왼쪽정렬)\
지시자 앞의 숫자앞에 문자또는 숫자 = 빈공간에 입력\
지시자 s 앞에 .숫자 = 부분출력

    printf("d=%전체자리.소수점아래자리f%n",d)

+ printf("%.2f"10.0/3); // 3.33f 소수점2자리표현
    
+       %B oolean 불리언

+       %D ecimeal 10진
        %O ctal 8진
        %he X a-decimal 16진

+       %F loating-point 부동소수점
        %E xponent 지수

+       %C haracter 문자
        %S tring 문자열

+       정수를 16진수로 출력
        ('%x", 15); // f      

        정수를 이진 문자열로 출력
        ("%s",Integer.toBinaryString(15)); 
        // 1111


지시자 앞에 #을 붙이면 접두사를 포함해 출력
        
    System.out.printf("%x",15) // f
    System.out.printf("%#x",15) // 0xf
    System.out.printf("%#X",15) // 0xF

실수 출력을 위한 지시자 %f - 지수형식( %e , 간략한 형식 %g )\
ㄴ 실수를 출력할 때는 f, 0이 많이 사용된 경우 e를 사용.

+       float f = 123.4567890f;
        System.out.printf("%f",f);
            // 123.456787 (정밀함 7)

+       double f = 123.456789;
        System.out.printf("%f",f);
            // 123.456789 (정밀함 15)

+      System.out.printf("%e",f); // 1.234568e+02
        %e: 마지막숫자는 반올림, e+01 = 10^2

+       System.out.printf("%g", 123.456789);
            // 123.457 = 점포함 7자리, 반올림
        System.out.printf("%g", 0.00000001); 
            // 1.00000e-8

# Scanner
화면으로부터 데이터를 입력받는 기능을 제공하는 클래스

    import java.util.Scanner; (Scanner 대신 *을 사용가능)
    
    스캐너 객체 생성
    Scanner scanner = new Scanner (System.in) ;

    사용
    int num = scanner.nextInt() ;
    
+       String input = scanner.nextLine() ;
        int num = Integer.perseInt(input) ; 
        // 문자열을 숫자로

--------------------------------
    
문자열.contains();
특정 문자열 존재여부 확인
