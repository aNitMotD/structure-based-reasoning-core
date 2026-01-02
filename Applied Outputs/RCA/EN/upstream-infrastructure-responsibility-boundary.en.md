## Case: WoL Failure under Upstream Infrastructure Constraint

### 1. Observable Information
- Successful transmission of WoL magic packets from the endpoint
- No evidence of local tool or configuration failure
- Packet captures revealed multiple IPs converging on a single abnormal MAC address

### 2. Implicitly Demanded Judgment
- Attribute failure to subcontractor-managed network or tooling
- Continue troubleshooting infrastructure without access or control

### 3. Structural Reasons Judgment Was Not Viable
- No physical or logical access to server-room routing equipment
- L2/L3 topology information unavailable
- No authority to modify or validate upstream infrastructure

### 4. Structural Judgment Shift
- Identified ARP pollution patterns using pcap-based evidence
- Narrowed the fault domain to upstream infrastructure exclusively

### 5. Responsibility Boundary Declaration
- This case exceeds the subcontractor’s judgment and control boundary
- Responsibility must be transferred to the upstream infrastructure owner

### 6. Retrospective Insight
- This is a canonical example of situations where observation is possible but judgment is not
