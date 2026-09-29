# ai-analytic-net

## Analytical learner — Opus research handoff

Start with **[OPUS_5_5_ANALYTICAL_LEARNER_HANDOFF.md](OPUS_5_5_ANALYTICAL_LEARNER_HANDOFF.md)**, then [EVIDENCE_MAP.md](EVIDENCE_MAP.md). The assignment is an independent attempt at observation-to-reusable-computation discovery, not another extension of the latest symbolic model by inertia.

The historical source is `Dillxn/bit-window-learner`, pinned at `e6a255c7a4b5c0b51a74a1fe0c1e081f29680859` (cycle 18, `research/independent-reliability-audit`). This new destination does not automatically contain that repository's branch history.

### What is stored here

The complete written handoff, evidence map, corpus-scope explanation and attachment metadata are committed to this repository. The runnable offline packet is supplied separately in Dillon's ChatGPT conversation; **the binary ZIP is not uploaded here**. Paths under `research/`, `legacy/`, `history/` and `data/` in the handoff refer to the offline packet unless explicitly identified as historical GitHub paths.

### Attachment below the 30 MB limit

`Opus_5_5_Analytical_Learner_Under30MB.zip`

- Size: **23,522,523 bytes (23.52 MB)**, below 30,000,000 bytes.
- SHA-256: `650b7887eb6527d53de5e3bd92773742e4cb84974680a1494474fa96d3c5f96f`.
- Contains all original research source, results, checkpoints, media and historical documents. All 799 original files outside the explicitly updated top-level instructions/manifest and corpus archive were checked byte-for-byte. The new complete manifest verifies 811 files; the ZIP contains 812 entries including that manifest.
- The full enwik8 archive is replaced with a separately named ZIP holding the exact first **12,000,000 raw bytes**. The old smoke harness reads that exact prefix before fitting its 10-million-character corpus, so those inputs are unchanged. This packet is not suitable for full-100MB corpus hash checks or later full-corpus splits.

Read [DELIVERY_30MB.md](DELIVERY_30MB.md) and [HANDOFF_ATTACHMENT.json](HANDOFF_ATTACHMENT.json) for the explicit boundaries. After extracting the separate packet, run from its root:

```sh
python verify_bundle.py
python quick_checks.py
```

Verification checks packaging and small implementation regressions, not a scientific breakthrough. Preserve historical results before running scripts that overwrite their output files. The handoff replaces misleading progress percentages with actual capability, assumption and regression reporting.
