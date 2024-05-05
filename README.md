# java-baseball-precourse
- - -
### *숫자 야구 게임*
- 플레이어가 컴퓨터의 랜덤 번호를 추측해서 맞추는 게임이다
- 랜덤 번호는 1 ~ 9 까지 서로 다른 수로 이루어진 3자리 수이다
- 사용자가 추측한 번호를 기반으로 힌트가 주어지며, 이를 활용해서 정답을 찾아가면 된다
- - -
### *구현할 기능 목록*

#### [ *컴퓨터* ]
- [x] **컴퓨터의 번호를 랜덤으로 생성한다**
    - 번호는 세자리 숫자이다
    - 각 자릿수의 범위는 1 ~ 9 이다
    - 각 자릿수는 모두 달라야한다
- [x] **전달받은 수와 자신의 세자리 수를 비교하여 힌트를 반환한다**
    - 숫자, 위치 모두 일치 → 스트라이크
    - 위치는 다르고 숫자만 일치 → 볼
    - 숫자, 위치 모두 불일치 → 낫싱

#### [ *게임 흐름 관리* ]
- [x] **플레이어로부터 숫자를 입력 받는다**
    - [x] 유효성 검증
        - 세자리가 맞는지
        - 모두 1 ~ 9의 숫자인지
        - 세자리가 모두 다른 수 인지
    - [x] 위 조건을 만족하지 않는다면 예외를 발생시키고 프로그램을 종료한다
- [x] **입력받은 숫자를 컴퓨터에게 전달하고, 컴퓨터가 반환한 힌트를 출력한다**
    - 정답을 맞췄다면 (3스트라이크)
        - [x] 게임 종료 메시지를 출력한다
        - [x] 게임 재시작 여부를 입력 받는다
            - 1 이면 재시작, 2 이면 종료한다
            - 1, 2가 아닌 값이 들어오면 예외를 발생시키고 프로그램을 종료한다
    - 정답이 아니라면
        - [x] 힌트를 출력한다
        - [x] 1번부터 다시 반복한다