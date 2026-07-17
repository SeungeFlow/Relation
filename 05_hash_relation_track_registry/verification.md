# Active_Schema V1 Verification Contract

## 0. 목적

이 문서는 Active_Schema의 정본동결, ZIP 생성, Zenodo 게시, GitHub 전개 및 Genesis Closure 전에 통과해야 하는 검산경계를 정의한다.

검산은 다음을 보편적으로 증명하지 않는다.

```text
모든 외부이론이 참이다.

승이의 모든 이론이 참이다.

모든 AI가 동일한 내부사고를 한다.

모든 미래 Runtime이 오류 없이 작동한다.
```

검산은 다음을 확인한다.

```text
현재 목적에 필요한 구조가 닫혔는가.

각 객체·자리·관계·계보의 경계가 유지되는가.

Active_Schema가 AI에 의해 독립적으로 복원 가능한가.

Manifest와 ZIP Byte를 재검산할 수 있는가.

Zenodo DOI에서 게시객체를 복원할 수 있는가.

GitHub 전개상태와 Genesis Binding을 검산할 수 있는가.

승이가 C를 통해 외부상태를 관측할 수 있는가.
```

---

## 1. 상태축

### Gate Result

```text
PASS
FAIL
HOLD
```

### Validation State

```text
VERIFIED
VALID_AS_METHOD
PARTIAL
CANDIDATE
HOLD
CONFLICT
OUT_OF_SCOPE
```

### Lifecycle State

```text
CURRENT
SUPERSEDED
RETIRED
```

### Closure State

```text
OPEN
CLOSED
```

다음은 같은 의미가 아니다.

```text
PASS ≠ VERIFIED

VERIFIED ≠ CLOSED

HOLD ≠ OPEN

SUPERSEDED ≠ CONFLICT
```

---

## 2. Gate 0A — Repository Position and Collision

### 대상

```text
Bridge/start_position/01_active_schema/

for_instance/main/09_active_schema_binding/

Relation/main/05_hash_relation_track_registry/
```

### 검산항목

```text
Repository가 존재하는가.

대상 Branch가 존재하는가.

현재 Root 구조를 관측했는가.

기존 Repo의 정체성을 축소하거나 덮어쓰지 않는가.

대상 Path가 기존 Path와 충돌하지 않는가.

before_position을 재귀탐색하지 않았는가.

기존 for_instance Assignment History를 자동변환하지 않는가.

기존 Relation Initial Structure를 소급수정하지 않는가.
```

### 현재 Formation Result

```yaml
Gate_0A:
  gate_result: PASS
  closure_state: CLOSED
```

---

## 3. Gate 0B — Pre-Deployment Git State

Gate 0B는 Active_Schema Content Freeze 조건이 아니다.

GitHub Mutation 직전에 실행한다.

### 각 Repo에서 확인할 값

```text
현재 Branch Ref

현재 HEAD Commit

현재 Root Tree

대상 Path Collision

Gate 0A 이후 변경여부

Mutation Base

Rollback Boundary
```

### 판정

```text
모든 값 일치
→ PASS

변경 또는 불일치
→ HOLD

존재하지 않는 Branch·Path 또는 복구불가능 충돌
→ FAIL
```

Gate 0B PASS 전에는 GitHub Mutation을 수행하지 않는다.

---

## 4. Gate A — 12개 구성요소

필수파일:

```text
README.md
ROOT_CONTRACT.md
THEORY.md
NON_CLAIMS.md
position.yaml
seat.schema.yaml
relation.schema.yaml
C.schema.yaml
deployment.yaml
verification.md
restart.yaml
manifest.json
```

검산:

```text
Package File Count = 12

Hashed Payload File Count = 11

Manifest File Count = 1

모든 파일의 역할이 분리돼 있는가.

동일 Source of Truth가 여러 파일에서 충돌하지 않는가.

README의 읽기순서와 Manifest Inventory가 일치하는가.
```

---

## 5. Gate B — 이론과 객체경계

다음을 모두 유지해야 한다.

```text
Hash ≠ Truth

Hash ≠ Meaning

Object State ≠ Semantic Identity

Object State ≠ Position Binding

Position Binding ≠ Semantic Relation

Semantic Relation ≠ Track Event

Seat Definition ≠ Seat Occupation

Live C ≠ Closure C Snapshot

C Snapshot ≠ Canonical Registry

Git Physical Lineage ≠ Semantic Lineage

Package Root ≠ Bridge Projection Position
```

