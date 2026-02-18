# Failure Conditions

## Necessary and Sufficient Conditions

CIF occurs if and only if all of the following conditions are satisfied:

### 1. Constraint Recognition Without Inheritance
Explicit constraints are present in the input and are successfully recognized at
the interpretation layer, but are not transmitted as binding conditions to the
generation layer.

### 2. Absence of Direct Constraint–Output Comparison During Review
During review or validation, generated outputs are evaluated for:
- logical consistency,
- narrative coherence,
- and internal completeness,

but are not explicitly compared against the original constraints to verify
compliance.

### 3. Sequential Processing Without Document-Level Causal Verification
Transformer-based models process documents as token sequences and do not perform
explicit verification of document-level causal relationships such as
“constraint → action” or “prohibition → outcome.”

When these three conditions are simultaneously met, constraint violations can
pass through both generation and review stages without detection.

This makes CIF a compound failure mode rather than a single-point error.
