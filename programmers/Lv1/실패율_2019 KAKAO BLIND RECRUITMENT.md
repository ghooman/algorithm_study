## 문제
https://school.programmers.co.kr/learn/courses/30/lessons/42889
## 풀이
```javascript
function solution(N, stages) {
    let result = [];
    let length = stages.length;
    
    for (let i = 1; i <= N; i++) {
        let noClear = stages.filter(e => e === i).length;
        let rate = noClear / length;
        length -= noClear;
        result.push({stage: i, value: rate})
    }
    result.sort((a, b) => {
        if (a.value === b.value) {
            return a.value - b.value
        }
        return b.value - a.value})
    
    return result.map(e => e.stage);
}

// result 빈 배열을 선언한다.
// 배열의 길이를 legth변수에 할당한다.
// 반복문으로 1번째부터 반복한다. N까지 (i)
// noClear 변수에 filter를 써서 i랑 같은거의 길이 할당
// failRate 변수에 noClear / length 할당
// length 에서 noClear를 뺀다.
// result에 {name: stages[i], value: failRate} 푸시

// result안에 밸류값을 내림차순으로 정렬한다.
// 만약 밸류값이 같으면 오름차순 시킨다.
// 맵을써서 네임값만 리턴한다.
```
## 다른 사람 풀이
```javascript
function solution(N, stages) {
    let result = [];
    for(let i=1; i<=N; i++){
        let reach = stages.filter((x) => x >= i).length;
        let curr = stages.filter((x) => x === i).length;
        result.push([i, curr/reach]);
    }
    result.sort((a,b) => b[1] - a[1]);
    return result.map((x) => x[0]);
}
```
배열만 사용하였고, 미리 길이를 선어해줘서 계속 빼나가는 번거로움 없이 필터로 길이를 정리한게 인상적이었다.