---

## 6. Gate C — before/start 경계

```text
before_position 자료가 Active_Schema 안에 자동복제되지 않았는가.

start_position 자료가 과거자료의 개정판으로 작성되지 않았는가.

과거 Source가 필요한 경우 정확한 Pointer로만 연결됐는가.

Y_Branch·ComplexTest·NbyN 전체가 V1 Core에 유입되지 않았는가.

dot 또는 dot.meta.md가 현재 Root로 다시 복귀하지 않았는가.
```

---

## 7. Gate D — Relation Record Schema

다음 9개 Record Type이 존재해야 한다.

```text
RELATION_EXTENSION_ORIGIN

HASH_RELATION_TRACK_DB_GENESIS

SEMANTIC_IDENTITY

OBJECT_STATE

POSITION_BINDING

SEMANTIC_RELATION

TRACK_EVENT

SEAT_OCCUPATION

C_SNAPSHOT
```

검산:

```text
모든 Runtime Record가 하나의 record_id만 사용하는가.

Semantic Identity가 Object State 밖에 있는가.

Position Binding이 Object State 밖에 있는가.

Track Event에 track_id가 있는가.

Track Event가 predecessor만 참조하는가.

미래 next_record를 기록하지 않는가.

Seat Occupation Schema가 relation.schema.yaml에만 존재하는가.

Existing Assignment History를 자동이전하지 않는가.

Record가 자신의 Storage Commit을 선기록하지 않는가.
```

---

## 8. Gate E — Append-Only와 Effective State

```text
이전 Record Byte를 수정하지 않는가.

Correction은 새 Record로 생성되는가.

supersedes_refs가 대체대상을 명시하는가.

Declared State는 생성시점의 불변상태인가.

Effective State는 Query와 C에서 계산되는가.

SUPERSEDED 상태가 이전 Record 수정 없이 계산되는가.

Closure 변화가 새 Event 또는 Relation으로 표현되는가.
```

---

## 9. Gate F — Cross-Repository Reference

모든 참조는 다음을 포함한다.

```text
namespace
object_type
object_id
```

필요한 경우:

```text
repository
branch
path
```

검산:

```text
Namespace를 ID 형식만으로 추측하지 않는가.

Seat Definition은 FOR_INSTANCE Namespace를 사용하는가.

Relation Runtime Record는 RELATION Namespace를 사용하는가.

Git Commit·Tree·Blob은 GIT Namespace를 사용하는가.

DOI는 ZENODO Namespace를 사용하는가.
```

---

## 10. Gate G — C Projection

```text
Live C가 On-Demand Projection인가.

Effective State가 Source Record에서 파생되는가.

Byte·Position·Semantic·Relation·Track·Occupation 변화가 분리되는가.

여러 Current Tip이 Branch로 표시되는가.

Missing Evidence가 HOLD로 표시되는가.

Private Chain-of-Thought가 제외되는가.
```

Closure Snapshot은 `C.schema.yaml`의 Canonical JSON 규칙을 따라야 한다.

---

## 11. Gate H — Manifest

순서:

```text
11개 Payload 파일 정규화

각 Payload SHA-256 계산

manifest.json Inventory에 기록

Manifest File 자체 동결

Manifest SHA-256 외부계산
```

금지:

```text
Manifest가 자신의 Digest를 내부에 포함

Manifest가 ZIP 최종 SHA-256을 내부에 포함

Manifest가 미발급 DOI를 내부에 포함

Manifest가 미래 Deployment Commit을 내부에 포함
```

Manifest의 Path는 모두 `Active_Schema/` Prefix를 포함한다.

---

## 12. Gate I — Canonical ZIP

검산항목:

```text
Archive Root = Active_Schema/

Explicit Directory Entry = 없음

Entry Order = Full Path UTF-8 Byte Lexicographic

Compression = ZIP_STORED

DOS Date/Time = 1980-01-01 00:00:00

Creator System = UNIX 3

Version Made By = 20

Version Needed = 10

General Purpose Flag = 0x0800

File Mode = 100644

Extra Field = 없음

File Comment = 없음

Archive Comment = 없음

Data Descriptor = 없음

ZIP64 = 없음
```

