# Remote Validation Contract

gpt.github는 Terminal Git을 사용한다.

```text
Local Bytes
→ git diff
→ commit
→ push
→ Remote Ref
→ Remote Commit
→ Remote Blob
→ Raw/Web surface observation
```

Web blob과 raw는 모두 외부 Web Surface다. 순간차이가 있으면 Commit/Blob/Ref/Time을 먼저 검산한다.

금지:

- force push
- history rewrite
- 원천파일 silent overwrite
- C와 B의 병합
- 별도 SHA-256 sidecar 생성
