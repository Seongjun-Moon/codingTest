### JadenCase 문자열 만들기

###### 문제 설명

JadenCase란 모든 단어의 첫 문자가 대문자이고, 그 외의 알파벳은 소문자인 문자열입니다. 문자열 s가 주어졌을 때, s를 JadenCase로 바꾼 문자열을 리턴하는 함수, solution을 완성해주세요.

##### 제한 조건

- s는 길이 1 이상인 문자열입니다.
- s는 알파벳과 공백문자(" ")로 이루어져 있습니다.
- 첫 문자가 영문이 아닐때에는 이어지는 영문은 소문자로 씁니다. ( 첫번째 입출력 예 참고 )

##### 입출력 예

| s                       |         return          |
| ----------------------- | :---------------------: |
| "3people unFollowed me" | "3people Unfollowed Me" |
| "for the last week"     |   "For The Last Week"   |



- 문제 풀이

```javascript
// 첫번째 풀이
function solution(s) {
    s = s.toLowerCase()
    const answer = s.split(' ').map(e => {
        const arr = e.split('')
        if(arr[0] != null) arr[0] = arr[0].toUpperCase()
        return arr.join('')
    }).join(' ')
    return answer;
}

- s문자열 각 단어의 첫글자만 대문자, 나머진 모두 소문자로 변경하면 되는 문제
- 먼저 s문자열 전체를 소문자로 변경 후
- s문자열을 배열로 만들고, 각 값들을 다시 배열로 만들어 각 단어의 0번째 문자가 null이 아니라면 arr[0].toUpperCase()
- 이 배열을 join('')한 뒤, 각 단어들을 다시 문자열로 조합해야 되기 때문에 join(' ')한 값을 return 하면 정답

// 그외의 풀이
function solution(s) {
    var answer = '';
    for (let i = 0; i < s.length; i++) {
      if (i === 0 || s[i-1] === " ") {
        answer += s[i].toUpperCase();
      } else {
        answer += s[i].toLowerCase();
      }
    }
    return answer;
}

- split을 사용하지 않고 그냥 for문으로 해결
- 문자열의 첫번째 혹은 해당 문자의 앞이 공백(" ")이라면 대문자로 바꾸는 풀이
```