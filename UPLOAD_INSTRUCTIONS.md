# Upload instructions — AISKG_02_Framework

```bash
git clone https://github.com/romenmeitei/AISKG_02_Framework.git
cd AISKG_02_Framework
# Copy all files from the upload-ready folder here, preserving directories.
python verify_repository.py
git add -A
git commit -m "Complete reproducibility release v2.0.0"
git push origin main
git tag -a v2.0.0 -m "Publication reproducibility release v2.0.0"
git push origin v2.0.0
```

The upload must include `reference_outputs/`, `.github/workflows/`, licensing
files, citation metadata, and the generated manifest/checksum files.
