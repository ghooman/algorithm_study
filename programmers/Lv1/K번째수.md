## 문제
https://school.programmers.co.kr/learn/courses/30/lessons/42748
## 풀이
```javascript
function solution(array, commands) {
    let result = [];
    for (let i = 0; i < commands.length; i++) {
        result.push(
            array.slice(
                commands[i][0]-1, commands[i][1]
            ).sort(
                (a, b) => a - b
            )[commands[i][2]-1]
        )
    }
    return result
}


// map을 써서 줄여보기
function solution(array, commands) {
    return commands.map(e => {
        return array.slice(e[0] - 1, e[1]).sort((a, b) => a - b)[e[2]-1]
    });
}

// 리턴에 사용할 빈배열을 만든다.
// 커맨즈를 반복문으로 돌려서 각 배열에 접근한다.
// 접근한 배열의 0번째의 -1 부터 1번째까지 자르고
// 오름차순으로 정렬한다.
// 그배열에 접근한배열2번째인덱스의 +1의 값을 찾는다.
// 그값을 빈배열에 넣는다.
// 반복문이 끝나면 리턴한다.
//
// arr.slice(2 - 1, 5)[3-1]
```

## 다른 사람 풀이
```javascript
function solution(array, commands) {
    return commands.map(command => {
        const [sPosition, ePosition, position] = command
        const newArray = array
            .filter((value, fIndex) => fIndex >= sPosition - 1 && fIndex <= ePosition - 1)
            .sort((a,b) => a - b)    

        return newArray[position - 1]
    })
}
```
구조분해할당을 사용하였고 slice대신 filter를 사용한게 인상적이었다.
