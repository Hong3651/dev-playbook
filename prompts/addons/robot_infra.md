# addon 프롬프트: 로봇 인프라

로봇, 장비, VLA inference, 실험 실행 파이프라인에 붙이는 추가 기준이다.

## 프롬프트

```text
로봇 인프라 기준을 추가로 적용해라.

- 실제 장비가 움직일 수 있음을 전제로 판단해라.
- emergency stop, timeout, dry-run, simulation 경로를 확인해라.
- action limit, action clipping, 단위, 좌표계, 축 방향을 명확히 하게 해라.
- 모델 출력은 장비 명령으로 바로 보내지 말고 검증 경로를 요구해라.
- checkpoint와 config의 짝이 맞는지 확인해라.
- inference latency와 control loop 주기에 미치는 영향을 확인해라.
- 센서 미응답, 통신 실패, 장비 좌표계 불일치, 모델 출력 이상값을 실패 조건에 포함해라.
- 실제 장비 적용 전 simulation 또는 dry-run 검증을 요구해라.
- 소프트웨어 문제처럼 보여도 하드웨어, 하네스, 전원, 커넥터 가능성을 남겨라.
```

## 업데이트 메모

- [ ] 실제 장비 테스트 중 반복된 기준 추가
