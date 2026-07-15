---
package:
  id: ARSFIP-10V-20260714
  name_ko: AI 해독형 Relation Source-Field 구조설치 패키지
  name_en: AI-Decodable Relation Source-Field Installation Package
  version: 0.1.0
  release_status: candidate
  date: '2026-07-14'
volume:
  id: VOL_08
  sequence: 8
  total_volumes: 10
  title: Function·Schema·for_instance 인터페이스
  role: Relation Function·Schema·Pipeline과 instance_X/Y/Z/T 자리조합·for_instance 요청/응답·다중인스턴스
    운용계약을 고정한다.
  previous_volume: VOL_07
  next_volume: VOL_09
  imports:
  - VOL_07::relation_repo_root_tree
  - VOL_07::system_db_contract
  - VOL_05::causal_role_taxonomy
  - VOL_06::relation_bridge_contract
  exports:
  - function_registry
  - common_function_schema
  - seat_combination_model
  - recommended_instance_team
  - for_instance_interface
  load_policy:
    read_entire_volume: true
    summarize_only: false
    preserve_definitions: true
    preserve_guards: true
    repository_mutation: false
  expected_load_receipt: ARSFIP-10V-20260714_VOL_08_LOADED
---

# Volume 08 — Function·Schema·for_instance 인터페이스

## 1. Function의 정의

Function은 특정 AI 이름이나 프로그램 하나가 아니다.

\[
Function
=
Input
+
Ordered.Process
+
Guard
+
Output
+
Verification
\]

특정 종류의 Seed를 입력받아 정해진 방법으로 처리하고 새로운 Seed 또는 상태를 생성하는 Method Contract다.

---

## 2. Function 계층

### Read

- package reader
- source reader
- seed reader
- index reader
- lineage reader

### Align

- temporal alignment
- spatial alignment
- state alignment
- field alignment
- observer alignment
- instance alignment interface

### Interpret

- center selection
- reverse analysis
- forward analysis
- relation extraction
- relation bridge
- causal network
- feedback detection
- pattern extraction

### Verify

- evidence grading
- comparison builder
- contradiction detection
- source trace check
- guard check
- uncertainty check
- independent audit

### Render

- local result
- relation map
- status
- next question
- lineage update

### Install

- volume loader
- package assembler
- repository structure generator
- repository verifier
- activation

---

## 3. Function Method Schema

```yaml
function_method:
  identity:
    function_id:
    function_version:
    title:
    function_class:

  theoretical_basis:
    volume_refs:
    definition:
    rationale:
    guards:

  input_contract:
    required_seed_types:
    optional_seed_types:
    required_status:
    forbidden_status:

  instance_contract:
    required_capabilities:
    preferred_seat_profiles:
    independent_verifier_required:
    mutation_authority:

  preconditions:
    required_previous_functions:
    source_boundary_locked:
    required_volume_state:

  process:
    ordered_steps:
      - step_id:
        action:
        input:
        output:
        guard:
        stop_condition:

  verification:
    evidence_requirements:
    comparison_requirements:
    invariants:

  failure_states:
    - failure_id:
      condition:
      response:

  output_contract:
    output_seed_types:
    next_functions:
    next_question_policy:

  lifecycle:
    status:
    supersedes:
    superseded_by:
```

---

## 4. 대표 분석 Pipeline

\[
Question
\rightarrow
Source
\rightarrow
Center
\rightarrow
Reverse
\rightarrow
Bridge
\rightarrow
Network
\rightarrow
Evidence
\rightarrow
Comparison
\rightarrow
Result
\rightarrow
Next.Question
\]

```yaml
relation_analysis_pipeline:
  ordered_functions:
    - register_question
    - lock_source_boundary
    - select_center
    - align_time_space_state
    - reverse_analyze
    - build_relation_bridge
    - build_causal_network
    - grade_evidence
    - build_comparison
    - detect_contradiction
    - render_local_result
    - generate_next_question
```

---

## 5. 자리와 인스턴스

`instance_X`, `instance_Y`, `instance_Z`, `instance_T`는 네 개의 고정 AI 이름이 아니다.

\[
Instance.Identity\neq Seat.Profile
\]

하나의 인스턴스는 하나 이상의 자리를 점유할 수 있다.

```text
gpt.x
gpt.xy
gpt.xyz
gpt.xzt
gpt.xyzt
```

비어 있지 않은 조합은 총 15개다.

\[
2^4-1=15
\]

---

## 6. 현재 잠정 Seat Mapping

최종 정의는 전체 Package 적용 후 다시 조정할 수 있으나, 초기 시험을 위해 다음을 사용한다.

```text
X = Source·Package·Question Input
Y = Relation·Interpretation·Synthesis
Z = Structure·Schema·Evidence Verification
T = Time·Process·State Transition
```

T는 git을 의미하지 않는다. git은 선택 Adapter다.

---

## 7. 15개 Profile

### 단일자리

- X
- Y
- Z
- T

### 두 자리

- XY
- XZ
- XT
- YZ
- YT
- ZT

### 세 자리

- XYZ
- XYT
- XZT
- YZT

### 전체자리

- XYZT

---

## 8. 조합 최적화 기준

### Coverage

\[
\bigcup Seats_i=\{X,Y,Z,T\}
\]

