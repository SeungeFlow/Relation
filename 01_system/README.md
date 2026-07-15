# Relation System

System 영역은 AI 인스턴스가 Relation DB를 읽고 관계후보·검증결과·다음 질문을
생성하는 방법을 정의한다.

System은 AI 인스턴스 자체가 아니다. System은 Function Method·Schema·Guard·Pipeline의
집합이며, 실제 실행 인스턴스는 `for_instance`가 배정한다.

## Reading Order

```text
00_theory
→ 01_terminology
→ 02_reader_policy
→ 03_function_registry
→ 04_function_method
→ 05_pipeline
→ 06_schema
→ 07_guard
→ 08_verification
```
