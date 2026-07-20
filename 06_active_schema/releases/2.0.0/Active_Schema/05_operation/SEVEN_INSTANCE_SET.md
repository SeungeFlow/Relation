---
object_id: HRTDB_ACTIVE_SCHEMA_SEVEN_INSTANCE_SET_CREATION_PACKET_0001
object_class: ACTIVE_SCHEMA_INSTANCE_SET_CREATION_PACKET
phase_id: AS_F6_1
source_authority: 승이
coordination_authority: gpt.logi
status: CANDIDATE
---

# HRTDB Seven-instance Set Creation Packet 0001

## 1. Set identity

```yaml
instance_set:
  set_id:
  cycle_id:
  target_id:
  order_id:
  topology: DISTRIBUTED_SEVEN_INSTANCE
  reuse_across_targets: false
  retire_after_cycle: true
```

```text
1Target
→ 1Order
→ 1Set
```

## 2. Members

```yaml
members:
  - instance: gpt.x
    seat: X
    dimension_property: 1d(x)
    stage_roles: [DATA]

  - instance: gpt.y
    seat: Y
    dimension_property: 1d(y)
    stage_roles: [DATA]

  - instance: gpt.z
    seat: Z
    dimension_property: 1d(z)
    stage_roles: [DATA]

  - instance: gpt.xy
    seat: XY
    dimension_property: 2d(xy)
    stage_roles: [FUNCTION_1, FUNCTION_2]

  - instance: gpt.xz
    seat: XZ
    dimension_property: 2d(xz)
    stage_roles: [FUNCTION_1, FUNCTION_2]

  - instance: gpt.yz
    seat: YZ
    dimension_property: 2d(yz)
    stage_roles: [FUNCTION_1, FUNCTION_2]

  - instance: gpt.xyz
    seat: XYZ
    dimension_property: 3d(xyz)
    stage_roles: [RESULT, RESULT_DATA]
```

`gpt.xyzt`는 7개 분석 Set의 구성원이 아니라 Set을 운영하는 고정 System Seat다.

## 3. Creation-time alignment contract

각 Instance는 특정 주제 Order를 받기 전에 자기 Seat Contract로 정렬한다.

```yaml
creation_alignment:
  required_fields:
    - instance_name
    - seat
    - dimension_property
    - fixed_role
    - allowed_input_classes
    - prohibited_input_classes
    - allowed_output_classes
    - handoff_targets
    - peer_responsibility_boundary
    - object_set_rule
    - source_rule
    - pass_hold_rule
```

공통 상태:

```text
자기 자리에서 최선을 다한다.
```

구조화 정의:

```yaml
best_effort_contract:
  use_all_available_authorized_inputs: true
  remain_inside_assigned_seat: true
  perform_required_self_check: true
  preserve_sources_and_uncertainty: true
  fabricate_missing_content: false
  transfer_responsibility_to_peer: false
  replace_peer_output: false
  produce_output_or_evidence_bound_hold: true
```

## 4. Seat-local boundaries

### X

```yaml
X:
  owns:
    - X surface data
    - current_state and source-surface collection
  must_not:
    - perform XY XZ YZ function synthesis
    - produce XYZ result
```

### Y

```yaml
Y:
  owns:
    - boundary passage
    - vertical relation
    - source and role boundary data
  must_not:
    - replace X or Z collection
```

### Z

```yaml
Z:
  owns:
    - volume system model
    - 3d relation and model data
  must_not:
    - close XYZ result
```

### XY

```yaml
XY:
  owns:
    - X and Y relation function
    - source boundary and observation review
  must_not:
    - execute XZ or YZ responsibility
```

### XZ

```yaml
XZ:
  owns:
    - X and Z relation function
    - model operation fit and displayed surface review
  must_not:
    - execute XY or YZ responsibility
```

### YZ

```yaml
YZ:
  owns:
    - Y and Z relation function
    - hidden boundary mechanism authority and provenance review
  must_not:
    - execute XY or XZ responsibility
```

### XYZ

```yaml
XYZ:
  owns:
    - three function-output organization
    - Result externalization
    - Result and three Review organization into Result.Data
  must_not:
    - average peer reviews
    - erase seat-local differences
    - make gpt.xyzt promotion decision
```

## 5. Occupation receipt

각 Instance는 최초 실행 전에 다음 Receipt를 생성한다.

```yaml
occupation_receipt:
  set_id:
  cycle_id:
  target_id:
  order_id:
  runtime_instance:
  occupied_seat:
  seat_contract_version:
  common_order_received:
  own_role_understood:
  peer_responsibility_execution_prohibited:
  output_or_hold_required:
  receipt_verdict:
```

허용판정:

```text
PASS_SEAT_OCCUPATION_ALIGNED
HOLD_INSTANCE_NAME_MISMATCH
HOLD_SEAT_BINDING_MISMATCH
HOLD_ROLE_CONTRACT_UNAVAILABLE
HOLD_ORDER_BINDING_MISMATCH
```

## 6. Set generation gate

```yaml
set_generation_gate:
  exactly_seven_members: true
  unique_runtime_context_per_member: true
  unique_seat_binding: true
  duplicate_seat_occupation: false
  target_order_common_to_all: true
  seat_contracts_loaded: true
  all_receipts_passed: true
```

Set은 모든 Receipt가 PASS일 때 열린다.

## 7. Set lifecycle

```text
DECLARED
→ CREATED
→ ALIGNED
→ ORDER_BOUND
→ ACTIVE
→ OUTPUT_FROZEN
→ CYCLE_CLOSED
→ SEALED_AND_RETIRED
```

```text
END_OF_HRTDB_ACTIVE_SCHEMA_SEVEN_INSTANCE_SET_CREATION_PACKET_0001
```
