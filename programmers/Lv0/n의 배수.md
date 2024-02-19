## 문제
https://school.programmers.co.kr/learn/courses/30/lessons/181937
## 풀이
```javascript
function solution(num, n) {
    if (num % n === 0) {
        return 1;
    } else {
        return 0;
    }
}
```
## 다른 풀이
```javascript
function solution(num, n) {
    return num % n === 0 ? 1 : 0;
}
```
