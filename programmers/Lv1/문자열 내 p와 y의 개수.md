## 문제
https://school.programmers.co.kr/learn/courses/30/lessons/12916?language=javascript#
## 풀이
```javascript
function solution(s){
    let upper = s.toUpperCase()
    let countP = 0;
    let countY = 0;

    for (let i = 0; i < upper.length; i++) { 
        if (upper[i] === 'P') countP++
        if (upper[i] === 'Y') countY++
    }
    return countP === countY ? true : false
}
```
## 다른 사람 풀이
```javascript
function numPY(s){
    return s.toUpperCase().split("P").length === s.toUpperCase().split("Y").length;
}
```
split()메서드 사용은 진짜 신박하다.
