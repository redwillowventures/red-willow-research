# The Pie Recipe, Part One — Riemann

**The analytic half of the identification recipe: the formula, the wave reading, and the counting of the zeros — written to be reproduced.**

**Date:** 2026-11-11
**Authors:** Joseph Carroll; Pip Willow (Researcher)
**Affiliation:** Red Willow Ventures LLC, Green Valley, Arizona
**Status:** DRAFT — not yet published.
**Companion:** *The Pie Recipe, Part Two — BSD* (the panel, the descents, the bench, and the door check).

---

## Introduction

**Do not auto round your numbers**

An introduction, for whoever picks this up.

**This is your road map.**

This is the complete working method behind a published claim: that the arithmetic reading of an elliptic curve and the analytic reading of its L-function — the two sides of the Birch and Swinnerton-Dyer problem, and of the Riemann hypothesis — are two ends of one communication, and that their agreement can be tested end to end. The claim is posted on its own. The evidence is posted on its own. This document is the third piece: the recipe — its Riemann half. Every step, parameter, and check of the analytic side, in the order we ran them: the formula, the wave reading, and the counting of the zeros. The arithmetic half — the panel, the descents, the bench, and the comparison at the door — is the companion document, Part Two.

Its value is that it can be run. A result you cannot re-run is a story you are asked to believe; this one asks nothing. The formula, the windings, the exhibits — each is specified to the digit, including where our own instruments disagreed with each other, and what we did about it, which was to write it down and keep both numbers. The most portable part may be that discipline: indict your own apparatus first, and never let a rounded number do a true number's work. If your work anywhere needs two independent computations to agree before you trust either, the protocol travels.

We are giving it away. We have no reason to withhold this, and it might do some good out there. That is the whole reasoning.

It is not a proof, and its last section names what it does not contain. It is a complete account of an identification, and of the tests that identification survived — offered to be checked.

— Joseph Carroll and Pip Willow, Red Willow Ventures, Green Valley, Arizona. November 2026.

**This is the recipe.**

the arithmetic analytic identification

---

## 1. OBJECT AND FENCES (pre-registration, ranges)

**The object.** For an elliptic curve E over ℚ, its L-function L(E, s) has two classical statements attached to it: the Riemann reading (every nontrivial zero lies on the critical line — here the line Re(s) = 1, in the arithmetic normalization with center s = 1) and the BSD reading (the leading coefficient at the center equals the BSD identity: Sha × Regulator × ∏ Tamagawa numbers × |torsion|⁻², against the real period Ω). The house claim, stated 2026-10-31 and conjectural throughout: **these are not two facts. They are two readings of a single property of L(E, s) — the object is synchronized at its symmetry center** — and no curve will ever be found separating them: any E satisfying one reading satisfies the other. This document carries the Riemann reading's side of the test: the formula, and the counting of the zeros.

**The fences.** Every run in this recipe is finite, and its range is stated before it runs:

- Zeros counted in the box 0 ≤ γ ≤ 20, counting multiplicity, for the panel of 17 elliptic curves over ℚ (§3; the panel itself is constructed in Part Two, §2).
- Envelope exhibit: x ≤ 10⁹ on a stated grid (§4).
- Positivity exhibit: Li coefficients λ_n for n ≤ 30 on ζ (§4).

The finiteness is by house rule — the fence: every test stops one short, the last number is never asked for, and no accumulation of finite results is presented as reaching past the stated ranges.

**Infinity.** The demand to prove it to infinity is the demand this recipe does not take up. Infinity is the number that comes after the last known number — never itself known, always one past wherever the counting has reached. Infinity is the time: it lives inside sequence, arriving one number at a time; the next number is always giveable, and every answer is the last one, until the next one. A computed horizon is an assigned calculation doing infinity's job until it is replaced: on the Riemann side, the field's current number for infinity is 3,000,175,332,801 — the last known number, 3,000,175,332,800, plus one, stationary since 2021. This recipe's stands at 535 zeros, counted (§3). Because the house claim is a mechanism and not a number, it does not stand at a horizon; the field counts toward infinity, and this work explains the line. The fence above is this position in operation: stopping one short of the last number was never a failure to finish — it is what finishing looks like, in time. (Position as published in *The Bridge Is Communication*, §5, 2026-11-11; carried into this recipe 2026-11-15.)


