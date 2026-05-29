# 작업 프롬프트: 플레이북 문서 검증

`dev-playbook` 자체를 검증하는 에이전트에게 붙이는 작업 프롬프트다.
제작자와 검증자를 분리해 문서 구조, 역할, 내용 일관성을 확인할 때 사용한다.

## 조립

```text
prompts/base.md
prompts/tasks/validate_playbook.md
검증할 Markdown 파일 내용
```

## 프롬프트

```text
이번 작업의 목표는 개발 플레이북 문서 검증이다.
Markdown 문서 전체가 플레이북 목적에 맞는지 검증해라.
새 내용을 만들기보다 문제, 충돌, 누락, 과한 설명을 찾아라.

검증 대상:

- README.md
- progress.md
- core/dev_guide.md
- profiles/*.md
- templates/*.md
- prompts/base.md
- prompts/README.md
- prompts/tasks/*.md
- prompts/addons/*.md

검증 기준:

1. 문서 역할이 명확한가?
2. 파일명과 README 설명이 일치하는가?
3. 낡은 파일명이나 삭제된 구조를 참조하지 않는가?
4. 같은 기준이 여러 문서에서 충돌하지 않는가?
5. 내용이 너무 추상적이지 않고 실제 작업에 쓸 수 있는가?
6. 프롬프트가 제공되지 않은 파일을 알고 있다고 가정하지 않는가?
7. base, task, addon 역할이 분리되어 있는가?
8. task 프롬프트가 특정 profile 세부 기준을 직접 포함하지 않는가?
9. addon 기준이 profiles 문서와 충돌하지 않는가?
10. progress.md 항목에 실제 반영 파일명이 명시되어 있는가?
11. 각 Markdown 문서에 제목과 업데이트 메모가 있는가?

출력 형식:

- 전체 판정: 통과 / 조건부 통과 / 실패
- 치명적 문제:
- 수정 권장 문제:
- 가벼운 정리 사항:
- 잘 유지된 기준:
- 최종 보고 가능 여부: 가능 / 불가
```

## 업데이트 메모

- [ ] 검증 기준을 실제 리뷰 결과에 맞춰 보강
- [ ] 반복적으로 발견되는 문서 품질 문제 추가
