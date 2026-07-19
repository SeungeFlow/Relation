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