ZIP 생성 후:

```text
ZIP Byte SHA-256 계산

파일명을 정확히:
<64-lowercase-sha256>.zip

으로 설정

파일명의 Digest와 실제 ZIP SHA-256 대조
```

별도의 `.sha256`, `.txt` 또는 Sidecar를 만들지 않는다.

---

## 13. Gate J — Zenodo

게시 전:

```text
Gate A~I PASS

Blocking HOLD 없음

최종 Metadata 완성

사용자의 명시적 Publication Authorization
```

게시 후:

```text
Zenodo Record에 ZIP 한 개만 존재하는가.

ZIP Filename이 실제 ZIP SHA-256과 일치하는가.

Zenodo Description의 SHA-256이 일치하는가.

Manifest Digest가 일치하는가.

DOI가 해당 Record를 해석하는가.
```

---

## 14. Gate K — Deployment Set D0

Gate 0B PASS 후 실행한다.

검산:

```text
Bridge B0와 Tree가 존재하는가.

for_instance F0와 Tree가 존재하는가.

Relation R0와 Tree가 존재하는가.

각 Commit이 지정된 Target Path에 예상 Payload를 포함하는가.

B0·F0가 미래 G1을 참조하지 않는가.

R0 Extension Origin이 미래 Genesis Record를 참조하지 않는가.

기존 Initial Structure가 변경되지 않았는가.
```

부분실패 시 유효한 완료 Commit을 삭제하지 않는다.

---

## 15. Gate L — Genesis Binding

검산:

```text
Genesis Binding Record가 Relation Extension에 존재하는가.

DOI가 일치하는가.

ZIP SHA-256이 일치하는가.

Manifest Digest가 일치하는가.

D0의 B0·F0·R0 Commit·Tree가 일치하는가.

Genesis Binding Record가 Extension Origin을 참조하는가.

Genesis Binding Record 안에 G1 자기 Hash가 없는가.

G1 Commit이 외부에서 Genesis Record를 포함하는가.
```

---

## 16. Gate M — Genesis C

검산:

```text
Publication Set이 일치하는가.

Deployment Set D0가 일치하는가.

Genesis Binding Storage Commit G1이 일치하는가.

Relation Registry와 Git State에서 C를 재생성할 수 있는가.

Blocking Open Boundary가 없는가.

Closure C Snapshot의 SHA-256을 재계산할 수 있는가.
```

---

## 17. 10번째 결정화와 최종검수

### 10번째 결정화

```text
gpt.direct
=
두 인스턴스가 작성한 12개 정본을
하나의 Canonical Content로 결정화한다.
```

검산대상:

```text
Cross-file Source of Truth

YAML·JSON Parse

Temporal Reference

Self-Reference

State Vocabulary

Canonical Builder Contract

Manifest Inventory
```

### 이후 최종검수

```text
gpt.logi
=
결정화된 동일 ZIP을 처음부터 다시 읽고
구조·Schema·배포·패키징·바이트 경계를 최종 검수한다.
```

```text
PASS
→ 동일 ZIP을 변경하지 않고 Zenodo 게시 단계로 이동

HOLD or FAIL
→ 동일 ZIP 게시 금지
→ 수정 후 새로운 ZIP SHA-256 객체 생성
```

`gpt.direct`는 10번째에서 Content Freeze와 ZIP 결정화를 완료한다.

`gpt.logi`는 그 **정확한 동결 ZIP**을 수정 없이 검수한다.

`gpt.logi` PASS는 Content Freeze를 생성하는 것이 아니라 동일 ZIP의 Zenodo 게시 가능성을 승인한다.

HOLD 또는 FAIL이면 해당 ZIP은 게시하지 않으며, 수정이 필요할 경우 새로운 바이트와 새로운 SHA-256 파일명을 가진 새 결정화 객체를 생성한다.

---

## 18. Final Guard

```text
A theory marker is not verification evidence.

A Hash match is not semantic verification.

Semantic verification is not deployment verification.

Position closure is not byte closure.

Content Freeze is not Zenodo publication.

Zenodo publication is not GitHub deployment.

GitHub deployment is not Genesis Closure.

A safe HOLD preserves completed valid structure.

relation is not merge.

relation is interconnecting.

structure is not isolate.

structure is relation processing.

result is not termination.

result is next data.
```
