---
object_id: HRTDB_ACTIVE_SCHEMA_TERMINOLOGY_AND_AUTHORITY_NORMALIZATION_0002
object_class: ACTIVE_SCHEMA_TERMINOLOGY_AND_AUTHORITY_NORMALIZATION
phase_id: AS_F8_3
status: PASS
---

# Terminology and Authority Normalization

## Canonical terms

```text
HRTDB = Hash Relation Track DataBase
Active_Schema = 공개 설계자산
Result.Data = Runtime 최종 기억자산 후보
Track DB = gpt.xyzt 승인 후 GitHub에 등록된 Canonical Result.Data
Hash DB = Track DB에서 파생되는 검색·주소·관계 관제구조
Singularity = Track DB로 승격되지 않은 실험·Hold Evidence
for_instance = Seat·Role·Bootstrap·Recovery가 모이는 기반장
gpt.xyzt = 고정 Overall Coordination Seat
gpt.logi = 현시점 gpt.xyzt 점유 Instance
Semantic Surface Name = 사람이 의미로 읽는 화면표시명
Hash Digest = Exact Byte에서 계산된 SHA-256 Fingerprint
Byte-address Filename = Hash Digest를 외부 파일명으로 배치한 주소표면
Transport Filename = Browser·Framework가 전달 중 중복회피 suffix를 붙인 이름
Raw Byte Object = 검산대상이 되는 실제 파일 Byte
```

## Required distinctions

```text
Seat ≠ Instance
Result.Data ≠ Track DB before registration
Semantic Object ID ≠ Exact Byte SHA-256
Semantic Surface Name ≠ Hash Digest
Hash Digest ≠ Byte-address Filename
Byte-address Filename ≠ Transport Filename
Transport Filename ≠ Raw Byte Object
Web Source URL ≠ Source Object ≠ Content Record ≠ Process Lineage
Operational support ≠ scientific universal proof
Architecture analogy ≠ physical component identity
Open ≠ merge or forced sameness
```

## Filename identity rule

```yaml
filename_layers:
  semantic_surface_name:
    example: "HRTDB Active_Schema Version 2.0.0 — Zenodo Publication ZIP"
    identity_role: HUMAN_READABLE_DISPLAY

  byte_address_filename:
    rule: "<sha256_of_exact_zip_bytes>.zip"
    identity_role: EXTERNAL_EXACT_BYTE_ADDRESS

  transport_filename:
    example: "<sha256>(1).zip"
    identity_role: DELIVERY_SURFACE
    numeric_suffix_part_of_identity: false

  raw_byte_object:
    identity_check: RECOMPUTE_SHA256
```

## Status vocabulary

```text
SOURCE_AUTHORITY_DEFINITION
REGISTERED_CANONICAL_TRACK
EXPERIMENTAL_SINGULARITY_EVIDENCE
COORDINATION_MANUSCRIPT
EXTERNAL_SOURCE_SUPPORTED
APPLICATION_CANDIDATE
DESIGN_ONLY
OPEN_FUTURE
NOT_PRESENT_IN_AVAILABLE_OBJECT_SET
```

## Normalization verdict

```yaml
ambiguous_bare_source_term_reduced: true
track_db_registration_boundary_explicit: true
hash_db_state_marked_design_only: true
singularity_remote_state_explicit: true
surface_and_byte_filename_layers_explicit: true
transport_suffix_identity_excluded: true
ibm_equivalence_claim_prohibited: true
universal_scientific_claim_prohibited: true
```
