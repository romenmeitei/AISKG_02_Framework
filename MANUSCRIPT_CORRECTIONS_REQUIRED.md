# Manuscript corrections required before repository release

The complete pipeline includes a consistency audit. The following values should be checked and corrected consistently in the abstract, Methods, Results, tables, captions, Discussion, and supplementary files.

## 1. Pair-set Jaccard

For 191 co-occurrence pairs, 86 evidence-filtered semantic pairs, and 38 shared pairs:

```text
Jaccard = 38 / (191 + 86 - 38) = 38 / 239 = 0.158996
```

Use **0.159**, not 0.122.

## 2. Candidate entity reference denominator

Five rejected records with a literal `(blank)` correction do not constitute real corrected concepts.

- audited corrected reference: **294** concepts;
- proposed recovery: **294/294**;
- frozen SciSpacy recovery: **292/294**;
- legacy-compatible reference: **299**, proposed 299/299, SciSpacy 292/299.

Report the audited analysis as primary or explicitly justify the legacy denominator. Do not conflate reference-concept recovery with candidate precision (290/300).

## 3. Relation correctness

Correctness and directionality must be adjudicated separately.

- relation correctness: **163/220 (74.1%)**;
- exact match to the final corrected directed triple: **163/220 (74.1%)**.

Do not report 169/220 unless a different, explicitly defined endpoint is introduced.

## 4. Relation-bearing denominator and baselines

- relation-bearing original-or-corrected gold triples: **184**, not 213;
- type-pair exact matches: 163/220 across all candidates and **163/184** among relation-bearing records;
- sentence co-occurrence baseline: precision **0.800**, recall **0.540**, F1 **0.645**, 110 predicted-positive records;
- proposed and type-pair exact-triple outcomes are identical over the paired candidate set; McNemar exact P = 1.000.

## 5. Aggregate versus temporal graphs

The aggregate semantic graph uses `support_documents >= 2` and contains 86 directed edges. The temporal graphs include all unique period-specific triples; therefore the 2020–2025 graph can contain 114 edges. State the different filtering rules explicitly.

## 6. Pathway endpoints

Keep these separate:

- initial pre-refinement expert validation: **11/52** pathways correct;
- post-refinement outcome-aware set: **52** clean pathways, score–stability R² ≈ **0.814**.

## 7. Held-out S4 provenance

The S4 second review is AI-assisted. Describe it as an **AI-assisted sensitivity/adjudication audit**, not independent dual-human expert validation.

## 8. Optional held-out entity results

When the 150-sentence entity evaluation is added to the manuscript, the proposed framework gives:

- common CHEMICAL/DISEASE schema: precision **0.927**, recall **0.985**, F1 **0.955**;
- full-domain descriptive evaluation: precision **0.946**, recall **0.830**, F1 **0.884**.

External model comparisons should be reported only from a separately frozen, fully auditable prediction set or from a clearly versioned live environment.
