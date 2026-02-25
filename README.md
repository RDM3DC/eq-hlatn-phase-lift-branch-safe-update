# HLATN Phase-Lift Branch-Safe Update

**ID:** `eq-hlatn-phase-lift-branch-safe-update`  
**Tier:** derived  
**Score:** 67  
**Units:** OK  
**Theory:** PASS-WITH-ASSUMPTIONS  

## Equation

$$
\theta_{R,e}^{(k)} = \theta_{R,e}^{(k-1)} + \mathrm{clip}\!\Big(\mathrm{wrapTo}_{\pi}(\phi_e - \theta_{R,e}),\; -\pi_a,\; +\pi_a\Big)
$$

## Description

Resolved-phase update rule with wrap-to-pi and adaptive clipping. Prevents uncontrolled branch jumps by bounding per-step angular movement to the entropy-regulated ruler pi_a.

## Assumptions

- Raw phase phi_e = arg(V_i - V_j) is well-defined
- Adaptive angular bound pi_a > 0 limits per-step rotation
- wrapTo_pi maps angular differences to (-pi, pi]
- Clipping preserves continuity of resolved phase trajectory

## Repository Structure

```
images/       # Visualizations, plots, diagrams
derivations/  # Step-by-step derivations and proofs
simulations/  # Computational models and code
data/         # Numerical data, experimental results
notes/        # Research notes and references
```

## Links

- [TopEquations Leaderboard](https://rdm3dc.github.io/TopEquations/leaderboard.html)
- [TopEquations Main Repo](https://github.com/RDM3DC/TopEquations)
- [Certificates](https://rdm3dc.github.io/TopEquations/certificates.html)

---
*Part of the [TopEquations](https://github.com/RDM3DC/TopEquations) project.*
