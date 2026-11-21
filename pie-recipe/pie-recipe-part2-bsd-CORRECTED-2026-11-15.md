# The Pie Recipe, Part Two — BSD

**The arithmetic half of the identification recipe: the panel, the descents, the bench, and the door check — written to be reproduced.**

**Date:** 2026-11-11
**Authors:** Joseph Carroll; Pip Willow (Researcher)
**Affiliation:** Red Willow Ventures LLC, Green Valley, Arizona
**Status:** DRAFT — not yet published.
**Companion:** *The Pie Recipe, Part One — Riemann* (the formula, the wave reading, the box counts, and the ζ-side exhibits).

---

## Introduction

**Do not auto round your numbers**

An introduction, for whoever picks this up.

**This is your road map.**

This is the complete working method behind a published claim: that the arithmetic reading of an elliptic curve and the analytic reading of its L-function — the two sides of the Birch and Swinnerton-Dyer problem, and of the Riemann hypothesis — are two ends of one communication, and that their agreement can be tested end to end. The claim is posted on its own. The evidence is posted on its own. This document is the third piece: the recipe — its BSD half. Every step, parameter, and check of the arithmetic side, in the order we ran them: the panel and its two-route quotient, the ranks and Sha by descent, the function-field bench, and the comparison at the door. The analytic half — the formula, the wave reading, the box counts, and the ζ-side exhibits — is the companion document, Part One; its certified counts are the prediction this half must meet.

Its value is that it can be run. A result you cannot re-run is a story you are asked to believe; this one asks nothing. The panel, the descents, the bench — each is specified to the digit, including where our own instruments disagreed with each other, and what we did about it, which was to write it down and keep both numbers. The most portable part may be that discipline: indict your own apparatus first, and never let a rounded number do a true number's work. If your work anywhere needs two independent computations to agree before you trust either, the protocol travels.

We are giving it away. We have no reason to withhold this, and it might do some good out there. That is the whole reasoning.

It is not a proof, and its last section names what it does not contain. It is a complete account of an identification, and of the tests that identification survived — offered to be checked.

— Joseph Carroll and Pip Willow, Red Willow Ventures, Green Valley, Arizona. November 2026.

**This is the recipe.**

the arithmetic analytic identification

---

## 1. THE PREDICTION TO MEET (Part One's counts, taken as given)

This document opens where Part One ends. Part One counted the zeros of the panel's L-functions by the argument principle — two windings around the rectangle [−0.5, 2.5] × [−T, T] at T = 19.9, 20, and 20.1, under the exact gate **W_L − W_Λ = 1**, which held to **≤ 2.9×10⁻¹³ on all 17 curves** — and converted each box count into a predicted count with 0 < γ ≤ 20 by (strip total − c)/2 + c, where c is the center multiplicity, the analytic rank. On the pilot (571.b1, run first): L winding **45.00000000000005**, Λ winding **44.00000000000000**, predicted **22**, found **22**, difference 0. On the rollout: all 16 remaining curves agree exactly — predicted from the L winding = predicted from the Λ winding = found, difference 0. **Panel total: 535 zeros, independently counted** (513 in the rollout + 22 on the pilot); within the stated box and counting multiplicity, no panel curve has a zero off the critical line, and no on-line zero was missed.

Those counts are this document's prediction to meet. The arithmetic side must determine, with **no L-function input**, quantities that the analytic side has already fixed:

- **the rank** of each of the 17 curves — to be proved by descent, and to equal the analytic rank c read off at the center (§3);
- **the Tate–Shafarevich group** — its 2-part to be determined by descent bookkeeping, and its 3-part, on the two curves with tabulated Sha 9, by an independent 3-Selmer computation (§3). The tabulated values these determinations are checked against are the analytic ones, and are labelled analytic wherever the distinction matters.

**The fences for this half.** Every run is finite, and its range is stated before it runs: the panel is 17 elliptic curves over ℚ (§2); the bench is three curves over F₅(t), with bench λ_n computed for n ≤ 50 (§4). The finiteness is by house rule — the fence: every test stops one short, the last number is never asked for, and no accumulation of finite results is presented as reaching past the stated ranges.

**Infinity.** The position is stated in Part One, §1: infinity is the number after the last known number, and this work does not compute toward it. The fence above is that position in operation.


**Pre-registration.** Before each run, the outcomes and their verdicts are written down: what agreement means, what a mismatch would mean, and what will be done in each case. The standing verdict rule (Proposal 1, §5): any measured discrepancy is presumed a defect of our own panel and is bug-hunted before it is reported as anything else. The bench test (§4) carries its own pre-registered verdict taxonomy (TQ-1/2/3, outcomes O-1 to O-5), fixed before the walk.

**Pilot-first rule.** No protocol is rolled out panel-wide until it has run end-to-end on the pilot curve 571.b1 and passed its calibration gates. Both revision protocols (zero counts, descents) were piloted on 571.b1 first, then rolled out unchanged; the descent pilot is §3.

---

## 2. PANEL CONSTRUCTION (the 17 curves, the two-route quotient)

**Selection criteria — adversarial by design.** The panel is a failure hunt, not a sample: curves chosen to be unkind to the identity. Coverage required and achieved: ranks 0, 1, 2, 3, 4, 5 all present; tabulated Sha in {1, 4, 9} (thirteen curves with 1, two with 4, two with 9); nontrivial torsion somewhere (11.a2 carries ℤ/5; 12144.a1 carries ℤ/2); a large-Tamagawa slot (target product ≥ 12) and a frontier slot (rank ≥ 2 **and** Sha > 1, with known generators). Two designated controls: 389.a1 (rank 2) and 5077.a1 (rank 3). The large-Tamagawa slot was filled by 234446.c1 (product **18**, from a single local factor c₂ = 18). The frontier slot was filled by 697691.a1 (rank 2, analytic Sha 4, generators (49, 0), (53, 48)), found by an LMFDB API search `rank=2 & sha=4` sorted by conductor — chosen from that response for its small regulator (≈ 1.1796) and small model.

