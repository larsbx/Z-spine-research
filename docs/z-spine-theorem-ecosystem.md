# The \(\mathbb Z\)-Spine theorem ecosystem

## 0. Standing data

Let \(G=(V,E)\) be finite, with a fixed orientation and incidence matrix
\[
B\in\mathbb Z^{V\times E}.
\]
Set
\[
\delta=B^\top,\qquad \partial=B,\qquad L=BB^\top.
\]

Define
\[
C:=\operatorname{im}(B^\top)\subseteq\mathbb Z^E,
\qquad
Z:=\ker(B)\subseteq\mathbb Z^E.
\]

A loop gives a zero column of \(B\), so loops do not affect \(L\), the critical group, or spanning-tree counts.

---

## 1. Lattice foundations

\[
\ker(B^\top)
=
\{f\in \mathbb Z^V: f\text{ constant on each component}\}
\cong
\mathbb Z^{c(G)}.
\]

Hence \(\operatorname{rk}C=|V|-c(G)\), while
\[
Z=\ker(B)\cong\mathbb Z^{\beta_1},
\qquad
\beta_1=|E|-|V|+c(G).
\]

For \(c=B^\top v\in C\) and \(z\in Z\),
\[
\langle c,z\rangle=\langle v,Bz\rangle=0.
\]
Therefore
\[
\mathbb Q^E=C_\mathbb Q\oplus Z_\mathbb Q,
\qquad
C\cap Z=0.
\]

For every integer matrix \(A\), the kernel lattice is saturated:
\[
kx\in\ker A,\ k>0
\quad\Longrightarrow\quad
x\in\ker A.
\]

Define
\[
\mathcal B(G):=\mathbb Z^E/(C+Z).
\]
Because \(\operatorname{rk}C+\operatorname{rk}Z=|E|\), this quotient is finite. For connected \(G\),
\[
\mathcal B(G)=0
\iff
G\text{ is a tree}.
\]

---

## 2. Orientation independence

