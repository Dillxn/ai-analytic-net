# Opus 5.5 handoff: solve observation-to-reusable-computation discovery

Prepared for Dillon Riecke, 2026-09-29. **Read this first.** This supersedes the research assignment and progress framing in older packet checkpoints; it does not overwrite their evidence. You are receiving working restricted algorithms and substantial negative evidence, not a nearly completed master learner.

## Delivery update: size-limited transfer

The destination requested by Dillon is **`Dillxn/ai-analytic-net`**. This document retains the historical source references below; those references do not imply the destination already contains the original branch history. The accompanying size-limited packet contains all original source/evidence/checkpoints/media, but only the **first 12,000,000 raw bytes** of enwik8, in `data/enwik8_prefix12m.zip` with member name `enwik8`. That is exactly the prefix consumed by the old 10-million-character smoke harness. The full 100-million-byte corpus is **not included**. Read `DELIVERY_30MB.md` and `provenance/REPACKAGE_30MB.json` before checking historical full-corpus hashes. No algorithm, score, or research constraint changed.

## 1. Your assignment

Help construct **one deterministic, analytically fitted learner that turns ordinary bit observations into reusable computation and useful predictions on unseen bitstrings**, with the same fitting and prediction mechanism across language and a genuinely different modality.

Do not merely propose an architecture, restate an objective, or identify a compact representation. The missing operation is:

> Given the observations, calculate the useful reusable relationships and operations—without receiving their structure, searching exponentially, or discarding the query information needed to answer.

A suitable public interface is:

```text
model = fit(observed_bit_pairs_or_corpus)
probabilities, answer_bits = predict(model, query_bits, requested_output_bits)
```

Alternative framing is allowed when transparent. Separate fitted models on different datasets are allowed; **the core algorithm must not change by modality or task**. An external evaluator may decode files, score audio differently from language, and know synthetic ground truth. Those conveniences must not leak into the learner.

You have authority to challenge the prior direction. In particular, **you are not assigned to keep improving modular arithmetic, group-table completion, probability calibration, or our small transformer**. Those are controls. Select the most promising route to the general discovery problem and make an actual cumulative advance. Do not let historical “next dependency” paragraphs lock you into the most recent local detour.

Aim to deliver a complete mechanism at the scope you can substantiate, with adversarial tests and explicit costs. If the broad goal is not reached, provide a concrete executable result or substantive derivation and identify exactly what remains. Do not replace the missing step with a reassuring name.

## 2. Authoritative state and how to use the packet

**Repository:** `https://github.com/Dillxn/bit-window-learner`

Latest state freshly checked while preparing this handoff:

```text
PR:       https://github.com/Dillxn/bit-window-learner/pull/18
Status:   open, draft, unmerged
Branch:   research/independent-reliability-audit
Head:     e6a255c7a4b5c0b51a74a1fe0c1e081f29680859
Base:     research/noisy-rectangle-consensus
Base SHA: e3c37957ae5aad04495eb8fb1bf0f273d21b7099
```

PR #18 is newer than the last detailed cycle-17 update displayed to the user. Do not accidentally resume at #17 or assume `main` includes these stacked research branches. Recheck the head before writing; an unmerged PR's synthetic merge-commit field does not establish a merge.

**Read order:** this document; `EVIDENCE_MAP.md`; then the source and executable adversaries relevant to your proposed mechanism. There is no reason to read every historical report or rerun every large experiment before thinking. The original broader specification is in `legacy/ULTRA_ANALYTICAL_LEARNER_HANDOFF.md`. The large historical research ledger is included for targeted searches, not mandatory front-to-back reading.

This is an **offline research bundle assembled from original run packets plus connector-fetched cycle-18 source**, not a claim to be a complete Git checkout at the pinned head. `provenance/` records source origins and file hashes. Where no original cycle-18 raw run artifact was available, the handoff distinguishes repository-reported results from included raw receipts. The bundled current code can regenerate its diagnostics.