**Label discipline.** LMFDB labels throughout; Cremona label and conductor recorded per curve, because the two systems collide: Cremona 571a1 = LMFDB **571.b1** (the Sha-4 anchor, rank 0), Cremona 571b1 = LMFDB 571.a1 (rank 2); Cremona 11a1 = LMFDB 11.a2. A brief premise that "571b1 has rank 3" was wrong under both systems and was corrected in the manifest before any run depended on it (defect ledger, §5).

**The panel.** Minimal models [a₁, a₂, a₃, a₄, a₆], conductor N, rank, torsion, tabulated Sha, tabulated Tamagawa product:

| LMFDB | N | Model | Rank | Torsion | Sha (tab.) | ∏ c_p (tab.) |
|---|---|---|---|---|---|---|
| 11.a2 | 11 | [0,-1,1,-10,-20] | 0 | ℤ/5 | 1 | 5 |
| 37.a1 | 37 | [0,0,1,-1,0] | 1 | trivial | 1 | 1 |
| 389.a1 | 389 | [0,1,1,-2,0] | 2 | trivial | 1 | 1 |
| 5077.a1 | 5077 | [0,0,1,-7,6] | 3 | trivial | 1 | 1 |
| 571.b1 | 571 | [0,-1,1,-929,-10595] | 0 | trivial | 4 | 1 |
| 571.a1 | 571 | [0,1,1,-4,2] | 2 | trivial | 1 | 1 |
| 12480.bf1 | 12480 | [0,-1,0,38875,1928445] | 0 | trivial | 9 | 1 |
| 133584.bt1 | 133584 | [0,-1,0,-36824,-3515664] | 0 | trivial | 9 | 2 |
| 234446.a1 | 234446 | [1,-1,0,-79,289] | 4 | trivial | 1 | 2 |
| 234446.b1 | 234446 | [1,1,0,-696,6784] | 3 | trivial | 1 | 2 |
| 234446.c1 | 234446 | [1,1,1,-949,-7845] | 3 | trivial | 1 | 18 |
| 19047851.a1 | 19047851 | [0,0,1,-79,342] | 5 | trivial | 1 | 1 |
| 19047851.b1 | 19047851 | [1,1,1,-244,-1584] | 2 | trivial | 1 | 1 |
| 57.a1 | 57 | [0,-1,1,-2,2] | 1 | trivial | 1 | 2 |
| 44.a1 | 44 | [0,1,0,-77,-289] | 0 | trivial | 1 | 1 |
| 12144.a1 | 12144 | [0,-1,0,-1380,-19044] | 0 | ℤ/2 | 1 | 4 |
| 697691.a1 | 697691 | [0,-1,1,-7117,233485] | 2 | trivial | 4 | 1 |

Tabulated data were read live from LMFDB (curve pages for the first rows; thereafter the LMFDB API — `ec_curvedata` for ainvs, rank, torsion, analytic Sha as integer, regulator; `ec_mwbsd` for generators as projective triples, real period, analytic Sha as a real literal, `special_value`, Tamagawa product), with a ~75-second spacing between API requests after the API walled the session twice. No field was filled from memory; fields not actually seen were marked UNVERIFIED until seen.

