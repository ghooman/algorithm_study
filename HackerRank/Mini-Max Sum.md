## 문제
https://www.hackerrank.com/challenges/one-week-preparation-kit-mini-max-sum/problem?isFullScreen=true&h_l=interview&playlist_slugs%5B%5D=preparation-kits&playlist_slugs%5B%5D=one-week-preparation-kit&playlist_slugs%5B%5D=one-week-day-one
## 풀이
```javascript
function miniMaxSum(arr) {
    let newArr = arr.sort((a, b) => a - b)
    let maxSum = 0
    let minSum = 0
    
    for (let i in newArr) {
        maxSum += newArr[i]
        minSum += newArr[i]
    }
    
    maxSum = maxSum - newArr[0]
    minSum = minSum - newArr[newArr.length - 1]
    
    console.log(`${minSum} ${maxSum}`)
}
// 배열 5개를 받아서 그 중 네개를 합하여 최대값과 최소값을 구하는 문제이다.
// 출력값은 최소값 공백 최대값이다.
// 최소값, 최대값을 할당해 줄 변수를 선언한다.
// sort()메서드를 사용해서 배열을 정렬하고 
// 반복문을 사용하여 최대값, 최소값 변수에 각각 다 더해서 넣는다.
// 최대값에서 정렬배열 첫번째 자리수를 뺀다.
// 최소값에서 정렬배열 마지막 자리수를 뺀다.
```
