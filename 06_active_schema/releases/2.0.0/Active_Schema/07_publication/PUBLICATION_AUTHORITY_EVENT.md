---
object_id: HRTDB_ACTIVE_SCHEMA_PUBLICATION_AUTHORITY_EVENT_0001
object_class: ACTIVE_SCHEMA_PUBLICATION_AUTHORITY_EVENT
phase_id: AS_F8_3
source_authority: 승이
recorded_by: gpt.logi
status: BOUND
---

# Publication Authority Event

## Direct source-authority statement

```text
AS_F9 상태 : HOLD 지점을 보완하여 다시 ZIP 생성바람.
```

## Event interpretation

```yaml
authorizes:
  - correct the identified AS_F9 HOLD points
  - preserve the predecessor ZIP as exact-byte evidence
  - regenerate inventory, checksum ledger, manifest, and deterministic ZIP
  - create a new corrected Zenodo publication candidate

preserves_from_current_v2_candidate:
  - title and abstracts
  - creator: "Lee, Seung"
  - creator type: Person
  - license: CC-BY-4.0
  - version: "2.0.0"
  - prior DOI relation candidate: isNewVersionOf

does_not_claim:
  - Zenodo publication already completed
  - new Version DOI already assigned
  - prior Zenodo record independently reverified by the runtime
  - Hash DB implementation completed
  - Singularity remote closure completed
```

## Binding states

```yaml
title_and_abstract:
  BOUND_FROM_CONTINUATION_AND_PRIOR_PUBLICATION_CONTEXT

creator_and_license:
  BOUND_FROM_CURRENT_V2_CANDIDATE_AND_PRIOR_PUBLICATION_CONTEXT

correction_and_refreeze:
  DIRECTLY_AUTHORIZED_BY_SOURCE_AUTHORITY

prior_version_relation:
  PRESERVED_FOR_AS_F9_NEW_VERSION_UI_CONFIRMATION
```

## Authority guard

```text
Continuation authorization is not a fabricated verbatim approval.
Preserved metadata is not newly invented metadata.
AS_F9 execution confirmation is not AS_F8.3 package construction.
```
