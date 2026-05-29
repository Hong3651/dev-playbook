# dev-playbook

새 개발 프로젝트를 시작할 때 좋은 코드베이스를 만들기 위한 개발 플레이북이다.

이 레포는 단순한 프롬프트 모음집이 아니다. 프로젝트마다 같은 폴더 구조와 같은 코드를 찍어내기 위한 저장소도 아니다. 

> 코드를 정형화하는 것이 아니라 판단 기준을 정형화한다.

## 목적

- 프로젝트 시작 전에 목적, 범위, 위험 요소를 먼저 정리한다.
- 모든 프로젝트에 공통으로 적용할 원칙을 짧고 강하게 유지한다.
- 프로젝트 타입별로 다른 기준은 `profiles/`에 나누어 둔다.
- 플레이북 자체의 개선 예정과 완료 항목은 `progress.md`에서 관리한다.
- AI에게 맡길 일과 사람이 직접 판단할 일을 구분한다.

## MD와 프롬프트의 차이

- `core/`, `profiles/`, `templates/`의 Markdown 문서는 지속되는 원칙, 규약, 체크리스트, 도메인 지식이다.
- `prompts/`의 Markdown 문서는 AI에게 이번 작업을 어떻게 수행할지 지시하는 실행 명령이다.
- `progress.md`는 이 플레이북 자체의 개선 예정과 완료를 관리하는 작업판이다.
- 문서는 판단 기준이고, 프롬프트는 작업 지시다.

## 사용 흐름

1. 새 프로젝트 목적을 짧게 적는다.
2. `core/dev_guide.md`를 확인한다.
3. 프로젝트 성격에 맞는 `profiles/` 문서를 고른다.
4. `templates/project_kickoff.md`를 복사해 프로젝트 시작 문서를 만든다.
5. 필요하면 `templates/product.md`, `templates/architecture.md`, `templates/plan.md`를 채운다.
6. AI에게 요청할 때는 `prompts/`의 실행 프롬프트를 상황에 맞게 사용한다.
7. 플레이북을 고칠 아이디어나 완료한 정리는 `progress.md`에 기록한다.

## 새 프로젝트 시작 시 우선 참고 문서

- 자동화 스크립트: `profiles/automation.md`
- 로봇 인프라: `profiles/robot_infra.md`
- 웹 서비스: `profiles/web_service.md`
- 코드베이스 요약: `templates/codebase_overview.md`

## 민감정보 금지

이 레포는 Public일 수 있다. 회사 비밀, API 키, 토큰, 고객사 정보, 실제 프로젝트 내부 경로, 장비 시리얼, 비공개 장애 사례를 기록하지 않는다.

필요하면 구체값 대신 다음처럼 쓴다.

- `API_KEY=<redacted>`
- `CUSTOMER_A`
- `internal-service.example`
- `장비 모델명 비공개`

## 업데이트 메모

- 개인 프로젝트를 시작할 때 실제로 참고한 항목을 추가한다.
- 반복되는 판단 실수는 적절한 가이드나 프로필 문서에 직접 반영한다.
- 플레이북 개선 작업의 예정과 완료는 `progress.md`에 남긴다.
