---
package:
  id: ARSFIP-10V-20260714
  name_ko: AI 해독형 Relation Source-Field 구조설치 패키지
  name_en: AI-Decodable Relation Source-Field Installation Package
  version: 0.1.0
  release_status: candidate
  date: '2026-07-14'
volume:
  id: VOL_07
  sequence: 7
  total_volumes: 10
  title: 'Relation Repo: System–DB 통합 아키텍처'
  role: Relation Repo 안에서 구조해석 System과 기억 DB가 함께 존재하고 for_instance가 별도 Repo로 실행주체를
    정렬하는 실체 아키텍처를 확정한다.
  previous_volume: VOL_06
  next_volume: VOL_08
  imports:
  - VOL_01::repo_role_boundary
  - VOL_04::grid_matrix_tensor_roles
  - VOL_05::historical_forest_model
  - VOL_06::evidence_taxonomy
  exports:
  - relation_repo_root_tree
  - system_area_contract
  - db_area_contract
  - system_db_contract
  - github_canonical_model
  load_policy:
    read_entire_volume: true
    summarize_only: false
    preserve_definitions: true
    preserve_guards: true
    repository_mutation: false
  expected_load_receipt: ARSFIP-10V-20260714_VOL_07_LOADED
---

# Volume 07 — Relation Repo: System–DB 통합 아키텍처

## 1. 핵심 정의

Relation Repo에는 두 영역이 함께 존재해야 한다.

\[
\boxed{
Relation.Repo
=
System.Area
+
DB.Area
+
System/DB.Contract
+
Book.Package
}
\]

### System 영역

- 이론
- 용어
- Reader Policy
- Function Registry
- Function Method
- Pipeline
- Schema
- Guard
- Verification
- Installation Method
- Audit Method
- System History

### DB 영역

- Field Registry
- Source Seed
- Data Seed
- Center Cell
- Relation Seed
- Evidence Seed
- Comparison Seed
- Result Seed
- Question Seed
- Lineage
- Execution History
- Index

### Contract 영역

- Function Input/Output
- Provenance
- Version Binding
- Mutation Policy
- Integrity
- for_instance Interface

### Book Package

- 10개 Volume
- Package Index
- Load Receipt
- Repo Mapping
- Release Bundle

---

## 2. System과 DB를 같은 Repo에 두는 이유

Data만 있고 방법이 없으면 후속 인스턴스가 다른 방식으로 읽는다.

방법만 있고 Data가 없으면 Result를 재현할 수 없다.

따라서 하나의 Version에서 다음을 함께 고정해야 한다.

\[
Function.Version
+
Input.Seed.Version
+
Guard.Version
+
Result.Version
\]

Relation Repo의 하나의 Version 상태는 다음을 보여 준다.

- 당시 이론
- 당시 Function
- 당시 Seed
- 당시 Evidence
- 당시 Result
- 당시 Question

---

## 3. System은 자율서버가 아니다

Relation System은 스스로 실행되는 서버 프로세스라고 정의하지 않는다.

정확한 의미는 다음이다.

> for_instance에서 배정된 AI 인스턴스가 Relation System의 Method와 Contract를 따라 Relation DB Seed를 읽고 새로운 Seed를 생성한다.

\[
Assigned.Instance
\rightarrow
System.Method
\rightarrow
DB.Mutation
\]

---

## 4. for_instance의 독립성

\[
for\_instance\not\subset Relation
\]

for_instance는 별도 Repo다.

Relation은 필요한 Function·Capability·Seat를 요청한다.

for_instance는 실제 인스턴스를 배정한다.

```yaml
relation_instance_request:
  request_id:
  function_ids:
  required_capabilities:
  required_seats:
  independent_verification:
  mutation_level:
```

```yaml
for_instance_assignment:
  request_id:
  assigned_instances:
  seat_profiles:
  handoff_order:
  mutation_authority:
  verifier:
```

Relation은 for_instance의 전체 Registry를 복제하지 않고 Assignment 참조만 DB에 남긴다.

---

## 5. Canonical Root Tree

```text
Relation/
├─ README.md
├─ 00_manifest/
├─ 01_system/
├─ 02_db/
├─ 03_system_db_contract/
└─ 04_book_package/
```

상세구조:

```text
00_manifest/
├─ REPO_IDENTITY.md
├─ PURPOSE.md
├─ SCOPE.md
├─ ROLE_BOUNDARY.md
├─ SOURCE_POLICY.md
├─ STATUS_POLICY.md
├─ NAMING_POLICY.md
└─ VERSION_POLICY.md
```

```text
01_system/
├─ 00_theory/
├─ 01_terminology/
├─ 02_reader_policy/
├─ 03_function_registry/
├─ 04_function_method/
├─ 05_pipeline/
├─ 06_schema/
├─ 07_guard/
├─ 08_verification/
├─ 09_installation/
├─ 10_audit/
└─ 11_history/
```

```text
02_db/
├─ 00_field_registry/
├─ 01_source_seed/
├─ 02_data_seed/
├─ 03_center_cell/
├─ 04_relation_seed/
├─ 05_evidence_seed/
├─ 06_comparison_seed/
├─ 07_result_seed/
├─ 08_question_seed/
├─ 09_lineage/
├─ 10_execution_history/
└─ 11_index/
```

```text
03_system_db_contract/
├─ 00_input_contract/
├─ 01_output_contract/
├─ 02_provenance/
├─ 03_version_binding/
├─ 04_mutation_policy/
├─ 05_integrity/
└─ 06_for_instance_interface/
```