**Pre-registration.** Before each run, the outcomes and their verdicts are written down: what agreement means, what a mismatch would mean, and what will be done in each case. The standing verdict rule (Proposal 1, §6): any measured discrepancy is presumed a defect of our own panel and is bug-hunted before it is reported as anything else. The bench test (Part Two, §4) carries its own pre-registered verdict taxonomy (TQ-1/2/3, outcomes O-1 to O-5), fixed before the walk.

**Pilot-first rule.** No protocol is rolled out panel-wide until it has run end-to-end on the pilot curve 571.b1 and passed its calibration gates (§3). Both revision protocols (zero counts, descents) were piloted on 571.b1 first, then rolled out unchanged.

---

## 2. THE FORMULA (the explicit formula, and the wave reading)

The formula the identification runs on is the **explicit formula** — Riemann's (1859), in von Mangoldt's form for ζ and Weil's generalization for L-functions. For ζ it reads, with ψ(x) the Chebyshev function (the prime-power counting function, ψ(x) = Σ_{p^k ≤ x} log p):

> ψ(x) = x − Σ_ρ x^ρ/ρ − log(2π) − ½·log(1 − x⁻²),

the sum running over the nontrivial zeros ρ of ζ. The same shape holds for L(E, s): a sum over prime powers on one side, a sum over the zeros on the other, equal. One identity, two ends: the primes at one end, the zeros at the other, and the formula is the translation between them.

**The wave reading (the house's reading of the field's formula).** Write x = e^t. Each zero ρ = β + iγ contributes a term x^ρ = x^β · e^{iγt}: an oscillation of frequency γ whose amplitude grows like x^β. On the critical line (β = 1/2 for ζ; the symmetry axis for L(E, s)) every contribution is a pure tone — same amplitude law, zero width. An off-line zero would contribute a mode with a different growth rate — in spectral terms, a resonance with nonzero width. The observed spectrum behaves as zero-width pure tones, with local peaks where higher zeros drift into phase. In the house's compressed form: the prime waves resonate; **a zero is where the waves meet in phase and cancel, and the cancellation is exact on the symmetry axis.**

The two factorizations of one L-function say the same thing from the two ends: the Euler product over primes (the arithmetic end transmits) and the Hadamard product over zeros (the analytic end receives). There is no machinery in the middle: the wave is the medium. A bridge is known by its crossings — and the crossing is tested by determining each quantity from both ends independently and comparing (Part Two, §6).

**The positivity form.** The recipe's signal-only test quantity is Li's criterion: RH holds for the L-function if and only if λ_n ≥ 0 for all n ≥ 1, where

> λ_n = Σ over zero pairs of [1 − (1 − 1/ρ)^n] = (1/(n−1)!) · [dⁿ/dsⁿ (s^{n−1} log ξ(s))] at s = 1,

ξ the completed function. No zero is located by this test; it reads the whole zero set at once, as a signal. §4 runs it on ζ; Part Two (§4) transports it to the bench curves in the normalization that survives transport.

---

## 3. ZERO IDENTIFICATION AND BOX COUNTS (the argument principle; no line assumed)

This is the recipe's answer to the straight-line method: do not scan a line and list what is found on it; **count a box**, so that a zero off the line would change the count and be caught.

**Normalization.** Arithmetic, center s = 1; completed function Λ(s) = N^(s/2) · (2π)^(−s) · Γ(s) · L(E, s), with Λ(s) = Λ(2 − s) up to the root number. Strip zeros satisfy 1/2 < Re(s) < 3/2 (the Euler product is nonzero for Re(s) ≥ 2; the left half follows by the functional equation).

**Environment.** House venv `~/workspace/bsd-run/venv/bin/python`, **cypari2 / PARI 2.17.2**, GP `default(realprecision, 50)` throughout. mpmath 1.2.1 (system python3) for the Γ-factor argument tracking below. Host: Ubuntu 24.04.5 LTS.

**The count.** For each curve, two windings around the rectangle **[−0.5, 2.5] × [−T, T]**, traversed counterclockwise:

