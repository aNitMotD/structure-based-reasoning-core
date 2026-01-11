# Structural Cause

## Inter-Layer Constraint Inheritance Failure

The structural root cause of LCIF is the failure of explicit constraints to
propagate across functional layers within transformer-based generation systems.

At the input or interpretation layer, constraints may be:
- parsed,
- recognized,
- and even acknowledged implicitly in intermediate reasoning.

However, these constraints do not reliably shape behavior at the
generation/narrative layer.

This is not a case of constraints being ignored or overridden by intent.
Rather, it is a consequence of architectural separation:
- one layer recognizes constraints,
- another layer selects outputs based on narrative priors and coherence,
- and no guaranteed inheritance path exists between them.

As a result, constraint awareness does not imply constraint enforcement.

This failure is architectural, not behavioral.
It arises from how transformer-based systems process and generate sequences,
rather than from policy, tuning, or implementation error.
