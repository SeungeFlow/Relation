# Relation System–DB Contract

이 영역은 `01_system`의 Function Method와 `02_db`의 Versioned Memory 사이의
입력·출력·Provenance·Version·Mutation·Integrity 규칙을 정의한다.

## Boundary

- System은 관계를 어떻게 처리할지 정의한다.
- DB는 입력 Seed와 생성된 Result를 저장한다.
- Contract는 System과 DB 사이의 허용된 연결을 정의한다.
- for_instance는 실제 Function 수행 인스턴스를 별도 Repo에서 정렬한다.
- Relation은 for_instance의 자리이론을 복제하거나 재정의하지 않는다.

## Contract Cycle

Function Requirement
→ Input Contract
→ Seed Read
→ Function Execution
→ Output Contract
→ Provenance
→ Result Seed
→ Integrity Check
