## Abstract

This document records a structural failure case observed in a complex software ecosystem.
A third-party tool’s core functionality becomes unusable due to global input mutation performed by a resident system-level service.
The issue persists across clean installations and stable versions, and cannot be mitigated at the application level.

This is not a bug report or a request for change.
It is a structural observation of how responsibility boundaries collapse under certain design assumptions.

---

## 요약

이 문서는 복잡한 소프트웨어 생태계에서 관측된 구조적 실패 사례를 기록한다.
시스템 상주 서비스의 전역 입력 변조로 인해 서드파티 도구의 핵심 기능이 무력화된다.
이 현상은 클린 설치 및 안정 버전에서도 재현되며, 애플리케이션 레벨에서 차단할 수 없다.

본 문서는 버그 리포트나 수정 요청이 아니다.
특정 설계 전제 하에서 책임 경계가 어떻게 붕괴되는지를 관측한 구조 분석 기록이다.
