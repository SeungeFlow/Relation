---
package:
  id: ARSFIP-10V-20260714
  name_ko: AI 해독형 Relation Source-Field 구조설치 패키지
  name_en: AI-Decodable Relation Source-Field Installation Package
  version: 0.1.0
  release_status: candidate
  date: '2026-07-14'
volume:
  id: VOL_03
  sequence: 3
  total_volumes: 10
  title: Local.Zero·역검산·양방향 시간
  role: 결과를 Local.Zero로 선택해 과거 형성과정과 이후 상태전이를 서로 다른 증거등급으로 해석하는 시간방법론을 고정한다.
  previous_volume: VOL_02
  next_volume: VOL_04
  imports:
  - VOL_01::global_guards
  - VOL_02::seed_fruit_cycle
  - VOL_02::concept_lineage_model
  exports:
  - local_zero_model
  - reverse_analysis_method
  - bidirectional_time_model
  - knowledge_boundary
  - comparison_requirements
  load_policy:
    read_entire_volume: true
    summarize_only: false
    preserve_definitions: true
    preserve_guards: true
    repository_mutation: false
  expected_load_receipt: ARSFIP-10V-20260714_VOL_03_LOADED
---

# Volume 03 — Local.Zero·역검산·양방향 시간

## 1. 중심기점의 정의

합의안·계약서·특정 연설·결정적 논문·전쟁발발·블랙홀 형성·폰지사기 붕괴·현재가격은 과거과정의 단순 끝점이 아니다.

이들을 분석의 출발점으로 선택하면 `Local.Zero`가 된다.

\[
Past.Roots
\longleftarrow
Local.Zero
\longrightarrow
Future.Seeds
\]

Local.Zero는 세계 전체의 절대기원이 아니다.

\[
Local.Zero\neq Absolute.Origin
\]

현재 질문에 맞춰 선택된 국소적 중심기점이다.

---

## 2. 중심기점의 유형

### 문서형

- 합의안
- 협의안
- 계약서
- 정책문서
- 특정 연설문
- 결정적 논문
- 경제보고서

### 사건형

- 전쟁발발
- 파업
- 제도시행
- 기업파산
- 자연재해 발생
- 기술 상용화
- 블랙홀 형성

### 가치형

- 주식가격
- 환율
- 금리
- 임금
- 성과급 비율
- 계약금액

### 현재상태형

아직 미래가 발생하지 않은 현재시점의 시스템·시장·조직상태.

---

## 3. 여러 시간층

하나의 사건에는 여러 시간이 존재한다.

```yaml
temporal_layers:
  formation_start_time:
  precursor_time:
  trigger_time:
  event_time:
  record_time:
  publication_time:
  effective_time:
  analysis_time:
  forward_horizon:
```

사건시간과 분석시간을 구분한다.

\[
t_e=\text{event time},\qquad t_a=\text{analysis time}
\]

후대 분석자는 사건 이후의 결과를 알고 있지만 당시 참여자는 알지 못했다.

\[
Knowledge(t_e)\neq Knowledge(t_a)
\]

---

## 4. Knowledge Boundary

```yaml
knowledge_boundary:
  available_at_event:
  available_to_specific_actor:
  unavailable_at_event:
  later_discovered_evidence:
  retrospective_interpretation:
  current_unknown:
```

사후에 전조처럼 보인다는 사실과, 당시 실제로 예측 가능한 신호였다는 주장은 다르다.

\[
Retrospective.Pattern
\neq
Prior.Predictability
\]

---

## 5. 역검산

역검산은 단순히 순서를 거꾸로 읽는 것이 아니다.

\[
Result
\rightarrow
Immediate.Prior.State
\rightarrow
Accumulated.Conditions
\rightarrow
Structural.Root.Candidates
\]

각 단계가 결과를 만드는 데 어떤 기능을 했는지 다시 분류한다.

### 관계역할

- background
- condition
- direct cause
- indirect cause
- precursor
- trigger
- amplifier
- suppressor
- feedback
- accompanying signal
- unknown

---

## 6. 역검산과 역인과

실제 인과방향은 다음이다.

\[
Past.Cause\rightarrow Result
\]

분석방향은 반대로 시작할 수 있다.

\[
Result\rightarrow Search.For.Past.Cause
\]

따라서,

\[
Reverse.Reading\neq Reverse.Causality
\]

---

## 7. 합의안의 역검산

```text
합의안
← 최종초안
← 수정안
← 협의
← 요구안
← 불신·불균형
← 제도·역사·이해관계
```

질문:

- 왜 이 문구가 필요했는가
- 무엇이 삭제되었는가
- 분모와 비율은 어떻게 바뀌었는가
- 누가 결정권을 갖게 되었는가
- 어떤 갈등은 해결되고 어떤 갈등은 다른 위치로 이동했는가
- 당시 각 주체의 목표와 기대는 무엇이었는가

---

## 8. 폰지사기의 역검산

