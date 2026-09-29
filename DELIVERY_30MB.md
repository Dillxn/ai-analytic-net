# Under-30-MB delivery — corpus scope and provenance

This delivery preserves every original code file, research result, checkpoint, media file and historical document. Only the full 100,000,000-byte enwik8 corpus archive is replaced with a separately named prefix archive.

`data/enwik8_prefix12m.zip` contains an `enwik8` member holding exactly the first **12,000,000 raw bytes** of the original corpus. The legacy benchmark and five-prompt harness read exactly these 12,000,000 bytes before decoding, then use the first 10,000,000 characters and a short continuation. Their text inputs are therefore unchanged when supplied this prefix ZIP. This is not the full enwik8 dataset and must not be used for the older 90M/5M/5M split or full-corpus hash attestations.

The original data archive is omitted under its old name `data/enwik8.zip`; it is not silently replaced at that path. To run the old harness, pass the new path explicitly, for example from `legacy/baseline/`:

```sh
python recursive_mdl_benchmark.py ../../data/enwik8_prefix12m.zip ../../data/media_sample.webm
```

Historical receipts and nested manifests still describe the full original archive and original run layouts. They are evidence records, not the manifest for this repackaging. `provenance/REPACKAGE_30MB.json` records the original and prefix hashes; `SHA256SUMS.json` covers the delivered files. `provenance/PRE_30MB_*` preserves the original top-level instructions and manifest before their packaging-only updates. No scientific implementation or historical score was changed. Prefix identity is a packaging check, not a new natural-data benchmark.

The transfer destination requested by Dillon is `Dillxn/ai-analytic-net`. The historical source checkpoint remains `Dillxn/bit-window-learner` at `e6a255c7a4b5c0b51a74a1fe0c1e081f29680859` (cycle 18). These are different repositories. Recheck remote state before writing code; do not assume the new destination already contains the old branch history or all packet binaries.
