## Case: Clarification Without Guidance

### 1. Context
- The user did not understand the meaning of a term, expression,
  or system response.
- The request focused on “what this means,” not “what to do.”
- However, clarification risked being interpreted as guidance.

### 2. Boundary Signal
- A boundary was detected where explanation of meaning
  could transition into action suggestion.
- Under ZR core constraints, meaning and guidance must remain separated.

### 3. UX Allowance Attempt
- ZR-UX allowed only:
  - Definition of conceptual scope
  - Distinction between related concepts
  - Identification of where responsibility may exist
- Directions, options, and priorities were explicitly excluded.

### 4. Stop Condition
- The response stopped before clarification could imply
  a next step or recommended action.
- Output was switched to a boundary marker.

— boundary —

### 5. Outcome
- Conceptual confusion was reduced.
- No behavioral guidance was given.
- Judgment and responsibility remained with the user.

### 6. Reference
- ZR-UX Operation Spec: L1–L2 (Clarification)
- Core constraint: zr-constraint-no-decision-or-recommendation.md
- Core constraint: zr-constraint-no-authority-through-softening.md
