# Track DB Instance Lineage

이 Directory는 Track DB Record의 인스턴스 처리계보를 보존한다.

## Required Lineage

- collected_by_instance
- function_1_processed_by_instance
- result_organized_by_instance
- function_2_reviewed_by_instance
- result_data_organized_by_instance
- structure_verified_by_system
- track_document_stored_by_instance

## Purpose

최종 Track DB Document에서 이상이 발견되었을 때
어느 인스턴스가 무엇을 표시했고,
어느 인스턴스가 다시 보아 무엇을 발견했는지 추적한다.

File명은 인스턴스 책임계보를 대신하지 않는다.
