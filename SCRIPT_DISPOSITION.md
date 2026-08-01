# Disposition of the earlier scripts

The public repository should present one authoritative workflow. Historical notebooks should be retained for provenance but moved out of the repository root.

| Earlier notebook | Disposition | Reason / material retained in v2 |
|---|---|---|
| `NLP_Mushroom_2026.ipynb` | Keep under `notebooks/upstream/` | Literature retrieval and early corpus processing; not needed for the deterministic validation rerun. |
| `NLP_Mushroom_2026_Stage_II.ipynb` | Keep under `notebooks/upstream/` | Upstream topic/corpus generation provenance. |
| `Mushroom_Knowledge_Graph_Stage_IV_VIII.ipynb` | Keep under `notebooks/upstream/` | Initial entity/relation extraction and graph construction provenance. |
| `Mushroom_KG_Advanced_Q1_Analyses.ipynb` | Keep under `notebooks/upstream/` | Exploratory and manuscript-generation analyses; final relevant metrics are recomputed by v2. |
| `Mushroom_StageV_Advanced_Knowledge_Discovery.ipynb` | Archive | Motif/exploratory modules not reported in the final manuscript were excluded; relevant graph summaries were rebuilt. |
| `Mushroom_StageVI_Semantic_Validation.ipynb` | Archive as superseded | Validation logic was folded into the canonical pipeline. |
| `Mushroom_StageVII_Outcome_Aware_Validation.ipynb` | Archive as superseded | Outcome reclassification, edge filtering, pathway reconstruction, and score–stability analysis were merged. The unsupported hard-coded 47/52 review result was discarded. |
| `Mushroom_StageVIII_Enhanced_Validation.ipynb` | Archive as superseded | Fixed 300/220/52 samples, dual review, adjudication, kappa, AC1, bootstrap, and Wilson analyses were merged. Unstable Python `hash()` sampling was replaced by SHA-256 stable seeding for future samples. |
| `Statistics.ipynb` | Keep under `notebooks/upstream/` or archive | Final manuscript statistics are recomputed in v2; retain only for provenance if it documents other analyses. |
| `Conventional_Cooccurrence_Analysis_Mushroom_Poisoning.ipynb` | Archive as superseded | Co-occurrence construction, thresholding, overlap, Jaccard, node metrics, and plotting were merged and corrected. |
| `ESWA_Biomedical_NLP_Benchmark_CORRECTED.ipynb` | Archive | Superseded benchmark version. |
| `ESWA_Biomedical_NLP_Benchmark_V4.ipynb` | Archive | Superseded benchmark version. |
| `ESWA_Biomedical_NLP_Benchmark_V4_1_FIXED (2).ipynb` | Archive; optional live audit only | Human-audited held-out projection/evaluation logic was merged. Live SciSpacy/PubTator3 calls are intentionally excluded from the zero-download path. |
| `ESWA_Expert_Validation_Analysis_v2_Key_Based.ipynb` | Archive as superseded | Key-based S4 adjudication and conservative sensitivity logic were merged. |
| `ESWA_Ontology_Aware_Relation_Addon.ipynb` | Archive as superseded | Deterministic alias and ontology-aware endpoint resolution were merged. |
| `ESWA_Toxin_Research_Representation_Analysis (1).ipynb` | Archive as superseded | Toxin mapping, representation, concentration, entropy, composite scores, and priority ranking were merged. |
| `Mushroom_NLP_KG_Benchmarking_Complete_GoogleColab (1).ipynb` | Archive | Older candidate benchmark; audited denominator and adjudication corrections are implemented in v2. |

## Do not permanently delete provenance

“Discard” here means **do not use as an authoritative manuscript-reproduction path**. Preserve the original notebooks in an archive branch or `archive/legacy_notebooks/`, ideally with read-only tags, so the development history remains inspectable.
