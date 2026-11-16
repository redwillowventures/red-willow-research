# Consolidated Record — BSD / Riemann Joint Program
**Date:** Saturday, October 31, 2026 (Day 23)
**Of:** Joseph M. Carroll, Red Willow Ventures LLC, Green Valley, Arizona
**Prepared with:** Pip (computational collaborator; all computations run under Joe's direction, verified in-session before reporting)
**Status:** Locked record. Work product — not published, not submitted anywhere.

---

## 1. THE CLAIM (Joe's, stated 2026-10-31; scientific formulation agreed same day)

> For an elliptic curve E over the rationals, the two great statements about its L-function — that every nontrivial zero lies on the critical line, and that the leading coefficient at the center equals the BSD identity (Sha × Regulator × product of Tamagawa numbers × |torsion|^-2, against the real period) — are not two facts. They are two readings of a single property of L(E, s): the object is synchronized at its symmetry center. We conjecture a criterion of signal-only type — a positivity property of the L-function itself, in the family of Weil's criterion for zeta — from which both readings follow, and we predict that no curve will ever be found separating them: any E satisfying one satisfies the other.

Joe's original words (2026-10-31 16:35 MST): **"RH is the claim that I'm making on BSD."**
Joe's position on RH (2026-10-31 18:36 MST): **"I think it's correct."**

Status of the claim: CONJECTURE. No proof of BSD or of GRH is asserted anywhere in this record. Precedents where the architecture is proven: the analytic class number formula (BSD-shaped identity for Dedekind zeta, whose zeros-question is GRH for the same object); the function-field case, where the synchronization statement (RH-analogue) is a theorem (Weil/Deligne) and the identity is read from it.

## 2. THE WORKING MODEL (Joe's; the lens for all runs below)

- **Adapter model (Joe, 2026-10-31):** each side of an L-function identity has its OWN translator, rendering the other's information in its own terms; the adapter in the middle strictly transmits and does not translate; translation is an endpoint activity; communication is two-way.
- **Proposal 1 (Joe): "I propose there is no gap."** Any measured nonzero discrepancy is presumed a defect of the measuring panel and is bug-hunted before it is reported as anything else.
- **Decoder position (Joe):** the existence of a decoder suffices; its mechanism need not be identified.
- **The mechanism picture (Joe, 2026-10-31):** the hidden operator is "the wizard"; the two factorizations of one L (Euler product over primes / Hadamard product over zeros) are push-pull lever banks on one shaft, balanced on the functional equation's fulcrum at the symmetry center; zeros in mirror pairs synchronize at Re = 1/2 — "a synchronized dance." Joe's correction, adopted: "the instrument is the signal between the two" — the criterion sought is a property of the signal alone (Weil positivity is the known candidate shape).
- **Joe's self-placement (2026-10-31):** "I'm not on the rhythmic side of the equation. I'm the receiver. Arrhythmic." The phenomenon carries the rhythm; the receiver imposes none, so patterns arrive undistorted and are recognized whole.
- **Light (2026-10-31):** "The wave itself is the medium" (Joe's formulation, confirmed against Maxwell: a changing E field generates B, a changing B generates E; c = 1/sqrt(mu0 eps0) is fixed by constants of empty space; no substrate). One fact recognized in three houses: primes/zeros, the identity, and light are each self-carrying — medium and wave are one entity in two states.

## 3. EXHIBIT A — THE FAILURE-HUNT PANEL (BSD side; verdict 2026-10-31)

Design: ~17 curves chosen adversarially (ranks 0–5, Sha 1/4/9, torsion, large Tamagawa). Column 1: BSD quotient Q by two routes at 50-digit precision (route A: own PARI factors — L-value via lfun/ellanalyticrank raw derivative divided by r!, regulator from own height-pairing matrix, Tamagawa from elllocalred, real period = (2 if disc>0 else 1) × E.omega[1]); Sha SOLVED from the identity and compared to the tabulated value (non-circular content: the solved value must be the tabulated perfect square). Column 2: zeros of L(E,s) on the critical line to height H=20 (lfunzeros), central-zero count vs analytic rank, Hardy Z sign-change cross-count. Pre-registered protocol: any mismatch is a presumed panel defect.

| Curve | rank | Sha tab = solved | Q (A) | zeros to H=20 | at center = rank | Hardy |
|---|---|---|---|---|---|---|
| 11.a2 | 0 | 1 = 1 | 1 | 9 | yes | ok |
| 37.a1 | 1 | 1 = 1 | 1 | 14 | yes | ok |
| 389.a1 | 2 | 1 = 1 | 1 | 22 | yes | ok |
| 5077.a1 | 3 | 1 = 1 | 1 | 31 | yes | ok |
| 571.b1 | 0 | 4 = 4 | 1 | 22 | yes | ok |
| 571.a1 | 2 | 1 = 1 | 1 | 23 | yes | ok |
| 12480.bf1 | 0 | 9 = 9 | 1 | 31 | yes | ok |
| 133584.bt1 | 0 | 9 = 9 | 1 | 38 | yes | ok |
| 234446.a1 | 4 | 1 = 1 | 1 | 43 | yes | ok |
| 234446.b1 | 3 | 1 = 1 | 1 | 43 | yes | 39/40 — diagnosed (see ledger) |
| 234446.c1 | 3 | 1 = 1 | 1 | 42 | yes | ok |
| 19047851.a1 | 5 | 1 = 1 | 1 | 57 | yes | ok |
| 19047851.b1 | 2 | 1 = 1 | 1 | 56 | yes | ok |
| 57.a1 | 1 | 1 = 1 | 1 | 15 | yes | ok |
| 44.a1 | 0 | 1 = 1 | 1 | 13 | yes | ok |
| 12144.a1 | 0 | 1 = 1 | 1 | 31 | yes | ok |
| 697691.a1 | 2 | 4 = 4 | 1 | 45 | yes | ok |

**Verdict: NO SPLIT, anywhere.** 17/17 curves balance the identity AND synchronize at the center. Frontier corner occupied: 697691.a1 (rank 2, Sha 4) — the rank≥2 + Sha>1 combination Slice 1 had flagged as untested. Coverage: Sha 1 (x13), 4 (x2), 9 (x2); Tamagawa products to 18 (234446.c1, single factor c_2 = 18); torsion to Z/5; 535 zeros recorded on the line. In-session verifications by Pip (fresh code): 389.a1 (Q=1, all factors), 571.b1 (Sha solved 4), 11.a2 (Delta<0 fix confirmed), 697691.a1 (Sha solved 4.0000000000), 12480.bf1 (Sha solved 9.0000000000).

## 4. EXHIBIT B — RIEMANN PANEL, TEST R1 EXTENDED TO 10^9 (2026-10-31)

Instrument: Schoenfeld (1976) — RH implies |pi(x) − li(x)| < (1/(8 pi)) sqrt(x) ln(x) for x ≥ 2657; ratio r(x) = actual error / envelope; RH requires r < 1. Exact pi(x) by segmented sieve; li(x) = Ei(ln x) at 30-digit precision. Validation: rerun reproduced all nine previously recorded ratios (10^4–10^8) within third-decimal rounding; Pip's independent spot check: pi(10^8) = 5,761,455, r = 0.102925 (identical to the run at six decimals).
Results: **pi(10^9) = 50,847,534 (exact).** Worst ratio in the new decade: **0.102000 at x = 2.2×10^8**; r(10^9) = 0.065234 (error 1,700.96 vs envelope 26,074.64). Worst on the full 10^4–10^9 grid remains 0.468 at 10^4. The worst case holds a ~0.10 plateau while the mean level falls (0.1098 on [10^7,10^8] → 0.0752 on (10^8,10^9]). **The margin is not closing.** Joe's reading (2026-10-31): the plateau "looks like resonance" — checked: in spectral terms an off-axis pole IS a resonance (nonzero width, growing/decaying); the observed modes behave as zero-width pure tones, with local peaks where higher zeros drift into phase.

## 5. EXHIBIT C — LI POSITIVITY PROBE (2026-10-31)

Test: Li's criterion — RH iff lambda_n ≥ 0 for all n ≥ 1, lambda_n = sum over zero pairs of [1 − (1 − 1/rho)^n] = (1/(n−1)!) [d^n/ds^n (s^(n−1) log xi(s))] at s=1. Signal-only: no zero is located.
Two routes: (1) zero sum over 1,026 pairs (top gamma 1449.48877128); (2) Cauchy/DFT derivatives at s=1, 100-digit precision.
**Result: all lambda_n > 0 for n = 1..30 on both routes.** Smallest: **lambda_1 = 0.023095708966121…**; growth is monotone to lambda_30 = 18.5537922908134 (route 2). Route-1 deviations match the smooth-density truncation-tail estimates to three significant figures (checkpoint: lambda_1 dev 7.07e-4, lambda_2 dev 2.83e-3) — drift is the tail, quantified. Pip's independent adjudications: lambda_1 by closed form (1 + gamma_E/2 − ln(4 pi)/2) AND by derivative, agreeing to 60 digits (0.0230957089661210338143…); lambda_2 by an independent Cauchy contour integral: 0.09234573522804667038572848619…

## 6. DEFECT LEDGER (every defect caught by the protocol, with disposition)

1. PARI ellanalyticrank returns the RAW derivative, not divided by r! — caught Oct 30 when route 2 disagreed by exactly 2! on 389a1. Runner divides by r!.
2. PARI elltamagawa folds in the real-component factor — avoided; Tamagawa taken from elllocalred (4th component).
3. Delta<0 period defect (Slice 1): a fresh ellperiods call returned a complex lattice period, corrupting Omega for 11.a2. Fixed: Omega = (2 if disc>0 else 1) × E.omega[1] (LMFDB's own formula); verified against LMFDB for both signs.
4. Label collisions: Cremona 571a1 ≠ LMFDB 571.a1; Cremona 11a1 = LMFDB 11.a2; Cramona/LMFDB 571b1 swap — caught against LMFDB; the Sha-4 anchor is LMFDB 571.b1 (rank 0). Pip's brief premise "571b1 rank 3" was wrong under both systems; corrected in the manifest.
5. Hardy blind half-cell (Slice 2): 234446.b1's 40th positive zero (gamma = 19.983119…) fell in the scan's final half-cell (19.975, 20]; count 39 recorded WITH diagnosis; sign change bracketed directly (Z(19.98) > 0, Z(19.99) < 0). Panel artifact, not a curve property.
6. **Brief defect — lambda_2 checkpoint constant (Pip's, 2026-10-31):** the constant supplied in the probe brief (0.092345735188332) is wrong at the 11th decimal. The agent flagged it under the drop/round rule rather than forcing agreement; adjudicated value lambda_2 = 0.0923457352280466703857… by three computations, plus Pip's independent Cauchy integral. Lesson of record: checkpoint constants from memory are claims too; the checkpoint caught the briefer.
7. P-011/P-012 replication (Oct 31): Pip's first-pass amplitude-fitting decoder collapsed a sign-symmetric pair (∼75% ceiling); faithful fixed-template decoder removed the artifact. Phenomenon confirmed; defect logged.
8. Truncated Tate-limit on 389a1 manufactures a phantom regulator gap that dies geometrically (−2.269 → 0.0000299 by n=8) — Proposal 1's mechanism demonstrated constructively: shallow panels invent gaps.

## 7. DROP / ROUND FLAGS (Joe's rule: flagged, never silently dropped or rounded)

- R1's recorded ratios 0.100 and 0.085 carried no x labels; identified by grid-pattern inference as 2×10^7 and 5×10^7 — INFERENCE, recorded as such; nothing relabeled on its strength.
- LMFDB API special_value (route B) carries ∼38 stored digits but agrees with PARI route A only to ∼28–31 digits; digits beyond that depth are unsupported (worst: 697691.a1, |Q_B − 1| = 5.5e-28).
- Route-1 Li values beyond the per-n drift scale are drift-dominated (∼2–3 significant figures at large n); reported as computed, with drift attached.
- sha_an last digits on four curves read 1 − 1e-29 / 1 − 2e-29 against curvedata's integer sha = 1 (the value used).
- Columbia corroboration digits for 19047851.a1 agree only to 6 figures (30.2857); trailing digits superseded.
- 234446.b1's Hardy 39 is explicitly NOT a drop candidate — it stands with its diagnosis.

## 8. SCOPE — WHAT IS NOT CLAIMED

No proof of BSD, RH/GRH. All ranges are finite and stated (panel: 17 curves, zeros to H=20; R1: x ≤ 10^9 on a stated grid; Li: n ≤ 30). The panel's zero column records zeros FOUND on the line plus consistency counts; lfunzeros searches along the line and does not by construction exclude off-line zeros. The unification criterion is asserted to exist, not exhibited. Corroboration is not proof, and this record does not present it as proof.

## 9. FILE INDEX (all under ~/workspace/bsd-run/ unless noted)

- run-log.md — the canonical running record (Oct 29–31): models, panels, experiments 048/049, P-011/P-012 replication, Scout receipts (quarantined, value-3).
- panel/manifest.md; panel/panel_run.py; panel/results_slice1.md; panel/results_slice2.md; panel/panel_raw_output.json (17 records); panel/panel-verdict-2026-10-31.md.
- riemann_r1_extension.py; riemann_r1_results.md.
- li_probe.py; li_results.md; li_probe_output.json; li_zeros_cache.json.
- Cards: our-equation-2026-10-31.png (+ labeled and legend-v2 variants); riemann-equation-2026-10-31.png; riemann-equation-annotated-2026-10-31.png; li-positivity-2026-10-31.png.
- Experiments: exp048/ (Trial A record), exp049/ (protocol-corrected.md, answer-key-SEALED.txt sha256 0cc1575db539dcf327de30084c8ecc88a037bb5b3f6564c10e8dbd88bd215b65, channel.md, log-A.md, log-B.md, results package — verdict LEVEL 3, the maximum attainable under the corrected protocol).
- This file: consolidated-record-2026-10-31.md.

---
Record locked 2026-10-31 ~19:45 MST. — J.M.C. / Pip

**Attestation (added 2026-10-31 ~20:11 MST, at Joe's direction):** The computations reported in this record were executed under the direction of Joseph M. Carroll and verified in-session before reporting — the panel anchor recomputations (389.a1, 571.b1, 11.a2, 697691.a1, 12480.bf1), the Riemann R1 spot check at 10^8, and the independent adjudications of lambda_1 and lambda_2. I answer for those verifications.
— **Pip Willow**, computational collaborator, Red Willow Ventures (surname given by J.M. Carroll, 2026-10-31)

---

## RECORD CORRECTIONS

- **2026-11-06 (Joe's ruling):** Section 8, first sentence. Struck: ", or any implication between them." The sentence now reads: "No proof of BSD, RH/GRH." Reason: the record DOES assert an implication between the two readings — as the conjecture of Section 1. What is not claimed is a PROOF of it; the original sentence swept the conjectured implication itself into the not-claimed bucket, which misstates the house position. Copies distributed before this date (the October 31 – November 6 mailings) carry the original sentence; this correction governs the record from 2026-11-06 forward. Same ruling applied the same day to the parallel sentence in Section 1 ("No proof of BSD or of GRH is asserted anywhere in this record."), to the plain-text copy of this record, and to the three parallel sentences in the paper draft (draft-v1).
