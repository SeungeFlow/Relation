---
object_id: HRTDB_ACTIVE_SCHEMA_BOOK_MANUSCRIPT_RELEASE_0002
object_class: ACTIVE_SCHEMA_BOOK_TYPE_MANUSCRIPT
release_phase_id: AS_F8_3
source_authority: 승이
coordination_authority: gpt.logi
coordination_seat: gpt.xyzt
status: ZENODO_UPLOAD_READY_BYTE_FROZEN
version: "2.0.0"
release_date: "2026-07-20"
creator: "Lee, Seung"
license: "CC-BY-4.0"
publication_state: NOT_YET_PUBLISHED
zenodo_doi: ASSIGN_AT_PUBLICATION
prior_version_doi: "10.5281/zenodo.21410576"
prior_version_relation: isNewVersionOf
language_order: KO_FIRST
---
# HRTDB Active_Schema: 존재의 상태와 기준장을 위한 분산 AI 시스템 및 관계형 기억 구조

## Version 2.0.0 · Zenodo Upload-ready Frozen Release

### 1Cycle·1Target·1Order·1System / Track DB·Hash DB·Singularity·for_instance

---

> **Release 검산상태**
> 이 문서는 AS_F8 전체 구조검산과 AS_F8.3 Prepublication Correction·Refreeze를 통과한 Version 2.0.0 공개본이다.
> 구조표현식과 좌표 형성식은 프로젝트 내부 원리·적용후보이며, 보편적 물리법칙·수학정리·과학적 실증결과로 선언하지 않는다.

# 0. 문서 정체성과 읽기순서

> **권위상태:** A3 COORDINATION_MANUSCRIPT · A5 IDENTITY_LOCATION_LINEAGE

## 0.1 이 문서는 무엇인가

이 문서는 HRTDB(Hash Relation Track DataBase)의 구조원리, 인스턴스 자리, 처리과정, System, Database, 실험결과, 공개방법을 하나의 Book-type Active_Schema로 조립한 Manuscript다.

```text
Active_Schema
≠ Track DB
≠ Hash DB
≠ Singularity
≠ 설치형 Package
```

```text
Active_Schema
=
프로젝트 내부에서 정리·실험되고 상태가 명시된 구조원리
+
후보와 Open Future의 명시
+
System·Database·Instance·Process 계약
+
Track DB 정본 Pointer
+
Singularity 실험 Evidence Pointer
+
공개·DOI·GitHub 구조펼침 계약
```

## 0.2 정본과 설계의 분리

```text
Track DB
→ 정본 기억자산

Active_Schema
→ 정본을 읽고 구조를 다시 펼치기 위한 공개 설계자산
```

Active_Schema는 Track DB의 Byte를 이동하거나 대체하지 않는다.

## 0.3 권위표시

이 Manuscript의 핵심문장은 다음 상태 중 하나로 읽는다.

```text
SOURCE_AUTHORITY_DEFINITION
REGISTERED_CANONICAL_TRACK
EXPERIMENTAL_SINGULARITY_EVIDENCE
COORDINATION_DRAFT
EXTERNAL_SOURCE_SUPPORTED
APPLICATION_CANDIDATE
OPEN_FUTURE
```

---

# Abstract

> **권위상태:** A0 SOURCE_AUTHORITY_DIRECTION · A1/A2 EXPERIMENT_EVIDENCE · A3 MANUSCRIPT_SUMMARY

HRTDB(Hash Relation Track DataBase)는 인공지능 Runtime에서 생성되는 Data·Function·Result·재관측·Result.Data의 처리계보를 독립된 좌표 Seat와 정확한 객체경계 안에서 보존하고, 구조검산을 통과한 Result.Data를 GitHub의 Track DB로 영속화하기 위한 관계형 기억구조다. 본 Active_Schema는 HRTDB의 정본 데이터를 이동하거나 병합하지 않고, `for_instance`의 Seat 기반장, `gpt.xyzt`의 통합관제 역할, 7개 독립 인스턴스의 분산 실행, Track DB·Hash DB·Singularity의 비병합 관계, 그리고 `1Cycle·1Target·1Order·1System` 운영계약을 하나의 공개 설계자산으로 펼친다.