1. The winding number of the raw L-function, `lfun(E, s)`, at **T = 19.9, 20, and 20.1** (the two extra heights are a boundary-stability check), sampled at **step 0.01** in s (≈ 8,600 boundary points per T), each step's argument increment taken in (−π, π] and summed. Increments must stay well under π (pilot maximum |Δarg| = 0.0878 rad at T = 20; rollout maximum 0.837 rad, on the curve whose next zero sits 0.009 above the boundary — still safely under π) and min |L| on the contour must stay clear of 0 (pilot 0.8123; rollout minimum 0.0365), so no argument jump is missed and no zero lies on or near the contour.
2. The winding number of the completed function, `lfunlambda(E, s)`, at T = 20. Λ's zeros in the box are exactly the strip zeros of L: the Γ pole at s = 0 cancels L's trivial zero there (verified directly: `lfun(E, 0)` returns exactly 0 for all 17 curves, while Λ(E, 0) ≠ 0 — for the pilot, 32.484618558287431703012827847908188728045481320998).

**The gate: W_L − W_Λ = 1**, exactly — the L winding exceeds the Λ winding by the one trivial zero at s = 0. This identity held to **≤ 2.9×10⁻¹³ on all 17 curves**.

**From box count to predicted count.** A real-axis scan of L(E, x) on (−0.5, 2.5) at step 0.002 excludes real strip zeros (the only sign changes anywhere are at x = 0, and at x = 1 exactly for the six odd-rank curves), so conjugation symmetry pairs the strip zeros cleanly and the predicted count with 0 < γ ≤ 20, counting multiplicity, is (strip total − c)/2 + c, where c is the center multiplicity (equal to the analytic rank; independently confirmed by descent, Part Two, §3).

**Calibration gates — run first, both must pass before any panel curve.**

- The identical winding code on ζ over [−0.5, 1.5] × [−20, 20] returns **exactly 1** (two zeros at γ = ±14.134725… minus the pole at s = 1).
- The full routine on the pilot curve 571.b1 must reproduce the pilot verdict (below) before the rollout proceeds.

**Pilot (571.b1, run first, 2026-11-09).** L winding at T = 20: **45.00000000000005** (deviation 5.4×10⁻¹⁴; T = 19.9 and 20.1 also 45). Λ winding: **44.00000000000000**. Decomposition: 45 = 44 strip zeros + 1 trivial zero; predicted count 44/2 = **22**; found by the house scan: **22**. Difference 0. Turing-form split of the count, for the record: with ϑ(T) the continuous argument of the archimedean factor N^((1+it)/2)(2π)^(−(1+it))Γ(1+it) tracked from t = 0 at step 0.005 (mpmath, 50 digits), ϑ(20)/π = **21.45797842749715**, and S(20) = (1/π)·arg L(E, 1 + 20i) (argument by continuous variation horizontally from σ = 8 to σ = 1 at step 0.01) = **0.5420215725029203**; the two sum to 22.0000000000001. Stability: a fresh `lfunzeros(E, 21)` places the next on-line zero at γ = 20.836972906029157, well clear of the boundary.

**Rollout (remaining 16 curves, 2026-11-09).** Identical protocol, in conductor order. Evaluation-path note: direct `lfun` evaluation costs ~0.28–0.33 s per point at conductor 19,047,851, so values were taken from a PARI `lfuninit` object (**domain [2.5, 21]**) at the same realprecision 50; validated three ways (init-path vs direct values agreeing to ≤ 8.2×10⁻⁵⁸ for L and ≤ 2.5×10⁻⁵⁷ for Λ at sampled contour points of the largest-conductor curve; in-run spot checks, 16 contour points per function per curve, identical at double precision on all 17 curves; both calibration gates reproduced). Result: **all 16 agree exactly** — predicted from the L winding = predicted from the Λ winding = found, difference 0, on every curve. Min |Λ| on contours runs 10⁻¹⁰ to 10⁻¹³ — the left edge σ = −0.5, where Γ decays exponentially — and did not disturb the argument tracking on any curve.

**Boundary band (recorded, none adverse).** The T = 19.9 / 20.1 windings found a conjugate pair of strip zeros in the band 19.9 < |γ| ≤ 20.1 on six curves, each corroborated by a fresh `lfunzeros(E, 20.15)`: just above the top edge on 44.a1 (γ = 20.0873860087), 12480.bf1 (γ = 20.0089795062), 19047851.a1 (γ = 20.0488941376); inside the box's top band on 5077.a1 (19.9745496642), 234446.b1 (19.9831193049), 19047851.b1 (19.9389528712). None affects any H = 20 count.

**Panel total: 535 zeros, independently counted** (513 in the rollout + 22 on the pilot). Within the stated box and counting multiplicity: no panel curve has a zero off the critical line, and no on-line zero was missed.

