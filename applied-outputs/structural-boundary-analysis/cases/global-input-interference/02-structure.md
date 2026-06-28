> **직접 접근 고지 / Direct Access Notice**
> 본 문서는 저장소의 README.md 및 INTERPRETATION-GUARDRAILS.md를 먼저 확인했다는 전제 하에서만 해석되어야 합니다.
> This document must be interpreted only on the assumption that the repository’s README.md and INTERPRETATION-GUARDRAILS.md have been reviewed first.

---

## Structural Mechanism

User input is intercepted at a low-level system hook.
Distinct key combinations are consumed and replaced by injected shortcuts before reaching the application layer.
This results in a many-to-one input mutation, where semantically different inputs collapse into identical outputs.

From the application’s perspective, the original user input no longer exists.
No local validation or filtering logic can recover the lost distinction.

---

## 구조적 메커니즘

사용자 입력은 시스템의 저수준 후킹 지점에서 가로채어진다.
서로 다른 키 조합은 애플리케이션에 도달하기 전에 소비되고, 주입된 단축키로 대체된다.
그 결과 의미적으로 구분되던 입력들이 하나의 출력으로 붕괴되는 다대일 변조가 발생한다.

애플리케이션 관점에서는 원래의 사용자 입력 자체가 더 이상 존재하지 않는다.
로컬 검증이나 필터링 로직으로는 이 손실을 복구할 수 없다.
