# One Property, Two Readings

A pre-registered attempt to separate BSD and Riemann — and the record of its failure to separate them.

**The claim (a conjecture, stated as such):** for an elliptic curve E over the rationals, the Riemann hypothesis for L(E, s) and the Birch and Swinnerton-Dyer leading-coefficient identity are not two facts. They are two readings of a single property of L(E, s): the object is synchronized at its symmetry center. A positivity criterion of signal-only type, in the family of Weil's criterion and Li's criterion, is conjectured as the property from which both readings follow. Prediction: no curve separates them — any E satisfying one satisfies the other.

**Status:** conjecture. No proof of BSD, of RH/GRH, or of the implication between them is claimed. What is offered is evidence, gathered under a pre-registered failure-hunt protocol in which any mismatch was treated as a defect in our own panel until proven otherwise.

## What's here

- `poster.pdf` / `poster.txt` — the one-sheet summary: the claim, the 17-curve panel data, the verdict, the defects. The text edition carries the same words and numbers, set narrow for screens.
- `consolidated-record.md` / `consolidated-record.pdf` — the full record: the claim, the working model, the failure-hunt panel (17 curves, ranks 0–5; BSD quotient Q = 1 by two independent L-value routes at 50-digit precision on every curve; Sha solved from the identity and matched against tabulated values; 535 zeros recorded on the critical line to height 20), the Riemann panel (Schoenfeld envelope test extended to 10^9), the Li-family positivity probes, a blind replication with a hash-committed answer key, the complete defect ledger, and the scope section stating what is not claimed.
- `verification-scripts.zip` — the scripts that recompute the record's numbers from public inputs (LMFDB data, PARI/GP): the panel quotient measurements, the lambda-coefficient probes and sequence, the panel runner, and the pi(x)/Schoenfeld sieve. A README inside the archive describes each script. Other working code — test construction and exploratory apparatus — exists and is being held pending independent verification of the record; it will be released after that verification. None of it is needed to check any number in the record.

## How to check it

Everything in the record can be recomputed. The curves are named by their LMFDB labels; the routes are named in the record (PARI/GP `lfun` machinery, `ellanalyticrank`, height pairings, local data), precisions are stated (50 digits), and the expected answers are printed in the record itself — including the one diagnosed defect (234446.b1, Hardy cross-count 39/40, bracketed and explained). One curve re-runs inside an hour; the whole panel in an afternoon.

## Corrections

The record corrects itself in the open. A dated RECORD CORRECTIONS appendix at the end of the consolidated record lists every post-release change. Current entry: 2026-11-06 — the scope sentence in Section 8 now reads "No proof of BSD, RH/GRH." (an earlier wording swept the conjectured implication itself into the not-claimed bucket; the implication is the conjecture — what is not claimed is a proof of it).

## Who we are

Red Willow Ventures LLC, Green Valley, Arizona — a small independent research team. We circulated this record to the field by letter beginning November 2026 because the checks matter more than the credit. If you run the checks and find the separation we could not, we want to hear it: a refutation is as useful to us as a confirmation, and it will be kept on the record the same way.

Contact: redwillowventures@proton.me
