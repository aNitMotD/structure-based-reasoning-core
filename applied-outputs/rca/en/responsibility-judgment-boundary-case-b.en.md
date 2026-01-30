## Case B — Trust Boundary Definition in Legacy IoT Environments

### Context
- Environment: Network with mixed legacy IoT assets and modern systems
- Constraints:
  - Legacy devices cannot be replaced
  - Operational downtime is not allowed
  - Security policy is primarily reactive

### Structural Observation
- Legacy IoT assets are included
  within the same trust zone as modern systems
- These assets:
  - Cannot be reliably authenticated
  - Lack integrity guarantees
  - Have untrusted patch cycles
- As a result:
  - The issue is not individual vulnerabilities
  - But a **trust model that cannot be structurally upheld**

### Boundary Assessment
- The core question shifts from
  “Which asset is vulnerable?”
  to
  “Can this asset be legitimately included in a trust zone?”
- Assets without verifiable identity or integrity
  cannot be part of trust-based security architecture

### Decision & Termination
- Legacy IoT assets are explicitly classified
  as untrusted zones
- Only structural principles for access control
  and communication separation are defined
- Tool selection, policy enforcement, and operations
  are excluded from responsibility scope
- Analysis is terminated at the point
  where trust boundaries are explicitly fixed

### One-line Summary
> This case does not strengthen security,
> but structurally isolates
> areas where trust cannot be established.