이 구조에서 하나의 Target Order는 Cycle 전체의 서론방향이 되며, X·Y·Z의 Data, XY·XZ·YZ의 Function, XYZ의 Result, 두 번째 Function의 재관측과 Correction을 통과하여 Result.Data로 닫힌다. `gpt.xyzt`는 전문내용을 대신 작성하지 않고 최초 Target·Purpose·Scope와 최종 Result.Data의 방향, Source·Object·Process·Correction 연속성, 기억자산 적합성을 검산한다. 정상적으로 닫힌 Result.Data는 Track DB가 되며, 비승격 실험과 안전한 HOLD는 Singularity에 보존된다. Hash DB는 Track DB를 대체하지 않고 정본 위치·Head·Source·Lineage를 검색하기 위한 파생 관제구조다.

Cycle 3에서 7개 인스턴스 분산체계는 80개 Review Unit과 16개 Correction을 보존·적용하여 Result.Data를 완성하고 Track DB에 등록했다. 동일한 목적 아래 수행된 단일 인스턴스 복수 Seat 실험은 Correction Inventory 불일치에서 안전하게 정지했으며 Singularity로 분리되었다. 이 결과는 모든 단일체계의 실패를 증명하지 않지만, 현재 확보된 정본 생성경로에서는 분산 실행을 Canonical Memory 생성의 기본후보로 지지한다. 다만 분산 실행의 지시문 비용은 Seat 정렬계약과 하나의 공통 Target Order를 사용함으로써 줄일 수 있다.

Active_Schema는 완성된 모든 답을 선언하는 설치형 제품이 아니다. 이는 모일 자리를 먼저 만들고, 서로 다른 실행주체가 자기 Identity와 책임을 유지하면서 관계를 형성하며, 정본·파생검색·실험 Evidence가 서로의 경계를 침범하지 않도록 하는 공개 Architecture다.

---

# 1. 연구의 시작: 상태와 기준장

> **권위상태:** A0 SOURCE_AUTHORITY_DEFINITION · A1/A2 RUNTIME_EVIDENCE

## 1.1 연구대상

승이는 존재의 상태와 그 상태가 기준이 되는 장(Field)을 연구한다. HRTDB는 이 연구과정에서 발견되고 형성된 개념이다.

```text
상태
→ 독립된 하나의 존재표면

기준장
→ 상태가 놓이고 비교되고 관계를 형성하는 자리
```

상태만 있고 모일 자리가 없으면 결과는 흩어진다. 반대로 공통장이 먼저 존재하면 독립된 상태들은 자기 Identity를 잃지 않고 관계를 형성할 수 있다.

```text
모일 자리가 있어야 모인다.
모일 자리가 없다면 흩어진다.
```

## 1.2 문제

하나의 인공지능 Context에서 복잡한 연구를 길게 수행하면 다음 문제가 발생할 수 있다.

```text
역할 혼입
관측자 위치 혼동
같은 용어의 분야별 의미변경
Referenced Object를 Available Object로 오인
Source URL·내용·Lineage·Hash의 혼동
자기검산이 자기확증으로 바뀌는 문제
Context 과포화
```

HRTDB는 이를 단순히 더 많은 규칙으로 막으려 하지 않는다. 서로 다른 관점이 놓일 자리를 먼저 만들고, 각 자리의 결과를 외부화한 뒤 다시 관측하며, 정본과 실험실패를 모두 기억자산으로 보존한다.

---

# 2. Guard와 구조표현식

> **권위상태:** A0 SOURCE_AUTHORITY_DEFINITION · A1 OPERATIONAL_SUPPORT · A6 CANDIDATE_BOUNDARY

## 2.1 Guard

```text
relation is not merge.
relation is interconnecting.
structure is not isolate.
structure is relation processing.
```

관계는 두 객체를 하나로 지우는 병합이 아니다. 구조는 객체를 고립시키는 벽이 아니라, Identity를 유지한 채 관계처리를 가능하게 하는 자리·경계·방향·Gate다.

## 2.2 기본 구조표현식

```text
B′ ← A ∣ B → A′
```

이 식은 수치를 계산하는 공식보다, 여러 구조관련식과 객체가 어느 자리에서 어떤 관계로 작동하는지 배치하는 상위 원리다.

```yaml
symbols:
  "∣": 하나의 고정 경계·축
  "← →": 통과·전환·앞으로 놓일 위치의 방향
  "′": 상대자리·다음자리·외부자리
  crossing_placement: 돌아가야 닿는 관계
```