Older reports sometimes have different wording/formatting from the committed reports. Do not compare an original raw-file SHA-256 to a reserialized repository JSON and announce data corruption. Use each provenance record's stated object/file convention. Integrity checks prove byte consistency, **not scientific correctness**. The packaging step does not independently reproduce all past results.

## 3. What “analytical” and “bits” mean here

**Final learner:** no gradient training, retained pretrained/neural weights, learner randomness, task-family IDs, modality-specific model routing, planted answers, or exponential program/feature/permutation enumeration. No concealed generic decoder, optimizer, oracle, or evaluation of the true function at unobserved points.

A deterministic finite sequence of elimination, indexing, counting, recursion, or explicit structure-building is allowed. “Fit once” does not mean “one loop” or “read each example once”; it means a reusable fit that is not retrained for every query. A single batch may have internal partitions. Recursion is not free parallelism, and renaming an iterative search “closed form” is not a solution.

Bits are the representation, not merely the final storage format of hand-supplied semantics. Byte packing, lengths, fixed binary framing, and transparent file decoding are allowed. Do not introduce a word parser, a pretrained image encoder, a special prompt recognizer, a task-dependent coordinate list, or a stable-token abstraction and claim these features were discovered. Stable whole-token equality was an imposed convenience of the recent symbolic controls, not an accepted general representation.

Data-derived parameters and explicitly described priors/codes are allowed when their role is clear. Do not call a half-count prior, fixed rank cap, finite grammar, or arbitrary resource cutoff assumption-free. Reject benchmark-tuned quality constants and rules selected using held-out answers.

Whole-query relevance means an earlier input position can affect the answer when the task needs it. It does **not** require every irrelevant bit to affect every answer, nor forbid a justified sufficient summary. A fixed suffix cutoff cannot silently replace the whole query.

For variable-length output, separate observed framing, externally requested length, and learned termination. A supplied `T` is not learned EOS. A generic “OTHER” probability category is not generation of a previously unseen token.

The practical goal includes a **useful natural-data smoke stack below 120 seconds**, with preparation, fitting, and inference included and hardware reported. This is not a deadline on the entire research session. Many tiny synthetic runs met a time limit while failing quality; none establishes the full goal. The ambition of substantially better efficiency than neural methods requires a genuinely **quality-matched** baseline, including all relevant training and inference costs.

State fit, query, working-memory, retained-model, arithmetic-precision, and output-writing bounds in bit operations/stored bits. Parameters should include total training bits N, example count m, input/query width Q, output length T, representation size R, and required numerical precision. Charge large integers, search, candidate generation, and lookup. An explicit polynomial cutoff is not a theorem that useful structure lies within the cutoff.

## 4. Essential conceptual corrections

The practical target is **not universal exact recovery of every compact computable function from arbitrary insufficient observations**. State noncircular coverage, class, distribution, or noise assumptions when a theorem needs them. Do not dismiss the practical objective using a stronger impossible statement the user did not require.

Conversely, “assume the useful basis is available,” “assume the target lies in my invented tiny family,” or “assume the right program is found” cannot be the general discovery result. A restricted theorem can be valuable, provided the restricted assumption is credited rather than hidden.

Keep six questions separate:

1. Can a model represent the computation compactly?
2. Can the observations identify it, at the claimed accuracy and query scope?
3. Is there an explicit efficient procedure to construct it from those observations?
4. Does its evaluator give valid, normalized predictions and terminate?
5. Does it generalize usefully, including under the specified nuisance/noise regime?
6. Does the full implementation meet the cost target at meaningful matched quality?

We repeatedly proved or tested one of these and initially spoke as if we had solved all six. Do not repeat that mistake. Also distinguish a flaw in a mechanism from a statistical ambiguity that no observation-only method can resolve under the stated assumptions.

## 5. Progress is real but fragmented