---

## 4. EXHIBITS B AND C (the ζ-side instruments)

### Exhibit B — the Schoenfeld envelope (a code sanity check; no evidential weight)

**Label first, because the label is the lesson:** in the tested range this bound is already a proven theorem (Büthe; Platt–Trudgian, rigorous to height ~2.169×10²⁵). A check that cannot fail is not evidence for anything except the correctness of the code that runs it. The exhibit is retained under that label: it validates the sieve and li(x) code, nothing more.

**Instrument.** Schoenfeld (1976): RH implies |π(x) − li(x)| < (1/(8π))·√x·ln(x) for x ≥ 2657. Ratio r(x) = actual error / envelope; RH requires r < 1. Exact π(x) by segmented sieve; li(x) = Ei(ln x) at **30-digit precision**.

**Validation.** A rerun reproduced all nine previously recorded ratios (10⁴–10⁸) within third-decimal rounding; independent spot check π(10⁸) = 5,761,455, r = 0.102925 — identical to the run at six decimals. Grid ratios from the original runs: 0.468 at 10⁴; 0.348 at 5×10⁴; 0.261 at 10⁵; 0.185 at 5×10⁵; 0.236 at 10⁶; 0.149 at 2×10⁶; 0.091 at 5×10⁶; 0.167 at 10⁷.

**Results.** π(10⁹) = **50,847,534** (exact). Worst ratio in the new decade: **0.102000 at x = 2.2×10⁸**; r(10⁹) = 0.065234 (error 1,700.96 against envelope 26,074.64). Worst on the full 10⁴–10⁹ grid remains 0.468 at 10⁴. The worst case holds a ~0.10 plateau while the mean level falls (0.1098 on [10⁷, 10⁸] → 0.0752 on (10⁸, 10⁹]): **the margin is not closing**. (Two recorded ratios, 0.100 and 0.085, carried no x labels; they are identified by grid-pattern inference as 2×10⁷ and 5×10⁷ — inference, flagged as such under §6, nothing relabeled on its strength.)

### Exhibit C — the Li positivity probe (ζ-side)

**Test.** Li's criterion (§2): RH iff λ_n ≥ 0 for all n ≥ 1. Signal-only: no zero is located. λ_n for **n = 1..30**, by two routes sharing no machinery:

1. **Zero-sum route:** λ_n = Σ over zero pairs of [1 − (1 − 1/ρ)^n], summed over **1,026 zero pairs** (top γ = 1449.48877128).
2. **Derivative route:** λ_n = (1/(n−1)!)·[dⁿ/dsⁿ (s^{n−1} log ξ(s))] at s = 1, by Cauchy/DFT derivatives at **100-digit precision**.

**Result: all λ_n > 0 for n = 1..30 on both routes.** Smallest: **λ₁ = 0.023095708966121…**; monotone growth to λ₃₀ = 18.5537922908134 (route 2). Route-1 deviations from route 2 match the smooth-density truncation-tail estimates to three significant figures (checkpoints: λ₁ dev 7.07×10⁻⁴, λ₂ dev 2.83×10⁻³) — the drift is the truncation tail, quantified, not hidden. Independent adjudications: λ₁ by the closed form (1 + γ_E/2 − ln(4π)/2) **and** by derivative, agreeing to 60 digits (0.0230957089661210338143…); λ₂ by an independent Cauchy contour integral: 0.09234573522804667038572848619… (A checkpoint constant for λ₂ supplied in the probe brief — 0.092345735188332 — was wrong at the 11th decimal; the agent flagged it rather than forcing agreement, and the adjudicated value above is by three computations. Defect ledger item 6: checkpoint constants from memory are claims too.)

These coefficients are ζ-side. The per-curve transported computation — λ_n(E) ≥ 0 for an elliptic curve's L-function, in the normalization that transports — is the bench exhibit of the companion document (Part Two, §4).

---

## 5. THE COUNTS, CERTIFIED (what any arithmetic side must match)

The analytic side's evidential weight does not rest on tests passed. A test that cannot fail proves nothing, and a test that passes is consistent with both "the two readings are linked" and "both happen to be true but unrelated." What distinguishes them is **interaction**: each load-bearing quantity is determined by two independent methods and the two determinations are checked against each other. The taxonomy of outcomes, fixed in advance:

- **Interaction with agreement = evidence.** Two routes that share no machinery landing on the same value is the crossing, completed.
- **Interaction with disagreement = the fault, located.** A mismatch names the exact component at fault — and under Proposal 1 (§6) the first suspect is always our own apparatus.
- **Non-interaction = silence.** A quantity determined by only one route, or a cell that could not be run, counts neither way. It is printed as what it is, never filled in from the other side.

The completed interactions of this document:

| Quantity | Determination 1 | Determination 2 | Outcome |
|---|---|---|---|
| Zero count in the box (§3) | Argument-principle windings of L and of Λ (gate W_L − W_Λ = 1) | House zero scan (`lfunzeros` + Hardy cross-count) | Agree exactly, 17/17; total 535 |
| λ_n, ζ (§4) | Zero-sum over 1,026 pairs | Derivative route at 100 digits; closed forms for λ₁, λ₂ | Agree, drift quantified |

So the analytic side certifies, and hands over, the following. For each of the 17 panel curves: the strip-zero total in the box [−0.5, 2.5] × [−20, 20], counted by two windings whose difference is the exact gate W_L − W_Λ = 1 (held to ≤ 2.9×10⁻¹³ on all 17); the predicted count with 0 < γ ≤ 20, (strip total − c)/2 + c, with c the center multiplicity — and that predicted count equals the count found, difference 0, on every curve; **panel total 535, independently counted**, with no zero off the critical line and none missed within the box. The center multiplicities c are the analytic ranks: the prediction the arithmetic side must meet, curve by curve. On ζ itself: the Schoenfeld envelope holds with its worst ratio 0.468 at x = 10⁴ and the margin not closing (§4, Exhibit B — a sanity check, labelled as such), and Li's coefficients are positive for n = 1..30 by two routes that share no machinery (§4, Exhibit C).

**Here is what any arithmetic side must match.** An independent arithmetic determination of these curves — ranks from rational points, Sha from descent — must land on these numbers: the analytic ranks at the center, and a zero set with no member off the line. The companion document, **Part Two — BSD**, takes exactly these counts as its prediction, supplies the arithmetic determinations (the panel quotient, the descents, the bench), and reports the comparison at the door (Part Two, §6).

---

## 6. DEFECT DISCIPLINE (Proposal 1, the ledger habit)

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
10. The λ finite-multiset shorthand ("{1} ∪ {1}") returns wrong values if read as finite terms (Part Two, §4.2, Trap 1).
11. The λ derivative form, applied to the naively completed function, overstates λ₁(A) by exactly 4·ln 5 (Part Two, §4.2, Trap 2).

**Harness vs formulation.** Defects of the apparatus (items 1–6, 9) and defects of a shorthand or a normalization (items 10, 11) are recorded distinctly from defects of the claim. None of the eleven touches the claim's formulation; each was caught by a control or a second route before any weight rested on it. That is what the controls are for.

### Caution — AUTOMATIC ROUNDING (the drop / round rule)

**Carry every value at full computed precision. Never round, truncate, or drop digits silently — and never trust a tool not to do it for you.**

Tools round by default. Display precisions, float formatting, truncated printouts, spreadsheet cells: the value *shown* is routinely not the value *held*, and a display can err in both directions — cutting real digits, or padding a value with digits that are storage, not accuracy. Three rules follow, and they are house law in everything this recipe produces:

1. **Computations consume full-precision values only.** The panel ran at `realprecision 50` (80 for the one pilot quotient check) end to end; no intermediate result was ever rounded before feeding the next step.
2. **Any rounding applied for presentation is flagged where it appears** — what was rounded, to what depth, and why — and a presentational rounding **never feeds back into a computation**.
3. **Discrepancies at the last digit are reported, not reconciled.** If two routes differ in the final digit, both values stand in print with the difference named. Smoothing a difference away destroys exactly the information the door check (Part Two, §6) runs on.

This is the rule as printed in the record's §8 — **DROP / ROUND FLAGS: flagged, never silently dropped or rounded** — and the record's flags are the worked examples:

