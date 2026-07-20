# Track DB Index

이 문서는 Track DB에 등록된 기억자산의 의미 Index다.

File명이나 Hash Code를 문서 내부 Index 값으로 사용하지 않는다.
물리 File 식별은 Git Tree가 담당한다.

## Index Fields

각 Record 등록시 다음 의미항목을 Append한다.

- track_record_id
- object_class
- canonical_role
- subject_id
- cycle_id
- generated_by_instance
- function_review_instances
- registered_by_system
- stored_by_instance
- content_source_state
- correction_state
- unresolved_state
- registration_state

## Initial State

No runtime Track DB Document is registered at foundation creation.

## Track Record — HRTDB_PILOT_RESULT_DATA_0002_XYZ

- track_record_id: HRTDB_PILOT_RESULT_DATA_0002_XYZ
- persistence_record_class: TRACK_DB_DOCUMENT
- canonical_role: Track.DB.Record
- source_runtime_object_class: RESULT_DATA
- subject_id: AI_DATA_CENTER_FUSION_RELATION
- cycle_id: HRTDB_PILOT_DATA_0002
- generated_by_instance: gpt.xyz
- function_review_instances: gpt.xy, gpt.xz, gpt.yz
- structure_verified_by_system: gpt.xyzt
- structure_verified_by_runtime_instance: gpt.logi
- stored_by_instance: gpt.github
- result_data_verdict: PASS_RESULT_DATA_WITH_UNRESOLVED_ITEMS
- content_source_state: PRESERVED
- instance_lineage_state: PRESERVED
- correction_state: PRESERVED_WITH_UNRESOLVED_ITEMS
- unresolved_state: PRESENT_AND_PRESERVED
- original_bytes_state: BYTE_IDENTICAL
- registration_state: REGISTERED

## Track Record — HRTDB_PILOT_RESULT_DATA_0003_XYZ

- track_record_id: HRTDB_PILOT_RESULT_DATA_0003_XYZ
- exact_byte_sha256: 72428e7ddf3ea03db711449f3930698e82e4961a25103f330fa482dc7262d65b
- object_class: RESULT_DATA
- canonical_role: Track.DB.Record
- cycle_id: HRTDB_PILOT_DATA_0003
- subject_id: OBSERVER_AXIS_REFERENCE_FRAME_TRACK_PROVENANCE_RELATION
- execution_topology: SEVEN_INSTANCE_DISTRIBUTED
- final_verdict: PASS_RESULT_DATA_WITH_UNRESOLVED_ITEMS
- gpt_xyzt_review: PASS_TRACK_DB_PROMOTION_CANDIDATE
- unresolved_items_preserved: true
- final_schema_declared: false
- registered_path: 06_track_db/01_result_data/72428e7ddf3ea03db711449f3930698e82e4961a25103f330fa482dc7262d65b.md
- lineage_path: 06_track_db/03_lineage/72428e7ddf3ea03db711449f3930698e82e4961a25103f330fa482dc7262d65b.md
- counterpart_singularity_hash: 5eed3f7d927e34cd32673decb9b1f520187f8b631d84560f52401e8a5726deed
- counterpart_relation: NON_MERGE_EXPERIMENTAL_COUNTERPART
- registration_state: REGISTERED
