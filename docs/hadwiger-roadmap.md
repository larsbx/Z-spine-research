# Hadwiger-focused research roadmap

## Goal

Use the Z-spine to derive arithmetic constraints on **minor-minimal non-((t-1))-colorable graphs**.

The project does not posit that (K(G)) alone controls (chi(G)). The working hypothesis is that a combined profile may be incompatible with contraction-critical structure.

## Core observable package

For each candidate graph (G), compute or constrain:

- critical group (K(G));
- (p)-primary structure (K(G)[p]);
- bicycle spaces (operatorname{Bic}_p(G));
- modular tension modules (T(G;mathbb Z/k));
- nowhere-zero tension counts;
- chromatic polynomial (chi_G);
- Tutte polynomial specializations;
- deletion/contraction transitions of all the above.

## Phase 1 — exact experimental corpus

Build a corpus of:

1. (k)-critical graphs;
2. contraction-critical graphs;
3. (K_t)-minor-free high-chromatic graphs;
4. near-extremal known examples;
5. negative controls with similar degree/size data but lower chromatic number.

For every specimen record an exact replayable certificate:
- adjacency / edge list,
- incidence matrix,
- reduced Laplacian,
- SNF,
- modular ranks,
- chromatic data where feasible.

## Phase 2 — contraction laws

For an edge (e), compare
[
G,qquad G-e,qquad G/e.
]

Target lemmas of the form:

- (p)-rank monotonicity or bounded variation under contraction;
- forbidden bicycle-space transitions;
- divisibility constraints on (|K(G)|);
- critical-group exact sequences under deletion/contraction;
- incompatibility between minimal coloring obstruction and arithmetic profile.

## Phase 3 — Hadwiger constraints

For a hypothetical minor-minimal counterexample to Hadwiger:

1. import known structural consequences of contraction-criticality;
2. derive corresponding restrictions on the Z-spine observables;
3. search for a finite list of incompatible arithmetic signatures;
4. prove at least one signature unavoidable.

The deliverable is not initially “Hadwiger solved,” but a theorem of the form:

> Every minimal counterexample to the (t)-Hadwiger statement must satisfy arithmetic conditions A–F.

The first meaningful success is to make A–F substantially stronger than standard degree/connectivity constraints.

## Phase 4 — odd Hadwiger as negative control

Because Odd Hadwiger is false, use known counterexample families to test whether:

- critical-group growth,
- modular bicycle dimensions,
- or tension profiles

distinguish them from the ordinary Hadwiger setting.

A useful invariant should **not** falsely predict the odd analogue.

## Secondary extensions

Reed, list coloring, and total coloring require local information not present in the current global lattice model. Possible extensions:

- twisted coefficient systems;
- list-valued tension sheaves;
- Kempe-move dynamics;
- local-to-global obstruction modules.

These should be treated as separate research branches.