```text
04_book_package/
├─ 00_package_index/
├─ 01_volumes/
├─ 02_load_receipts/
├─ 03_package_state/
├─ 04_installation_contract/
├─ 05_repo_mapping/
├─ 06_schema_mapping/
├─ 07_function_mapping/
├─ 08_guard_mapping/
├─ 09_audit/
└─ 10_release_bundle/
```

---

## 6. Manifest

`00_manifest`는 Repo의 자기정체성을 고정한다.

필수 선언:

```text
Relation은 for_instance가 아니다.
Relation은 SeungeFlow가 아니다.
Relation은 Linux DB가 아니다.
Relation은 거래신호 Repo가 아니다.
Relation은 System과 DB가 함께 있는 GitHub 기반 관계해석 Seed Base다.
```

---

## 7. System 영역

### Theory

역사·Local.Zero·역검산·공간·상태·다중인과·relation.bridge·질문순환.

### Terminology

용어의 현재정의와 Concept Lineage 참조.

### Reader Policy

무엇을 어떤 순서로 읽는가.

### Function Registry

사용 가능한 Function·Version·Capability.

### Function Method

입력·과정·Guard·출력·검증.

### Pipeline

Function 연결순서.

### Schema

Seed의 최소구조계약.

### Guard

오류·권한·Evidence 경계.

### Verification/Audit

System과 DB의 정합성 검사.

---

## 8. DB 영역

### Source Seed

원문의 위치·발행자·시간·역할.

### Data Seed

Source에서 현재 질문에 필요해 선택된 최소 Data.

### Center Cell

Local.Zero의 완전한 국소 Bundle.

### Relation Seed

Edge·Bridge·Path·Network·Pattern.

### Evidence Seed

사실·기록·해석·비유·반대근거.

### Comparison Seed

비교군.

### Result Seed

Local Answer.

### Question Seed

다음 Process를 여는 입력.

### Lineage

개념·Center·Result·Question·Function 변화계보.

### Index

AI가 필요한 Seed를 찾는 Reader 좌표.

---

## 9. System–DB 순환

\[
DB.Question
\rightarrow
System.Function
\rightarrow
DB.Source/Data
\]

\[
\rightarrow
System.Interpretation
\rightarrow
DB.Relation
\]

\[
\rightarrow
System.Verification
\rightarrow
DB.Result
\]

\[
\rightarrow
System.NextQuestion
\rightarrow
DB.Question
\]

Result는 다음 질문을 만들고 DB 상태는 진화한다.

\[
DB_n\xrightarrow{System_n}DB_{n+1}
\]

---

## 10. Provenance

모든 Result는 다음 경로로 역추적되어야 한다.

\[
Result
\rightarrow
Function.Version
\rightarrow
Relation.Seeds
\rightarrow
Data.Seeds
\rightarrow
Source.Seeds
\]

```yaml
analysis_provenance:
  analysis_id:
  system_version:
  function_ids:
  input_seed_ids:
  relation_ids:
  evidence_ids:
  comparison_ids:
  output_result_id:
  next_question_ids:
```

---

## 11. Status Policy

```text
candidate
sourced
aligned
verified
disputed
local_closed
superseded
rejected
unknown
```

기존 Seed를 덮어쓰지 않고 새로운 Version과 Lineage를 만든다.

---

## 12. GitHub의 역할

GitHub는 Relation System과 DB가 설치되는 Canonical 공간이다.

git은 선택 Adapter이며 GitHub의 존재이유를 대신하지 않는다.

AI는 승이를 통해 GitHub의 Repo 구조·문서·Seed·Index를 시스템재료로 사용한다.

\[
AI\leftrightarrow 승이\leftrightarrow GitHub.Relation
\]

---

## 13. 최소 Relation Repo

빈 Skeleton만으로는 Repo의 역할을 알 수 없다.

최소한 하나의 완전순환 Sample이 있어야 한다.

\[
Question
\rightarrow
Source
\rightarrow
Data
\rightarrow
Center
\rightarrow
Relation
\rightarrow
Evidence
\rightarrow
Comparison
\rightarrow
Result
\rightarrow
Next.Question
\]

이 Sample은 Volume 09에서 구체화한다.

---

## 14. Repo Mapping Index

```yaml
repo_mapping:
  concept: Local.Zero
  theory_path: 01_system/00_theory/local_zero.md
  schema_path: 01_system/06_schema/center_cell.schema.yaml
  method_path: 01_system/04_function_method/select_center.yaml
  db_path: 02_db/03_center_cell/
  guard_path: 01_system/07_guard/time_guard.md
```

논문의 모든 핵심개념은 최소한 하나의 System Path와 하나의 DB 또는 Contract Path에 대응되어야 한다.

---

## 15. Guard

- System과 DB를 다른 Repo로 분리하지 않는다.  
- System 설명과 DB Seed를 같은 파일에 무경계로 섞지 않는다.  
- Function과 인스턴스 이름을 동일시하지 않는다.  
- for_instance를 Relation 안으로 흡수하지 않는다.  
- SeungeFlow 원문을 현재해석으로 덮어쓰지 않는다.  
- GitHub를 단순 Remote로 축소하지 않는다.  
- 빈 Skeleton을 설치완료로 판정하지 않는다.  
- Result에서 Source까지 Provenance가 끊기지 않아야 한다.  

---

## 16. Volume 07의 결정화 결과

```yaml
volume_result:
  relation_repo:
    system_and_db_same_repo: true
    system_and_db_same_file: false
    for_instance_separate: true
    github_canonical: true
    minimum_complete_cycle_required: true

  next_seed:
    volume: VOL_08
    topic: function_schema_for_instance_interface
```

---

## 17. Load Marker

```text
ARSFIP-10V-20260714_VOL_07_LOADED
```
