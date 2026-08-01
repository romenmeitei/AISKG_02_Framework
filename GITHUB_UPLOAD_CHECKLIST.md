# Public-release checklist — Section 2

- [ ] Upload every file and preserve `reference_outputs/` and
  `.github/workflows/`.
- [ ] Confirm the Colab badge opens the current repository notebook.
- [ ] Run `python verify_repository.py`.
- [ ] Run the canonical notebook and confirm 94 PASS checks and
  `PIPELINE_SUCCESS.txt`.
- [ ] Confirm the manuscript uses the values in `RESULTS_ALIGNMENT_NOTES.md`.
- [ ] Confirm S4 is described as AI-assisted sensitivity/adjudication.
- [ ] Confirm the copyright statement is compatible with institutional and
  contributor agreements.
- [ ] Create GitHub release `v2.0.0` and archive it with a DOI.
- [ ] Add the DOI to `CITATION.cff` and the manuscript.
