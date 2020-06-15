### 문자열 내 p와 y의 개수

- 문제 설명

행렬의 덧셈은 행과 열의 크기가 같은 두 행렬의 같은 행, 같은 열의 값을 서로 더한 결과가 됩니다. 2개의 행렬 arr1과 arr2를 입력받아, 행렬 덧셈의 결과를 반환하는 함수, solution을 완성해주세요.



- 제한 조건

행렬 arr1, arr2의 행과 열의 길이는 500을 넘지 않습니다.



- 입출력 예

| arr1           | arr2           | return         |
| -------------- | -------------- | -------------- |
| [[1,2], [2,3]] | [[3,4], [5,6]] | [[4,6], [7,9]] |
| [[1], [2]]     | [[3], [4]]     | [[4], [6]]     |



- 문제 풀이

```javascript
//첫번째 풀이
function solution(s){
    var answer = true;
    let arr=s.split("")
    let a=0
    let b=0
    for (let i=0; i<arr.length; i++){
        if(arr[i] == "p" && "P"){
            a.push(1)
        } else if(arr[i] == "y" && "Y"){
            b.push(1)
        }
    }
    if (a!==b){
        return answer
    }else {
        return "false"
    }
    console.log(s.split(""))
    return answer;
}
// split으로 배열을 만들고 p와P가 있으면 개수 a=+1,y와 Y가 있으면 b=+1
// a와 b의 개수를 비교하여 true 혹은 false를 return
// 코드 다시 짜기


// 두번째 풀이
function solution(s){
    let arr = s.toUpperCase().split('');
    let a =0;
    let b =0;
    for(let i=0; i<arr.length; i++){
        if(arr[i] === 'P'){
            a++;
        }else if(arr[i]==='Y'){
            b++;
        }
    }
    if(a === b){
        return true;
    }else{
        return false;
    }
}
// 첫번째 풀이에서 split 하기 전에 toUpperCase를 통해 대문자로 다 통일시키고 개수를 비교


// 다른 풀이
function numPY(s){
    return s.toUpperCase().split("P").length === s.toUpperCase().split("Y").length;
}
// 간결...
```