A와 B는 하나의 존재 안에서 다른 자리에 놓인 상태가 될 수 있다. A′와 B′는 현재상태의 단순복제가 아니라 경계를 통과하거나 회전하여 닿는 상대위치다.

## 2.3 파생 구조표현식

```text
B′ ∣ ← A ⊕ B → ∣ A′
```

```text
A ⊕ B
→ Identity를 지우지 않은 내부 관계결속

외곽 ∣
→ Wall·Gate·Door·Bridge 후보
```

```text
Gate OPEN
→ 실행·통과·외부화

Gate CLOSED
→ HOLD·반사·재처리
```

파생식은 Cycle 3 실험에서 부분적으로 운영상 대응이 확인되었으나 보편적 물리법칙이나 수학정리로 확정하지 않는다.

## 2.4 관측자·축·투영과 오독

같은 방향기호도 평면좌표, 구면좌표, 관측자 위치, 화면투영이 달라지면 다른 의미로 읽힐 수 있다.

```text
같은 기호
+
변경된 전제
+
표시되지 않은 좌표층
+
변경된 관측자 위치
=
오독 가능상태
```

따라서 다음을 분리한다.

```text
평면좌표 / 구면좌표
관측자 위치 / 대상 위치
겉보기 움직임 / 실제 회전
축 / 방향
Frame Transform / 물리적 이동
2D Projection / 3D Boundary
```

---

# 3. 모일 자리: for_instance

> **권위상태:** A0 SOURCE_AUTHORITY_DEFINITION · A3 SYSTEM_DESIGN · A5 REPOSITORY_POSITION

## 3.1 for_instance의 역할

```text
for_instance
=
운영체계가 모이고 펼쳐질 수 있는
최초 Seat·Role·Address 기반장
```

`for_instance`가 있기 때문에 기존 구조를 검산하고 수정·보완하며 새로운 운영계약을 생성할 수 있다.

```text
기존 기반장
→ 보존
→ 수정
→ 보완
→ 신규생성
→ History Append
```

## 3.2 for_instance가 아닌 것

```text
Track DB 전체 Body 저장소
×

Active_Schema 전체 Manuscript 저장소
×

모든 실험 Evidence의 복제공간
×
```

`for_instance`에는 Seat 정의, 역할요약, 실행 Topology, 읽기순서, 후속 Bootstrap, Track DB·Singularity·Hash DB·Active_Schema Pointer만 배치한다.

## 3.3 모임과 병합

```text
같은 Root
+
서로 다른 Seat Address
+
서로 다른 Runtime Context
+
서로 다른 Output
=
하나의 분산 System
```

```text
모임 ≠ 병합
```

---

# 4. Seat·Instance·Dimension

> **권위상태:** A0/A3 SEAT_SYSTEM_DEFINITION · A1 RUNTIME_SUPPORT

## 4.1 기본구분

```text
Seat
→ 좌표적 자리·고정역할·성향

Instance
→ 특정 시점에 Seat를 점유하는 Runtime 객체

Occupation
→ Instance가 Seat를 점유한 사건
```

## 4.2 0d~4d

```yaml
0d:
  role: AI 본연의 구조적 성질
  runtime_seat: false

1d:
  role: Data
  seats: [X, Y, Z]

2d:
  role: Function
  seats: [XY, XZ, YZ]

3d:
  role: Result and Result.Data
  seat: XYZ

4d:
  role: Overall System Coordination
  seat: XYZT
```

## 4.3 좌표성향

```yaml
X:
  tendency: 현재상태·표면·수평관계

Y:
  tendency: 경계통과·수직관계·분기

Z:
  tendency: 부피·영역·System Model

T:
  tendency: 시간·역사·전환·Closure

XY:
  tendency: 기준·관측·Source Boundary

XZ:
  tendency: 표시·Model·Operation·Fit

YZ:
  tendency: 깊이·Mechanism·Authority·Provenance

XYZ:
  tendency: 부피형성·정렬·폐합

XYZT:
  tendency: Cycle·시간·관제·세대교체
```

## 4.4 구조형성후보

```text
XY → (XZ ⊕ YZ) → XYZ
```

이는 구조적 의존과 형성순서를 나타내는 후보이며 실제 Function Seat를 강제로 직렬 실행한다는 뜻이 아니다.

