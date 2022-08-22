## 문제
https://www.hackerrank.com/challenges/one-week-preparation-kit-time-conversion/problem?isFullScreen=true&h_l=interview&playlist_slugs%5B%5D=preparation-kits&playlist_slugs%5B%5D=one-week-preparation-kit&playlist_slugs%5B%5D=one-week-day-one
## 풀이
```javascript
function timeConversion(s) {
    // Write your code here
    let arr = s.split(':')
    let hour = arr[0]
    let minute = arr[1]
    let second = arr[2]
    
    if (second.includes("PM")) {
        if (hour === '12') {
            hour = '12'
        } else {
            hour = Number(hour) + 12
        }
    }
    
    if (second.includes("AM")) {
        if (hour === '12') {
            hour = '00'
        }
    }
    second = second.slice(0, 2)
    
    return `${hour}:${minute}:${second}`
}

// 시간을 24시간제로 바꾸는 문제이다.
// 12AM => 00 / 12PM => 12
// s 파라미터를 split한다.
// hour, minute, second 변수를 선언한다.
// split한것을 각 변수에 할당한다.
// hour가 12이고 PM이면 그냥 12
// second에  PM이 있으면 + 12를 더한다.
// hour가 12이고 am이면 00
// second 는 am, pm을 없애야되므로 slice를 사용한다.
```