The user objected—correctly—to repeated “0%” headlines. Older `PROGRESS.json` files awarded 25 points only when an enormous end-to-end gate was fully complete. **That is an all-or-nothing acceptance checklist, not a measure of scientific progress. Do not use it as a progress estimate.** Do not replace it with an invented 30%, either.

We have runnable restricted fitters, genuine unseen-input successes, useful noise repairs, and explicit counterexamples. What we do not have is one core that accumulates those capabilities while reducing the supplied assumptions. Report progress as: capability improved; prior capability retained/lost; assumption removed/still needed; evidence supporting that statement. Commits, passing unit checks, and additional specialized algorithms are not progress units by themselves.

The recent symbolic work is a detour relative to language/media. Its high scores are not evidence that broad coherence is nearly solved. You may discard its architecture while retaining its lessons and tests.

## 6. High-value results and failures to preserve

### A. Original natural-data baseline and contaminated-looking successes

The old `recursive_mdl_learner.py` is a bounded suffix/statistical voter, despite stronger historical naming. The supplied old natural smoke ran in **29.7794 seconds externally**, about 1.85 GiB peak RSS, but used only 32-byte held-out snippets. Recorded bit accuracy: text 64.45%, audio 52.73%, video 45.70%; previous-frame video scored 78.52%. It was fast enough for that old protocol, not a successful master learner. [S1]

For `what is your name ?`, it emitted the fragment:

```text
 ǝ || [[Albert II o
```

Four unrelated questions produced the same longer Austria fragment, while a fifth produced an Alaska fragment. A plausible name was not question-sensitive understanding. Keep both the exact prompts and raw outputs visible. Earlier hand-authored role/name pairs (including `what is your role ? → Answer: an analytical learner` and `identity name ? → Aria`) were fixture inputs, not emergent discoveries; do not recycle them as success evidence. [S1]

### B. Early analytical operators, finite features, and sparse compression

The rank-two ordered operator recovered exact frequencies but once predicted **37/26** as a next-bit probability. Positive realizations repaired validity, not reliable long-history inference. One changed episode could erase an early-prefix effect. Three-bit marginal accuracy did not control rare long conditionals. [S2]

Explicit joint GF(2) relation extraction recovered masked parity and AND/XOR rules even when individual future marginals were fair. But its declared degree-two family failed cubic rules; one erroneous label could destroy an exact relation; a uniform solution-set law failed frequency calibration. Repeated-context majority repairs succeeded only while those majorities were nearly correct. [S3]

Sparse tensor-train factorization of empirical amplitudes produced valid distributions yet preserved zero empirical support on every unseen complete input; the uniform escape supplied over 99.95% of the prediction weight. Compact interpolation is not a discovery mechanism. Some fixed linear/tensor representations also need exponential state for compact register tasks. This rejects those representations/estimators, not all analytic learning. [S4]

### C. Small neural instruments: useful specimens, not an extracted master algorithm

The user explicitly allowed a **research-only** neural exception. A 17,537-parameter frozen in-context model accepts 48 eight-bit examples and new queries. It receives neither task IDs nor query labels. Whole-rule identities were split; a single seeded training/extension protocol was used. It learned some two-bit interactions, remained weak on higher-order transfer, and exploited shortcuts on nonlinear aggregates. The inference context was not its total meta-training data. [S5]

Causal patches and exact first-attention decompositions were executed. Some label dependence travels through query-conditioned aggregation, some through support-to-support processing. Pair-only summaries did not explain the whole network. Degree-two interventions helped XOR2 but hurt XOR3; support-only selection partly repaired clean tradeoffs but remained noise-sensitive. Eight-bit Walsh tables are **exponential analysis tools**, not an admissible final general constructor. Every decomposed neural kernel still uses trained weights. [S5]

A separate exact pair posterior was stronger than this network on noisy XOR2, but was supplied the pair hypothesis class. Failure to imitate the network is not a defect in a better independent learner; it only defeats the claim of faithful mechanism extraction. Do not spend the entire session reproducing the imperfect network's mistakes.

The actual checkpoint is included:

