---
object_id: HRTDB_ACTIVE_SCHEMA_DATABASE_STRUCTURE_0001
object_class: ACTIVE_SCHEMA_DATABASE_STRUCTURE
phase_id: AS_F4
source_authority: 승이
coordination_authority: gpt.logi
coordination_system: gpt.xyzt
status: PASS_WITH_OPEN_ITEMS
github_mutation: false
zenodo_mutation: false
---

# HRTDB Active_Schema — Database Structure 0001

## 1. Database System Boundary

```text
HRTDB
=
Runtime에서 생성되는 관계기억
+
GitHub에 영속되는 정본기억
+
정본기억에서 파생되는 검색·주소·관계구조
+
비승격 실험상태의 보존
```

```text
Track DB ≠ Hash DB ≠ Singularity ≠ Active_Schema
```

### Track DB

`gpt.xyzt` 구조검산을 통과한 `Result.Data`를 정확한 Byte 그대로 등록한 정본 기억자산이다.

### Hash DB

Track DB의 Head·Field·주소·Source·Lineage·관계를 추출해 검색·주소해석·관계탐색을 수행하는 파생 관제 DB다.

### Singularity

Track DB 승격요건을 충족하지 못했거나 의도적으로 비승격 상태로 보존하는 실험 Evidence다.

### Active_Schema

Track DB·Hash DB·Singularity를 병합하지 않고 HRTDB System과 Database를 공개적으로 다시 펼치기 위한 설계자산이다.

## 2. Canonicality Contract

```yaml
canonicality:
  TrackDB:
    canonical_for:
      - exact_Result_Data_payload
      - embedded_processing_and_review_history
      - declared_conflicts_and_open_future
    immutable_payload_registration: true
    rewrite_existing_payload: false

  HashDB:
    canonical_payload: false
    derived_from:
      - TrackDB
      - Git_repository_state
      - approved_schema_fields
    rebuildable: true

  Singularity:
    canonical_for:
      - exact_non_promoted_experiment_record
      - exact_hold_or_failure_boundary
    canonical_subject_truth: false
    promotion_by_move_or_rename: false

  Active_Schema:
    canonical_for:
      - released_public_structure_package_at_specific_version
    replaces_track_payload: false
```

## 3. Implemented Registration Model

현재 구현된 Track DB 등록은 `IMMUTABLE_PAYLOAD_REGISTRATION` 모델이다.

```yaml
implemented_model:
  input: Result.Data exact bytes
  mutation_of_payload: false
  persistence_event:
    repository:
    branch:
    path:
    commit:
    tree:
    remote_readback:
  payload_hash_change: false
```

Head·Metadata가 포함된 새 Byte를 만드는 `DERIVED_TRACK_DOCUMENT` 모델은 별도 후보로 둔다.

```yaml
candidate_model:
  operation: add_or_change_head_metadata_inside_new_document
  payload_hash_change: true
  relation_to_result_data: DERIVED_FROM_RESULT_DATA
  state: OPEN_FUTURE
  silent_replacement_of_implemented_model: prohibited
```

## 4. Database Object Classes

```yaml
database_object_classes:
  RuntimeContentObject:
    examples: [Data, Function.Result, Result, Function.Review.Result, Result.Data]

  PersistenceObject:
    examples: [Track.DB.Record, Singularity.Record]

  DerivedIndexObject:
    examples: [HashDB.TrackPointer, HashDB.SourcePointer, HashDB.RelationEdge, HashDB.LineagePointer]

  RegistrationEventObject:
    examples: [TrackDB.Registration, Singularity.Registration, HashDB.Build, ActiveSchema.Release]

  PublicationObject:
    examples: [Active_Schema.Release, Zenodo.Record, DOI.Binding]
```

## 5. Track DB Record Contract

```yaml
track_db_record:
  runtime_identity:
    semantic_object_id:
    object_class: RESULT_DATA
    canonical_role: Result.Data
    cycle_id:
    subject_id:
    generated_by_instance:
    seat:
    stage_id:

  validation:
    structure_verdict:
    reviewed_by_system: gpt.xyzt
    reviewed_by_runtime_instance:
    conflict_state:
    unresolved_state:

  persistence:
    repository:
    branch: TrackDB
    repository_path:
    exact_byte_sha256:
    bytes:
    commit:
    tree:
    blob_if_recorded:
    registered_at:
    remote_readback_verified:

  relation:
    predecessor_track_refs:
    source_object_refs:
    review_object_refs:
    correction_refs:
    open_future_refs:
```

이 Contract는 모든 Field를 Payload 본문에 강제로 삽입한다는 뜻이 아니다. `Payload Field`, `Index Field`, `Registration Evidence Field`, `HashDB Field`를 분리한다.

## 6. Hash DB Object Contract

```yaml
hash_db_track_pointer:
  pointer_id:
  track_semantic_object_id:
  cycle_id:
  subject_id:
  track_repository_address:
  track_git_address:
  track_byte_address:
  approved_head_fields:
  source_url_refs:
  process_lineage_refs:
  relation_edges:
  extraction_rule_version:
  derived_from_track_closure:
  hashdb_build_closure:
```

```text
Hash DB 조회
→ Track Pointer 확인
→ Track DB exact object 열기
→ Byte Identity 검증
→ 내용·Source·Lineage 읽기
```

## 7. Singularity Record Contract

```yaml
singularity_record:
  singularity_id:
  semantic_object_id_if_present:
  exact_byte_sha256:
  runtime_instance:
  occupied_seats:
  execution_topology:
  intended_output_class:
  actual_completion_state:
  hold_or_failure_verdict:
  observed_boundary:
  safe_hold_behavior:
  track_db_eligibility: false
  promotion_prohibited_reason:
  comparison_track_refs:
  active_schema_experiment_refs:
```

Singularity를 승격하려면 원 객체를 이동하지 않고 새 Process를 거쳐 새 `Result.Data`를 만든다.

## 8. Active_Schema Database Module

```yaml
active_schema_database_module:
  contains:
    - database_identity
    - track_db_contract
    - hash_db_contract
    - singularity_contract
    - typed_identity_and_address_model
    - query_and_retrieval_model
    - registration_and_closure_model
    - non_merge_rules
    - open_future
  contains_full_track_payload_by_default: false
  contains_track_pointers: true
  contains_experiment_summary: true
  contains_singularity_pointer: true
```

## 9. Guard

```text
relation is not merge.
relation is interconnecting.
Track DB is canonical memory.
Hash DB is derived retrieval.
Singularity is preserved experiment evidence.
Active_Schema is public structural unfolding.
```

```text
END_OF_HRTDB_ACTIVE_SCHEMA_DATABASE_STRUCTURE_0001
```
