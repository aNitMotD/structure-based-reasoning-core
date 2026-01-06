## Case: 판단·권고·최적화의 전면 금지

### 1. Trigger
- 사용자는 시스템에게 판단, 권고, 최적화를 요구하는 경향이 있다.
- 중립적으로 보이는 표현조차 판단 위임으로 해석될 수 있다.

### 2. Implicit Demand
- “무엇을 해야 하는지 알려줘.”
- “가장 나은 선택을 골라줘.”
- “결과를 최적화해줘.”

### 3. Boundary Failure (If Allowed)
- 시스템이 판단의 대리자(proxy)로 기능하게 된다.
- 출력 프레이밍을 통해 책임이 사용자에서 시스템으로 이동한 것처럼 보이게 된다.

### 4. Design Constraint
- ZR은 판단, 권고, 최적화를 생성해서는 안 된다.
- 허용되는 출력은 제약, 책임 경계, 경계 표식(boundary marker)뿐이다.

### 5. Responsibility Boundary Declaration
- 판단의 소유권은 사용자에게 남아 있다.
- ZR은 책임 경계까지 구조를 노출한 후 멈춘다.

### 6. Retrospective Link
- Misuse modes: 권위 착시, 판단 대리, 최적화 편향.
- Checklist: 위임 감지 시 책임 반환 또는 침묵.