```text
research/neural_microscope/extension/selected_model.pt
SHA-256 ad2fdadadb1e968ed2521896d307797b9e299cbbf989e571e4a45fdb5c0e22b8
```

It is our small bit-rule microscope, **not** the external modular-addition checkpoint.

### D. Neural-guided program search did not establish neural invention

Cycle 13 used a 1,153-parameter neural ranker over **576 supplied fitting programs**. The final exported fitter ran without neural dependencies and handled represented noisy XOR2/XOR3/AND-XOR tasks. However, the final winner was already in the common unguided initialization. The grammar, two construction rounds, and readout were supplied. Every feature depends on at most three coordinates; uniform XOR4 defeats the entire language. Do not claim the neural guide invented the useful algorithm or that one extra grammar round resolves general discovery. [S6]

Neural research remains allowed, but any new use should have a measurable advantage over matched unguided search or expose a genuinely useful transferable operation. Export an algorithm that fits **new datasets**, not a task's answers or a neural-weight formula.

### E. Learned translation coordinates: promising representation, failed nuisance test

Cycle 14 ranked label agreements for **actual observed XOR differences** and fitted probability tables on resulting quotient coordinates. It removed the fixed small interaction-order cap and performed strongly on small parity and hidden-coordinate nonlinear controls. Yet appending 24 irrelevant bits while keeping the exact original labels and targets drove noisy parity from 100% to chance and clean hidden-switch accuracy to 48.44%. Exact full-space differences stopped repeating. Nonrepeated input strings had still supplied repeated relational evidence in the small cube. [S7]

This is a central raw-bit failure to revisit. Do not “repair” it by handing the fitter the informative prefix or a target-dependent projection. A different representation/constructor is allowed. Coherent nuisance assumptions and sample scaling must be stated.

### F. Modular-extraction image: credible compression, supplied arithmetic structure

The inspected public script in `SauersML/gam` at `5648d1c24770178fdd67102ab9ce19854d665848` supplied the numeric token cycle and projected onto an `a+b` formula. Full neural rewrite, pruned executable, and four-amplitude approximation are distinct objects. The original checkpoint `addition_s0.pt` was **not recovered**; its reported KL/rotation results were not rerun. Formula-only controls do not reproduce that network. [S8]

Missing external checkpoint SHA-256:
`1229d0a024fd6cb3caeb5f914a958a390099980f47fab217b74f28cf3663e48b`.

Do not block the whole project on it, substitute a new network and claim it is the original, or treat task-program extraction as an algorithm for learning arbitrary new tasks.

### G. Exact opaque-symbol recovery and rectangle noise repair

Cycle 16 imposed **L(a)+R(b)=O(c) in an abelian group**, then learned token maps and the integer quotient from opaque-symbol observation triples. At approximately 30% operand-pair coverage it recovered all large-task withheld addition, subtraction, affine, and nonzero-multiplication answers. No numeric token order, modulus, or operation ID was supplied—but the abelian-coordinate hypothesis was. One wrong label among 3,830 collapsed all output codes. Stable symbols repeat, unlike arbitrary raw-bit nuisance. The simple HNF implementation has no completed worst-case intermediate-bit-growth proof; reported stage-value maxima are not certified maxima of all temporaries. [S9]

Cycle 17 imposed the **quadrangle property**: equal ordered triples of rectangle labels imply equal fourth labels. Counting finite observed witnesses instead of forcing equations yielded all 8,939 withheld addition answers correct at each of two seeds after 383/3,830 dispersed replacements. At 957 replacements, it scored **17,626/17,878 = 98.59%**. These are fixed-hash corruption experiments, not arbitrary-error guarantees. Votes overlap; normalized vote fractions are not calibrated probabilities. [S10]

