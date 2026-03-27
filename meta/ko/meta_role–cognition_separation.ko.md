## Meta: Role–Cognition Separation

- Principle:
  Role (직무)와 Cognition (사고)은 서로 다른 레이어에 속한다.

- Structure:
  Cognitive Engine (invariant)
        ↓
  Role / Context (variable)
        ↓
  Output (observable)

- Constraint:
  Role을 기반으로 Cognition을 직접 추론할 수 없다.

- Common Failure:
  Role–Cognition Collapse
  → 직무를 사고로 동일시하는 해석 오류

- Cause:
  - 내부 상태 비가시성 (observability limit)
  - 최소 모델 추론 (minimal inference)
  - 시간 동기화 가정 (temporal alignment assumption)

- Example (QA Case):
  - Observation:
    “사용자는 2020년부터 QA로 근무했다.”

  - Common Interpretation:
    “사용자의 사고방식은 2020년부터 QA 중심으로 형성되었다.”

  - Structural Correction:
    사고엔진은 직무 이전에 존재하며,
    QA라는 역할은 해당 사고엔진의 출력 형태를 특정 방향으로 제한한 것에 불과하다.

- Implication:
  Role은 사고를 정의하지 않고,
  출력 형태만 제한한다.

- Boundary:
  Cognition은 직접 관측 불가능하며,
  Role은 관측 가능한 출력 제약 조건에 불과하다.
  
- Correlation Clause:
  관측 가능한 직무 이력은 출력 패턴과 일정한 상관을 가질 수 있다.
  그러나 그 상관성은 내부 사고 구조에 대한 직접 추론이나 단정을 정당화하지 않는다.

- Non-Inference Clause:
  관측 가능한 출력 정보로부터
  내부 사고 구조를 결정하거나 단정할 수 없다.

- Summary:
  직무는 사고를 만들지 않는다.
  단지 어떻게 드러날지를 제한한다.

- Final Note:
  Method-Trait도 구조적 동형이다.