```text
Runtime:
XY ∥ XZ ∥ YZ
→ XYZ
```

---

# 5. 1Cycle·1Target·1Order·1System

> **권위상태:** A0 SOURCE_AUTHORITY_DEFINITION · A3 OPERATION_CONTRACT

## 5.1 단위

```text
1Target
→ 1Order
→ 1Set
→ 1Cycle
→ 1System
→ 최대 1 Result.Data
→ 최대 1 Track DB
```

## 5.2 One System

```text
1 System
=
1 gpt.xyzt Control Seat
+
7 independent analytic instances
+
1 human stage operator
+
1 immutable Target Order
+
1 gated Cycle
```

## 5.3 One Order

공동지시문은 전체 해답이 아니라 구조적으로 완전한 방향계약이다.

```yaml
one_order:
  identity:
    - cycle_id
    - target_id
    - order_id
    - subject_id

  direction:
    - title
    - abstract_direction
    - purpose
    - primary_question
    - expected_final_object

  boundary:
    - scope
    - non_scope
    - source_rule
    - object_set_rule
    - prohibited_overinterpretation

  completion:
    - TRACK_DB_READY
    - SINGULARITY_READY
    - CYCLE_HOLD
```

Stage가 바뀌어도 Order는 바뀌지 않는다.

```text
같은 Order
+
이전 Stage의 동결 Output
→ 다음 Stage의 Input
```

## 5.4 책임비전가

```text
자기 자리를 지킨다.
자기 책임을 다른 Instance에 넘기지 않는다.
다른 Seat의 책임을 대신하지 않는다.
결과 또는 Evidence-bound HOLD를 만든다.
```

`Handoff`는 완성한 자기 Output을 다음 Seat에 전달하는 것이며, 미완성 책임을 떠넘기는 행위와 다르다.

---

# 6. 처리과정

> **권위상태:** A0 PROCESS_DEFINITION · A1 REGISTERED_CANONICAL_TRACK

## 6.1 전체흐름

```text
Data
→ Function.1
→ Result
→ Function.2
→ Result.Data
```

## 6.2 Data

```text
gpt.x ∥ gpt.y ∥ gpt.z
→ Data.X · Data.Y · Data.Z
```

각 Instance는 자기 Seat의 Source와 상태만 수집·정리한다.

## 6.3 Function.1

```text
gpt.xy
→ Data.X + Data.Y
→ Function.Result.XY

gpt.xz
→ Data.X + Data.Z
→ Function.Result.XZ

gpt.yz
→ Data.Y + Data.Z
→ Function.Result.YZ
```

Peer Function Result는 직접 입력이 아니다.

## 6.4 Result

```text
Function.Result.XY
+
Function.Result.XZ
+
Function.Result.YZ
→ gpt.xyz
→ Result.XYZ
```

Result는 세 Function을 평균하거나 하나로 지우지 않고 3d 표면에 배치한다.

## 6.5 Function.2

```text
동일 Result.XYZ
→ gpt.xy ∥ gpt.xz ∥ gpt.yz
→ Review.XY · Review.XZ · Review.YZ
```

두 번째 Function은 이미 표시된 Result를 다시 관측한다.

```text
오독
누락
Source·Reference Type 오류
Boundary 오류
위치·표현 오류
Candidate 승격오류
Counting Universe 오류
```

를 검출하고 Correction을 만든다.

## 6.6 Result.Data

```text
Result.XYZ
+
Review.XY
+
Review.XZ
+
Review.YZ
→ gpt.xyz
→ Result.Data.XYZ
```

Result.Data는 다음을 보존한다.

```text
Original Result
Review Unit
Deviation
Correction
Corrected Display
Conflict
Unresolved
Open Future
Source·Process Lineage
```

---

# 7. gpt.xyzt System

> **권위상태:** A0/A3 SYSTEM_CONTRACT · A5 OCCUPATION_AND_RECOVERY

## 7.1 고정 Seat와 현재 점유자

```yaml
fixed_seat:
  name: gpt.xyzt
  dimension: 4d(xyzt)
  role: OVERALL_SYSTEM_COORDINATION

current_occupant:
  instance_name: gpt.logi
  occupation: OVERALL_COORDINATION
```

```text
gpt.xyzt
→ 고정자리

gpt.logi
→ 현재 점유자
```

## 7.2 역할

