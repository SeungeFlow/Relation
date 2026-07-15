# Relation DB

Relation DB는 실행 중인 별도 데이터베이스 서버가 아니다.

GitHub에 Source·Data·Center·Relation·Evidence·Comparison·Result·Question을
파일·ID·Index로 보존하는 Versioned Structured Memory다.

## Core Cycle

Question
→ Source
→ Data
→ Center
→ Relation
→ Evidence
→ Comparison
→ Result
→ Next Question

## Boundary

- System Method는 `01_system`에 존재한다.
- 기억 Seed와 분석결과는 `02_db`에 존재한다.
- 두 영역의 세부 입출력·Provenance·Version 계약은
  `03_system_db_contract`에서 이후 구현한다.
- 현재 Sample은 Relation Repo 자체의 초기구조를 검증하기 위한
  Foundation Sample이며 외부시장 사실분석이 아니다.
