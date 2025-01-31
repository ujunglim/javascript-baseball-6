# 미션1 - 숫자 야구⚾

## 문제 요약

컴퓨터가 랜덤하게 1부터 9까지 서로 다른 수로 만든 3자리의 수를 사용자가 맞추는 게임입니다.

- 같은 수가 같은 자리에 있으면 스트라이크
- 다른 자리에 있으면 볼
- 같은 수가 전혀 없으면 낫싱
- 1에서 9까지 서로 다른 임의의 수 3개
- 사용자가 잘못된 값을 입력한 경우 throw문을 사용해 예외를 발생시킨후 애플리케이션은 종료된다

## 기능 목록

- [x] 1. 컴퓨터가 1~9까지 서로다른 숫자 3개를 생성한다
- [x] 2. 게임시작 인사말을 출력한다 `숫자 야구 게임을 시작합니다.`
- [x] 3. `숫자를 입력해주세요 : `를 출력해 사용자에게 3자리 숫자를 입력받는다
- [x] 4. 입력값 예외처리 (밑의 에러를 출력하고 애플리케이션 종료)
  - [x] 숫자가 아닌 문자열일시 `숫자가 아닌 문자열을 입력할 수 없습니다`
  - [x] 숫자에 0이 있을시 `0은 입력할 수 없습니다`
  - [x] 숫자가 세자리가 아닐 시 `세자리 숫자를 입력해주세요`
  - [x] 숫자가 중복될시 `중복이 없는 숫자를 입력해주세요`
- [x] 5. 입력의 결과를 출력한다

  - [x] 볼을 판단하는 메소드
  - [x] 스트라이크를 판단하는 메소드
  - [x] 낫싱을 판단하는 메소드

- [x] 6. 3스트라이크이면 게임종료 말을 출력한다 `3개의 숫자를 모두 맞히셨습니다! 게임 종료`
     </br>또한 리플레이할지 끝낼지를 물어본다 `게임을 새로 시작하려면 1, 종료하려면 2를 입력하세요.`
  - [x] `1`을 입력하면 리플레이이므로 위의 3번부터 시작한다, `2`를 입력하면 게임을 종료한다.
  - [x] 입력값 예외처리: `1`, `2`외의 것을 입력하면 `게임을 다시 시작하려면 1, 끝내려면 2만 입력할 수 있습니다`에러메시지 출력하고 애플리케이션 종료

## 입력값 처리

1. 공백제거
2. 배열로 변환
3. 배열 안의 각 요소를 숫자로 변환

## 예외처리

1. 문자열아나 소수를 입력한 경우
2. 0을 포함하는 숫자를 입력한 경우
3. 세자리가 아닌 수를 입력한 경우
4. 중복되는 숫자를 입력한 경우
5. 게임이 종료 된후 1, 2가 아닌 다른 수를 입력한 경우

## 리펙토링

기능을 모두 완성한 후 코드컨벤션과 각 메소드마다 단일기능을 수행하여 기능 자체의 의미가 더 잘 표현할 수 있도록 수정했다.

- `readLineAsync`를 사용하며 `try catch`문이 중첩됬는데 과제가 끝나고 난뒤 피드백을 받아 이대로 써도 될지 어떤식으로 변경해야할지 피드백을 받은 뒤 다시 수정하자.
- `InputView` 의 `getNumbers` 메소드가 입력을 받을때의 `catch`문에 어떤 예외를 잡아야하는지 보충
