---
object_id: HRTDB_ACTIVE_SCHEMA_AS_F5_TOPOLOGY_EXPERIMENT_CONSOLIDATED_RECOVERY_0001
object_class: ACTIVE_SCHEMA_TOPOLOGY_EXPERIMENT_RECOVERY
phase_id: AS_F5_RECOVERY_DURING_AS_F7
source_authority: 승이
coordination_authority: gpt.logi
status: RECOVERED_WITH_CAUSAL_LIMITS
recovery_reason: DISTINCT_AS_F5_EXACT_BYTE_ARTIFACT_NOT_PRESENT_IN_CURRENT_WORKSPACE
---

# HRTDB AS_F5 Topology Experiment — Consolidated Recovery

## 1. Comparison identity

```text
DISTRIBUTED_SEVEN_INSTANCE
vs
SINGLE_INSTANCE_MULTI_SEAT
```

실험은 같은 Cycle 목적과 동일한 Semantic Result.Data ID를 사용했으나 모든 상위 입력 Byte가 동일한 완전통제실험은 아니다.

```yaml
experiment_class: QUASI_CONTROLLED_TOPOLOGY_COMPARISON
operational_difference_observed: true
topology_only_causation_proved: false
```

## 2. Distributed route

```yaml
topology: DISTRIBUTED_SEVEN_INSTANCE
instances:
  - gpt.x
  - gpt.y
  - gpt.z
  - gpt.xy
  - gpt.xz
  - gpt.yz
  - gpt.xyz
coordinator:
  seat: gpt.xyzt
  occupant: gpt.logi
```

```yaml
result:
  object_id: HRTDB_PILOT_RESULT_DATA_0003_XYZ
  exact_byte_sha256: 72428e7ddf3ea03db711449f3930698e82e4961a25103f330fa482dc7262d65b
  review_units: 80
  deviations: 16
  corrections: 16
  blocking_corrections: 7
  nonblocking_corrections: 9
  applied_corrections: 16
  correction_conflicts: 0
  result_data_cells: 70
  final_verdict: PASS_RESULT_DATA_WITH_UNRESOLVED_ITEMS
  persistence: TRACK_DB_REGISTERED
```

## 3. Single-instance route

```yaml
topology: SINGLE_INSTANCE_MULTI_SEAT
runtime_instance: gpt.idea
occupied_seats: [X, Y, Z, XY, XZ, YZ, XYZ]
```

```yaml
result:
  exact_byte_sha256: 5eed3f7d927e34cd32673decb9b1f520187f8b631d84560f52401e8a5726deed
  expected_corrections: 16
  actual_corrections: 11
  applied_corrections: 0
  result_data_cells: 0
  final_verdict: HOLD_CORRECTION_INVENTORY_MISMATCH
  result_data_completed: false
  memory_asset_eligibility: false
  persistence_class: SINGULARITY_ONLY
```

## 4. Direct observations

```yaml
observed_differences:
  distributed:
    seat_runtime_separation: PRESENT
    independent_review_runtime: PRESENT
    handoff_count: HIGHER
    correction_inventory_match: PASS
    memory_asset_completion: PASS

  single_instance:
    seat_runtime_separation: ABSENT
    continuous_context: PRESENT
    handoff_count: LOWER
    correction_inventory_match: HOLD
    memory_asset_completion: NOT_REACHED
```

## 5. Strengths and limits

### Distributed

```text
Strengths
→ Seat 독립성
→ 교차 오독검출
→ 책임·Lineage 분리
→ 부분 재실행
→ Canonical Memory 형성에 적합

Limits
→ 전달객체가 많음
→ Identity·Handoff 관리비용
→ 관제부담
```

### Single instance

```text
Strengths
→ Context 연속성
→ 전달손실 감소
→ 빠른 예비탐색

Limits
→ Seat Context 결합
→ 자기확증 위험
→ Variant 선택혼동
→ Authority Snapshot Drift
→ Context 포화 집중
```

## 6. Directive packaging refinement

분산 실행과 지시문 포장은 다른 축이다.

```yaml
execution_topology: DISTRIBUTED_SEVEN_INSTANCE
primary_directive_model: ONE_TARGET_ONE_ORDER
stage_transport: SAME_ORDER_WITH_NEW_STAGE_INPUTS
fallbacks:
  - FIVE_SHARED_STAGE_DIRECTIVES
  - ELEVEN_SEAT_SPECIFIC_DIRECTIVES
```

```text
지시문 1개
≠ Instance 1개
≠ Context Window 1개
≠ Output 1개
```

## 7. Current topology decision

```yaml
distributed_topology:
  state: REGISTERED_RUNTIME_SUPPORTED
  role: CANONICAL_MEMORY_DEFAULT_CANDIDATE

single_instance_topology:
  state: EXPERIMENTAL_SINGULARITY_EVIDENCE
  role: NON_CANONICAL_EXPERIMENTAL_ROUTE

hybrid_topology:
  state: OPEN_FUTURE
```

## 8. Verdict

```yaml
verdict: PASS_AS_F5_EXPERIMENT_RECOVERED_WITH_CAUSAL_LIMITS
```

```text
END_OF_HRTDB_ACTIVE_SCHEMA_AS_F5_TOPOLOGY_EXPERIMENT_CONSOLIDATED_RECOVERY_0001
```
