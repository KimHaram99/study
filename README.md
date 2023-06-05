# study
# python_입력 input(), split()
a,b=map(int,input().split())

import sys\
a, b = map(int,sys.stdin.readline().split())


# python_출력 print(), format, join()
print("{0:빈공간표시,정렬,부호,자리수,콤마}".format(입력))\
print("{0:^<+30,}".format(10000000000))\
+10,000,000,000^^^^^^^^^^^^^^^

print(f"{0:.자릿수f}")\
print("{0:.2f}".format(5/3)) 둘째자리까지 반올림\
1.67

print('\n'.join(map(str,[a+b, a-b, a*b, a//b, a%b])))

# python_list[]
출력\
print(*list)\
변경\
list[i], list[j] = list[j], list[i]\
list[i:j+1] = list[j:i-1:-1]\
추가\
list.append("0")

# python_반복 for, while
while True:\
    try:\
        A, B = map(int,input().split())\
    except:\
        break
