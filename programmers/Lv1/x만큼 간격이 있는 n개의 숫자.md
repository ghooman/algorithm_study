## 문제
https://school.programmers.co.kr/learn/courses/30/lessons/12954
## 풀이
```javascript
function solution(x, n) {
    let result = [];
    for (let i = 1; i <= n; i++) {
            result.push(x * i)
        }
    return result
}

// 빈 배열을 만든다.
// 반복문을 돌려서 n번째가 될때까지 x의 배수를 넣는다.
```
## 다른 사람 풀이
```
function solution(x, n) {
    return Array(n).fill(x).map((v, i) => (i + 1) * v)
}
```
n길이 만큼의 배열을 미리 만들고 fill()과 map()메서드를 사용하여 채워주었다.