A separate certificate packs observation-disjoint seven-triple witnesses. If t witnesses agree, the true target satisfies the quadrangle law, and fewer than t observed triples are corrupt, at least one witness is clean. This is a useful conditional argument, **not family discovery or an inferred error budget**. An out-of-class table admits a syntactically valid certificate with a wrong conclusion. A coherent two-row reinterpretation changes only 69 labels yet produces zero conflicts and 0/157 answers correct against the originally intended target. [S10]

Sparse coverage severely regresses: at 10% clean coverage the rectangle method answers 1,607/11,493 correctly, while the exact method gets all 11,493. Occurrence-specific irrelevant suffixes cause fallback. A score over a renamed group table is not natural multimodal coherence.

### H. Latest cycle 18: calibration is not discovery

The fresh repository checkpoint adds a fixed five-model bank: prior, raw exact, raw rectangle, calibrated exact, calibrated rectangle. Core fitting, calibration, and audit use separate portions of the available observations; the candidates are not refitted after audit. Calibration counts actual held-out examples rather than overlapping motif votes. Sparse/dense clean addition selects exact inference and succeeds. At 10% dispersed replacement, calibrated rectangle predicts **2,042/2,048** clean answers correctly; mean mass on the clean answer rises from approximately .244 to .896. [S11]

But reserving 20% of training observations for calibration/audit destroys motif coverage at 25% corruption: selected accuracies are **65.43% and 62.89%**. The same rectangle core with all available training labels and the identical query sets scores **99.22% and 98.44%**. The latter cannot simultaneously claim an untouched post-fit audit guarantee. More calibration is not the missing discovery step. [S11]

The confidence layer has explicit IID observed-label average-risk guarantees; the actual hash diagnostics do **not** establish those sampling premises. A clean-target extension needs an external audit-label corruption budget. Hard-error and bounded-Brier bound families each use delta; the combined failure budget is at most 2delta. Coherent reinterpreted semantics pass the observed-label audit while failing all 36 affected original targets at about 99.968% confidence. Distinguish observed risk, hidden clean intent, average risk, and subgroup/pointwise risk. [S11]

## 7. What would constitute a meaningful next advance

Seek a **shared observation-to-structure calculation** that improves an existing central failure while retaining previously useful capabilities on comparable data and cost. You are free to replace the whole architecture. It need not reproduce the latest symbolic interfaces if a more general mechanism is better.

The most revealing stress combines three things we have repeatedly separated: useful joint dependence invisible to marginal tests; noisy, nonrepeated observations; and irrelevant detail that destroys exact raw-context matching. Preserve held-out compositions, not just new coordinates in familiar templates. Also retain sparse clean controls so a noise repair is not silently paid for with dramatically more evidence.

Do not claim the entire goal from one synthetic task. Equally, do not insist that no partial result counts until all natural modalities work. A genuine new reusable operation with explicit discovery, a substantive theorem, and a demonstrated reduction in assumptions is meaningful progress.

Specific examples to use selectively:

- Sparse parity and masked-output relations; nonlinear AND/XOR; genuinely held-out composition/switch tasks. Individual marginals may be uninformative while joint structure is predictive.
- Early-prefix/identical-suffix pairs: prove the mechanism can use the old bits, then test actual useful effects rather than measuring mere nonzero sensitivity.
- The same noisy task before/after appended or interleaved irrelevant coordinates. Keep labels, partitions, and query targets fixed; do not give the learner the relevant coordinates.
- Nonuniform outcome frequencies, unseen output support, and stochastic targets. Positive probabilities are not automatically calibrated.
- A clean sparse-data case and its matched noisy version with identical total-label budgets. Count samples spent on calibration, architecture selection, and neural meta-training.
- An ambiguity case with two clean sources consistent with the same corrupted observations. Do not demand impossible recovery of unspecified intent; state the additional assumption or correct risk target.

Respect each theorem's assumptions when adversarially testing it. Distinguish: implementation bug; wrong probability law; representation limit; lack of informative observations; inefficient discovery; estimator failure with adequate information; distribution shift; semantic failure. This classification should determine the repair.

## 8. Do not spend another cycle on these non-solutions

