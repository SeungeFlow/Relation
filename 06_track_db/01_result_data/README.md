# Result.Data-Derived Track Records

이 Directory에는 `Result.Data`의 구조검산을 통과한
`Track DB Document`만 저장한다.

## Admission Gate

1. `gpt.xyz`가 `Result.Data`를 생성한다.
2. `gpt.xyzt`가 내용·웹출처·인스턴스계보·오독교정 흐름을 검산한다.
3. PASS된 객체만 `Track DB Document`로 생성한다.
4. `gpt.github`가 이 Directory에 저장한다.

## Filename Rule

각 Runtime Record의 외부 File명은
완성된 정확한 File Byte의 SHA-256이다.

일반 의미 File명, 자동 `(숫자)` 이름, 기존 문서명 재사용을 금지한다.

## Document Internal Rule

Record 문서 내부에는 다음을 기록하지 않는다.

- File명
- Hash Code
- Framework Transport Suffix
- 로컬 경로

다음은 기록한다.

- 내용
- 실제 웹출처 URL
- 표시한 인스턴스
- 처리한 인스턴스
- 재관측한 인스턴스
- 발견된 오독·착시·오판·착오
- 수정과 미해결 상태
