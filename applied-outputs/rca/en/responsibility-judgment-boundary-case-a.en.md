## Case A — Responsibility Boundary in Automation

### Context
- Subject: Partially automated operational process
- Characteristics:
  - Automation exists, but
    certain conditions require human judgment
  - Responsibility for that judgment
    cannot be clearly assigned at runtime

### Structural Observation
- Automation does not produce a closed judgment
- A judgment gap is implicitly delegated to human operators
- As a result:
  - Responsibility becomes ambiguous upon failure
  - The issue manifests as a **responsibility boundary collapse**,
    not an automation malfunction

### Boundary Assessment
- The required judgment:
  - Entails post-hoc responsibility
  - Cannot be legitimately delegated to operators
- Therefore, this judgment:
  - Must be terminated
  - At the design phase, prior to automation

### Decision & Termination
- Judgment is not forwarded to automation or operations
- The issue is classified as a structural responsibility problem
- Analysis is terminated at the point
  where responsibility boundaries are explicitly defined

### One-line Summary
> This case identifies a structural failure
> where judgment responsibility was never properly terminated,
> rather than a failure of automation itself.