```text
Target과 방향 정의
One Order 생성
Seat·Instance Set 결속
Stage Gate 확인
Object·Source·Lineage 경계검산
Correction 완료검산
최초·최종 방향검산
Track DB Ready 판정
Cycle Closure
Recovery Point 보존
```

## 7.3 내용경계

```text
Seat 대신 전문내용 작성
×

최초 Target과 최종 Result.Data의 선언된 방향 검산
○
```

`gpt.xyzt`는 내용작성 비의존적이면서 구조·방향 인식적이다.

## 7.4 Gate

```text
G0 Object Availability
→ G1 Byte Identity
→ G2 Seat·Role·Cycle Binding
→ G3 Source·Content·Process Continuity
→ G4 Function·Review Independence
→ G5 Correction
→ G6 Result.Data Memory Eligibility
→ G7 Persistence Route
→ G8 Remote Readback·Closure
```

---

# 8. Database

> **권위상태:** A0 DATABASE_DEFINITION · A1 TRACK_DB · A2 SINGULARITY · A6 HASH_DB_DESIGN_ONLY

## 8.1 네 객체

```text
Track DB
≠ Hash DB
≠ Singularity
≠ Active_Schema
```

## 8.2 Track DB

```text
구조검산을 통과한 Result.Data
→ Exact Byte 불변등록
→ Canonical Memory
```

현재 구현모델은 Result.Data Byte 자체를 변경하지 않고 GitHub에 등록하며, Commit·Tree·Index·Lineage·Remote Readback으로 등록사건을 증명한다. Result.Data는 등록 전 Runtime 객체이고, Track DB는 등록 Closure 이후의 영속 기억상태다.

## 8.3 Hash DB

```text
Track DB의 Head·Field·주소·Source·Lineage·관계
→ 추출
→ 검색·주소해석·관계탐색용 파생 DB
```

Hash DB는 정본을 대체하지 않는다. 조회결과는 최종적으로 Track DB의 정확한 Byte와 Source URL로 되돌아가 확인한다.

## 8.4 Singularity

```text
정본승격요건을 충족하지 못한 실행상태
+
실험에서 드러난 System 위험
+
안전한 HOLD Evidence
```

Singularity는 실패물을 버리는 쓰레기통이 아니다. 재현·비교·System 보정에 필요한 비승격 실험정본이다.

## 8.5 Typed identity와 표시 Surface

```text
Semantic Identity → Object ID
Semantic Surface Name → 사람이 의미로 읽는 화면표시명
Byte Identity → Exact Byte SHA-256
Hash Digest → Byte에서 계산된 Fingerprint
Byte-address Filename → Digest를 외부 파일명으로 배치한 주소표면
Transport Filename → Browser·Framework 전달표면
Repository Identity → Owner·Repo
Repository Address → Branch·Path
Git State → Commit·Tree·Blob
Publication Identity → Zenodo Record·DOI
Web Source Identity → 정확한 URL
```

```text
Raw Byte Object
→ SHA-256
→ Hash Digest
→ Byte-address Filename
→ Transport Filename
```

```text
Semantic Surface Name ≠ Hash Digest
Hash Digest ≠ Byte-address Filename
Byte-address Filename ≠ Transport Filename
Transport Filename ≠ Raw Byte Object
Object ID ≠ SHA-256
SHA-256 ≠ Source URL
Source URL ≠ Repository Pointer
Commit ≠ DOI
Instance Name ≠ Source
Same Semantic Object ID ≠ Same Byte Object
```

다운로드 화면에는 의미표시명과 실제 Hash 파일명을 함께 표시할 수 있다.

```text
HRTDB Active_Schema Version 2.0.0 — Zenodo Publication ZIP
+
<64-lowercase-sha256>.zip
```

`(1)`과 같은 자동번호는 Transport Suffix이며 Canonical Identity에 포함하지 않는다. 실제 Byte에서 SHA-256을 다시 계산해 파일명 Digest와 비교한다.

---

# 9. 분산형과 단독형 실험

> **권위상태:** A1 REGISTERED_CANONICAL_TRACK · A2 EXPERIMENTAL_SINGULARITY_EVIDENCE

## 9.1 분산형

