### 약수의 합(python)

- 문제 설명

정수 n을 입력받아 n의 약수를 모두 더한 값을 리턴하는 함수, solution을 완성해주세요.



- 제한 조건

`n`은 0 이상 3000이하인 정수입니다.



- 입출력 예

| n    | return |
| ---- | ------ |
| 12   | 28     |
| 5    | 6      |



- 문제 풀이

```python
def solution(n):
    answer = 0
    for i in range(1, n+1) :
        if n%i<1 :
            answer += i 
    return answer

# 한줄 풀이
return sum([i for i in range(1, n+1) if not n%i])
```

