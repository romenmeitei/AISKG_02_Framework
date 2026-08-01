# GitHub upload checklist

1. Upload the files in this package to the repository root.
2. Keep `Mushroom_KG_Complete_Reproducibility_Pipeline_v2.ipynb` as the only canonical manuscript-reproduction notebook in the root.
3. Upload the cleaned `Mushroom_KG_Reproducibility_Inputs_v2.zip`; do not replace its reviewer workbooks with the original externally linked versions.
4. Put upstream generation notebooks under `notebooks/upstream/` and superseded notebooks under `archive/legacy_notebooks/`.
5. Add a clear archive notice so legacy stored outputs are not interpreted as authoritative.
6. Open the canonical notebook in Colab, select **Run all**, and confirm `PIPELINE_SUCCESS.txt` and 94 PASS checks.
7. Apply every item in `MANUSCRIPT_CORRECTIONS_REQUIRED.md` before submission.
8. Confirm that the GitHub Data Availability statement points to the public release rather than a personal or broken URL.
9. Create a numbered release (for example, `v2.0.0`) and archive it with Zenodo or another DOI-issuing repository.
10. Cite the permanent software/data release in the manuscript and preserve the release used for peer review.
11. Add a license only after all authors and the institution approve the reuse terms.
