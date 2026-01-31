# Legacy Presence Trust Illusion

## Summary
This document records a structural pattern where
the mere *presence* of a legacy system inside an operational environment
creates an implicit trust attribution,
despite the system being incapable of assuming responsibility.

---

## Observed Pattern
In legacy or constrained environments (e.g., unpatchable IoT devices),
systems are often treated as trusted participants
simply because they are connected, operational, or historically accepted.

This produces an illusion where:
- presence is conflated with trust
- connectivity is mistaken for responsibility
- operational necessity overrides boundary definition

---

## Structural Characteristics
- the system cannot be updated or corrected
- the system does not participate in decision-making
- yet it is included within the same trust boundary as active agents

Responsibility is therefore *implicitly assigned without capability*.

---

## Boundary Distortion
The distortion does not arise from malicious behavior,
but from structural convenience:
keeping the system operational is prioritized over redefining boundaries.

As a result, trust becomes a side-effect of topology rather than intent.

---

## Notes
This pattern is recorded for structural recognition only.
No mitigation or architectural recommendation is defined here.
