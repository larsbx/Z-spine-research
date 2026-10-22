# Z-spine research

This repository develops the **\(\mathbb Z\)-spine** viewpoint for graph coloring and related combinatorics.

The organizing principle is:

- over \(\mathbb Q\), cut and cycle spaces split cleanly;
- over \(\mathbb Z\), the split fails by a finite lattice defect;
- over \(\mathbb Z/k\), finite coloring and tension obstructions appear.

The project packages these regimes through incidence matrices, cut/cycle lattices, critical groups, discriminant groups, chromatic and Tutte polynomials, bicycle spaces, and regular matroids.

## Canonical documents

- `docs/z-spine-theorem-ecosystem.md` — current theorem system.
- `docs/audit-2026-10-22.md` — audit of the originating thread and corrected claims.
- `docs/hadwiger-roadmap.md` — research program for minor-based coloring applications.

## Research discipline

Claims should be marked as one of:

- **proved internally**,
- **standard theorem used as input**,
- **computationally verified**,
- **conjectural / research direction**.

The project does **not** assume that critical groups determine colorability. The research question is whether combined arithmetic data can constrain minimal counterexamples to major coloring conjectures.