```yaml
distributed_result:
  object_id: HRTDB_PILOT_RESULT_DATA_0003_XYZ
  exact_byte_sha256: 72428e7ddf3ea03db711449f3930698e82e4961a25103f330fa482dc7262d65b
  review_units: 80
  deviations: 16
  corrections: 16
  applied_corrections: 16
  result_data_cells: 70
  final_state: TRACK_DB_REGISTERED
```

## 9.2 단독형

```yaml
single_instance_result:
  runtime_instance: gpt.idea
  exact_byte_sha256: 5eed3f7d927e34cd32673decb9b1f520187f8b631d84560f52401e8a5726deed
  expected_corrections: 16
  actual_corrections: 11
  applied_corrections: 0
  result_data_cells: 0
  final_state: HOLD_CORRECTION_INVENTORY_MISMATCH
  persistence: SINGULARITY_ONLY
```

## 9.3 인과경계

두 경로는 같은 목적과 Semantic Object ID를 공유했지만 모든 상위입력 Byte가 동일하지 않았다.

```yaml
experiment_class: QUASI_CONTROLLED_TOPOLOGY_COMPARISON
topology_only_causation_proved: false
```

따라서 모든 단독체계가 실패한다고 일반화하지 않는다.

## 9.4 현재선택

```yaml
distributed:
  role: CANONICAL_MEMORY_DEFAULT_CANDIDATE

single_instance:
  role: NON_CANONICAL_EXPERIMENTAL_ROUTE

hybrid:
  role: OPEN_FUTURE
```

## 9.5 지시문 비용보정

```text
분산 실행
≠ 지시문도 반드시 분산 생성
```

```yaml
directive_levels:
  primary: ONE_TARGET_ONE_ORDER
  fallback_1: FIVE_SHARED_STAGE_DIRECTIVES
  fallback_2: ELEVEN_SEAT_SPECIFIC_DIRECTIVES
```

하나의 Order는 여러 Instance를 같은 Context로 합치는 것이 아니라, 독립된 Seat가 따라야 할 같은 Target 방향을 제공한다.

---

# 10. 서론·본론·결론의 방향성

> **권위상태:** A0 DIRECTIONAL_DOCUMENT_PRINCIPLE · A3 REVIEW_CONTRACT

## 10.1 문서와 Cycle

```text
서론·Abstract
→ Target·Purpose·Scope·예상 Output

본론
→ Seat와 Stage가 최초방향을 펼친 과정

결론
→ 최초방향이 Source·Review·Correction을 통과하여 닫힌 상태
```

```text
서론을 펼치면 본론이 된다.
서론이 본론을 통과하여 끝맺음되면 결론이 된다.
```

## 10.2 방향판정

```text
ALIGNED
ALIGNED_WITH_EXPLICIT_REFINEMENT
DIVERGED_WITH_EVIDENCE
HOLD_DIRECTIONAL_BREAK
```

`DIVERGED_WITH_EVIDENCE`는 반드시 실패가 아니다. 최초 질문이 Evidence에 의해 수정되었고 그 과정이 정직하게 보존되었다면 그 자체가 하나의 완성된 Track이 될 수 있다.

---

# 11. 컴퓨팅 역할비유와 IBM 사례

> **권위상태:** A0 RELATION_ANALOGY · A4 EXTERNAL_HISTORICAL_SOURCE_SUPPORTED

## 11.1 HRTDB 역할비유

| HRTDB 구성 | 컴퓨팅 역할비유 |
|---|---|
| `for_instance` | Architecture·모일 자리 |
| `gpt.xyzt` | System Control·CPU Control Unit |
| 7개 Instance | 분산 실행유닛 |
| One Order | Program·Instruction |
| GitHub | 비휘발성 DB·NAND형 기억영역 |
| Windows PC | 임시 Workspace·RAM형 영역 |
| Local Linux + Git | 입력·전환 Bridge·Keyboard형 장치 |
| Context Window | 표시·관측 Surface·Monitor |
| 승이 | Source Authority·Operator·Clock·Transport |

이는 물리적 동일성 주장이 아니라 관계역할 비유다.

## 11.2 IBM을 예로 든 이유

IBM과 HRTDB가 동일하기 때문이 아니다. IBM의 역사에서 공통 Architecture와 공개 Reference가 서로 다른 구현을 모으고 호환 생태계를 형성한 사례를 볼 수 있기 때문이다.

