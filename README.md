# AISKG Section 2 — post-extraction analysis and validation

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/romenmeitei/AISKG_02_Framework/blob/main/Mushroom_KG_Complete_Reproducibility_Pipeline_v2.ipynb)

This repository contains the canonical deterministic workflow for all
manuscript-facing post-extraction analyses. The upstream literature retrieval,
topic modelling, and ontology-guided extraction workflow is in
[AISKG Section 1](https://github.com/romenmeitei/AISKG_01_Framework).

## Canonical notebook

`Mushroom_KG_Complete_Reproducibility_Pipeline_v2.ipynb`

The notebook uses one checksum-verified input ZIP and generates one complete
results ZIP. It does not call live bibliographic APIs, retrain BERTopic,
download biomedical NLP models, or depend on external Excel links.

## Analyses reproduced

- corpus, thematic, trend, chi-square, and diversity statistics;
- semantic-edge reaggregation, graph filtering, centrality, communities, and
  temporal graph analysis;
- outcome-aware pathway refinement and stability regression;
- blinded validation of 300 entities, 220 relations, and 52 pre-refinement
  pathways, including Cohen's kappa, Gwet's AC1, bootstrap intervals,
  adjudication, and Wilson intervals;
- candidate-level and 150-sentence held-out biomedical NLP benchmarks;
- sentence co-occurrence and type-pair baselines with McNemar analysis;
- conventional co-occurrence network and semantic-pair overlap;
- toxin representation, HHI, entropy, composite scores, and priority ranking;
- manuscript consistency and 94 fixed-result checks.

## Run in Google Colab

1. Open the notebook using the badge above.
2. Select **Runtime → Run all**.
3. The notebook downloads `Mushroom_KG_Reproducibility_Inputs_v2.zip` from this
   repository when possible; a manual upload fallback is available.
4. Download `Mushroom_KG_Complete_Reproducibility_Outputs.zip`.

The Section 1 bridge ZIP is also accepted when uploaded manually.

## Interpretation safeguards

- The 11/52 expert-validation result and the separate 52-pathway
  score–stability dataset are different endpoints.
- The S4 second review is AI-assisted sensitivity/adjudication, not independent
  dual-human validation.
- The audited pair-set Jaccard value is 0.159.
- The audited relation correctness is 163/220 (74.1%).
- The primary corrected entity reference contains 294 valid concepts.

See `RESULTS_ALIGNMENT_NOTES.md` for definitions and values.

## Key files

| Path | Purpose |
|---|---|
| `Mushroom_KG_Complete_Reproducibility_Pipeline_v2.ipynb` | Canonical Colab workflow |
| `Mushroom_KG_Reproducibility_Inputs_v2.zip` | Frozen checksum-verified input bundle |
| `pipeline_core.py` | Matching command-line implementation |
| `requirements.txt` | Compatible dependency ranges |
| `expected_results.json` | Fixed numerical expectations |
| `reference_outputs/` | Tested reference output archive |
| `TEST_STATUS.md`, `TESTED_ENVIRONMENT.txt`, `RELEASE_VALIDATION_REPORT.md` | Test evidence |
| `RESULTS_ALIGNMENT_NOTES.md` | Audited result definitions |
| `SCRIPT_DISPOSITION.md` | Legacy-script consolidation record |
| `PACKAGE_MANIFEST.csv`, `PACKAGE_CHECKSUMS.sha256` | File inventory and hashes |
| `CITATION.cff` | Machine-readable citation metadata |
| `LICENSE`, `COPYRIGHT.md`, `DATA_LICENSE.md` | Rights and reuse terms |

## Verify locally

```bash
python verify_repository.py
sha256sum -c PACKAGE_CHECKSUMS.sha256
```

## Run locally

```bash
unzip Mushroom_KG_Reproducibility_Inputs_v2.zip -d extracted_inputs
INPUT_DIR=$(dirname "$(find extracted_inputs -name input_checksums.csv -print -quit)")
python pipeline_core.py --input-dir "$INPUT_DIR" --output-dir outputs
```

## Release and citation

This publication package is version **2.0.0**. Create the GitHub release tag
`v2.0.0`, archive it in a DOI-issuing repository, and then add the DOI to
`CITATION.cff` and the manuscript. Original software is MIT-licensed.
