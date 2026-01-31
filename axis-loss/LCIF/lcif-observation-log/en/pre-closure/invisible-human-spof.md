# Invisible Human SPOF

## Summary
This document records a pattern where
human intervention repeatedly prevents observable failure,
causing the underlying single point of failure (SPOF)
to remain structurally invisible.

---

## Observed Pattern
A system appears stable because:
- failures are silently absorbed by human judgment
- ad-hoc intervention prevents escalation
- no incident artifacts are generated

Over time, the human actor becomes the true SPOF,
without being recognized as such.

---

## Structural Characteristics
- failure conditions exist but are preempted
- system metrics show normal operation
- responsibility concentrates in human decision points

The absence of failure is misinterpreted as absence of risk.

---

## Boundary Distortion
Responsibility is concealed rather than misassigned:
it accumulates silently in human cognition and availability.

The system appears robust,
while its actual stability depends on continuous human presence.

---

## Notes
This pattern is documented as a recognition case.
It does not prescribe automation or process redesign.