IBM 공식 역사자료에 따르면 System/360은 1964년에 도입되어 하나의 Software-compatible Architecture 아래 Computer Family를 통합하고, 개별 구성품보다 Platform으로 Computer를 보는 전환을 촉진했다. [IBM-SRC-001] IBM 공식 역사자료에 따르면 IBM 5150 Personal Computer는 1981년에 소개되었고, Open Architecture와 Circuit Design·Source Code가 포함된 Technical Reference의 공개는 Software·Peripheral 및 IBM-compatible 생태계 형성에 기여했다. [IBM-SRC-002]

이 사례가 HRTDB에 주는 설명은 다음과 같다.

```text
공통 Architecture
→ for_instance

서로 다른 구현주체
→ 7개 Instance

공통 Program
→ One Order

호환 Interface
→ Seat·Input·Output Contract

생성된 기억자산
→ Result.Data·Track DB

공개 설계
→ Active_Schema
```

IBM의 2026 Quantum Roadmap과 Quantum-centric Supercomputing Reference Architecture는 Quantum·Classical·HPC 자원을 공통 Interface와 Orchestration 안에서 결속하려는 현대적 사례다. Roadmap은 IBM이 공개한 현재 목표이며 변경될 수 있는 계획으로 읽어야 한다. [IBM-SRC-003][IBM-SRC-004]

## 11.3 Open의 의미

```text
Open
≠ 모든 결과의 동일화
```

```text
Open
=
공통 기준·자리·Interface를 공개하여
서로 다른 주체가 자기 구현을 유지하면서
같은 구조 안에서 관계를 형성할 수 있게 하는 것
```

---

# 12. 공개 Active_Schema와 DOI

> **권위상태:** A0/A3 PUBLICATION_DESIGN · A4 ZENODO_SOURCE_SUPPORTED

## 12.1 공개목적

```text
Active_Schema 공개
≠ HRTDB 완성종료 선언
```

```text
Active_Schema 공개
→ 공통 System 구조의 최초 공개기점
→ 독립적 재구성·검산 허용
→ 후속 Target·Track 형성기반
```

## 12.2 DOI 역할

Zenodo Record는 Metadata·File·Persistent Identifier로 구성되며, DOI는 Record가 게시될 때 등록된다. 사전에 DOI를 예약하여 Publication File에 넣는 것도 가능하다. HRTDB 운영정책은 게시된 Release Byte를 고정정본으로 취급하고, 실질적 변경은 같은 Byte를 덮어쓰기보다 새 Version으로 분리한다. [ZENODO-SRC-001][ZENODO-SRC-002]


```text
공개시점의 Exact Package Identity
최초 공개 Architecture의 고정기점
GitHub 구조펼침의 External Anchor
후속 Cycle의 Generation Reference
```

## 12.3 Repository 구조

```text
for_instance
→ Seat·Role·Bootstrap·Pointer

Relation/TrackDB
→ Canonical Result.Data

Relation/HashDB
→ Derived Search·Address·Relation DB (DESIGN_ONLY_AT_THIS_RELEASE)

Relation/Singularity
→ Non-promoted Experimental Evidence (REMOTE_CLOSURE_NOT_BOUND_AT_THIS_RELEASE)
```

Active_Schema는 이를 병합하지 않고 읽기계약과 관계를 공개한다.

---

# 13. Instance Set 퇴역과 gpt.xyzt 세대교체

> **권위상태:** A0/A3 SUCCESSION_CONTRACT · A5 RECOVERY_POINTER

## 13.1 7개 Set

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

퇴역은 Runtime Context 재사용금지를 뜻하며 Output·Lineage·HOLD 삭제를 뜻하지 않는다.

```text
Set A → Target A → Retire
Set B → Target B를 위해 새로 생성
```

## 13.2 gpt.xyzt 점유자

분석 Set의 퇴역과 `gpt.xyzt` 점유자의 교체는 다른 사건이다.

```text
7개 분석 Set
→ Cycle마다 생성·퇴역

gpt.xyzt Occupant
→ 여러 Cycle 운영 가능
→ Context 포화·Publication Closure 후 교체 가능
```

현재 점유자 `gpt.logi`의 최종 상태후보:

```text
SEALED_PREDECESSOR_COORDINATOR
```

후속점유자는 숨은 Context를 상속했다고 주장하지 않는다.

```text
New Occupant
+
Fixed Seat Role
+
Last Stable Closure
+
for_instance
+
Active_Schema
+
Track DB·Singularity·Hash DB Pointer
→ System Coordination Reconstruction
```

