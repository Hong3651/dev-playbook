# prompts

AI에게 전달할 실행 프롬프트를 조립하는 폴더다.
하나의 거대한 프롬프트를 유지하지 않고, 공통 기준과 작업 기준과 분야 기준을 나눠 붙인다.

## 조립 순서

기본 순서:

1. `base.md`
2. `tasks/*.md` 중 하나
3. 필요한 `addons/*.md` 0개 이상
4. 실제 요청, 파일 목록, 기대 동작, 제약 조건

예시:

```text
prompts/base.md
prompts/tasks/implement_feature.md
prompts/addons/robot_infra.md
실제 요청과 관련 파일
```

웹 대시보드가 장비 명령을 실행하는 경우처럼 기준이 겹치면 addon을 여러 개 붙인다.

```text
prompts/base.md
prompts/tasks/design_review.md
prompts/addons/web_service.md
prompts/addons/robot_infra.md
설계안
```

## 파일 역할

- `base.md`: 모든 AI 작업에 항상 적용할 공통 원칙
- `tasks/`: 이번 작업이 무엇인지 정하는 프롬프트
- `addons/`: 프로젝트 분야별로 추가할 실행 기준

## 주의점

- `core/`와 `profiles/`는 사람이 읽는 기준 문서다.
- `prompts/`는 AI에게 바로 붙이는 실행 지시다.
- addon은 profile 내용을 전부 복사하지 말고, AI가 지켜야 할 기준만 짧게 둔다.
- 작업에 필요한 기준이 없으면 새 addon을 만들기보다 먼저 `profiles/`에 사람용 기준이 필요한지 판단한다.

## 업데이트 메모

- [ ] 실제 조립 예시 추가
- [ ] 자주 쓰는 조합 추가
