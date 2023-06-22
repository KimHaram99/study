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
+ println=printline
+ psvm 입력 또는 main 입력
+ sout 입력
+ shift+f10 실행단축키
+ ctrl+d 복붙
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
    
실수값(double,float)

    double score = 10.1; 정밀함
    float score = 10.1F; 짧은

    boolean pass = true; or False;

변수이름조건

    _, 문자, 숫자 
    소문자로 시작
    공백 불가
    예약어 불가
    
    한번 정의되면 절대 변하지 않는 상수는 대문자로 정의
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

    println(s.length());

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
        public..main(..) {
            String contactNumber = getNumber();
            System..ln("호텔 전화번호:"+contactNumber)
        }