# SEAT_OCCUPATION

Record runtime occupation of a stable for_instance Seat Definition.

이 Directory는 `SEAT_OCCUPATION` Runtime Record의 Namespace Index다.

- 모든 Record는 `record_id` 하나만을 Canonical Runtime Identity로 사용한다.
- Record Byte는 Append-Only다.
- Correction은 기존 Record 수정이 아니라 새 Record와 `supersedes_refs`로 표현한다.
- Storage Commit Hash는 Record 내부에서 미리 선언하지 않는다.
- JSON은 YAML 1.2의 유효한 부분집합이지만, 이 Registry의 생성 Record는 검산 가능한 YAML로 기록한다.