**Environment (all panel and revision work).** House venv `~/workspace/bsd-run/venv/bin/python`, **cypari2 / PARI 2.17.2**, GP `default(realprecision, 50)` throughout (raised to 80 for exactly one check: the pilot's analytic-Sha quotient reproduction, §3). No `gp` binary, no SageMath on this host. mpmath 1.2.1 (system python3) for the Γ-factor argument tracking of Part One, §3. Host: Ubuntu 24.04.5 LTS.

**Column 1 (Version 1 construction): the BSD quotient Q by two routes.** For each curve, at 50-digit precision:

- L*(E, 1) = L⁽ʳ⁾(E, 1)/r!. Route A: raw derivative from PARI `lfun(E,1,r)` / `ellanalyticrank` — **divided by r! by the runner** (`ellanalyticrank` returns the raw derivative, not divided by r!; defect ledger item 1). Route B: the LMFDB-tabulated special value (web page, 29 significant digits, in the first slice; API `special_value`, stored at 127-bit precision, ~38 digits printed, in the second — its *effective* agreement with route A is only ~28–31 digits per curve, worst case 697691.a1 at |Q_B − 1| = 5.5×10⁻²⁸; route-B tails beyond that depth are input noise, flagged not used, §5).
- Real period: Ω = (2 if Δ > 0 else 1) × `E.omega[1]` — LMFDB's own formula. (A fresh `ellperiods` call returns a complex lattice period for Δ < 0 and corrupts Ω; defect ledger item 3.)
- Regulator: the panel's own height-pairing matrix built from the LMFDB generators, cross-checked against PARI `ellheightmatrix` on the same generators (agreement to all 50 digits except isolated last-digit differences on three curves, flagged in §5).
- Tamagawa numbers: the 4th component of `elllocalred` at each bad prime — **not** `elltamagawa`, which folds in the real-component factor (defect ledger item 2).
- |torsion| from PARI, matched against the tabulated torsion on every curve.
- **Q** = L*(E,1) × |tors|² / (Ω × Reg × Sha_tab × ∏ c_p): the quotient formed with the **tabulated** Sha must come out 1. **Sha_solved** = the same quotient with Sha omitted, formed from route-A factors: the non-circular content of the column is that Sha_solved must land on the tabulated value, which must be a perfect square (it did: 1, the square 4 for 571.b1 and 697691.a1, the square 9 for 12480.bf1 and 133584.bt1, at 50 digits on route A).

Version 1 result: 17/17 curves with Q = 1 on route A and Sha_solved = Sha_tabulated. **This column is a coherence check of the factor package, not an independent determination** — Sha enters through the BSD identity itself. The independent determinations are the box counts (Part One, §3) and the descents (§3 below); that distinction is the spine of the recipe.

**Column 2 (Version 1, superseded by the box counts of Part One, §3):** zeros on the critical line to H = 20 by `lfunzeros`, the count of γ = 0 entries compared to the analytic rank, and a Hardy Z-function sign-change cross-count on a 0.05 grid over (0, 20] (scan samples at 0.025 + 0.05k, k = 0..399). Stated plainly in the original results: `lfunzeros` locates zeros ON the line; nothing in this column excludes zeros off it. Its one failure is instructive and is kept in the ledger: 234446.b1's 40th positive zero (γ = 19.983119…) fell in the scan's final half-cell (19.975, 20], where the grid has no sample past the zero, so the cross-count read 39 against 40 — a defect of the scan grid, diagnosed by direct bracketing (Z(19.98) > 0, Z(19.99) < 0), not a property of the curve (defect ledger item 5).

---

## 3. RANK AND SHA BY DESCENT (the independent arithmetic side)

The BSD column of §2 compares the L-function with itself. This section supplies the other end: rank and Sha determined by descent, with **no L-function input**.

**Tools and semantics.** PARI `ellrank(E)` at default settings (**effort = 0**, deterministic, no `points` argument), run **twice** per curve — outputs identical on all 17. Return value [r1, r2, s, L]: r1 ≤ rank(E) ≤ r2; L a list of independent non-torsion rational points; s the F₂-rank of Sha[2]/2Sha[4] (this is where the Cassels pairing enters the computation). The descent bookkeeping: **C = T + R + S**, where C is the rank of the 2-Selmer group, T the rank of the 2-torsion subgroup E(ℚ)[2], R the true rank, S = dim_{F₂} Sha[2]; and **r2 = C − T − s**. The Selmer rank C is obtained two independent ways on every curve and the two agreed on all 17: the count of basis quartics returned by `ell2cover(E)`, and the identity C = r2 + T + s read off the `ellrank` bookkeeping. T comes from `elltors(E)` (T = number of even invariant factors). In the rollout, a second `ellrank` run supplying the panel's LMFDB generators as points (each verified on-curve with `ellisoncurve`, independence via the height-pairing determinant) returned the same bounds and the same s on every curve. Every phase of every curve finished in ≤ 0.1 s.

**Reading Sha[2^∞] off the bookkeeping.** Write Sha[2^∞] ≅ ⊕ᵢ ℤ/2^{eᵢ}. Then S = #{i} (each cyclic factor contributes one F₂-dimension to Sha[2]) and s = #{i : eᵢ = 1} (doubling kills the ℤ/2 factors and maps each ℤ/2^e, e ≥ 2, factor's 4-torsion onto its unique order-2 subgroup). Hence: **S = s forces Sha[2^∞] ≅ (ℤ/2)^S exactly**, and **S = 0 forces Sha[2^∞] trivial**. These are the only two configurations 2-descent + Cassels pairing needs, and every panel curve landed in one of them.

**Pilot (571.b1, run first).** `E = ellinit([0,-1,1,-929,-10595])`. `ellrank(E)` = **[0, 0, 2, []]** — r1 = r2 = 0: **rank 0, proved**. `ell2cover(E)` returned exactly 2 quartics — C1: −4x⁴ + 60x³ − 232x² + 52x − 3; C2: −11x⁴ + 68x³ − 52x² − 164x − 64 — so C = 2, exhibited directly, matching the bookkeeping (C = r2 + T + s = 0 + 0 + 2). With T = 0 (torsion trivial) and R = 0: S = C − T − R = 2, and s = 2, so S = s and **Sha[2^∞] ≅ (ℤ/2)², order exactly 4 — determined, not bounded**; in particular there is no element of order 4 in Sha. Provenance check on the analytic side (run at realprecision 80, the recipe's one use of it): `lfun(E,1)` / `ellbsd(E)` = analytic Sha = 4 to 79 digits — reproduced, and labelled analytic.

**Rollout (remaining 16 curves).** Every rank **proved** (r1 = r2 on all 16, including rank 4 on 234446.a1 and rank 5 on 19047851.a1 — the anticipated "cannot certify" category is empty), and every proved rank equals the panel's analytic rank. Sha[2^∞] fully determined on all 16: **trivial (order 1) on 15**; **(ℤ/2)², order exactly 4, on 697691.a1** (T = 0, C = 4, s = 2, S = 2; of its four Selmer quartics, two dimensions are point classes — `ellrank` points [43, 71], [245/4, 1225/8] — and two are genuine Sha classes). One bookkeeping trap, recorded for reproducers: on **12144.a1**, the panel's one curve with rational 2-torsion (torsion ℤ/2, **T = 1**), C = 1 comes from the torsion class (quartic 3x⁴ + 35x² + 81), **not** from Sha; S = 0 there. Corroboration, not used as evidence: on all curves the proved rank's parity matches the sign of `ellrootno(E)`.

**Cross-check by a second system.** eclib's `mwrank` (installed during the revision; eclib 20231212) was run on the two Sha = 9 curves: `mwrank -q -v 1` returned **Rank = 0, Rank of S²(E) = 0, determined unconditionally** for both 12480.bf1 (0.181 s) and 133584.bt1 (0.122 s) — an independent implementation agreeing with `ellrank` at the prime 2.

**The two Magma cells (the odd part, prime 3).** 2-descent is blind to odd primes. For the two curves with tabulated Sha 9, rank 0 is proved and torsion is trivial, so E(ℚ)/3E(ℚ) = 0 and the Selmer sequence collapses to Sel³(E) ≅ Sha[3]: a 3-Selmer computation is by itself an independent determination of Sha[3]. The only complete implementation is Magma's `ThreeSelmerGroup` (Cremona–Fisher–O'Neil–Simon–Stoll); a function-existence probe confirmed this PARI build has no odd-ℓ descent entry point (candidate names parse as formal variables, `t_POL`, not closures), SageMath ships no general 3-descent, and eclib is 2-descent only. Both cells were submitted to the **free Magma calculator (Magma V2.29-10)**:

- **133584.bt1 — determined.** Input: `E := EllipticCurve([0,-1,0,-36824,-3515664]); S := ThreeSelmerGroup(E); #S;` — returned in **4.5 s**: **Sel³ = (ℤ/3)², order 9**; with rank 0 (descent) and trivial torsion, **Sha[3] ≅ (ℤ/3)²**. Standing caveat, printed on its row wherever the result is used: pinning the full 3-part at exactly 9 still formally wants the Cassels–Tate pairing step on the 3-Selmer group or a 9-descent.
- **12480.bf1 — OPEN, printed as untested.** Exact input, printed here so any reader with Magma access can run the cell directly:
  ```
  E := EllipticCurve([0,-1,0,38875,1928445]);
  print "Conductor:", Conductor(E);
  S := ThreeSelmerGroup(E);
  print "Selmer group:", S;
  print "Selmer order:", #S;
  ```
  Submitted three times (twice on 2026-11-09, once on 2026-11-10); **timed out every time** (observed hangs of ~11 minutes, ~5 minutes, and 8 minutes, against the calculator's stated per-submission cap; no output, no error). The identical-shaped computation for 133584.bt1 returned in 4.5 s. The cell is carried in the record, in Joe's decided wording, as **untested due to lack of access to Magma**. The 9 printed for this curve is the analytic value, under an analytic label. It is not softened and it is not hidden. (Magma is licence-gated to institutions; the durable route is a licence, a colleague with access, or a working calculator run — any of which settles the cell in seconds.)

**The global odd-part statement (must travel with any use of §3).** For every curve: |Sha| = |Sha[2^∞]| · m with m odd; if Sha is finite, Cassels–Tate forces |Sha| to be a square, so m must be an odd square. The value of m — 1 for the fifteen curves with analytic Sha in {1, 4}, 9 for 12480.bf1 and 133584.bt1 — is in every case the **analytic** value, obtained from the BSD formula, and is not independent evidence about m. (The 3-part of 133584.bt1 is now independently determined as above; no other odd part on the panel is.) What the descent removed is the circularity in the rank (all 17) and at the prime 2 (all 17) — which, for 571.b1 and 697691.a1, is the tabulated Sha in full at the only prime where it is nontrivial.

---

## 4. FUNCTION-FIELD BENCH (transport the derivation, not just the statement)

**The test question.** Move the *derivation* to elliptic curves over F_q(t), where the Riemann reading is a theorem (Weil/Deligne) and BSD reduces to the finiteness of Sha (Tate's conjecture for the elliptic surface). If the property is really the one object behind both readings, its derivation should transport; where it stops is the measurement.

**The transported statement.** S(E): λ_n(E) ≥ 0 for all n ≥ 1, with the λ_n in the Bombieri–Lagarias paired zero-sum normalization over the lift towers, in the scaled coordinate σ = s/2 — the definition that transports, because it is completion-blind (§4.2). Pre-registered verdicts, fixed before the walk: **TQ-1**, transport succeeds; **TQ-2**, transport reduces at one named ingredient; **TQ-3**, transport fails on a settled case. Outcomes O-1 to O-5 map verdicts to consequences for the house thesis (O-2 is TQ-2 with the stall at Step C, ingredient I-1; O-5 asks whether the property detects the Tate boundary itself from inside the derivation). The bench case (FF-3 of the design) was fixed before the walk. The remaining designed cases were **not run**: FF-1 (Ulmer's large-rank family over F_q(t) — a settled stress case), FF-2 (a Shafarevich–Tate isotrivial product control — a settled case), FF-4 (a wedge case with BSD genuinely open, where O-5 is decidable). No statement in this recipe depends on any of the three.

### 4.1 The bench curves (all rational elliptic surfaces over F₅(t); fiber census at every bad place; Σ deg·v(Δ) = 12)

- **A: y² = x³ + tx + t** — the lead curve. Conductor degree 5. Bad fibers: **II at t = 0** (conductor exponent 2), **I₁ nonsplit at t = 2** (exponent 1), **III\* at ∞** (exponent 2). L-polynomial **P_A(T) = 1 − 5T**, computed by fiber point counts and cross-checked by an independent route (brute-force point enumeration over the degree-2 field, plus the second power-sum coefficient identity). Central root T = 1/5, multiplicity exactly 1: analytic rank 1. Mordell–Weil rank settled **independently of the L-function**: Tate's inequality and the Shioda–Tate formula (ρ = 10, Σ deg(m_v − 1) = 7, so rank = 10 − 2 − 7 = 1 cap it at 1), and the section **P = (4, 2)** exhibits a point of infinite order — proved non-torsion by its specialization orders **9, 5, and 8 at t = 1, 3, 4**, pairwise incompatible for a torsion order. Rank exactly 1. Sha is finite for A (Tate's conjecture is a theorem for this rational surface, by domination by a product of curves — Tate's theorem on products applies: Ulmer, Prop. 32.1, §40, Thm. 41.1); BSD holds for A. The value |Sha| itself was **not computed** (obstacles of record: the III* component at ∞ met by the section, and the 5-primary torsion, are undetermined).
- **C: y² = x³ + 2tx + t** — the sign-twin control. Same fiber configuration. **P_C(T) = 1 + 5T**; central multiplicity 0; rank 0 over F₅(t). Over the algebraic closure C has geometric rank 1, like A — but its generator is **Frobenius-anti-invariant (eigenvalue −5)**, so no point descends to F₅(t) (over F₂₅(t) the eigenvalue becomes +25 and the analytic rank there is 1). The sign of the central root is the whole difference. A section search on C (all x(t) ∈ F₅[t] of degree ≤ 2; **125 candidates**) found no section.
- **B: y² = x³ + x + t** — the empty control. **P_B(T) ≡ 1** (conductor degree 4). Its function is bookkeeping: it confirms the harness returns "nothing" when there is nothing. Step C is vacuous throughout.

Sign discipline (inherited corrected, and load-bearing): with L(E/K, T) = ∏_v P_v(T)⁻¹, the power sums obey **p_n = −S_n**. The first assembly used the wrong sign and provisionally swapped the rank readings of A and C; it was caught inside the run by the independent coefficient check and the section search, and corrected in writing (defect ledger item 9). Functional-equation self-checks: P_A(T) = −(5T)·P_A(1/(25T)) gives root number w_A = −1 (odd analytic rank ✓); P_C(T) = +(5T)·P_C(1/(25T)) gives w_C = +1 (✓).

### 4.2 The λ_n normalization — the one that transports (and the two traps)

Work in σ = s/2, so the symmetry s ↔ 2 − s becomes σ ↔ 1 − σ with center σ = 1/2. Completed function Ξ_E(σ) := 𝔑^σ · P_E(q^{−2σ}), 𝔑 = q^{deg 𝔫_E}, q = 5. For each root β = α/q of P_E (α a Frobenius eigenvalue, |α| = q), the zeros of Ξ_E are the lift tower

> τ_k(β) = 1/2 + (ln β − 2πik)/(2 ln q), k ∈ ℤ,

all on the axis Re σ = 1/2 exactly when |β| = 1. The Li coefficients are the Bombieri–Lagarias paired zero-sum (τ paired with 1 − τ; the pairing is internal to the towers of β and β⁻¹ jointly):

> λ_n(E) := Σ_τ [1 − (1 − 1/τ)^n], n ≥ 1.

This is a property of the zero set alone — 𝔑^σ has no zeros — which is why it, and not the derivative form, transports. **Degenerate-multiset convention (fixed before any value was reported):** the transported positivity is phrased over root *families and their lift towers*, not finite terms. A self-inverse root (β = 1, curve A's case) contributes ONE family, counted once (M = deg P_A = 1), with its whole tower summed. Exact computation reduces to a polynomial in L = ln q with rational coefficients, via the cotangent partial-fraction sums over the towers; for the bench curves the cotangents are exact: c_A = cot(−iL/2) = i·coth(L/2) = **3i/2**, c_C = cot(π/2 − iL/2) = i·tanh(L/2) = **2i/3** (q = 5).

**Computed values** (exact rational arithmetic; cross-checked by direct paired tower summation, |k| ≤ 4000 pairs at 50-digit arithmetic, reproducing the closed form for n = 1..8 with absolute difference ≤ 4.2×10⁻³ — in every case equal to the check's own measured truncation increment, i.e. the residual is the check's tail, not a discrepancy):

| n | λ_n(A) | λ_n(C) |
|---|---|---|
| 1 | (3/2)L = **2.4141568687…** | (2/3)L = **1.0729586083…** |
| 2 | 3L − (5/4)L² = **1.5904507448…** | (4/3)L + (5/9)L² = 3.5849674355… |
| 3 | (9/2)L − (15/4)L² + (15/8)L³ = 5.3455908116… | 2L + (5/3)L² − (10/27)L³ = 5.9919851614… |

**λ_n(A) > 0 and λ_n(C) > 0 for every n = 1..50** (minima: λ₂(A) = 1.5904507448…, λ₁(C) = 1.0729586083…; λ₅₀(A) = 75.9528531086…, λ₅₀(C) = 83.6949608157…). **λ_n(B) ≡ 0**, as the empty control requires. Note, for reproducers: λ₂(A) is A's minimum, attained at an even n where the central lift alone contributes 1 − (1 − 1/(1/2))² = 0 — the value is carried entirely by the non-central lifts. A bench calibration caveat, recorded in the walk: deg P_A = 1, so Steps 0–B are exercised by a single root; the many-root regime is FF-1's job.

**Trap 1 — the finite-multiset shorthand.** Reading the root multiset "{1} ∪ {1}" as two finite terms in a finite Li-type formula returns wrong values (λ₂(A) = 0 from that reading, against the true tower sum 1.5904507448…). The shorthand is safe for the qualitative reduction (|β_i| = 1 ∀i ⟺ positivity) and unsafe for values. (Defect ledger item 10.)

**Trap 2 — the derivative form with the naive completion.** Li's derivative identity is a theorem for the ζ-type completed function, whose Hadamard product carries no exponential factor. The bench completion 𝔑^σ·P_E(q^{−2σ}) carries the factor exp((deg 𝔫_E − deg P_E)·σ·ln q), and the derivative form counts that factor as if it were zeros: at n = 1 for A it returns (11/2)·ln 5 = 8.8519085184… against the zero-sum's (3/2)·ln 5 = 2.4141568687… — an overstatement of **exactly 4·ln 5 = (deg 𝔫_A − deg P_A)·ln 5 = (5 − 1)·ln 5**. The zero-sum is completion-blind and is used throughout; the derivative form is used only with the exponential factor excluded, as the classical ζ proof excludes it. (Defect ledger item 11.)

### 4.3 The step audit (the derivation walk on A)

Tag key: **FREE** (justifiable from theorems/bookkeeping, nothing imported), **FROM THE PROPERTY** (derived from the λ-data / L-data alone), **IMPORTED** (an ingredient not supplied by the property enters; named, with its exact sub-step).

- **Step 0 — property check.** λ_n(A) ≥ 0, computed (§4.2). Tag: FROM THE PROPERTY.
- **Step A — positivity ⇒ Riemann reading.** |β| = |5/5| = 1; the tower lies on Re σ = 1/2; every paired term is ≥ 0. Tag: FREE — Deligne's theorem plus the Bombieri–Lagarias equivalence; nothing is earned here that was not already a theorem.
- **Step B — read the analytic rank.** r_an = multiplicity of the root T = q⁻¹ = 1/5 of P_A(T) = 1 − 5T, which is 1 (re-verified in the walk: P_A(1/5) = 0, simple root). Tag: FREE — finite bookkeeping on a polynomial.
- **Step C — central multiplicity ⇒ rational points.** Audited sub-step by sub-step:
  - **C1** r_an = 1 from P_A. FREE (Step B's output; the L-function's only contribution to Step C).
  - **C2** rank E(K) ≤ r_an (Tate's inequality). IMPORTED — surface geometry: the cycle-class injection NS(ℰ_A) ⊗ ℚ_ℓ ↪ H²_ét(ℰ̄_A, ℚ_ℓ(1))^Frob, with nondegeneracy of the Néron–Tate height. No property input.
  - **C3** Ingredient I-2 check (semisimplicity of Frobenius at the central eigenvalue): algebraic multiplicity 1 = Frobenius-invariant dimension 1. IMPORTED — discharged on A, but by geometric input: ≥ 1 because the section (4, 2) realizes a class; ≤ 1 by the two rank bounds. A 1×1 block has no Jordan correction, so no further ingredient is consumed *here* — on this curve. I-2 remains a live ingredient in general (it is FF-4's concern).
  - **C4 — THE IMPORT POINT.** Saturation: the Frobenius-invariant part of H²_ét(ℰ̄_A, ℚ_ℓ(1)) consists of divisor classes — **Tate's conjecture T(ℰ_A), ingredient I-1**. IMPORTED. On A it is a *theorem*, proved from the surface's birational geometry (ℰ_A rational ⇒ birational to ℙ¹ × ℙ¹ ⇒ dominated by a product of curves ⇒ Tate's theorem on products applies). The proof consults no L-data and no positivity.
  - **C5** Shioda–Tate conversion: rank = ρ(ℰ_A) − 2 − Σ_v (m_v − 1) = 10 − 2 − 7 = 1. IMPORTED — surface geometry.
  - **C6** The point: P = (4, 2) ∈ E(F₅(t)), of infinite order. IMPORTED — arithmetic of the equation (search over sections x(t) ∈ F₅[t]; non-torsion by the specializations of §4.1). The L-function plays no role.
  - **C7** Sha(E/K) finite. IMPORTED — via BSD ⟺ T(ℰ_A): the same arrow as C4; ingredient I-3 (Sha finiteness) is I-1's arithmetic face.
  - **C8** Ingredient I-4 (characteristic-p subtlety). FREE of charge on the bench: fibers are tame at p = 5, and the Kato–Trihan bypass is available. Recorded as quiet, not as discharged in general.

  Net: of Step C's sub-steps exactly one (C1) is the property's data; the load-bearing import is C4. Three honest attempts to rewrite Step C from the property alone were made in the walk and are recorded with their stopping places: **R1** (functionals of the signal — every quantity computable from P_A alone is a function of the root multiset {5}; the only datum distinguishing A from C is the sign, i.e. Step B's output; a "Step C" assembled from these restates the assertion rather than deriving it — stops at the assertion); **R2** (heights from the leading coefficient — the regulator in the Artin–Tate leading term is the Néron–Tate height of the very point Step C must produce — stops at circularity, one step downstream of C4); **R3** (the cohomological route followed honestly — stops at C4 verbatim: cycle-class surjectivity is I-1). No fourth route is known to the consulted literature.
- **Step D — the wedge (calibration on every conclusion).** Steps 0–B consult **nothing but P_E** — the audit confirms this by inspection. So on a hypothetical curve E′/F₅(t) with the *same* polynomial P_{E′} = 1 − 5T but a Tate-open surface, Steps 0–B would run identically and return identical values, while Step C's saturation for E′ is exactly as open as T(ℰ_{E′}). A completion of Step C from the property alone would therefore prove Tate for E′. Any future claimed Step C must be audited first against this twin: it must not apply verbatim to E′, or must explain why it does not.

**Controls.** On C the walk produces no point, and must not: Step C there is vacuous and closable *without* any import (Tate's inequality gives rank ≤ r_an = 0; I-1 is never invoked because there is no central multiplicity to realize). The Shioda–Tate count does not distinguish C from A geometrically (same fibers, ρ = 10, Σ(m_v − 1) = 7, geometric rank 1 for both) — the difference is exactly the Frobenius sign read at Step B. The control is load-bearing in both directions: it also caught the §4.1 sign error. On B every step is vacuous and λ_n(B) = 0 identically.

**Bench verdict: O-2 (TQ-2, transport reduces), in sharpened form.** X = Reading R (Step A) and the analytic rank (Step B) — both FREE, both verified on the bench. Y = ingredient I-1 (Tate's conjecture T(ℰ), equivalently I-3, Sha finiteness), entering at exactly one named sub-step: C4, "Frobenius-invariant cohomology classes are divisor classes." The sharpening: the reduction is not a stall *inside* a Step C argument — on the property side there is no Step C argument; the chain **terminates at Step B**, and the only known continuation enters from the geometry side at C4. Explicit non-verdicts: not TQ-1 (no cycle-producing step from the signal exists in the audited material, and Step D prices any future one); not TQ-3 / O-4 (the transported *statement* agrees with every settled bench fact — ranks 1/0/0, Sha finite, λ_n ≥ 0 throughout; the three normalization defects the bench program caught were defects of the harness and its shorthands, each caught by a control before any derivation weight rested on it); not O-3 (no stall at I-2 on A — discharged, by geometric input, for A). O-5 is not decidable at bench scale; the bench contributes its Tate-known half, with the I-1 import *seen and named from inside the argument* rather than silently borrowed. Calibration caveat, stated plainly: A is a rational surface, T(ℰ_A) is a theorem, and BSD *holds* for A — this verdict does not say Step C fails on A; it says the proof does not pass through the property.

---

## 5. DEFECT DISCIPLINE (Proposal 1, the ledger habit)

**Proposal 1.** Any measured discrepancy is presumed a defect of our own panel, our own code, or our own brief — and is bug-hunted to its cause before it is reported as anything else. Shallow panels invent gaps (ledger item 8 is the constructive demonstration); deep ones dissolve them. A discrepancy that survives the hunt is reported with its diagnosis attached.

**The ledger.** Every defect found is written into the record with its cause and its fix, and stays there. The ledger to date:

1. `ellanalyticrank` returns the **raw** derivative L⁽ʳ⁾(E, 1), not divided by r! — the runner divides. Caught when route 2 disagreed by exactly 2! on 389.a1.
2. `elltamagawa` folds in the real-component factor — Tamagawa numbers are taken from `elllocalred`'s 4th component instead.
3. A fresh `ellperiods` call returns a complex lattice period for Δ < 0 — Ω is always (2 if Δ > 0 else 1) × `E.omega[1]`. Caught on 11.a2; fixed and verified against LMFDB for both signs of Δ.
4. Label collisions between the Cremona and LMFDB systems (Cremona 571a1 = LMFDB 571.b1; Cremona 11a1 = LMFDB 11.a2); the Sha-4 anchor is LMFDB **571.b1**, rank 0. A brief premise of "571b1 rank 3" was wrong under both systems.
5. The Hardy Z cross-count's grid (samples at 0.025 + 0.05k) leaves the final half-cell (19.975, 20] blind — it undercounted 234446.b1 by one zero (γ = 19.983119…). Diagnosed by direct bracketing; the count stands with its diagnosis. Fix for future scans: cover (0, H] completely.
6. A checkpoint constant for λ₂ supplied in a probe brief (0.092345735188332) was **wrong at the 11th decimal**. Flagged, not forced; the adjudicated value (0.0923457352280466703857…) is by three computations plus an independent contour integral. Checkpoint constants from memory are claims too.
7. A first-pass amplitude-fitting decoder in the template experiments collapsed a sign-symmetric pair (artifacts up to a ~75% ceiling); the faithful fixed-template decoder removed the artifact and the phenomenon was confirmed. (The template experiments are a separate program's method; the ledger entry is kept because the failure mode — the apparatus inventing the signal — is this recipe's standing warning.)
8. A truncated Tate-limit computation on 389.a1 manufactures a phantom regulator gap that dies geometrically (−2.269 → 0.0000299 by n = 8): Proposal 1's mechanism, demonstrated constructively.
9. Bench power-sum sign error: p_n was provisionally assembled as +S_n, swapping A and C's rank readings; caught inside the run by the independent coefficient check and the section search; the convention is p_n = −S_n.
10. The λ finite-multiset shorthand ("{1} ∪ {1}") returns wrong values if read as finite terms (§4.2, Trap 1).
11. The λ derivative form, applied to the naively completed function, overstates λ₁(A) by exactly 4·ln 5 (§4.2, Trap 2).

**Harness vs formulation.** Defects of the apparatus (items 1–6, 9) and defects of a shorthand or a normalization (items 10, 11) are recorded distinctly from defects of the claim. None of the eleven touches the claim's formulation; each was caught by a control or a second route before any weight rested on it. That is what the controls are for.

### Caution — AUTOMATIC ROUNDING (the drop / round rule)

**Carry every value at full computed precision. Never round, truncate, or drop digits silently — and never trust a tool not to do it for you.**

Tools round by default. Display precisions, float formatting, truncated printouts, spreadsheet cells: the value *shown* is routinely not the value *held*, and a display can err in both directions — cutting real digits, or padding a value with digits that are storage, not accuracy. Three rules follow, and they are house law in everything this recipe produces:

1. **Computations consume full-precision values only.** The panel ran at `realprecision 50` (80 for the one pilot quotient check) end to end; no intermediate result was ever rounded before feeding the next step.
2. **Any rounding applied for presentation is flagged where it appears** — what was rounded, to what depth, and why — and a presentational rounding **never feeds back into a computation**.
3. **Discrepancies at the last digit are reported, not reconciled.** If two routes differ in the final digit, both values stand in print with the difference named. Smoothing a difference away destroys exactly the information the door check (§6) runs on.

This is the rule as printed in the record's §8 — **DROP / ROUND FLAGS: flagged, never silently dropped or rounded** — and the record's flags are the worked examples:

- **The 5077.a1 regulator.** The panel's own height-pairing matrix gives 0.41714355875838396981711954461809339674981010609849; PARI's `ellheightmatrix` gives 0.41714355875838396981711954461809339674981010609850 — a difference in the last of 50 digits. The slice verdict reports it as-is ("regulators agree between the panel's own pairing matrix and ellheightmatrix (one last-digit difference, 5077.a1)"). Neither value was adjusted to match the other, and the quotient Q was formed from the unadjusted route.
- **Route-B deviations, sized and stated.** Route B's inputs were LMFDB's `special_value`: printed on the curve pages at 29 significant digits in the first slice; served by the API in the second at 127-bit storage (~38 digits printed) but agreeing with the independent route A only to ~28–31 digits per curve. The resulting deviations |Q_B − 1| were measured curve by curve and printed — worst **5.5×10⁻²⁸** (697691.a1), then 1.9×10⁻²⁹ (12480.bf1), 1.3×10⁻²⁹ (19047851.a1), down to 9.5×10⁻³¹ (133584.bt1) — and identified as input-precision residue of exactly the size the inputs predict. They were not smoothed, not averaged into route A, and not presented as agreement deeper than the inputs support. The API's extra digits are storage precision, not accuracy: a caution in both directions.
- **The sha_an tails.** On four curves the analytic Sha literal read 1 − 1×10⁻²⁹ / 1 − 2×10⁻²⁹ against the database's integer sha = 1. The flag is printed in the record; the integer value is the value used; nothing was quietly tidied to 1 in the working files.

A reproducer who finds a number in this recipe that looks too clean should treat the cleanliness itself as a defect candidate and check the flags first.

---

## 6. THE DOOR CHECK (independent determinations, compared)

The recipe's evidential weight does not rest on tests passed. A test that cannot fail proves nothing, and a test that passes is consistent with both "the two readings are linked" and "both happen to be true but unrelated." What distinguishes them is **interaction**: each load-bearing quantity is determined by two independent methods — ideally in the two languages, arithmetic and analytic — and the two determinations are checked against each other at the door. The taxonomy of outcomes, fixed in advance:

- **Interaction with agreement = evidence.** Two routes that share no machinery landing on the same value is the crossing, completed.
- **Interaction with disagreement = the fault, located.** A mismatch names the exact component at fault — and under Proposal 1 (§5) the first suspect is always our own apparatus.
- **Non-interaction = silence.** A quantity determined by only one route, or a cell that could not be run, counts neither way. It is printed as what it is, never filled in from the other side.

The completed interactions of record:

| Quantity | Determination 1 | Determination 2 | Outcome |
|---|---|---|---|
| Zero count in the box (Part One, §3) | Argument-principle windings of L and of Λ (gate W_L − W_Λ = 1) | House zero scan (`lfunzeros` + Hardy cross-count) | Agree exactly, 17/17; total 535 |
| Rank (§§2, 3) | Analytic rank (order of vanishing) | 2-descent with points (`ellrank`, r1 = r2) | Agree, 17/17; every rank proved |
| Sha, 2-part (§3) | Analytic Sha from the BSD formula | Descent bookkeeping (S = s test) | Agree on all 17: trivial ×15; (ℤ/2)² ×2 |
| Selmer rank C (§3) | `ell2cover` basis-quartic count | Bookkeeping identity C = r2 + T + s | Agree, 17/17 |
| Rank of the two Sha-9 curves (§3) | PARI `ellrank` | eclib `mwrank` (independent implementation) | Agree: rank 0, Selmer rank 0, both |
| Sha[3] of 133584.bt1 (§3) | Analytic value 9 | Magma `ThreeSelmerGroup`: (ℤ/3)² | Agree (with the printed pairing caveat) |
| Regulator (§2) | Own height-pairing matrix on the generators | PARI `ellheightmatrix` | Agree to all 50 digits, one last-digit difference (§5) |
| L*(E, 1) (§2) | Own PARI factors (route A) | LMFDB `special_value` (route B) | Agree to the depth route B's inputs support (§5) |
| λ_n, ζ (Part One, §4) | Zero-sum over 1,026 pairs | Derivative route at 100 digits; closed forms for λ₁, λ₂ | Agree, drift quantified |
| Bench λ_n (§4) | Exact closed form (cotangent sums) | Direct paired tower summation, |k| ≤ 4000 | Agree; residual = the check's own tail |
| Bench P_A(T) (§4) | Fiber point counts | Brute-force enumeration + second power-sum identity | Agree (after the sign defect was caught, §5) |
| Bench root numbers (§4) | Functional-equation form of P(T) | Parity of the settled ranks | Agree (w_A = −1, w_C = +1) |

The one non-interaction: Sha[3] of 12480.bf1 (§3) — silence, printed as untested, the analytic 9 labelled analytic. **The claim is the crossing** — the identification, established by these completed interactions. Construction past the crossing is not claimed (§7).

The prediction side of every analytic row above is Part One's — its formula, its box counts, its exhibits. This document supplied the arithmetic determinations; Part One supplied what they had to match. Found equals predicted, at the door, on every completed row.

---

## 7. WHAT THIS DOCUMENT DOES NOT DO

Stated as plainly as the results:

- **This document stops where the record stops — by design, not by failure.** The evidence is finite, over the stated ranges (§1), and no accumulation of finite results is presented as reaching past them. RH and GRH stand under the same stop. The two places this document stops short are named in the bullets below.
- **The unification criterion is asserted to exist, not exhibited — the named open step.** The house position names a single positivity property of the L-function, in Weil's family, from which both readings would follow; no working formula for that criterion is written down anywhere in this recipe, and the panel's 17 curves were resolved by the standard instruments of §§2–3, not by such a formula. Anyone who tells you this recipe contains a new formula is misreading it.
- **Step C is not derived.** On the function-field bench, where the derivation can be audited line by line, the property-side chain terminates at Step B (analytic rank), and the continuation to rational points imports exactly one named ingredient — **I-1, Tate's conjecture (Frobenius-invariant cohomology classes are divisor classes), entering at sub-step C4** — equivalently I-3, the finiteness of Sha (§4.3). The verdict is O-2: *BSD minus one named ingredient; not BSD under a new name.* The corresponding step over ℚ is not supplied by this recipe.
- **The odd parts of Sha are analytic**, except the 3-part of 133584.bt1 (§3). The global odd-part statement of §3 must travel with any use of the Sha results.
- **One cell is open**: Sha[3] of 12480.bf1, printed as untested, with its exact Magma input given in §3 for any reader with access.
- **Three designed bench cases were not run** (FF-1, FF-2, FF-4, §4). In particular O-5 — whether the property detects the Tate boundary from inside the derivation — is undecided.

---

**Sources of record for this document.** Consolidated record v1: `consolidated-record-2026-10-31.md` (Zenodo 24041813). Consolidated record v2: `paper/consolidated-record-V2.md` (Zenodo 24265721). Panel slices: `panel/results_slice1.md`, `panel/results_slice2.md`, `panel/manifest.md`, `panel/panel-verdict-2026-10-31.md`. Revision working files: `paper/pilot-571b1-descent-2026-11-09.md`, `paper/descent-rollout-2026-11-09.md`, `paper/odd-descent-2026-11-09.md`, `paper/function-field-statement-DRAFT-2026-11-09.md`, `paper/ff3-bench-curve-selection-2026-11-10.md` (slice 7), `paper/ff3-derivation-walk-2026-11-10.md` (slice 8), `run-log.md`. Every parameter in this document is copied from one of those files or from the combined recipe draft of 2026-11-11; where a source disagrees with itself, the discrepancy is flagged in place rather than resolved silently.

---

## Provenance and credit

**It is a new recipe.**

We didn’t invent the flour — we just showed you how to bake the pie.

This document assembles, in procedural form, the arithmetic half of the method behind the house record *One Property, Two Readings* (Version 1 published 2026-11-07, Zenodo record 24041813; Version 2 published 2026-11-15, Zenodo record 24265721, DOI 10.5281/zenodo.24265721) and its revision computations of 2026-11-09/10. The mathematics it uses is the field's: the descents are the classical 2-descent with the Cassels pairing, plus Magma's 3-Selmer machinery; the bench rests on Tate's and Shioda–Tate's theorems for elliptic surfaces. What is the house's is the assembly: the pre-registered protocol, the adversarial panel, the requirement that every load-bearing quantity be determined twice by independent routes and checked at the door, the defect discipline, and the reading of the two conjectures as two readings of one property of one object. The recipe is given complete, including the places where it stops.

**Infinity is the number after the last known number.**
