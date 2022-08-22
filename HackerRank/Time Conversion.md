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
```
