### 짝수와 홀수(python)

- 문제 설명

정수 num이 짝수일 경우 Even을 반환하고 홀수인 경우 Odd를 반환하는 함수, solution을 완성해주세요.



- 제한 조건

num은 int 범위의 정수입니다.

0은 짝수입니다.



- 입출력 예

| num  | return |
| ---- | ------ |
| 3    | "Odd"  |
| 4    | "Even" |



- 문제 풀이

```python
def solution(num):
    answer =""
    if num%2!=0 :
        answer="Odd"
    else :
         answer= "Even"
    return answer

# 한줄 풀이
return "Odd" if num%2 else "Even"
```

