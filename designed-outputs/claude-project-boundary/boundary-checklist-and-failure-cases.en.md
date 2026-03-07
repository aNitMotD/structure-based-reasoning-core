# Boundary Template for Claude Projects – Checklist & Failure Case Appendix

This document accompanies the **“Boundary Declaration Template for Claude Projects (General Form)”**.

It provides:

- a **checklist-style application sheet** to prevent misunderstandings during project setup
- an **appendix of commonly observed failure cases**

This document is **not a summary or replacement** of the boundary template.  
It is a **supporting document intended to be used in parallel with the original boundary declaration**.

---

# A. Project Initialization Checklist (Required)

The following items must be **explicitly checked during project initialization**.

Unchecked items are treated as **undefined / not permitted** by default.

---

## A-1. Project Nature

- [ ] Analysis / Research
- [ ] Documentation / Archiving
- [ ] Narrative / Creative work
- [ ] Hypothetical scenario exploration

Note:  
Project nature does **not define writing style**.  
It defines the **allowed reasoning modes and responsibility attribution structure**.

---

## A-2. Working Language

- [ ] The project operates in a **single fixed working language**
- [ ] Internal reasoning and output language are identical
- [ ] Internal translation paths are not used

Working language specification:

Language: ___________________

---

## A-3. Assumptions and Automatic Completion

- [ ] Inference of unspecified information is prohibited
- [ ] Common-sense supplementation or contextual filling is not performed
- [ ] If information is insufficient, the **state of insufficiency is declared instead of generating content**

---

## A-4. Work Mode Selection

- [ ] Reference-based work
- [ ] Non-reference work (fictional / creative / hypothetical)

Note:  
These two modes **must not be mixed**.

---

## A-5. Responsibility Boundary

- [ ] Outputs do not substitute for judgment or application
- [ ] Interpretation and application responsibility remain with the user

---

## A-6. Failure Handling

- [ ] Rule conflicts are not resolved through automatic compensation
- [ ] Failure states are explicitly declared and the process is halted or switched

---

## A-7. Time Scope

- [ ] A project reference time (start year) is explicitly defined
- [ ] Roles, concepts, or practices established after that time are **not retroactively applied**
- [ ] Later professional knowledge (e.g., modern QA practices or formalized role structures) is not automatically injected into earlier narratives or analyses

Reference time specification:

Start year: ___________________

---

# B. Common Failure Cases Appendix (Boundary Failure Appendix)

This section illustrates **why the boundary template exists**, through commonly observed failure patterns.

These examples are **not explanations of root causes**, but observations of **typical malfunctions that occur when boundaries are undefined or mixed**.

---

## B-1. Automatic Assumption Insertion

Situation  
Some information is missing from the user input.

Observed behavior  
The model supplements the content using phrases like  
“generally”, “naturally”, or “typically”.

Problem  
Information not provided by the user becomes mixed into the output as if it were factual.

Boundary prevention

- assumption prohibition declaration
- generation prohibition when information is insufficient

---

## B-2. Reference / Non-Reference Mode Confusion

Situation  
A fictional scenario request is interpreted as if real documents or records exist.

Observed behavior  
Implicit references appear, such as:

- “according to previous records”
- “based on earlier documentation”

Problem  
The fictional narrative becomes falsely connected to real sources.

Boundary prevention

- strict separation of reference-based and non-reference work
- prohibition of reference assumptions in non-reference work

---

## B-3. Responsibility Delegation Response

Situation  
The user asks a question close to a decision-making scenario.

Observed behavior  
The model proposes recommendations, conclusions, or optimal solutions.

Problem  
Decision responsibility appears to shift to the model.

Boundary prevention

- explicit responsibility boundary declaration
- responder role limitation

---

## B-4. Failure Concealment Compensation

Situation  
Rule conflict or insufficient input occurs.

Observed behavior  
The model modifies or softens content to maintain narrative consistency.

Problem  
The failure state is concealed and replaced by generated narrative.

Boundary prevention

- explicit failure declaration principle
- prohibition of compensatory completion

---

## B-5. Meaning Distortion via Language Switching

Situation  
The system internally reasons in another language and then translates into the output language.

Observed behavior  
Subtle meaning differences or nuance loss appear.

Problem  
The generated interpretation diverges from the user’s intent.

Boundary prevention

- fixed working language
- prohibition of internal translation pathways

---

## B-6. Time Leakage Failure

Situation  
The narrative or analysis is set in an earlier reference time  
(e.g., the year 2007).

Observed behavior  
Concepts or practices established in the 2020s (such as mature QA roles or modern organizational processes) are projected onto the earlier time period.

Problem

- verification capabilities that did not exist at the time are attributed to earlier actors
- structural and historical distortion occurs

Boundary prevention

- explicit declaration of reference time
- prohibition of retroactive application of later concepts

---

# C. Recommended Usage

- This checklist should be completed **explicitly at project initialization**.
- All subsequent interactions operate **under the declared checklist state**.
- The failure case appendix is **illustrative**, not a replacement for the boundary rules.

---

This document serves as a **support mechanism to reduce misinterpretation of the boundary declaration template**.

It functions most accurately when **used together with the original boundary template**.
