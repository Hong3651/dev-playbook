# 진행 관리

이 문서는 `dev-playbook` 자체를 개선하기 위한 작업 상태를 관리한다.
프로젝트 개발 TODO가 아니라, 이 플레이북 문서의 개선 예정/완료 항목을 기록한다.

핵심 원칙은 간단하다.

- 실제 내용은 해당 Markdown 파일에 반영한다.
- `progress.md`에는 작업 상태와 반영 대상 파일명을 남긴다.
- 반영 대상 파일이 불명확한 항목은 바로 작업하지 않고 먼저 정리한다.

## 항목 작성 형식

모든 항목은 아래 형식을 따른다.

```md
- [ ] 작업 내용
  - 반영 파일: `path/to/file.md`
  - 상태: 예정 / 진행 중 / 완료 / 보류
```

여러 파일에 반영해야 하면 모두 적는다.

```md
- [ ] 작업 내용
  - 반영 파일: `README.md`, `templates/project_kickoff.md`
  - 상태: 예정
```

## 예정

- [ ] README 문체를 더 실무 메모처럼 줄일지 검토
  - 반영 파일: `README.md`
  - 상태: 예정

- [ ] 프로젝트 타입별 사용 기준 정리
  - 반영 파일: `profiles/automation.md`, `profiles/robot_infra.md`, `profiles/web_service.md`
  - 상태: 예정

## 완료

- [x] 템플릿 문서가 실제로 복사해서 쓰기 좋은지 점검
  - 반영 파일: `templates/project_kickoff.md`, `templates/product.md`, `templates/architecture.md`, `templates/plan.md`, `templates/codebase_overview.md`
  - 상태: 완료


- [x] 일반 프롬프트와 profile 세부 기준을 분리
  - 반영 파일: `prompts/start_project.md`, `prompts/design_review.md`, `prompts/implement_feature.md`, `prompts/verify_code.md`, `prompts/summarize_changes.md`, `prompts/validate_playbook.md`
  - 상태: 완료


- [x] 프롬프트를 플레이북 문서에 의존하지 않는 독립 실행형으로 정리
  - 반영 파일: `prompts/start_project.md`, `prompts/design_review.md`, `prompts/implement_feature.md`, `prompts/verify_code.md`, `prompts/summarize_changes.md`, `prompts/validate_playbook.md`
  - 상태: 완료


- [x] 검증 에이전트 지적 사항 정리
  - 반영 파일: `README.md`, `templates/project_kickoff.md`, `progress.md`
  - 상태: 완료


- [x] 프롬프트별로 실제 필요한 문서 역할만 남기고 과한 구조 설명 제거
  - 반영 파일: `prompts/start_project.md`, `prompts/design_review.md`, `prompts/implement_feature.md`, `prompts/verify_code.md`, `prompts/summarize_changes.md`
  - 상태: 완료

- [x] 플레이북 전체 문서 검증용 프롬프트 추가
  - 반영 파일: `prompts/validate_playbook.md`, `progress.md`
  - 상태: 완료

- [x] `core/` 문서를 단일 개발 가이드로 통합
  - 반영 파일: `core/dev_guide.md`, `README.md`
  - 상태: 완료

- [x] 개발 가이드를 `MUST / SHOULD / AVOID` 중심으로 재작성
  - 반영 파일: `core/dev_guide.md`
  - 상태: 완료

- [x] 경험 기록용 별도 폴더 대신 진행 관리 방식으로 전환
  - 반영 파일: `progress.md`, `README.md`
  - 상태: 완료

- [x] 임시 메모 방식 대신 `progress.md`로 플레이북 개선 작업을 관리하도록 변경
  - 반영 파일: `progress.md`, `README.md`
  - 상태: 완료

- [x] 진행 항목에 실제 반영 파일명을 명시하는 규칙 추가
  - 반영 파일: `progress.md`
  - 상태: 완료

## 보류

- [ ] 반복 실수와 패턴을 별도 문서로 관리할지 여부
  - 반영 파일: `core/dev_guide.md`, `progress.md`
  - 상태: 보류

## 업데이트 메모

- [ ] 완료된 항목이 많아지면 날짜별 완료 이력으로 정리
- [ ] 보류 항목은 반영 파일이 정해질 때까지 작업하지 않기
