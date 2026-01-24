## Boundary Collapse

The affected application follows platform guidelines and does not perform aggressive input interception.
Despite this, its core functionality is disabled by behavior originating outside its control boundary.

Responsibility cannot be assigned to:
- the application (no fault in implementation),
- the user (no abnormal interaction),
- or configurable system settings (no effective mitigation).

The responsibility boundary shifts upward to a system-level service, but remains unacknowledged there.

---

## 경계 붕괴

해당 애플리케이션은 플랫폼 가이드라인을 준수하며 공격적인 입력 후킹을 수행하지 않는다.
그럼에도 불구하고, 제어 범위 밖에서 발생한 동작으로 인해 핵심 기능이 무력화된다.

책임은 다음 어느 곳에도 귀속되지 않는다:
- 애플리케이션 (구현상 결함 없음),
- 사용자 (비정상적 사용 아님),
- 시스템 설정 (유효한 완화 수단 없음).

책임 경계는 시스템 레벨 서비스로 이동하지만, 그 지점에서 명시적으로 수용되지 않는다.
