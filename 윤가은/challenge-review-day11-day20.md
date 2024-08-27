# 지난 10일 나의 목표는?!
- [x] 매일 1 commit 달성
- [x] 코딩테스트 문제 10개 풀이

# 10일 돌아보면 잘한 점
- 매일 잔디를 심었다.
- 어려운 부분을 스스로 생각해서 해결하였다.
  
# 10일 돌아보며 아쉬운 점
- 문제를 풀 때 시간복잡도 ... 를 고려를 안 한 것 같다.
  

# 10일 동안 공부한 내용
- 문제 : https://school.programmers.co.kr/learn/courses/30/lessons/131705 
- 재귀함수 풀이
1. reduce 메서드로 합쳐서 0이 되는 조합을 찾으면 result 에 1을 더해준다.
2. 배열의 요소를 한개씩 추가하면서 재귀함수를 돌리는데, 배열의 길이가 3이 되면 합쳐서 0이 되는 지 검사한다.
0이 되던, 안되던 (3개만 모이면 if문에 걸려서) return 하여 해당 조합의 턴을 끝내고 for문으로 다른 조합을 찾아낸다.
3. combination( ) 재귀함수를 돌릴 때 두 번째 인자로 i + 1을 넘겨서 같은 수의 조합이 중복되지 않도록 한다.
```
function solution(number) {
    let result = 0;

    const combination = (current, start) => {
        if (current.length === 3) {
            result += current.reduce((acc, cur) => acc + cur, 0) === 0 ? 1 : 0;
            return;
        }

        for (let i = start; i < number.length; i++) {
            combination([...current, number[i]], i + 1);
        }
    }
    combination([], 0);
    return result;
}
```
# 느낀점 
- 문제는 나름 푼다고 생각 했는데 아니었던 거 ... 같다.
  위에 문제 3중 for문으로 쉽게 풀었는데 실행시간이 너무 길어서 반성하게 되었다.
  그리고 재귀함수는 아직도 어려운 것 같다...
  앞으로 문제 풀 때도 시간 복잡도를 생각하면서 풀어야지~

# 앞으로 10일 동안 나의 목표는?!
- [ ] 매일 잔디 심기
- [ ] Inforsion 개발하기
