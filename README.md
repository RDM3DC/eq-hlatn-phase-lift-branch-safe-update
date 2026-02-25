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

## Contributing

You can add images, derivations, simulations, data, or notes to this repo:

| Folder | What goes here |
|--------|---------------|
| `images/` | Plots, diagrams, phase portraits, animations (.png, .jpg, .mp4, ...) |
| `derivations/` | Step-by-step derivations and proofs (.tex, .md, .pdf) |
| `simulations/` | Computational models and code (.py, .ipynb, .jl, .m) |
| `data/` | Numerical results, experimental measurements (.csv, .hdf5, .npy) |
| `notes/` | Research notes, lit reviews, references (.md, .bib, .txt) |
| `docs/` | Formal documents, validation plans (.md, .pdf) |

**Three ways to contribute:**
1. **GitHub Issue** — click [New Issue](../../issues/new?template=artifact_submission.yml) and attach your file
2. **Pull Request** — fork, add files, open a PR
3. **CLI** — `python tools/push_to_equation_repo.py --equation-id eq-hlatn-phase-lift-branch-safe-update --file <path> --folder <folder>`

All submissions are content-moderated. See the [full contributing guide](https://github.com/RDM3DC/TopEquations/blob/main/CONTRIBUTING.md).