A global MDL/Bayesian/least-program objective without a constructive algorithm; a recursive call that hides the same missing discovery step; exhaustive truth tables or variable-degree feature banks hidden behind a “kernel”; maximum-likelihood decoding of unrestricted noisy constraints with no cost bound; supplied group laws/hidden bases counted as learned structure; counts over repeated/overlapping evidence treated as independent; neural weights rewritten as formulas; or a program proposer whose human-built grammar already encodes the successful algorithm.

These ideas are not prohibited research tools. What is prohibited is **promoting their unresolved dependency to the solution**. Revisit a rejected approach only with a precise mathematical difference that addresses the recorded failure, not a new name.

An unrelated solver selected by task name or an evaluator-known property is not one core. Generic data-driven internal decomposition may be legitimate, but construct it explicitly and account for the discovery work.

## 9. Natural-data packet and honest evaluation

The original media and the exact corpus prefix required by the historical smoke harness are included. The full corpus archive is not included in this under-30-MB delivery:

```text
data/enwik8_prefix12m.zip
  archive SHA256 ac136ddf2b2afb3fb7bb05ec5920fd97eed8754120181c449621ae9a0607467b
  member enwik8: exactly 12,000,000 raw bytes
  member SHA256 0e19ce0424451c69be4acb0fea64f7706d786dd47c6a3fa137764c292707f53b
data/media_sample.webm
  SHA256 ef7db6e47f4f35653ba69a0c14e3916bfe083c2e491109d37823a94ad9d6a0ef
```

The old text protocol reads 12,000,000 bytes of the ZIP member, decodes UTF-8 with replacement, takes 10,000,000 Unicode characters, then re-encodes: **10,048,009 bytes**, not 10 million bytes. The included prefix preserves that exact input and its short test continuation. Pass `data/enwik8_prefix12m.zip` explicitly to the old harness rather than its former archive path. Original full-corpus hashes remain historical evidence only; consult `DELIVERY_30MB.md` and `provenance/REPACKAGE_30MB.json` for this package's scope. Any improved bit-level split/protocol must be frozen and labeled separately. A later test using a fresh region of the full 100,000,000-byte corpus requires retrieving the original corpus, not pretending it is present here.

The old media protocol decodes mono 4 kHz unsigned 8-bit PCM and 16×9 grayscale frames at 2 fps, using the first three quarters for training. It is a tiny smoke setup, not perceptual-quality validation. Read `legacy/baseline/recursive_mdl_benchmark.py` for exact decoding and framing. Compressed container bytes alone are not decoded audio/video. A useful new claim needs longer fresh held-out segments, meaningful simple comparators, and unchanged learner code across modalities.

The name question is a visible semantic regression, not a magic identity oracle. Show the actual response to `what is your name ?` when a candidate supports it, together with unrelated prompts and early-context counterfactuals. Do not force a canned name, hardcode a response, or count training-pair memorization as coherence. If the module cannot accept natural queries, state “not run/not supported” and do not claim that gate passed.

## 10. A practical way to use the next session

**Start with the mechanism, not another benchmark tour.** Read this handoff and a few relevant source/adversary files. Summarize the single bottleneck you intend to remove and why your proposal is not equivalent to an already rejected construction. An independent route is welcome; the prior assistant's conclusions are evidence to audit, not axioms.

Specify representation, fitting calculation, unseen-query semantics, assumptions, termination, and costs before a broad implementation. Alternate constructor and adversary roles; use separate agents only if actually available. Keep or discard a proposal for an explicit reason. Do not hide unresolved work in `discover_*`, `best_model`, `compress`, `learn_representation`, an unrestricted argmin, or an unstated subroutine.

Use Lean for substantive general claims when feasible. Earlier ledger entries report some narrow compiled lemmas; later cycle environments lacked Lean/lake. **Do not generalize either fact to “the project has a verified master theorem” or “no Lean work ever exists.”** Locate actual proof sources/logs and state exact versions, assumptions and axiom dependencies. A file containing a statement or `sorry` is not verification. Tool failure is not proof failure; continue honestly with paper status where necessary.

