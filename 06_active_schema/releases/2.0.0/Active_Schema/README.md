# HRTDB Active_Schema — Version 2.0.0

```yaml
release_state: ZENODO_UPLOAD_READY_BYTE_FROZEN
release_phase: AS_F8_3
version: "2.0.0"
release_date: "2026-07-20"
creator: "Lee, Seung"
license: "CC-BY-4.0"
current_release_doi: ASSIGN_AT_ZENODO_PUBLICATION
prior_version_doi: "10.5281/zenodo.21410576"
prior_version_relation: isNewVersionOf
```

## Purpose

`Active_Schema` is a public, AI-readable architecture for coordinating independent seat-bound AI instances and preserving their process as HRTDB relational memory assets.

```text
for_instance
→ gathering, seat, role, and alignment field

gpt.xyzt
→ fixed system-control seat

7 independent instances
→ distributed Data·Function·Result·Review·Result.Data execution

Relation/TrackDB
→ canonical persisted Result.Data memory
```

## Package identity and display surfaces

The archive contains one root:

```text
Active_Schema/
```

```yaml
semantic_surface_name:
  HRTDB Active_Schema Version 2.0.0 — Zenodo Publication ZIP

external_byte_address:
  filename_rule: "<64-lowercase-sha256>.zip"
  resolution_state: RESOLVED_OUTSIDE_PAYLOAD_AFTER_BYTE_FREEZE

transport_filename:
  possible_form: "<64-lowercase-sha256>(1).zip"
  numeric_suffix_part_of_identity: false
```

```text
Semantic Surface Name
≠ Hash Digest
≠ Byte-address Filename
≠ Transport Filename
≠ Raw Byte Object
```

The download surface should show the semantic name and the actual Hash filename together. The package does not contain its own final ZIP hash because embedding it would change the bytes being hashed. It does not predeclare the new Zenodo DOI.

## Read order

1. `ACTIVE_SCHEMA_KO.md`
2. `ABSTRACT_EN.md`
3. `00_identity/AUTHORITY_AND_TERMINOLOGY.md`
4. `01_principles/STRUCTURE_PRINCIPLES.md`
5. `02_system/SYSTEM_STRUCTURE.md`
6. `03_database/`
7. `04_experiment/TOPOLOGY_EXPERIMENT.md`
8. `05_operation/`
9. `06_references/`
10. `07_publication/PUBLICATION_AUTHORITY_EVENT.md`
11. `07_publication/`
12. `08_open_future/OPEN_FUTURE.md`
13. `99_manifest/REVIEW_REPORT.md`
14. `99_manifest/RELEASE_CLOSURE.md`

## Version relation

Version 2.0.0 is bound as a new major version of the locally preserved Active_Schema V1 publication associated with DOI `10.5281/zenodo.21410576`. The preserved V1 package ZIP has SHA-256 `42bb7089e5cdfb52eb951b3bb53613c7ed75168337c2a76524a0e47b5eefb88c`.

## Publication boundary

```text
Frozen ZIP
→ upload as one Zenodo file
→ publish as a new version
→ receive the new version DOI
→ bind DOI to GitHub structure in AS_F10
```

## Guard

```text
relation is not merge.
relation is interconnecting.
structure is not isolate.
structure is relation processing.
result is not termination.
result is next data.
```
