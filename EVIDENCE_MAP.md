# Evidence and execution map

Read the main handoff first. This bundle merges original local run packets and adds byte-verified cycle-18 source fetched from GitHub. It is not a complete Git checkout; root `history/cycleNN` snapshots can be stale and must not override the main handoff.

## Fast navigation

| Question | Start with these files |
|---|---|
| Exact assignment and constraints | `OPUS_5_5_ANALYTICAL_LEARNER_HANDOFF.md` |
| Original goals, baseline limitations, prompt outputs | `legacy/ULTRA_ANALYTICAL_LEARNER_HANDOFF.md`, `legacy/evidence/` |
| Useful whole-query operators versus invalid or unstable extrapolation | `research/operator_validity/REPORT.md`, `POSITIVE_APPROXIMATION_REPORT.md`, `CYCLE4_REPORT.md`, `CYCLE5_REPORT.md` |
| Exact/noisy joint relation discovery and degree/frequency failures | `research/joint_relations/CYCLE6_REPORT.md`, `CYCLE7_REPORT.md`, corresponding tests |
| Why empirical tensor compression failed | `research/sparse_born/CYCLE8_REPORT.md`, `adversary.py` |
| Small neural specimen and causal tests | `research/neural_microscope/README.md`, `extension/RESULTS.json`, `research/neural_mechanism/CYCLE10_REPORT.md` |
| Attention decomposition and why it still needs learned weights | `research/attention_kernel/CYCLE11_REPORT.md`, `label_kernel.py` |
| Support-only interaction selection | `research/interaction_selection/CYCLE12_REPORT.md` |
| Program proposal experiment and attribution failure | `research/program_discovery/REPORT.md`, `EXPORT_AUDIT.json`, `selected_learner.py` |
| Most useful raw-bit nuisance adversary | `research/translation_quotient/REPORT.md`, `coverage_audit.py`, `COVERAGE_RESULTS.json` |
| External image/source audit; missing checkpoint | `research/modular_extraction_audit/REPORT.md`, `SOURCE_NOTES.json` |
| Clean opaque-symbol fitting / brittle exact constraints | `research/opaque_symbol_relations/REPORT.md`, `learner.py`, `adversary.py` |
| Noise repair / conditional certificates / sparse failure | `research/rectangle_consensus/REPORT.md`, `learner.py`, `adversary.py`, `assumption_audit.py` |
| Latest: reliability layer and coverage cost | `research/validated_selection/REPORT.md`, `learner.py`, `test_learner.py`, `experiment.py`, `adversary.py` |
| Older theoretical arguments including narrow Lean reports | `history/Analytical_Learning_Research_Ledger.md` — search selectively |

## Actual data and neural weights

`data/media_sample.webm` is the unchanged original upload. `data/enwik8_prefix12m.zip` contains exactly the first 12,000,000 raw bytes of the original enwik8 member; the full corpus ZIP is omitted. This preserves the input consumed by the existing 10-million-character smoke harness, not a full-corpus experiment. See `DELIVERY_30MB.md`. The legacy handoff documents decoding and exact hashes. The baseline script's relative imports require running from its own directory. Decode the media before learning; do not treat a compressed container as equivalent to PCM/frame observations.

Our small research model is present at `research/neural_microscope/extension/selected_model.pt`, SHA-256 `ad2fdadadb1e968ed2521896d307797b9e299cbbf989e571e4a45fdb5c0e22b8`. Other `.pt` checkpoints and raw neural predictions are included. The absent external `addition_s0.pt` is a different model; do not confuse them.

## Start cheaply

Run from the packet root:

```sh
python verify_bundle.py
python quick_checks.py
```

`quick_checks.py` runs only the three recent standard-library unit suites, in separate processes to avoid their common module names colliding. It does not run the full experiment sequence or overwrite original result JSON. Unit success verifies copied code/plumbing, not a master-learning claim.

For source-specific work, run from the corresponding module directory:

```sh
# Clean symbol presentation
cd research/opaque_symbol_relations
python -m unittest -v test_learner
# Optional independent HNF comparator uses SymPy:
python oracle_check.py

# Noisy symbolic control
cd ../rectangle_consensus
python -m unittest -v test_learner
# experiment.py writes RESULTS.json; preserve original before rerunning:
python experiment.py
python adversary.py
python assumption_audit.py

# Latest independent calibration/audit
cd ../validated_selection
python -m unittest -v test_learner
python experiment.py
python adversary.py
python audit_export.py
```

Do not run these all just to orient yourself. The last three cycle-18 commands regenerate raw files that were not available in the supplied original run archives. New runs have their own timestamps, hardware and provenance; do not relabel them as the prior run.

Neural scripts require PyTorch/NumPy; use their recorded dependency files and small checkpoint, not a large downloaded model. FFmpeg is needed only for media decoding. A direct source-download attempt during packaging failed DNS; the GitHub connector reads succeeded. Do not assume the next runtime has the same connectivity or packages.

## Current repository reference

```text
Dillxn/bit-window-learner
research/independent-reliability-audit
PR #18 — open, draft, unmerged at packaging read
e6a255c7a4b5c0b51a74a1fe0c1e081f29680859
```

The prior cycle-17 branch is `research/noisy-rectangle-consensus` at `e3c37957ae5aad04495eb8fb1bf0f273d21b7099`. Branches are stacked. Check the current head before edits. This handoff preparation did not write to or merge the historical `Dillxn/bit-window-learner` source repository. Written transfer instructions are now being added to the separately requested `Dillxn/ai-analytic-net` repository; its source history and the packet binaries are not implicitly migrated.

## Provenance and limits of this package

`provenance/ARCHIVE_INPUTS.json` lists original archives and their hashes. `EXTRACTION_INDEX.json` maps extracted files to original paths. Only one overlapping raw filename had different bytes; both versions are preserved and indexed in `SUPERSEDED_FILES.json`. No scientific source change was made when flattening archive paths.

`provenance/CYCLE18_SOURCE_VERIFICATION.json` matches all seven latest Python files, plus the latest report, to their Git blob hashes. The two base implementations are unchanged copied sources. Original cycle-18 raw full results/clock receipts were not available locally; only the source and report were retrieved here. Historical measurements quoted from cycle 18 are repository-reported unless a new explicitly labeled rerun is provided.

The historical ledger is a Library version retrieved during packaging, not a new proof audit. Its earlier narrow Lean claims are not upgraded to current general guarantees. Later reports of missing Lean executables describe those environments, not the whole project's proof history.

`PACKAGING_CHECKS.json` records this handoff's own integrity and small test checks. It must not be used as a new multimodal benchmark or as independent replication of all historical scores. `SHA256SUMS.json` covers every delivered file except itself. Run verification before changing files; reruns that write reports will legitimately change hashes.

The original reports retain their historical “0%” strings. The main handoff explicitly supersedes that progress-reporting convention without altering evidence.

Old manifests and absolute `/mnt/data/...` paths describe their original run layouts. They are preserved for provenance and may not resolve directly after flattening. Use this packet’s `SHA256SUMS.json` and current relative paths; do not spend research time chasing stale sandbox links.
