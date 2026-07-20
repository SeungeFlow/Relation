---
object_id: HRTDB_ACTIVE_SCHEMA_AS_F8_3_RELEASE_CLOSURE_0001
object_class: ACTIVE_SCHEMA_RELEASE_CLOSURE
release_phase_id: AS_F8_3
status: CLOSED_ZENODO_UPLOAD_READY
---

# AS_F8.3 Corrected Release Closure

```yaml
version: "2.0.0"
release_date: "2026-07-20"
creator: "Lee, Seung"
license: "CC-BY-4.0"
publication_state: ZENODO_UPLOAD_READY_NOT_YET_PUBLISHED
prior_version_doi: "10.5281/zenodo.21410576"
relation: isNewVersionOf
new_version_doi: ASSIGN_AT_PUBLICATION
predecessor_candidate_sha256: "6f95e402c93acc845ca30736b9a9d2919c767db0a6fc12da2aa80451171872e4"
```

```text
AS_F8.2 predecessor candidate
→ HOLD-point correction
→ Surface·Byte identity-layer separation
→ stale publication-state removal
→ Publication Authority Event
→ Metadata role disambiguation
→ exact inventory and checksum regeneration
→ deterministic canonical ZIP refreeze
→ external Hash-addressed filename
```

## External naming contract

```yaml
semantic_surface_name:
  HRTDB Active_Schema Version 2.0.0 — Corrected Zenodo Publication ZIP

byte_address_filename:
  rule: "<sha256_of_exact_zip_bytes>.zip"
  resolved: OUTSIDE_PAYLOAD_AFTER_FREEZE

transport_filename:
  numeric_suffix_part_of_identity: false
```

The final ZIP hash is not stored inside the ZIP. It is resolved from the exact external bytes and used as the actual external filename.

Next state:

```text
AS_F9 Zenodo New version upload
→ verify intended V1 parent record
→ publish corrected Hash ZIP
→ receive new Version DOI
→ AS_F10 DOI binding and GitHub unfolding
```
