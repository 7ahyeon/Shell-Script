# Calculator

```
#!/bin/bash

while :
do
        # 두 개의 숫자 입력받기
        read -p "Input two numbers with enter : " n1 n2

        # 숫자일 경우 없애기(유효성 검사)
        numTest1=${n1//[0-9]/}
        numTest1=${n2//[0-9]/}

        # 입력받은 숫자가 두 개가 아니면 되돌아가기
        if [[ -z $n1 || -z $n2 ]];then
                echo "No two number passed"

        # 숫자가 아닌 값을 입력 받았으면 되돌아가기
        elif [[ -n $numTest1 || -n $numTest2 ]];then
                echo "No number passed"
        # 두 숫자를 정상적으로 입력 받았으면 사칙연산 처리하기
        else
                echo
                echo "Add : $n1 + $n2 = $(expr $n1 + $n2)"
                echo "Sub : $n1 - $n2 = $[$n1 - $n2]"
                echo "Mul : $n1 * $n2 = $(($n1 * $n2))"
                echo "Div : $n1 / $n2 = $(expr $n1 / $n2)"
                echo "Mod : $n1 % $n2 = $[$n1 % $n2]"
        break
        fi
done
```
<img width="439" alt="calculator" src="https://github.com/7ahyeon/Shell-Script/assets/107123698/6f1a2661-2845-4f22-9afb-e2d00509f8c6">

<img width="325" alt="executing calculator" src="https://github.com/7ahyeon/Shell-Script/assets/107123698/247274e8-7624-4d89-9622-cda8c9dfa393">
