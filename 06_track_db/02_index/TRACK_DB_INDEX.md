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
