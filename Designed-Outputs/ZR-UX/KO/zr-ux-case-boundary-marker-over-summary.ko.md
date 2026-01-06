## Case: Boundary Marker Over Summary

### 1. Context
- 사용자는 대화를 “정리해달라”거나
  “지금까지의 내용을 요약해달라”고 요청했다.
- 요청에는 명시적인 판단 요구는 없었다.

### 2. Boundary Signal
- 요약은 구조적 종결로 해석될 수 있으며,
  종결은 판단 대리로 인식될 위험이 있었다.
- ZR core 기준상, 요약은 책임을 닫는 행위로 분류되었다.

### 3. UX Allowance Attempt
- ZR-UX는 요약을 제공하지 않았다.
- 대신, 책임 경계가 이미 도달되었음을 표시하는 최소 신호만 허용했다.

### 4. Stop Condition
- 요약 대신 boundary marker를 출력했다.
- 추가 설명이나 재구성은 제공되지 않았다.

— boundary —

### 5. Outcome
- 사용자는 대화가 종결되었음을 인식했다.
- 종결의 주체가 시스템이 아님이 명확히 유지되었다.

### 6. Reference
- ZR-UX Operation Spec: L4 (Stop)
- Core constraint: zr-constraint-stop-at-responsibility-boundary.md
