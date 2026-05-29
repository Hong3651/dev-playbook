# dev-playbook

새 개발 프로젝트를 시작할 때 쓰는 개발 플레이북이다.
목표는 코드를 찍어내는 것이 아니라 판단 기준을 재사용하는 것이다.

> 코드를 정형화하지 말고, 판단 기준을 정형화한다.

## 쓰는 순서

1. 프로젝트 목적을 한 문장으로 적는다.
2. `core/dev_guide.md`로 공통 원칙을 확인한다.
3. 프로젝트 성격에 맞는 `profiles/` 문서를 고른다.
4. `templates/project_kickoff.md`를 복사해 시작 문서를 만든다.
5. 필요할 때만 `product.md`, `architecture.md`, `plan.md`, `codebase_overview.md`를 추가한다.
6. AI에게 맡길 때는 `prompts/`의 실행 프롬프트를 사용한다.
7. 플레이북 자체의 개선 사항은 `progress.md`에 남긴다.

## 문서 역할

- `core/dev_guide.md`: 모든 프로젝트에 공통으로 적용할 원칙
- `profiles/automation.md`: 파일 처리, 로그 정리, 반복 작업 자동화
- `profiles/robot_infra.md`: 로봇, 장비, VLA inference, 실험 파이프라인
- `profiles/web_service.md`: API 서버, 대시보드, admin tool, 웹 UI
- `templates/`: 프로젝트 문서로 복사해서 채우는 양식
- `prompts/`: AI에게 바로 전달하는 실행 지시
- `progress.md`: 이 플레이북 자체의 개선 상태

## 먼저 볼 파일

새 프로젝트 시작:

- `core/dev_guide.md`
- `templates/project_kickoff.md`
- 필요한 `profiles/*.md`

기존 코드베이스를 AI에게 설명:

- `templates/codebase_overview.md`
- `prompts/implement_feature.md`
- `prompts/verify_code.md`

플레이북 자체를 점검:

- `progress.md`
- `prompts/validate_playbook.md`

## 민감정보 금지

이 저장소는 public일 수 있다.
다음 정보는 기록하지 않는다.

- 회사 비밀
- API 키, 토큰, 세션 값
- 고객사 정보
- 실제 내부 URL과 경로
- 장비 시리얼
- 비공개 장애 사례

필요하면 구체값 대신 이렇게 쓴다.

- `API_KEY=<redacted>`
- `CUSTOMER_A`
- `internal-service.example`
- `장비 모델명 비공개`

## 업데이트 기준

- 반복되는 판단 실수는 관련 가이드나 profile에 직접 반영한다.
- 새 프로젝트에서 실제로 도움 된 항목은 문서에 남긴다.
- 개선 예정과 완료 상태는 `progress.md`에서 관리한다.
