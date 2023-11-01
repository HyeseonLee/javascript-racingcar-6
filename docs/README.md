# 게임 정리
1. 게임 시작
2. 자동차 이름을 플레이어로부터 입력 받기
3. 이름에 대한 유효성 검사 진행, 실패시 오류 발생시키기
4. 진행할 라운드 횟수를 플레이어로부터 입력 받기
5. 라운드 횟수에 대한 유효성 검사 진행, 실패시 오류 발생시키기
6. 게임 메인 로직
    1. 각 자동차마다 랜덤 값을 구한 후, 전진/머무름 판단하기
    2. 랜덤값 4이상시, 전진도에 1 더하기
    3. 해당 라운드 결과 각 자동차마다의 누적 전진도 출력하기
 7. 게임 종료 상황
    1. 라운드 진행 횟수만큼 진행하면 종료한다.
    2. 가장 많이 전진한 자동차가 우승자이다.
    3. 최종 우승자를 출력한다.
 8. 게임 종료

# 기능 요구사항

## 게임 초기 세팅
1. 게임 진행 데이터를 관리할 객체 생성
   - 자동차 이름
   - 진전도
2. 자동차 이름을 플레이어로부터 입력 받기
   - 입력값에서 자동차 이름을 쉼표(,)로 구분하기
3. 자동차 이름에 대한 유효성 검사 실행
   - 이름의 길이는 5글자 이하
   - 이름의 중복은 허용 안함
   - 오류시 "[ERROR] 자동차 이름을 5글자 이하로 입력하세요." 출력
4. 진행할 라운드 횟수를 플레이어로부터 입력 받기
5. 라운드 횟수에 대한 유효성 검사 진행
   - 숫자 이외의 값에 대해 오류 처리
   - 0에 대해 오류 처리
   - 오류시 "[ERROR] 시도할 횟수는 숫자로 입력하세요." 출력

## 게임 로직
1. 입력 받은 라운드 수 (n) 동안에 각 라운드마다 아래 기능 실행
   1. 각 자동차마다 랜덤 값을 구하기
   2. 랜덤값을 4 기준으로 그 이상이면 전진도에 1을 더하고, 그 미만이면 전진도에 0을 더하기
   3. 라운드 실행 결과 출력
        - (예시)
          pobi : -
          woni :
          jun : -
2. 입력 받은 라운드 수 (n)를 모두 실행했다면, 게임 종료 상황에 마주한 것임
   1. 최종 우승 자동차를 결정하기 
      - 전진도 숫자 값이 가장 높은 자동차가 최종 우승 자동차임
      - 2대 이상일 경우 쉼표와 띄어쓰기(, )로 구분
   2. 최종 우승자 결과 출력
      - (예시)
        최종 우승자 : pobi, jun    