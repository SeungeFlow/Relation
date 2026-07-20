---
object_id: HRTDB_ACTIVE_SCHEMA_EXTERNAL_SOURCE_REGISTRY_0002
object_class: EXTERNAL_SOURCE_REGISTRY
phase_id: AS_F8
status: SOURCE_URL_AND_SCOPE_REVIEWED
---

# External Source Registry

## IBM historical example

```yaml
- source_id: IBM-SRC-001
  url: https://www.ibm.com/history/system-360
  publisher: IBM
  title: The IBM System/360
  confirmed_scope:
    - introduced in 1964
    - unified a computer family under one software-compatible architecture
    - strengthened the platform and compatibility model
  project_use: historical architecture example only

- source_id: IBM-SRC-002
  url: https://www.ibm.com/history/personal-computer
  publisher: IBM
  title: The IBM PC
  confirmed_scope:
    - IBM 5150 introduced in 1981
    - open architecture
    - technical reference included circuit designs and source codes
    - supported third-party software and peripheral ecosystem
  project_use: open reference and ecosystem example only

- source_id: IBM-SRC-003
  url: https://www.ibm.com/roadmaps/quantum/2026/
  publisher: IBM
  title: Quantum 2026 — IBM Technology Atlas
  confirmed_scope:
    - quantum and HPC integration goals
    - heterogeneous workflow goals
    - goals are current intent and may change
  claim_state: COMPANY_STATED_GOAL_NOT_COMPLETED_FACT

- source_id: IBM-SRC-004
  url: https://research.ibm.com/blog/quantum-centric-supercomputing-system-reference-architecture
  publisher: IBM Research
  title: Unveiling the first reference architecture for quantum-centric supercomputing
  publication_date: 2026-03-12
  confirmed_scope:
    - reference architecture for quantum-centric supercomputing
    - integration of quantum and classical/HPC environments
  project_use: modern heterogeneous architecture example only
```

## Zenodo publication contract

```yaml
- source_id: ZENODO-SRC-001
  url: https://help.zenodo.org/docs/deposit/about-records/
  publisher: Zenodo
  confirmed_scope:
    - record consists of metadata, files, and persistent identifier
    - DOI is registered on publication
    - versioning creates a new record/version for changed files

- source_id: ZENODO-SRC-002
  url: https://help.zenodo.org/docs/deposit/describe-records/reserve-doi/
  publisher: Zenodo
  confirmed_scope:
    - DOI may be reserved before publication
    - reserved DOI may be included in uploaded files
    - DOI registration occurs when record is published

- source_id: ZENODO-SRC-003
  url: https://help.zenodo.org/docs/deposit/describe-records/licenses/
  publisher: Zenodo
  confirmed_scope:
    - license field is required
    - default license is CC BY 4.0
    - standard and custom licenses are supported

- source_id: ZENODO-SRC-004
  url: https://help.zenodo.org/docs/deposit/create-new-upload/
  publisher: Zenodo
  confirmed_scope:
    - upload files, fill required metadata, preview, publish
    - creators are included in citation
    - resource type and title are required basic information

- source_id: ZENODO-SRC-005
  url: https://help.zenodo.org/docs/deposit/manage-files/
  publisher: Zenodo
  confirmed_scope:
    - ZIP packaging is recommended for larger multi-file sets
    - substantive changes should use versioning
```

## Use boundary

```text
External historical source
≠ HRTDB proof

Zenodo operational documentation
≠ Source Authority publication decision
```