Once specified, freeze source and protocol before inspecting fresh test outputs. Keep constructor inputs separate from evaluator truth. Record fit and query costs separately, cold preparation and warm reuse, failures as well as successes, and empirical vs theorem assumptions. Rerun only relevant regressions first. Avoid spending the whole session repackaging old results or doing neural training with no measurable discovery hypothesis.

For an acceptable final learner/export, test fresh `fit(D)` and predictions in an isolated process with no retained neural checkpoint or target metadata. Report what remains human supplied. Do not claim generality because a function has a generic name or accepts bits.

## 11. What to return to Dillon

Return the concrete construction or a completed substantive derivation, its strongest adversary, and the actual achieved scope. A useful update answers:

```text
What can the same mechanism do now that it could not do before?
What earlier capability did it retain or lose on matched evidence?
Which assumption was removed, and which remains?
What is the explicit observation-to-model calculation?
What is proved, what was executed, and what is conjectured?
What did the name/media regressions actually output, or why were they not run?
What are the fit/query/memory/precision costs and reproducible commands?
```

Do not substitute a speculative percentage, another polished prospectus, or a broad impossibility statement for these answers. Pursue the original goal seriously, but do not manufacture certainty or a completion date.

The user has authorized research in the existing workflow. Preserve old sources/evidence; use a separate research module/branch for changes. No merges, deployments, paid compute or external account changes are requested by this handoff. No background-work claim unless a process/task was actually started and its status is known. Check concurrent changes before editing. You do not need a Mac or a paid browser for this packet.

**The deliverable is a useful reusable learning computation, not another narrow success whose decisive structure was supplied by us. The experiments have exposed that difference; your assignment is to make progress across it.**

---

## Source references

The source map in `EVIDENCE_MAP.md` gives exact paths. All URLs here identify research evidence, not instructions to contact external services. The currently pinned GitHub revision is `e6a255c7a4b5c0b51a74a1fe0c1e081f29680859`.

[S1] Original Ultra handoff and `legacy/evidence/real_run`, `legacy/evidence/five_prompts`, plus original frozen baseline. Read source/raw outputs before inheriting early docstring claims.

[S2] `research/operator_validity/`: cycle 2–5 code, reports and adversaries; early ordered-model evidence also in history/ownership packet where included.

[S3] `research/joint_relations/`: cycles 6–7, exact and soft joint constructors with noise/degree/frequency adversaries.

[S4] `research/sparse_born/`: cycle 8 code, control results, and support/rank counterexamples.

[S5] `research/neural_microscope/`, `research/neural_mechanism/`, `research/attention_kernel/`, `research/interaction_selection/`: cycles 9–12 and frozen checkpoint.

[S6] `research/program_discovery/REPORT.md`, `EXPORT_AUDIT.json`, `selected_learner.py`, tests and raw search traces.

[S7] `research/translation_quotient/REPORT.md`, `COVERAGE_RESULTS.json`, `coverage_audit.py`.

[S8] `research/modular_extraction_audit/`: source audit and formula-only controls; source pin `SauersML/gam@5648d1c24770178fdd67102ab9ce19854d665848`.

[S9] `research/opaque_symbol_relations/REPORT.md`, `learner.py`, `adversary.py`, `COMMITTED_RECEIPT.json`; PR #16.

[S10] `research/rectangle_consensus/REPORT.md`, `learner.py`, `adversary.py`, `assumption_audit.py`, original raw results; PR #17.

[S11] Fresh connector reads of PR #18, `PROJECT_STATE.md`, and `research/validated_selection/REPORT.md`, `learner.py`, tests and evaluators, at the pinned revision. Current report:
`https://github.com/Dillxn/bit-window-learner/blob/e6a255c7a4b5c0b51a74a1fe0c1e081f29680859/research/validated_selection/REPORT.md`.