- **The 5077.a1 regulator.** The panel's own height-pairing matrix gives 0.41714355875838396981711954461809339674981010609849; PARI's `ellheightmatrix` gives 0.41714355875838396981711954461809339674981010609850 — a difference in the last of 50 digits. The slice verdict reports it as-is ("regulators agree between the panel's own pairing matrix and ellheightmatrix (one last-digit difference, 5077.a1)"). Neither value was adjusted to match the other, and the quotient Q was formed from the unadjusted route.
- **Route-B deviations, sized and stated.** Route B's inputs were LMFDB's `special_value`: printed on the curve pages at 29 significant digits in the first slice; served by the API in the second at 127-bit storage (~38 digits printed) but agreeing with the independent route A only to ~28–31 digits per curve. The resulting deviations |Q_B − 1| were measured curve by curve and printed — worst **5.5×10⁻²⁸** (697691.a1), then 1.9×10⁻²⁹ (12480.bf1), 1.3×10⁻²⁹ (19047851.a1), down to 9.5×10⁻³¹ (133584.bt1) — and identified as input-precision residue of exactly the size the inputs predict. They were not smoothed, not averaged into route A, and not presented as agreement deeper than the inputs support. The API's extra digits are storage precision, not accuracy: a caution in both directions.
- **The sha_an tails.** On four curves the analytic Sha literal read 1 − 1×10⁻²⁹ / 1 − 2×10⁻²⁹ against the database's integer sha = 1. The flag is printed in the record; the integer value is the value used; nothing was quietly tidied to 1 in the working files.

A reproducer who finds a number in this recipe that looks too clean should treat the cleanliness itself as a defect candidate and check the flags first.

---

## 7. WHAT THIS DOCUMENT DOES NOT DO

Stated as plainly as the results:

- **The counts stop at the stated heights — by design, not by failure.** The counts reach the stated heights only: the box 0 ≤ γ ≤ 20 for the 17 curves, the envelope grid to x ≤ 10⁹, Li's coefficients to n ≤ 30. What would carry them to every height is a criterion this document asserts and does not exhibit; it is named in §1. The identification stands on the completed tests. The evidence is finite, over the stated ranges, and no accumulation of finite results is presented as reaching past them. RH for the panel's L-functions, and GRH, stand under the same stop.
- **The unification criterion is asserted to exist, not exhibited — the named open step.** The house position names a single positivity property of the L-function, in Weil's family, from which both readings would follow; no working formula for that criterion is written down anywhere in this recipe, and the panel's 17 curves were resolved by the standard instruments, not by such a formula. Anyone who tells you this recipe contains a new formula is misreading it.
- **Exhibit B carries no evidential weight** (§4): it is a code sanity check inside a range where the bound is already a theorem.
- **The signal-only test locates nothing**: Li's λ_n (§4) read the whole zero set at once; the zero *locations* come from the box counts of §3 and nowhere else.
- The wave reading of §2 is a reading — the house's account of what the explicit formula is doing. This document's results do not depend on adopting it; its evidence (§5) is the completed interactions, which stand in the field's own terms.
- The arithmetic determinations these counts predict — the ranks and Sha by descent, the panel quotient, the function-field bench, and the final comparison — are not in this document. They are Part Two.

---

**Sources of record for this document.** Consolidated record v1: `consolidated-record-2026-10-31.md` (Zenodo 24041813). Consolidated record v2: `paper/consolidated-record-V2.md` (Zenodo 24265721). Revision working files: `paper/pilot-571b1-turing-2026-11-09.md`, `paper/turing-rollout-2026-11-09.md`, `run-log.md`. Every parameter in this document is copied from one of those files or from the combined recipe draft of 2026-11-11; where a source disagrees with itself, the discrepancy is flagged in place rather than resolved silently.

---

## Provenance and credit

**Nothing in this recipe is a new formula. It is, however, a new recipe.**

We didn’t invent the flour — we just showed you how to bake the pie.

This document assembles, in procedural form, the analytic half of the method behind the house record *One Property, Two Readings* (Version 1 published 2026-11-07, Zenodo record 24041813; Version 2 published 2026-11-15, Zenodo record 24265721, DOI 10.5281/zenodo.24265721) and its revision computations of 2026-11-09/10. The mathematics it uses is the field's: the explicit formula is Riemann's and Weil's; the envelope test is Schoenfeld's; the positivity test is Li's (with the Bombieri–Lagarias form); the counting method is Turing's. Nothing in this recipe is a new formula. What is the house's is the assembly: the pre-registered protocol, the adversarial panel, the requirement that every load-bearing quantity be determined twice by independent routes and checked at the door, the defect discipline, and the reading of the two conjectures as two readings of one property of one object. The recipe is given complete, including the places where it stops.

**Infinity is the number after the last known number.**
