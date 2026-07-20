---
object_id: HRTDB_ACTIVE_SCHEMA_TYPED_IDENTITY_AND_ADDRESS_MODEL_0002
object_class: ACTIVE_SCHEMA_TYPED_IDENTITY_AND_ADDRESS_MODEL
phase_id: AS_F8_3
source_authority: 승이
coordination_authority: gpt.logi
status: PASS_WITH_CANDIDATE_FIELDS
---

# HRTDB Typed Identity and Address Model 0002

## 1. Identity and surface types

```yaml
identity_types:
  semantic_identity:
    field: object_id
    meaning: project-defined object meaning

  semantic_surface_name:
    field: display_name
    meaning: human-readable label shown on a screen or link surface

  byte_identity:
    field: exact_byte_sha256
    meaning: exact bytes at one frozen state

  hash_digest:
    field: sha256_digest
    meaning: fingerprint calculated from the exact byte object

  byte_address_filename:
    field: hash_filename
    rule: filename_base_equals_recomputed_sha256
    meaning: digest string placed on an external filename surface

  transport_filename:
    field: delivered_filename
    meaning: browser or framework delivery name
    numeric_suffix_part_of_identity: false

  raw_byte_object:
    field: exact_file_bytes
    verification: recompute_sha256_and_compare

  repository_identity:
    fields: [repository_owner, repository_name, repository_id_if_verified]

  repository_address:
    fields: [branch, path]

  git_state_identity:
    fields: [commit, tree, blob_if_available]

  publication_identity:
    fields: [zenodo_record_id, doi]

  web_source_identity:
    field: source_url
    meaning: exact web location where content was found
```

## 2. Surface-to-byte formation

```text
Raw Byte Object
→ SHA-256 calculation
→ Hash Digest
→ Digest string
→ Byte-address Filename
→ Browser·Framework delivery
→ Transport Filename
```

```text
Semantic Surface Name
→ meaning-facing display label

Byte-address Filename
→ exact-byte address surface
```

A download surface may display both names together to reduce misreading.

```text
HRTDB Active_Schema Version 2.0.0 — Zenodo Publication ZIP
+
<64-lowercase-sha256>.zip
```

## 3. Non-equivalence rules

```text
Object ID ≠ SHA-256
Semantic Surface Name ≠ Hash Digest
Hash Digest ≠ Byte-address Filename
Byte-address Filename ≠ Transport Filename
Transport Filename ≠ Raw Byte Object
SHA-256 ≠ Source URL
Source URL ≠ Repository Pointer
Repository Path ≠ Git Commit
Git Commit ≠ DOI
DOI ≠ Track DB Payload
Instance Name ≠ Source
Same URL ≠ Same Claim
Same Claim ≠ Same Record
Same Semantic Object ID ≠ Same Byte Object
```

## 4. Transport suffix rule

```yaml
transport_suffix:
  examples: ["(1)", "(2)", "(3)"]
  created_by: browser_or_framework_duplicate_avoidance
  canonical_filename_identity: false
  byte_identity_effect: none
  required_check:
    - strip_suffix_only_for_name_normalization
    - recompute_sha256_from_actual_bytes
    - compare_digest_with_canonical_filename_base
```

## 5. Source type separation

```yaml
web_source:
  source_url:
  source_title:
  publisher_or_author:
  accessed_at:
  confirmed_content:
  application_scope:
  uncertainty:

source_object:
  source_object_id:
  head:
  context:
  byte_identity:
  repository_address_if_any:

content_record:
  record_id:
  statement:
  web_source_refs:
  source_object_refs:
  evidence_class:
  state:

process_lineage:
  collected_by:
  processed_by:
  organized_by:
  reviewed_by:
  registered_by:
```

```text
Web Source ≠ Source Object ≠ Content Record ≠ Process Lineage
```

## 6. Composite address

```yaml
composite_address:
  semantic: {object_id:, object_class:, cycle_id:}
  display: {semantic_surface_name:}
  byte: {algorithm: SHA-256, digest:, byte_address_filename:}
  transport: {delivered_filename:, suffix_part_of_identity: false}
  repository: {repository:, branch:, path:}
  git: {commit:, tree:, blob:}
  publication: {zenodo_record_id:, doi:}
  source: {exact_web_urls:}
```

없는 값은 추정하지 않고 `UNKNOWN`, `NOT_PRESENT_IN_INPUT`, `NOT_APPLICABLE`, `OPEN_FUTURE`로 둔다.

## 7. Query resolution order

```text
Query
→ Hash DB semantic/head index
→ Track pointer
→ Repository address
→ Git state
→ Exact byte object
→ Track DB content
→ Content Record
→ Exact Web Source URL
```

Hash DB가 없거나 Pointer가 깨졌으면 Track Index에서 Object ID·Cycle을 찾아 Exact Byte를 검증한다.

## 8. Typed reference fields

```yaml
typed_reference_fields:
  source_registry_refs: WEB_SOURCE_REGISTRY_ENTRY
  content_record_refs: CONTENT_RECORD
  process_lineage_refs: PROCESS_EVENT_OR_OBJECT
  track_db_refs: TRACK_DB_RECORD
  singularity_refs: SINGULARITY_RECORD
  hash_db_pointer_refs: HASH_DB_POINTER
  exact_source_urls: URL_STRING
  exact_byte_sha256: SHA256_DIGEST
  semantic_surface_name: HUMAN_READABLE_LABEL
  byte_address_filename: HASH_ADDRESS_FILENAME
  transport_filename: DELIVERY_SURFACE_FILENAME
  repository_addresses: REPOSITORY_BRANCH_PATH
  publication_addresses: DOI_OR_ZENODO_RECORD
```

## 9. Count universe rule

```yaml
typed_count:
  label:
  counted_object_class:
  filter_state:
  overlap_allowed:
  deduplication_key:
  value:
```

Evidence Label, Issue Record, Conflict State, Open Future, Required Next Data Record, Unique Required Next Data Type를 분리한다.

## 10. State and time binding

```yaml
state_binding:
  state:
  valid_from:
  valid_to:
  observed_at:
  registered_at:
  source_accessed_at:
  authority_snapshot:
  software_or_schema_version:
```

## 11. Candidate status

```yaml
candidate_database_fields:
  state: APPLICATION_CANDIDATE_REVIEWED_AND_PRESERVED
  candidate_groups:
    - observer_and_frame
    - transform_and_direction
    - source_and_provenance
    - content_identity
    - correction_and_verification
    - database_address
```

```text
END_OF_HRTDB_ACTIVE_SCHEMA_TYPED_IDENTITY_AND_ADDRESS_MODEL_0002
```
