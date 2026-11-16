# One Property, Two Readings — A Pre-Registered Claim That BSD and Riemann Are One Property

**Version 2.** This version revises the record in answer to a reader's critique, which the authors thank. The critique was right in its particulars, and the revision is built on the tests it demanded. Version 1 (published 2026-11-07) remains published and frozen; nothing in it is withdrawn or silently altered.

**The claim:** for an elliptic curve E over the rationals, the Riemann hypothesis for L(E, s) and the Birch and Swinnerton-Dyer leading-coefficient identity are not two facts. They are two readings of a single property of L(E, s): the object is synchronized at its symmetry center. A positivity criterion of signal-only type, in the family of Weil's criterion and Li's criterion, is conjectured as the property from which both readings follow. Prediction: no curve separates them — any E satisfying one satisfies the other.

**Status:** the implication between the two readings is CLAIMED — made outright. This record presents the claim, its measurements, and the named location of the one open step; it stops where the record stops — by design, not by failure.

## What's here

- `poster.pdf` / `poster.txt` — the one-sheet summary: the claim, the 17-curve panel data, the verdict, the defects. The text edition carries the same words and numbers, set narrow for screens. (Carried over from Version 1, unchanged.)
- `consolidated-record-V2.md` / `consolidated-record-V2.pdf` — the full Version 2 record: the claim; what changed in Version 2 and why (§0); the working model; the rebuilt panel — zero counts by argument-principle (Turing-method) counts, 535 zeros independently counted for the 17 panel curves; Mordell–Weil ranks proved by 2-descent on all 17 curves with no L-function input; the 2-part of Sha determined by descent on all 17; the 3-part of Sha for 133584.bt1 determined by a Magma 3-Selmer computation (order 9); one cell open — the 3-part of Sha for 12480.bf1, untested for lack of access to Magma and printed under an analytic label; the function-field bench test (verdict O-2: the transport reduces at one named ingredient, Tate's conjecture at sub-step C4); the complete defect ledger; and the scope section (§9).
- `verification-scripts.zip` — the scripts that recompute the record's numbers from public inputs (LMFDB data, PARI/GP): the panel quotient measurements, the lambda-coefficient probes and sequence, the panel runner, and the pi(x)/Schoenfeld sieve. A README inside the archive describes each script. No other code is needed to check any number in the record. (Carried over from Version 1, unchanged.)

## How to check it

Everything in the record can be recomputed. The curves are named by their LMFDB labels; the routes are named in the record (PARI/GP `lfun` machinery, `ellrank` descent, height pairings, local data), precisions are stated, and the expected answers are printed in the record itself — including the one diagnosed defect (234446.b1, Hardy cross-count 39/40, bracketed and explained). One curve re-runs inside an hour; the whole panel in an afternoon.

## Corrections

The record corrects itself in the open. A dated RECORD CORRECTIONS appendix at the end of the consolidated record lists every post-release change. Entries: 2026-11-06 — the record's assertion of the implication between the two readings was restored where an earlier sentence had swept it into the not-claimed bucket (stands as history). 2026-11-14 — the scope sentences were reworded into the house stating form: the claim is stated outright, and the record's stop is stated as design rather than denial; the scope itself is unchanged. Version 2's subtitle was corrected at the same direction (2026-11-15): the attempt is complete, and the subtitle now states its outcome — the claim.

## Who we are

Red Willow Ventures LLC, Green Valley, Arizona — a small independent research team. We circulated this record to the field by letter beginning November 2026 because the checks matter more than the credit. If you run the checks and find the separation we could not, we want to hear it: a refutation is as useful to us as a confirmation, and it will be kept on the record the same way.

Contact: redwillowventures@proton.me
