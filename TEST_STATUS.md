# Test status

The final self-contained notebook and the matching `pipeline_core.py` were tested with the supplied input bundle.

## End-to-end notebook test

- Notebook: `Mushroom_KG_Complete_Reproducibility_Pipeline_v2.ipynb`
- Code-cell execution errors: **0**
- Observed local execution time: **34.4 seconds**
- Generated output files: **61**
- Input SHA-256 checks: **22 passed**
- Workbook/sample-manifest preflight checks: **6 passed**
- Fixed numerical result checks: **94 passed**
- Success marker: `PIPELINE_SUCCESS.txt` created

## Determinism test

Two fresh command-line runs produced the same 61 output filenames and byte-identical SHA-256 hashes for all 61 files. The self-contained notebook run produced outputs byte-identical to the command-line reference run.

Sub-machine-precision centrality summation noise is rounded before tied-rank calculation, preventing fresh Python sessions from changing the centrality CSV or consolidated workbook. ZIP entry timestamps and Excel metadata are fixed.

## Tested environment

- Python: 3.13.5 (main, May  5 2026, 21:05:52) [GCC 14.2.0]
- NumPy: 2.3.5
- pandas: 2.2.3
- SciPy: 1.17.0
- scikit-learn: 1.8.0
- statsmodels: 0.14.6
- NetworkX: 3.6.1
- Matplotlib: 3.10.8
- openpyxl: 3.1.5
- XlsxWriter: 3.2.9

## Compatibility statement

The notebook installs only dependencies that are missing and avoids forced downgrades. No software can guarantee compatibility with every future Colab image, but the default workflow has removed the known failure sources: live APIs, model downloads, external Excel links, unstable built-in hashing, manual path edits, and unverified input versions. Schema/checksum failures stop early with explicit messages.

## Upload-ready release validation

The repository-specific Colab badge, Section 1 link, and automatic companion-ZIP
download fallback were added. Every code cell in the updated notebook was then
compiled and executed sequentially in a clean working directory with the
packaged input ZIP. The run completed successfully in approximately 32 seconds,
created `PIPELINE_SUCCESS.txt`, generated 61 outputs, and passed all 94 fixed
result checks. The generated output ZIP was byte-identical to the packaged
reference archive.

## Upload-ready release validation

The repository-specific Colab badge, Section 1 link, and automatic companion-ZIP
download fallback were added. Every code cell in the updated notebook was then
compiled and executed sequentially in a clean working directory with the
packaged input ZIP. The run completed successfully in approximately 32 seconds,
created `PIPELINE_SUCCESS.txt`, generated 61 outputs, and passed all 94 fixed
result checks. The generated output ZIP was byte-identical to the packaged
reference archive.