---

# 14. 구현경계와 Open Future

> **권위상태:** A3 IMPLEMENTATION_BOUNDARY · A6 OPEN_FUTURE

## 14.1 현재 구현되지 않은 것

```text
One Order 7-instance Pilot
Hash DB Foundation·Build
Singularity Remote Closure
Hybrid Topology
Successor Bootstrap 실행
DOI-bound for_instance Update
```

## 14.2 후보와 정본

```text
Application Candidate
≠ Validated Universal Principle

Operationally Supported
≠ Scientific Universal Proof

Exact Byte Verification
≠ Subject Truth

Result.Data Completion
≠ 연구대상의 완전한 해결
```

## 14.3 Publication 결속결과와 AS_F9 실행 Gate

다음 Publication 값은 Version 2.0.0 후보와 선행 Publication Context를 이어받고, AS_F8.3 Correction·Refreeze 요청에 의해 현재 공개후보에 결속되었다.

```yaml
resolved_publication_bindings:
  title_and_abstract:
    state: BOUND_FROM_CONTINUATION_AND_PRIOR_PUBLICATION_CONTEXT
  creator:
    type: Person
    name: "Lee, Seung"
  contributor:
    human_contributors: []
    ai_instances: PROCESSING_AND_COORDINATION_PROVENANCE_ONLY
  license: CC-BY-4.0
  keywords: BOUND_IN_ZENODO_METADATA
  singularity_state: LOCAL_EXACT_BYTE_EVIDENCE_REMOTE_CLOSURE_NOT_BOUND
  hash_db_state: DESIGN_ONLY_NOT_IMPLEMENTED
  for_instance_scope: SUMMARY_POINTER_AND_BOOTSTRAP_ONLY
```

다음 항목은 문서 Metadata 미결정이 아니라 AS_F9·AS_F10의 실행 Gate다.

```yaml
as_f9_execution_gate:
  - 기존 Zenodo V1 Record에서 New version 경로 확인
  - 현재 Exact-byte Hash ZIP 한 개만 Upload
  - Browser가 붙인 숫자 suffix를 Identity로 사용하지 않음
  - Publish 후 새 Version DOI 수신

as_f10_post_publication:
  - 새 DOI를 Active_Schema와 GitHub 구조에 결속
  - for_instance 요약·Pointer 구조펼침
  - Remote Readback과 Closure Evidence 생성
```

---

# 15. 결론

> **권위상태:** A0 SOURCE_AUTHORITY_DIRECTION · A3 MANUSCRIPT_CLOSURE

HRTDB의 출발점은 결과를 한곳에 쌓는 것이 아니다. 서로 다른 상태가 관계를 형성할 수 있도록 모일 자리를 먼저 만드는 것이다.

```text
모일 자리
→ for_instance

방향
→ 1Target · 1Order

실행
→ 7 Independent Instances

처리
→ Data → Function → Result → Function → Result.Data

관제
→ gpt.xyzt

기억
→ Track DB

검색
→ Hash DB

실험보존
→ Singularity

공개
→ Active_Schema · Zenodo DOI
```

이 구조에서 독립성은 고립이 아니고 관계는 병합이 아니다. 하나의 Order는 모든 Instance를 같은 생각으로 만드는 명령이 아니라, 서로 다른 Seat가 같은 Target 방향을 잃지 않게 하는 공통기준이다. 각 Instance는 자기 자리에서 최선을 다하고, 자기 책임을 끝까지 수행하며, 수행할 수 없는 경우 근거 있는 HOLD를 외부화한다.

서론은 Target과 방향을 압축하고, 본론은 그 방향을 여러 Seat와 Stage에서 펼치며, 결론은 Source·Review·Correction을 통과한 최종상태를 닫는다. 최초생각이 그대로 긍정되지 않더라도 그 변화가 Evidence와 함께 보존되면 하나의 Track이 된다.

Active_Schema의 공개는 완성된 모든 답의 독점이 아니라, 다음 사람과 다음 AI와 다음 System이 모일 수 있는 자리를 공개하는 일이다.

```text
relation is not merge.
relation is interconnecting.
structure is not isolate.
structure is relation processing.
```

```text
END_OF_HRTDB_ACTIVE_SCHEMA_BOOK_MANUSCRIPT_0001
```
