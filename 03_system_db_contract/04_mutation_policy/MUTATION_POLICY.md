# Mutation Policy

설계검산과 구현검산을 구분한다.

```text
VALIDATION_PASSED
→ CLOSED_FOR_VALIDATION
→ OPEN_FOR_IMPLEMENTATION
```

새로운 실제 결함근거 없이 완료된 검산을 재개하지 않는다.

```text
MAJOR_CONCEPT_CHANGE
→ CUTOVER_REQUIRED
→ CURRENT_STATE_FREEZE
→ NEW_BASELINE
→ NEW_HANDOFF
```

기존 Result를 수정해 과거 분석상태를 제거하지 않는다.
새 해석은 새 Result Seed와 Provenance를 생성한다.
for_instance의 자리·역할 이론을 Relation에서 재정의하지 않는다.
Relation은 Function Requirement와 Assignment Reference만 보존한다.
