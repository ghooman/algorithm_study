## 문제
https://www.hackerrank.com/challenges/one-week-preparation-kit-plus-minus/problem?isFullScreen=true&h_l=interview&playlist_slugs%5B%5D=preparation-kits&playlist_slugs%5B%5D=one-week-preparation-kit&playlist_slugs%5B%5D=one-week-day-one
## 풀이
```javascript
function plusMinus(arr) {
    let length = arr.length
    let plus = 0
    let minus = 0
    let zero = 0
    
    for (let el of arr) {
        if (el > 0) plus++
        if (el < 0) minus++
        if (el === 0) zero++
    }
    
    console.log((plus / length).toFixed(6))
    console.log((minus / length).toFixed(6))
    console.log((zero / length).toFixed(6))
}
// arr의 개수에서 양수, 음수, 0의 갯수를 각각 나누는 문제.
// 표기는 소수점 6번째 자리까지이다.
// 소수점 자리수 지정 toFixed()메서드 사용.(반올림 되는데.. 아무래도 10의 -4승까지 오차범위라서 가능한듯하다..)
// 양수, 음수, 0의 갯수를 카운트하는 각각의 변수 선언
// 각각을 길이로 나눈것을 출력(리턴x)
```