정방향 표면:

\[
고수익약속\rightarrow 초기지급\rightarrow 신뢰\rightarrow 재투자\rightarrow 신규유입의존\rightarrow 붕괴
\]

붕괴에서 역방향으로 읽으면 다음 기능후보가 나타난다.

| 표면 | 역검산 기능후보 |
|---|---|
| 반복지급 | 신뢰형성 비용 |
| 교육 | 내부 해석언어 형성 |
| 공동체 | 신규참여자 전달망 |
| 재투자 | 자금유출 억제 |
| 고수익 약속 | 최초 유입을 여는 Door |

다만 정상구조에도 지급·교육·재투자가 존재할 수 있으므로, 실제 현금흐름과 비교군이 필수다.

---

## 9. 전쟁발발의 역검산

\[
War.Outbreak
\leftarrow
Immediate.Trigger
\leftarrow
Mobilization
\leftarrow
Diplomatic.Breakdown
\leftarrow
Accumulated.Conflict
\]

단일 직선으로 닫지 않는다.

\[
\{
Political, Economic, Military, Social, Cultural, International
\}
\rightarrow
War.Local.Zero
\]

---

## 10. 양방향 시간

### 과거방향

이미 발생한 기록을 이용해 형성과정을 복원한다.

### 이후방향

두 상태를 분리한다.

1. 이미 발생한 후속결과  
2. 아직 실현되지 않은 기대·가정·시나리오  

현재를 중심으로 둘 때 미래는 사실이 아니다.

\[
Expectation\neq Realized.Future
\]

그러나 기대는 현재행동의 실제 원인이 될 수 있다.

\[
Expectation_t\rightarrow Action_t\rightarrow Current.Result_t
\]

---

## 11. 시작점·종료경계

역검산은 무한히 과거로 가지 않는다.

```yaml
analysis_boundary:
  center_id:
  reverse_end:
    earliest_relevant_time:
    earliest_relevant_root:
    stop_reason:
  forward_end:
    time_horizon:
    next_center:
    stop_reason:
```

분석 중 중심기점을 바꾸면 그 이유를 기록한다.

```yaml
center_revision:
  previous_center:
  new_center:
  reason:
  affected_results:
```

---

## 12. 비교군

역검산은 반드시 비교군과 결합한다.

1. 같은 결과·다른 과정  
2. 같은 과정·다른 결과  
3. 유사조건·사건 미발생  
4. 같은 사건·다른 관측자  
5. 초안·수정안·최종안 Version 비교  

비교군 없이 결과에서 과거를 고르면 그럴듯한 사후서사가 될 수 있다.

---

## 13. Local.Zero Schema

```yaml
local_zero:
  center_id:
  center_type:
  title:
  selection_reason:

  temporal:
    event_time:
    analysis_time:
    formation_start:
    effective_time:
    forward_horizon:

  knowledge_boundary:
    available_at_event:
    later_discovered:
    retrospective:
    unknown:

  observed_result:
  unresolved_elements:

  reverse_analysis:
    immediate_prior_state:
    conditions:
    precursors:
    triggers:
    amplifiers:
    suppressors:
    root_candidates:

  forward_analysis:
    observed_consequences:
    ongoing_transitions:
    actor_expectations:
    conditional_scenarios:
    invalidation_conditions:
    unknowns:

  comparisons:
  evidence:
  next_questions:
```

---

## 14. Repo Mapping

| 시간방법 | Relation Repo |
|---|---|
| Local.Zero | `02_db/03_center_cell/` |
| 역검산 | `01_system/04_function_method/reverse_analysis/` |
| 시간정렬 | `01_system/04_function_method/temporal_alignment/` |
| Knowledge Boundary | `02_db/05_evidence_seed/knowledge_boundary/` |
| 비교군 | `02_db/06_comparison_seed/` |
| 다음 질문 | `02_db/08_question_seed/` |

---

## 15. Guard

- Local.Zero는 절대기원이 아니다.  
- 역검산은 역인과가 아니다.  
- 사후에 보이는 조짐은 당시 예측 가능성의 증명이 아니다.  
- 미래 기대는 실현된 사실이 아니다.  
- 결과가 같아도 과정은 다를 수 있다.  
- 과정이 비슷해도 결과는 다를 수 있다.  
- 중심이동은 기록한다.  
- 분석 종료경계를 사전정의한다.  

---

## 16. Volume 03의 결정화 결과

```yaml
volume_result:
  local_zero:
    status: fixed_method
    absolute_origin: false

  reverse_analysis:
    status: fixed_method
    reverse_causality: false
    comparison_required: true

  bidirectional_time:
    past: evidence_reconstruction
    future: observed_result_or_conditional_scenario

  next_seed:
    volume: VOL_04
    topic: space_state_coordinate_cell_grid_matrix_tensor
```

---

## 17. Load Marker

```text
ARSFIP-10V-20260714_VOL_03_LOADED
```
