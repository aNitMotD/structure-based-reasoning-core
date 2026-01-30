# Observational Memo — Constraint Lifecycle Inheritance Failure

## Observation (EN)

A recurring pattern is observed where constraints are:
- Explicitly defined or acknowledged in early phases (design, review, approval),
- Yet fail to survive across later phases (operation, incident, post-analysis).

The constraint does not disappear due to error,
but appears to **lose inheritance across the lifecycle**.

This memo records a possible failure mode:
constraint validity is locally preserved,
but globally non-persistent across phases.

(No definition, no classification, no prescription.)

---

## 관측 메모 (KO)

다음과 같은 반복 패턴이 관측된다:

- 제약이 설계·검토·승인 단계에서는 명시되거나 인지되었으나,
- 운영·사고·사후 단계로 넘어가며 더 이상 작동하지 않는 상태.

이 제약은 오류로 인해 사라진 것이 아니라,
**생애주기를 건너며 상속되지 못한 것처럼 보인다**.

본 메모는 다음 가능성을 기록한다:
제약은 국소적으로는 유지되지만,
단계 전반에서는 지속되지 않는다.

(정의 없음, 분류 없음, 처방 없음.)
