# Results-alignment notes

The canonical pipeline reproduces the audited manuscript-facing values below.
The corrected manuscript should use these definitions and values consistently.

## Network overlap

For 191 co-occurrence pairs, 86 evidence-filtered semantic pairs, and 38 shared
pairs, the pair-set Jaccard coefficient is:

```text
38 / (191 + 86 - 38) = 0.158996 ≈ 0.159
```

## Entity benchmark

The primary audited corrected reference contains 294 valid concepts. The five
rejected `(blank)` correction records are retained only in a labelled legacy
sensitivity calculation.

- proposed framework: 294/294 valid corrected concepts;
- frozen scispaCy recovery: 292/294;
- candidate-level expert precision: 290/300.

## Relation benchmark

- relation correctness and exact corrected directed triple: 163/220 (74.1%);
- relation-bearing gold set: 184 triples;
- type-pair exact matches: 163/220 across all candidates and 163/184 among
  relation-bearing candidates;
- sentence co-occurrence baseline: precision 0.800, recall 0.540, F1 0.645;
- paired McNemar exact P = 1.000 for the proposed and type-pair exact outcomes.

## Graph filters

The aggregate semantic graph applies `support_documents >= 2` and contains 86
directed edges. Period-specific temporal graphs include all unique triples in
each period, so a temporal graph can contain more than 86 edges.

## Pathway endpoints

Keep the two 52-pathway datasets separate:

- 11/52 correct: independently reviewed pre-refinement candidate pathways;
- 52 clean pathways with R² ≈ 0.814: post-refinement outcome-aware set used for
  score–stability analysis.

## Held-out review provenance

The S4 second review is AI-assisted. It is a sensitivity/adjudication audit and
must not be described as independent dual-human validation.
