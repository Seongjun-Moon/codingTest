### 정수 제곱근 판별(python)

- 문제 설명

임의의 양의 정수 n에 대해, n이 어떤 양의 정수 x의 제곱인지 아닌지 판단하려 합니다.
n이 양의 정수 x의 제곱이라면 x+1의 제곱을 리턴하고, n이 양의 정수 x의 제곱이 아니라면 -1을 리턴하는 함수를 완성하세요.



- 제한 조건

`n`은 1이상, 50000000000000 이하인 양의 정수입니다.



- 입출력 예

| n    | return |
| ---- | ------ |
| 121  | 144    |
| 3    | -1     |



- 문제 풀이

```python
def solution(n):
    import math
    answer = 0
    num = math.sqrt(n)
    if math.sqrt(n) == int(math.sqrt(n)) : 
        return pow(num+1, 2)
    else :
        return -1
    return answer

# 다른풀이
# math 쓰지 않고
    for i in range(1, n+1):
        if n == i ** 2:
            return (i+1) ** 2
    return -1
```

