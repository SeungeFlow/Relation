---
package:
  id: ARSFIP-10V-20260714
  name_ko: AI 해독형 Relation Source-Field 구조설치 패키지
  name_en: AI-Decodable Relation Source-Field Installation Package
  version: 0.1.0
  release_status: candidate
  date: '2026-07-14'
volume:
  id: VOL_06
  sequence: 6
  total_volumes: 10
  title: relation.bridge·Evidence·비교군·인식구조
  role: 서로 다른 Field를 연결하는 relation.bridge의 최소조건과 Evidence·비교군·편향·기대심리·문서 Operator
    검증체계를 고정한다.
  previous_volume: VOL_05
  next_volume: VOL_07
  imports:
  - VOL_03::comparison_requirements
  - VOL_05::causal_role_taxonomy
  - VOL_05::historical_forest_model
  - VOL_04::space_state_model
  exports:
  - relation_bridge_contract
  - evidence_taxonomy
  - comparison_schema
  - observer_state_model
  - document_operator_model
  load_policy:
    read_entire_volume: true
    summarize_only: false
    preserve_definitions: true
    preserve_guards: true
    repository_mutation: false
  expected_load_receipt: ARSFIP-10V-20260714_VOL_06_LOADED
---

# Volume 06 — relation.bridge·Evidence·비교군·인식구조

## 1. relation.bridge의 정의

`relation.bridge`는 서로 다른 두 대상·Tree·Field 사이에서 실제 전달·변환·영향경로를 구성하는 관계다.

\[
Bridge
=
Source
+
Transferred.Object
+
Carrier/Medium
+
Route
+
Destination
+
State.Transition
\]

두 대상이 비슷하게 보인다는 이유만으로 Bridge가 존재하는 것은 아니다.

\[
Similarity\neq Relation
\]

---

## 2. Bridge의 구성요소

### Source

영향·물질·정보·자본·행동이 시작된 위치.

### Transferred Object

무엇이 전달되었는가.

예:

- 물질
- 정보
- 자본
- 신뢰
- 병원체
- 기술
- 계약권리
- 정책효과

### Carrier

전달대상을 운반하는 주체.

예:

- 사람
- 차량
- 문서
- 금융계약
- 네트워크
- 종자
- 장비

### Medium

전달이 이루어지는 환경.

예:

- 토양
- 물
- 공기
- 인터넷
- 금융시장
- 법률체계
- 교육
- 언론
- 사회적 신뢰망

### Route

Source에서 Destination까지의 구체적 경로.

### Destination

영향을 받은 위치·대상.

### State Transition

Destination에서 무엇이 바뀌었는가.

\[
State_{before}\rightarrow State_{after}
\]

---

## 3. Bridge 최소조건

1. Source와 Destination 식별  
2. 시간순서 정렬  
3. 전달대상 식별  
4. Carrier 또는 Medium 식별  
5. Route 식별  
6. Destination의 상태변화  
7. Source·Path·Destination Evidence  
8. 대안경로와 비교군  
9. 불확실성 표시  

이 중 일부가 없으면 `candidate` 또는 `unknown`으로 남긴다.

---

## 4. Bridge 상태

```text
candidate
sourced
path_identified
evidence_aligned
comparison_checked
verified_local
disputed
rejected
unknown
```

`verified_local`은 전체세계의 영구진리가 아니라 현재 질문과 Source 경계 안의 국소판정이다.

---

## 5. relation.bridge Schema

```yaml
relation_bridge:
  bridge_id:
  title:

  source_side:
    field_id:
    tree_id:
    center_id:
    seed_ids:

  target_side:
    field_id:
    tree_id:
    center_id:
    seed_ids:

  bridge_structure:
    transferred_object:
    carrier:
    medium:
    route:
    boundary_crossings:
    state_before:
    state_after:

  temporal_alignment:
    source_time:
    transmission_time:
    target_change_time:

  evidence:
    source_evidence:
    path_evidence:
    destination_evidence:
    counter_evidence:

  comparison:
    similar_bridge:
    similar_condition_no_bridge:
    alternative_route:

  classification:
    status:
    uncertainty:
```

---

## 6. Evidence 분류

### verified_fact

직접 기록과 검증 Source로 확인.

### contemporary_record

사건 당시 작성되었으나 작성자 위치와 목적을 함께 봐야 함.

### later_discovered_evidence

후대 조사·발굴·분석으로 추가.

### retrospective_interpretation

자료를 연결한 후대 해석.

### disputed_claim

주체 간 사실 또는 의미가 충돌.

### structural_analogy

관계후보를 생성하는 비유.

### counter_evidence

기존 관계후보를 약화하는 근거.

### missing_data

필요하지만 없는 자료.

### conditional_scenario

미래조건과 가정.

### unknown

현재 판단불가.

---

## 7. 과학적 사실과 비유

블랙홀은 인간욕망의 사실모형이 아니다.

- 블랙홀 물리학: 과학적 사실·이론층
- 욕망·집중·흡수: 구조적 비유
- 폰지사기·권력집중: 별도의 역사 Evidence로 검증할 사회가설

\[
Analogy\neq Evidence
\]

비유는 질문을 만들고, Evidence는 답을 지지하거나 기각한다.

---

