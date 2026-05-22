# 프로필: 로봇 인프라

로봇, 장비, 하네스, 센서, 액추에이터, VLA inference, 실험 실행 파이프라인처럼 실제 시스템과 연결되는 작업에 적용한다.

이 프로필은 로봇 제어만 뜻하지 않는다.
모델 실행, robot client/server, 데이터 흐름, latency, safety, config, checkpoint 관리까지 포함한다.

## 적용 범위

- 로봇 제어 코드
- 장비와 하네스 연동
- 센서/액추에이터 통신
- VLA inference 실행
- robot client/server 구조
- 실험 실행 파이프라인
- 모델 checkpoint와 config 관리
- latency, timeout, safety가 중요한 코드

## 최우선 기준

실제 장비가 움직일 수 있다는 점을 항상 전제로 둔다.
소프트웨어 변경이 물리적 동작, 충돌, 파손, 안전 문제로 이어질 수 있다.

반드시 고려할 것:

- emergency stop
- timeout
- dry-run
- simulation
- action limit
- action clipping
- control loop 주기
- inference latency
- 장비 적용 전 수동 점검

## 실패 조건

정상 상황만 가정하지 않는다.

- 센서 미응답
- 통신 실패
- 전원 불안정
- 케이블 단선
- 커넥터 접촉 불량
- 노이즈
- 장비 좌표계와 코드 좌표계 불일치
- 모델 출력 이상값
- inference 지연
- checkpoint/config 불일치

소프트웨어 문제처럼 보여도 하드웨어, 하네스, 전원, 커넥터가 원인일 수 있다.

## 단위와 좌표계

단위는 문서와 코드에서 명확히 한다.

- 거리: `mm`, `m`
- 각도: `deg`, `rad`
- 전압/전류: `V`, `A`
- 시간: `ms`, `s`
- 주기: `Hz`

좌표계, 원점, 축 방향, 회전 방향을 명확히 기록한다.

## 모델과 inference 기준

- 모델 입력과 출력 형식을 문서화한다.
- checkpoint와 config의 짝을 명확히 관리한다.
- 모델 출력은 바로 장비 명령으로 보내지 말고 검증한다.
- action 범위, 단위, 클리핑 정책을 명확히 한다.
- inference latency가 control loop에 미치는 영향을 확인한다.
- 장애 시 마지막 명령을 계속 유지할지, 정지할지 정한다.

## 장비 적용 전 점검

1. dry-run 또는 simulation으로 명령 흐름을 확인한다.
2. 최소 속도와 제한 범위로 테스트한다.
3. emergency stop 동작을 확인한다.
4. 센서 값이 비정상일 때 동작을 확인한다.
5. timeout이 실제로 동작하는지 확인한다.
6. 전원, 하네스, 커넥터 상태를 확인한다.
7. 로그가 재현 가능한 수준으로 남는지 확인한다.

## 체크리스트

- [ ] 실제 장비가 움직일 가능성을 고려했는가?
- [ ] dry-run 또는 simulation 경로가 있는가?
- [ ] timeout과 emergency stop이 있는가?
- [ ] 단위와 좌표계가 명확한가?
- [ ] 모델 출력 검증과 action limit이 있는가?
- [ ] inference latency와 control loop 주기를 확인했는가?
- [ ] 하드웨어/하네스 문제 가능성을 점검했는가?

## 업데이트 메모

- [ ] 장비별 점검 항목 추가
- [ ] VLA inference 운영 중 반복된 문제 추가
- [ ] 실제 장애 원인과 재발 방지 기준 추가
