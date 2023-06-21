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

# java_기초_intellij
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
    