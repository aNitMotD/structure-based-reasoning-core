## Case: On-Demand Archiving under Automation Boundary

### 1. Observable Information
- Random process crashes observed when running an asynchronous engine (Playwright) on Windows
- Binary-level conflicts identified between greenlet C-extension and Windows linking behavior
- Recurrent port conflicts and zombie processes from external middleware (BGUtil)
- Repeated session expiration and authentication failures observed

### 2. Implicitly Demanded Judgment
- Treat runtime instability as an operational issue tolerable during execution
- Manage port conflicts through manual intervention
- Handle authentication expiration as a recurring human task

### 3. Structural Reasons Judgment Was Not Viable
- Runtime instability caused by C-level dependencies is not controllable at the operational layer
- Fixed-port middleware is structurally incompatible with OS-reserved port ranges
- Any reliance on human intervention violates the zero-touch automation requirement

### 4. Structural Judgment Shift
- Removed C-level async dependencies and migrated to a synchronous Selenium-based model
- Replaced fixed ports with dynamic runtime port allocation
- Moved authentication continuity into a system-level self-healing mechanism

### 5. Responsibility Boundary Declaration
- Runtime stability and authentication persistence are not valid subjects of human operational judgment
- These concerns must be fully resolved at the system design layer

### 6. Retrospective Insight
- This case illustrates a failure pattern where automation structures still demand human judgment
- The core issue was not intervention quality, but whether judgment was required at all
