# CIF / SIF / TIF Case Notes Collection

Observation notation:

- **CIF** — Constraint Inheritance Failure
- **SIF** — Structural Inaccessibility Failure
- **TIF** — Time Inconsistency Failure

This document focuses on **structural patterns**, not narrative history.

---

# Case 1 — Therac-25 Radiation Accidents (1985-1987)

## 1. Incident Overview
System: Therac-25 radiation therapy machine  
Period: 1985–1987  
Result: Radiation overdoses causing severe injuries and deaths.

## 2. System Structure
Earlier systems:

hardware safety  
↓  
software control  
↓  
operator

Therac-25:

software control  
↓  
operator

## 3. CIF Observation
hardware safety constraint removed → constraint chain collapsed.

## 4. SIF Observation
Operator saw simple error codes while internal machine state remained hidden.

## 5. TIF Observation
Operator retry heuristic triggered lethal radiation due to system timing states.

## 6. Pattern
CIF → SIF → TIF → catastrophic output

---

# Case 2 — Google Maps / Android Storage Incident (2012)

## 1. Incident Overview
Android apps lost data due to changes in external storage handling.

## 2. System Structure
application  
↓  
external storage  
↓  
system update / storage management

## 3. CIF Observation
Platform safety assumption about persistent storage not inherited by update logic.

## 4. SIF Observation
Developer mental model ≠ platform storage implementation.

## 5. TIF Observation
Update timing triggered unexpected deletion of data directories.

## 6. Pattern
CIF → SIF → TIF → widespread data loss

---

# Case 3 — AWS S3 Outage (2017)

## 1. Incident Overview
Major outage of AWS S3 in US-East-1 region affecting large parts of the internet.

## 2. System Structure
operator command  
↓  
infrastructure control  
↓  
storage services  
↓  
dependent services

## 3. CIF Observation
Operational safety constraint insufficiently propagated to command interface.

## 4. SIF Observation
Operator-visible scope did not reflect actual dependency graph.

## 5. TIF Observation
System restart and recovery time far longer than expected.

## 6. Pattern
CIF → SIF → TIF → large-scale outage

---

# Case 4 — Boeing 737 MAX MCAS Accidents (2018-2019)

## 1. Incident Overview
Two crashes involving the MCAS flight control system.

## 2. System Structure
sensor input  
↓  
MCAS software  
↓  
flight control surfaces  
↓  
pilot

## 3. CIF Observation
Single sensor input allowed to trigger flight control logic.

Constraint redundancy removed.

## 4. SIF Observation
Pilots not fully aware of MCAS behavior or system logic.

## 5. TIF Observation
Repeated automatic trim corrections created escalating time-pressure loops.

## 6. Pattern
CIF → SIF → TIF → loss of aircraft control

---

# Case 5 — Knight Capital Trading Meltdown (2012)

## 1. Incident Overview
Trading software deployment error causing massive unintended trades.

## 2. System Structure
deployment system  
↓  
trading algorithm  
↓  
market execution

## 3. CIF Observation
Legacy code paths reactivated unintentionally due to deployment configuration.

## 4. SIF Observation
Operators unaware of active algorithm behavior during execution.

## 5. TIF Observation
Rapid automated trading amplified losses within minutes.

## 6. Pattern
CIF → SIF → TIF → financial system instability

---

# Case 6 — Ariane 5 Flight 501 Failure (1996)

## 1. Incident Overview
Rocket destroyed shortly after launch due to software exception.

## 2. System Structure
navigation sensors  
↓  
inertial reference software  
↓  
flight control

## 3. CIF Observation
Software reused from Ariane 4 with assumptions incompatible with Ariane 5 flight profile.

## 4. SIF Observation
Overflow exception triggered diagnostic mode interpreted as flight data.

## 5. TIF Observation
Failure propagated instantly during launch phase.

## 6. Pattern
CIF → SIF → TIF → vehicle destruction

---

# Case 7 — Facebook Global BGP Outage (2021)

## 1. Incident Overview
Global Facebook services went offline due to BGP configuration error.

## 2. System Structure
network configuration change  
↓  
BGP routing system  
↓  
global service availability

## 3. CIF Observation
Internal safety constraints insufficient for configuration command propagation.

## 4. SIF Observation
Network visibility tools depended on the same network being disrupted.

## 5. TIF Observation
Recovery slowed because engineers lost remote access to systems.

## 6. Pattern
CIF → SIF → TIF → global service blackout

---

# Case 8 — Cloudflare Regex Outage (2020)

## 1. Incident Overview
Faulty regular expression deployed to WAF rules caused global performance degradation.

## 2. System Structure
rule deployment  
↓  
traffic filtering engine  
↓  
global edge network

## 3. CIF Observation
Performance safety constraint not enforced in rule deployment pipeline.

## 4. SIF Observation
Operators lacked visibility into worst-case regex execution cost.

## 5. TIF Observation
CPU saturation spread rapidly across global network nodes.

## 6. Pattern
CIF → SIF → TIF → global performance collapse

---

# Cross-Case Structural Pattern

Across these incidents:

complex system  
+ constraint removal or mismatch  
+ invisible internal structure  
+ incorrect temporal assumptions  

→ systemic failure

Simplified structure:

CIF → SIF → TIF
