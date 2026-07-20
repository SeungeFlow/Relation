---
object_id: HRTDB_ACTIVE_SCHEMA_CANONICAL_AND_EXPERIMENT_REFERENCE_MAP_0001
object_class: ACTIVE_SCHEMA_REFERENCE_MAP
phase_id: AS_F8
status: BYTE_IDENTITY_REVERIFIED
---

# Canonical and Experimental Reference Map

## Track DB canonical references

```yaml
- object_id: HRTDB_PILOT_RESULT_DATA_0002_XYZ
  exact_byte_sha256: 9dfff9d3a75cc7387f10ae2571190964c94b22213cf0a43077afbdfaf9507ba4
  persistence: Relation/TrackDB
  state: REGISTERED_CANONICAL_TRACK

- object_id: HRTDB_PILOT_RESULT_DATA_0003_XYZ
  exact_byte_sha256: 72428e7ddf3ea03db711449f3930698e82e4961a25103f330fa482dc7262d65b
  persistence: Relation/TrackDB
  commit: de0a6e1f6435ef78e5b95f02f8bd5b8d5459d3f1
  tree: c822f3a644bb58f29ddbf262a3f727a3da3cbdcc
  remote_readback_verified: true
  state: REGISTERED_CANONICAL_TRACK
```

## Singularity experimental references

```yaml
- exact_byte_sha256: 5eed3f7d927e34cd32673decb9b1f520187f8b631d84560f52401e8a5726deed
  role: SINGLE_INSTANCE_HOLD_EXECUTION_RECORD
  state: SINGULARITY_ONLY
  remote_registration_closure: NOT_BOUND_IN_AVAILABLE_OBJECT_SET

- exact_byte_sha256: a8496009a5ca77b4c80b2c08723d4d47a11c04cb527b32d5bc8107e92823e468
  role: SINGLE_INSTANCE_SINGULARITY_ANALYSIS
  state: EXPERIMENT_ANALYSIS
  remote_registration_closure: NOT_BOUND_IN_AVAILABLE_OBJECT_SET
```

## Non-merge rule

```text
Same Semantic Object ID
+ different Byte Hash or Topology or Validation State
→ different object variants
→ no merge or replacement by name alone
```