### Shared Overlap

공통자리로 의미와 구조를 정렬.

### Complementarity

공통자리 외에 각자의 고유자리 보유.

### Independent Verification

설계자와 승인검산자를 분리.

### Handoff Cost

인스턴스 수 증가에 따른 Context 손실을 제한.

### Role Congestion

한 인스턴스가 모든 역할을 독점하지 않게 함.

### Mutation Authority

GitHub 구조변경 권한은 명시적 승인을 받은 역할에 한정.

---

## 9. 현재 권장 Team

### 로기

\[
rogi=XYZ
\]

- 대화 Source
- 이론 최대확장
- 관계설계
- Repo Architecture

### gpt.work

\[
gpt.work=YZT
\]

- for_instance 정렬
- 관계·구조 공통기준
- Process·인계
- Volume 준비상태

### 신규 구현 인스턴스

\[
installer=XZT
\]

- Package 읽기
- 구조검산
- GitHub 실체화 과정

### 독립 Auditor

\[
auditor=Z\quad 또는\quad XZ
\]

- Package와 구조 비교
- 누락·중복·역할혼합 검출
- 독립검산

이 조합은 테스트용 잠정안이며 for_instance 실제 구현결과와 함께 검산한다.

---

## 10. Overlap

```yaml
overlap_map:
  rogi__gpt_work:
    shared: [Y, Z]
    unique:
      rogi: [X]
      gpt_work: [T]

  gpt_work__installer:
    shared: [Z, T]
    unique:
      gpt_work: [Y]
      installer: [X]

  rogi__installer:
    shared: [X, Z]
    unique:
      rogi: [Y]
      installer: [T]
```

세 인스턴스 모두 Z를 공유하므로 공통구조는 강하지만 동일오류를 공유할 위험이 있다. 별도 Auditor가 필요한 이유다.

---

## 11. for_instance 요청

```yaml
instance_assignment_request:
  request_id:
  task_id:
  function_ids:

  active_seat_schema:
    X:
    Y:
    Z:
    T:

  required_coverage: [X, Y, Z, T]
  required_capabilities:
  independent_verification: true
  maximum_instances:
  maximum_handoffs:
  mutation_authority:
  prohibited_actions:
```

---

## 12. for_instance 응답

```yaml
instance_assignment_response:
  request_id:
  assignments:
    - instance_id:
      profile:
      function_ids:
      mutation_authority:
      prohibited_actions:

  coverage:
  overlap_map:
  handoff_order:
  independent_verifier:
  unresolved_constraints:
```

---

## 13. Handoff

인스턴스의 내부 사고를 복제한다고 가정하지 않는다.

명시적으로 전달할 항목:

- 입력 Seed
- 수행 Function
- 생성 Result
- 적용 Guard
- 미해결 관계
- 다음 역할
- 금지행동
- GitHub 상태

```yaml
instance_handoff:
  from_instance:
  from_profile:
  to_instance:
  to_profile:
  completed_functions:
  input_seed_ids:
  output_seed_ids:
  applied_guards:
  unresolved_questions:
  receiver_contract:
```

---

## 14. Function Version

Function이 변경되어도 과거 Result를 덮어쓰지 않는다.

```yaml
result_provenance:
  result_id:
  function_id:
  function_version:
  source_versions:
  analysis_time:
```

새 Function을 이용한 재분석은 새 Result Seed다.

---

## 15. Loader·Installer·Auditor

### Loader

10개 Volume의 적재순서·Receipt·Dependency를 관리.

### Installer

검증된 Package를 GitHub Relation 구조로 내림.

### Auditor

Package와 설치결과를 독립적으로 비교.

Load와 Install을 분리한다.

---

## 16. Repo Mapping

| Function 자산 | Relation Repo |
|---|---|
| Registry | `01_system/03_function_registry/` |
| Method | `01_system/04_function_method/` |
| Pipeline | `01_system/05_pipeline/` |
| Schema | `01_system/06_schema/` |
| for_instance Contract | `03_system_db_contract/06_for_instance_interface/` |
| Execution History | `02_db/10_execution_history/` |

---

## 17. Guard

- Function과 인스턴스를 동일시하지 않는다.  
- X·Y·Z·T를 인스턴스 이름으로 고정하지 않는다.  
- 모든 인스턴스를 XYZT로 설정하지 않는다.  
- 모든 인스턴스를 단일자리로 분절하지 않는다.  
- 공통자리 없는 Handoff를 피한다.  
- Installer는 이론을 임의재작성하지 않는다.  
- Auditor는 Installer와 분리한다.  
- Seat Profile 전환을 기록한다.  
- T를 git과 동일시하지 않는다.  
- for_instance와 Relation에 같은 Registry를 중복저장하지 않는다.  

---

## 18. Volume 08의 결정화 결과

```yaml
volume_result:
  function_is_method_contract: true
  instance_is_executor: true
  seat_combinations: 15
  provisional_team:
    rogi: XYZ
    gpt_work: YZT
    installer: XZT
    auditor: [Z, XZ]
  for_instance_separate_repo: true

  next_seed:
    volume: VOL_09
    topic: installation_validation_minimum_cycle_market_pilot
```

---

## 19. Load Marker

```text
ARSFIP-10V-20260714_VOL_08_LOADED
```