## 8. 비교군

### 같은 결과·다른 과정

붕괴·합의·가격하락이 서로 다른 원인으로 발생할 수 있다.

### 같은 과정·다른 결과

유사한 갈등·긴장·실적에서도 다른 결과가 나타날 수 있다.

### 유사조건·사건 미발생

원인후보가 있었지만 사건이 발생하지 않은 사례.

### 같은 사건·다른 관측자

회사·노동자·주주·정부·언론·후대연구자의 해석차이.

### 문서 Version 비교

초안·수정안·잠정안·최종안·시행안.

---

## 9. Comparison Schema

```yaml
comparison_seed:
  comparison_id:
  target_center:
  comparison_type:
  compared_items:
  common_conditions:
  different_conditions:
  source_quality_difference:
  result_difference:
  interpretation:
  uncertainty:
```

비교군을 찾지 못한 경우에도 그 부재를 기록한다.

---

## 10. 목표·기대심리·인식구조

### 목표

\[
Goal=Selected.Future.State
\]

### 기대심리

\[
Expectation=Goal+Belief+Emotion+Estimated.Probability
\]

### 인식구조

무엇을 보고 무엇을 중요하게 연결할지를 결정하는 내부 기준장.

\[
Perception\rightarrow Goal\rightarrow Expectation\rightarrow Data.Selection\rightarrow Interpretation
\]

목표가 사실보다 앞서면 원하는 결론을 정당화하는 자료만 선택할 위험이 있다.

---

## 11. 편향

\[
Bias
=
Position
+
Interest
+
Available.Information
+
Desired.Result
\]

편향은 사실근거가 아니지만, 주체가 왜 특정 행동과 해석을 선택했는지를 역검산하는 자료다.

---

## 12. 감정배제

감정을 없애는 것이 아니다.

\[
Emotion:
Decision.Root
\rightarrow
Observed.State
\]

다음과 같이 기록할 수 있다.

```yaml
observer_state:
  actor:
  goal:
  expectation:
  perception_structure:
  emotional_state:
  attention_effect:
  decision_risk:
  information_boundary:
```

---

## 13. 문서 Operator

합의안·계약서·보고서의 작은 단어가 전체방향을 바꿀 수 있다.

### 의무

- 하여야 한다
- 지급한다

### 재량

- 할 수 있다
- 필요한 경우

### 예외

- 다만
- 제외한다

### 시간

- 즉시
- 추후
- 기간 내

### 권한

- 결정한다
- 선정한다
- 승인한다
- 합의한다
- 협의한다

### 범위

- 전부
- 일부
- 해당 대상
- 포함
- 제외

\[
Document.Meaning
=
Terms
+
Operators
+
Writer.Field
+
Reader.Field
\]

---

## 14. 작성자와 독자

### 작성자 Hidden Field

- 역사
- 학문
- 법·제도
- 경험
- 이해관계
- 권력
- 예상독자
- 시간압력

### 독자 Field

- 목표
- 기대
- 지식수준
- 감정
- 소속집단
- 손익위치
- 선택적 주의

문구가 모호하다고 의도적 기만을 자동확정하지 않는다.

```text
unintentional_ambiguity
technical_complexity
different_interpretation
strategic_ambiguity
deliberate_deception
```

을 분리한다.

---

## 15. 관계검증 흐름

\[
Candidate.Bridge
\rightarrow
Source.Check
\rightarrow
Time.Alignment
\rightarrow
Path.Check
\rightarrow
State.Transition
\]

\[
\rightarrow
Evidence.Grade
\rightarrow
Comparison
\rightarrow
Local.Status
\]

---

## 16. Repo Mapping

| 검증개념 | Relation Repo |
|---|---|
| Bridge | `02_db/04_relation_seed/bridge/` |
| Path | `02_db/04_relation_seed/path/` |
| Evidence | `02_db/05_evidence_seed/` |
| Comparison | `02_db/06_comparison_seed/` |
| Observer State | `02_db/02_data_seed/observer_state/` |
| Document Operator | `01_system/01_terminology/` 및 Data Seed |
| Evidence Function | `01_system/04_function_method/evidence_grading/` |

---

## 17. Guard

- 유사성은 관계가 아니다.  
- Carrier 없는 Bridge를 확정하지 않는다.  
- Route 없는 인과를 확정하지 않는다.  
- 상태변화 없는 Bridge를 확정하지 않는다.  
- 편향은 Evidence가 아니다.  
- 감정은 결론이 아니다.  
- 모호성은 기만의 증명이 아니다.  
- 기대는 미래사실이 아니다.  
- 문서의 큰 숫자보다 작은 Operator가 더 강할 수 있다.  
- 비교군이 없는 관계는 Candidate로 남긴다.  

---

## 18. Volume 06의 결정화 결과

```yaml
volume_result:
  relation_bridge:
    required_path: true
    required_state_transition: true
    similarity_only: false

  evidence:
    analogy_is_evidence: false
    uncertainty_required: true

  observer:
    bias_as_data: true
    emotion_as_verdict: false

  next_seed:
    volume: VOL_07
    topic: relation_repo_integrated_system_database_architecture
```

---

## 19. Load Marker

```text
ARSFIP-10V-20260714_VOL_06_LOADED
```