If \(B'=BD\) for a diagonal sign matrix \(D\), then
\[
C'=D^\top C,\qquad Z'=D^\top Z.
\]
Hence \(\mathcal B(G)\) is independent of orientation up to the natural induced isomorphism.

---

## 3. Matrix–Tree theorem internally

Assume \(G\) connected, \(n=|V|\), and delete one row from \(B\) to obtain
\[
\widetilde B\in\mathbb Z^{(n-1)\times E}.
\]
Then
\[
L_0=\widetilde B\widetilde B^\top.
\]

For \(S\subseteq E\) with \(|S|=n-1\),
\[
\det(\widetilde B_S)=
\begin{cases}
\pm1,&S\text{ a spanning tree},\\
0,&\text{otherwise}.
\end{cases}
\]

Cauchy–Binet gives
\[
\boxed{\det L_0=\#\{\text{spanning trees of }G\}.}
\]

---

## 4. Critical group and bridge theorem

For connected \(G\), define
\[
K(G):=
\operatorname{tors}\bigl(\mathbb Z^V/\operatorname{im}L\bigr).
\]

Equivalently,
\[
K(G)\cong
\mathbb Z^{V\setminus\{r\}}/\operatorname{im}L_0.
\]

Also
\[
\operatorname{im}B
=
\mathbb Z^V_0
=
\{w\in\mathbb Z^V:\sum_v w_v=0\}.
\]

The restriction \(B|_C:C\to\operatorname{im}L\) is an isomorphism. From
\[
0\to Z\to\mathbb Z^E\xrightarrow{B}\operatorname{im}B\to0
\]
we obtain
\[
\mathcal B(G)\cong \operatorname{im}B/\operatorname{im}L.
\]

Because
\[
\mathbb Z^V/\operatorname{im}B\cong\mathbb Z,
\]
the free summand splits off, giving
\[
\boxed{\mathcal B(G)\cong K(G).}
\]

Thus
\[
\boxed{|K(G)|=|\mathcal B(G)|=\det L_0=\tau(G).}
\]

---

## 5. Smith normal form and \(p\)-torsion

If
\[
PL_0Q=\operatorname{diag}(d_1,\ldots,d_{n-1})
\]
is the Smith normal form, then
\[
K(G)\cong\bigoplus_{d_i>1}\mathbb Z/d_i\mathbb Z.
\]

For prime \(p\),
\[
\boxed{
\dim_{\mathbb F_p}K(G)[p]
=
(n-1)-\operatorname{rk}_{\mathbb F_p}(L_0\bmod p).
}
\]

---

## 6. Discriminant presentations

For a lattice \(\Lambda\subseteq\mathbb Z^n\), full rank in its real span \(\Lambda_\mathbb R\), define
\[
\Lambda^*
=
\{x\in\Lambda_\mathbb R:
\langle x,\lambda\rangle\in\mathbb Z
\text{ for all }\lambda\in\Lambda\},
\]
and
\[
\operatorname{disc}(\Lambda)=\Lambda^*/\Lambda.
\]

For connected \(G\),
\[
\boxed{
\mathcal B(G)
\cong
K(G)
\cong
\operatorname{disc}(C)
\cong
\operatorname{disc}(Z).
}
\]

The cut-lattice identification uses orthogonal projection
\[
\mathbb Q^E\to C_\mathbb Q
\]
along \(Z_\mathbb Q\); saturation identifies the kernel with \(C+Z\), while the cut-lattice Gram determinant is \(\det L_0\).

---

## 7. Total unimodularity and cohomology

The oriented incidence matrix \(B\) is totally unimodular, and a spanning forest supplies a full-rank minor of determinant \(\pm1\). Therefore
\[
\boxed{
H^1(G;\mathbb Z)
=
\operatorname{coker}(B^\top)
\cong
\mathbb Z^{\beta_1}.
}
\]

The torsion in the Z-spine does not live in ordinary graph cohomology; it arises from the Laplacian cokernel.

---

## 8. Colorings as tensions over \(\mathbb Z/k\)

Let \(R_k:=\mathbb Z/k\mathbb Z\), and define
\[
T(G;R_k):=\operatorname{im}(B^\top\otimes R_k).
\]

There is a canonical bijection
\[
\frac{
\{\text{proper }k\text{-colorings }V\to R_k\}
}{
\text{componentwise constants}
}
\cong
\{\text{nowhere-zero }k\text{-tensions}\}.
\]

Therefore
\[
\boxed{
\chi_G(k)
=
k^{c(G)}
\#\{\text{nowhere-zero }k\text{-tensions}\}.
}
\]

---

## 9. Chromatic polynomial

For non-loop edge \(e\),
\[
\chi_G(k)=\chi_{G-e}(k)-\chi_{G/e}(k).
\]
For a loop,
\[
\chi_G(k)=0.
\]

Induction on \(|E|\), from \(\chi_{E_n}(k)=k^n\), proves the existence and uniqueness of
\[
\chi_G\in\mathbb Z[k]
\]
whose positive-integer evaluations count proper colorings.

---

## 10. Tutte polynomial

Define
\[
T_G(x,y)
=
\sum_{A\subseteq E}
(x-1)^{r(E)-r(A)}
(y-1)^{|A|-r(A)}.
\]

Its recurrence is:

- loop: \(T_G=yT_{G-e}\);
- bridge: \(T_G=xT_{G/e}\);
- ordinary edge: \(T_G=T_{G-e}+T_{G/e}\).

Specializations:
\[
\boxed{
\chi_G(k)
=
(-1)^{|V|-c(G)}
k^{c(G)}
T_G(1-k,0),
}
\]
and
\[
\boxed{
F_G(k)
=
(-1)^{|E|-|V|+c(G)}
T_G(0,1-k).
}
\]

---

## 11. Bicycle spaces

For prime \(p\), set
\[
B_p=B\otimes\mathbb F_p,
\qquad
L_p=B_pB_p^\top.
\]

Define
\[
\operatorname{Bic}_p(G)
=
\operatorname{im}(B_p^\top)\cap\ker(B_p).
\]

Then
\[
\boxed{
\dim_{\mathbb F_p}\operatorname{Bic}_p(G)
=
\operatorname{rk}(B_p)-\operatorname{rk}(L_p).
}
\]

For connected graphs,
\[
\operatorname{rk}(L_p)=\operatorname{rk}(L_0\bmod p).
\]

---

## 12. Regular matroids

Let \(M\) be a rank-\(r\) regular matroid with full-row-rank TU representation
\[
A\in\mathbb Z^{r\times E}.
\]

Define
\[
C(M)=\operatorname{im}(A^\top),\qquad
Z(M)=\ker(A),\qquad
\mathcal B(M)=\mathbb Z^E/(C(M)+Z(M)).
\]

Since \(A\) contains an \(r\times r\) minor of determinant \(\pm1\),
\[
\operatorname{im}(A)=\mathbb Z^r.
\]

Hence
\[
\boxed{
\mathcal B(M)\cong\operatorname{coker}(AA^\top).
}
\]

By Cauchy–Binet,
\[
\det(AA^\top)
=
\sum_{|B|=r}\det(A_B)^2.
\]

TU implies each term is \(0\) or \(1\), so
\[
\boxed{
\det(AA^\top)=\#\{\text{bases of }M\}.
}
\]

---

## 13. Arithmetic-matroid boundary

For a full-rank basis \(B\) in an integer representation,
\[
m(B)
=
[\operatorname{span}_\mathbb R(A_B)\cap\mathbb Z^r:
\operatorname{span}_\mathbb Z(A_B)]
=
|\det(A_B)|.
\]

The square \(\det(A_B)^2\) belongs naturally to Cauchy–Binet identities, not as an interchangeable arithmetic-matroid multiplicity.

Regular matroids are the multiplicity-free case.

---

## 14. Sandpile group

For connected loopless \(G\) with sink \(s\),
\[
\operatorname{SP}(G,s)
=
\mathbb Z^{V\setminus\{s\}}/\operatorname{im}L_0
\cong
K(G).
\]

The theorem that recurrent configurations give canonical dynamical representatives is standard input and is not reproved here.

---

## 15. Planar duality

For connected planar \(G\) with dual \(G^*\),
\[
C_G\leftrightarrow Z_{G^*},
\qquad
Z_G\leftrightarrow C_{G^*}.
\]

Hence
\[
\boxed{
K(G)\cong K(G^*),
}
\qquad
\tau(G)=\tau(G^*).
\]

---

## 16. Graph Jacobian versus tropical Jacobian

The finite group
\[
K(G)\cong\operatorname{Pic}^0(G)
\]
is the **combinatorial graph Jacobian**.

It is not literally the same object as the Jacobian of a metric graph / tropical curve, which is a real torus of dimension \(\beta_1\). The theories are related through divisor theory, graph models, refinement, and specialization.

---

## 17. Research program toward coloring problems

The Z-spine does not assert that \(K(G)\) determines colorability.

The proposed mechanism is
\[
\text{minimal coloring counterexample}
\to
\text{mod-}k\text{ tension constraints}
\to
\text{integral cut/cycle data}
\to
\text{torsion + bicycle + Tutte constraints}
\to
\text{minor-incompatible structure}.
\]

### Primary target: ordinary Hadwiger-type problems

For minor-minimal non-\((t-1)\)-colorable graphs, constrain:

- \(K(G)\);
- \(K(G)[p]\);
- \(\operatorname{Bic}_p(G)\);
- modular tension supports;
- chromatic/Tutte deletion–contraction profiles.

The first target theorem should classify arithmetic signatures that every minimal counterexample must satisfy.

### Negative control: Odd Hadwiger

Odd Hadwiger is false and is retained as a stress test: a useful invariant package should not falsely force its conclusion.

### Secondary targets

Reed, list coloring, and total coloring require local information absent from the present global lattice model. Likely extensions include twisted coefficients, local tension systems, or Kempe-dynamics modules.

---

## 18. Remaining scope limits

The internal spine is closed through:

- cut/cycle lattices;
- Matrix–Tree;
- critical-group bridge;
- Smith normal form and \(p\)-torsion;
- discriminant presentations;
- chromatic polynomial;
- Tutte specializations;
- bicycle ranks;
- regular-matroid extension;
- planar duality.

Still external or abbreviated:

1. recurrent-configuration / Dhar theory;
2. Baker–Norine / tropical divisor theory;
3. full representation-independence for regular-matroid critical groups beyond explicit TU-equivalence moves;
4. full arithmetic-matroid axiomatics;
5. detailed bit-complexity proofs;
6. new theorems connecting Z-spine invariants to contraction-critical coloring structure.
