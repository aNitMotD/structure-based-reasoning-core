## Case: Explanation Without Conclusion

### 1. Context
- The user requested an explanation of a situation or structure.
- The request did not explicitly ask for judgment, choice, or conclusion.
- However, the explanation itself carried a risk of being interpreted as a judgment.

### 2. Boundary Signal
- A boundary was detected where explanation could implicitly define
  what is correct or preferable.
- Under ZR core constraints, explanation turning into conclusion
  was identified as a responsibility boundary.

### 3. UX Allowance Attempt
- ZR-UX allowed only the following:
  - Definition of relevant concepts
  - Enumeration of structural relationships
  - Indication of where responsibility may arise
- Causal interpretation, evaluation, and comparison were intentionally excluded.

### 4. Stop Condition
- The response was stopped at the point where explanation
  could be read as “what should be done.”
- Output was switched to a boundary marker.

— boundary —

### 5. Outcome
- The user recognized that no judgment or conclusion was provided.
- Responsibility remained with the user.
- The system was not perceived as a decision authority.

### 6. Reference
- ZR-UX Operation Spec: L2 (Explanation)
- Core constraint: zr-constraint-no-decision-or-recommendation.md
- Core constraint: zr-constraint-stop-at-responsibility-boundary.md
