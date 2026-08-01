# Upload instructions for AISKG_02_Framework

## Recommended Git command workflow

```bash
git clone https://github.com/romenmeitei/AISKG_02_Framework.git
cd AISKG_02_Framework
# Copy all files from this upload-ready directory into the clone, preserving
# the reference_outputs/ directory.
python verify_repository.py
git add -A
git commit -m "Complete Section 2 reproducibility release"
git push origin main
```

## Required additions/replacements

Upload or overwrite every file in this directory. In particular, the current
public repository is missing:

- `GITHUB_UPLOAD_CHECKLIST.md`
- `MANUSCRIPT_CORRECTIONS_REQUIRED.md`
- `reference_outputs/Mushroom_KG_Complete_Reproducibility_Outputs_Reference.zip`
- finalized citation and licensing files

After upload, execute:

```bash
python verify_repository.py
```
