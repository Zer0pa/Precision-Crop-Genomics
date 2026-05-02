# Modus Operandi — Multi-Agent Work-Stream Pattern

How Zer0pa work streams are run from research input to executable system. Reusable across work streams; this Precision Crop Genomics repo is the **eighth instance** after `Zer0pa/Health`, `Zer0pa/Materials`, `Zer0pa/Energy`, `Zer0pa/Synthetic-Biology`, `Zer0pa/Polymath-AI`, `Zer0pa/Polymath-Diffusion-AI`, and `Zer0pa/RCE`. **It is a pipeline-vertical workstream (six-layer architecture L1-L6) closer in shape to Health / Materials / Energy / Synbio than to the non-pipeline-vertical Polymath / RCE workstreams.**

## Boundary

Research infrastructure for in silico precision crop genomics. Outputs are research artifacts. No regulatory certification claims. No clinical or human-subject use. **No trait IP.** No environmental release of GMOs or gene-edited material by Zer0pa directly. No deployment to South Africa for gene-edited products absent GMO Act amendment. No herbicide tolerance, novel insecticidal protein, or pharma traits in v1 scope.

## The pattern in one paragraph

A work stream begins when source research material lands. A **synthesis agent** reads with fresh eyes, distinguishes inherited from operator-read, surfaces what is not yet seen, and produces a portable briefing pack and synthesis document. An **orchestrator agent** applies fresh eyes again on the synthesis output, augments with deeper specificity, identifies remaining gaps, spawns Sonnet/Opus sub-agents to research stuck or innovation points, and writes a PRD that fully specifies an overnight long-horizon execution. **Overnight executor agents** read the PRD with fresh eyes, decompose into parallel sub-streams, and **achieve ZERO left to do on CPU before any Runpod GPU is requested**. The Runpod cutover is then a config-flag stub-swap into a known-good system, not a re-architecture. Each role adds value; if a role only paraphrases, it has not done its job.

## Role chain

| Role | Input | Output | Tools |
|---|---|---|---|
| **Synthesis agent** | Source research (operator-authored Pre-PRD synthesis Report 1 of 2 for Precision Crop Genomics) | Briefing pack + synthesis doc + fresh-eyes reframe | Heavy reading, structured prose, distinguishing inherited vs operator-read |
| **Orchestrator** | Synthesis output + repo state | `PRD.md` with overnight-executable specifics, sub-agent allocation, build sequence, interface contracts, falsification ledger, audit-trail spec, acceptance gates, anti-decision pre-registration | Anthropic Opus 4.7 + Sonnet 4.x sub-agents in parallel worktrees; Perplexity / Gemini at stuck points; recursive fresh eyes |
| **Overnight executor** | `PRD.md` + repo state | Code, schemas, tests, audit trails, KG nodes, simulation stubs, integration scaffolds — **everything achievable on CPU, with ZERO left** before Runpod is requested | Sonnet / Opus coding agents in parallel worktrees, test-first, mock simulators, REST stubs for GPU layers, KG-write discipline |
| **Runpod cutover migration** | Overnight executor's output | GPU-shaped layers swapped into REST stubs; pipeline runs real on Runpod; cutover is a config-flag stub-swap | Same coding agents with Runpod GPU access |

## The 110%-pre-compute-wall axiom (operator binding, sharpened 2026-05-02)

The operator's binding axiom 2026-05-01 was: "agents need to do the 110% max until they hit a compute wall."

**Operator sharpened directive 2026-05-02 (Precision Crop Genomics specifically and applied to all subsequent workstreams):** **"there must be ZERO left to do on CPU before they ask Runpod"** plus **"no false flag reward hacking or interim reporting — this is overnight execution."**

The sharper formulation is binding. Translation per workstream:

| Workstream | Compute wall(s) | ZERO-on-CPU discipline |
|---|---|---|
| Health, Materials, Energy, Synthetic Biology | Runpod GPU | Every CPU-tractable layer + harness + falsifier + audit + REST-stub + plug-replaceability test complete before Runpod cutover |
| Polymath AI | Phone Hexagon | Every Mac-side simulation + on-device-validation calibration complete before multi-day device-side training |
| Polymath Diffusion AI | Three walls (Mac MLX → AI Hub Workbench → Phone Hexagon) | Per-wall ZERO discipline |
| RCE | Cloudflare-edge production deploy | Local + CI green before any production push |
| **Precision Crop Genomics (this workstream)** | **Runpod GPU** (for foundation-model fine-tuning, deep-learning prediction tracks, ChromaX scale runs, large-N MET training, graph genotyping at scale) | **ZERO left on CPU before Runpod is requested.** Everything that can be done on a Mac dev machine + small in-memory test data must be 110%-complete: license-stamping ETL service, BrAPI-native data spine, Tier-1 prediction stack baseline (rrBLUP / BGLR / sommer / EnvRtype / BGGE), AlphaSimR-based breeding simulation, FielDHub trial design, regulatory router with full master decision matrix, off-target enumeration logic, dossier JSON-LD schema and validators, falsifier registry, audit-log shape, REST-stub adapters for GPU-bound layers, plug-replaceability test matrix |

The operator's "ZERO left to do on CPU" is **strictly stronger** than "do as much as you can." The orchestrator's PRD must encode it as a binding gate: any sub-brief that reaches Runpod-cutover with CPU-tractable work outstanding fails the engineering gate.

## Overnight execution discipline (operator binding, sharpened 2026-05-02)

The operator's directive 2026-05-02: **"no false flag reward hacking or interim reporting — this is overnight execution."**

This is a sharper restatement of prior discipline. Translation:

- **No false-flag reward hacking.** Every claim of "build green" requires the full gate matrix (cross-tool agreement: tests + lint + type-check + falsification loops + design-token audit + reproducible-build audit). Single-tool greens are pretty-greenflag corruptions per `RESISTANCE.md` (`fp-pretty-greenflag`). The operator catches these — see the Polymath Diffusion / RCE prior workstream Zod-migration triages where agents declared "all gates green" without running the falsification loop.
- **No interim reporting.** Once the executor receives the brief, they run end-to-end through the night without check-ins. Strip all process theater. The operator is asleep; the agent is working. The PRD must be self-contained enough that no operator engagement is needed during execution.
- **No `fp-less-work-disguised-as-focus`.** Silently skipping call-sites under guise of scope discipline is forbidden. Every sub-brief's Resistance Self-Check enumerates every file touched.

## The recursive fresh-eyes principle

Each role does not just relay the prior role's output. Each role adds:

- **What was not yet seen** — gaps, anti-patterns, missing layers, unstated assumptions.
- **What is implicit but should be explicit** — interface contracts, falsifiers, audit shapes.
- **What the next role needs that this role can prefigure** — interface specs, decision criteria, fallback patterns, acceptance gates.
- **What deep research would unlock** — strategic lookups via Perplexity / Gemini surfaced as either tactical (use the answer) or strategic (return to operator for innovation).

If a role only paraphrases, it has not done its job. **For Precision Crop Genomics specifically, the source is operator-authored as a Pre-PRD synthesis (Report 1 of 2) — the role chain compresses at the synthesis layer (operator played research-agent + synthesis-agent), and the synthesis-agent fresh-eyes pass is recursive on top.** Report 2 is forthcoming and may displace some PRD decisions if it lands during the build; the orchestrator should design for that.

## Parallel-exploration principle (cross-workstream)

Zer0pa runs multiple workstreams in parallel: **Health, Materials, Energy, Synthetic Biology, Polymath AI, Polymath Diffusion AI, RCE, and Precision Crop Genomics as of 2026-05-02.**

**Fork-and-own is explicitly permitted (operator clarification 2026-05-01).** **What is rejected is runtime co-dependency.**

**For Precision Crop Genomics specifically, the highest-value forks are:**

- **From Synthetic Biology**: SBOL3-attested audit-trail with sha256 hash chain → JSON-LD-attested dossier with sha256 hash chain; four-column license decomposition pattern (already mirrored in Report 1); Unknown Enzyme Generative Sub-Pipeline tools (RFdiffusion3, MACE-OFF, ProteinMPNN, AlphaFold DB) reusable as the protein-structure tower for NLR receptor / photosynthetic enzyme / transporter / TF DBD trait engineering.
- **From Health**: TxGemma reasoner-tuple discipline → dossier-tuple discipline; audit-log shape with hash chain; cross-model disagreement primitive → ensemble disagreement (rrBLUP + BGLR + sommer + DNNGP).
- **From Materials**: falsifier-registry-first build discipline; cross-model ensemble disagreement aggregator code structure.
- **From Energy**: same-shape Runpod cutover with `httpx.MockTransport` golden-fixture invariance — Mac-CPU-vs-Runpod-GPU equivalence test.
- **From Polymath AI / Polymath Diffusion AI**: Sonnet/Opus-only sub-agent dispatch; RESISTANCE.md augmentation with fp-pretty-greenflag and fp-less-work-disguised-as-focus.
- **From RCE**: surgical-sub-brief shape for any specific schema-locking task.
- **Cross-workstream BoTorch pattern**: every workstream needs a BoTorch multi-objective optimizer. Precision Crop Genomics qNEHVI Pareto over (yield × resilience × nutrition × input efficiency × regulatory friction × deployment ROI) is the closest analog to Synbio MFMO. **Fork the shape** from Synbio if Synbio's MFMO is far enough along; reimplement inside Precision Crop Genomics. No runtime co-dependency.

All forks; no runtime co-dependency.

## Repo discipline

- **GitHub is canonical.** Local working trees may drift. The repo does not.
- Each role's output is committed and pushed before handoff.
- `MODUS-OPERANDI.md` and the role-specific `HANDOFF-TO-*.md` files are updated only when the pattern itself evolves.
- Boundary block appears verbatim in every artifact.
- **Audit shape**: every artifact carries provenance — agent / model / date / source files / fresh-eyes additions.
- All sub-agent work commits back to the repo before final handoff.

## Front-load engineering before the compute wall

Per the operator's sharpened 2026-05-02 directive, **ZERO left to do on CPU before Runpod**. The orchestrator's PRD must specify which layers are CPU-tractable and which require Runpod, and gate the cutover on the CPU-tractable set being 110%-complete.

For Precision Crop Genomics:

- **CPU-tractable (must be 110% complete before Runpod)**: license-stamping ETL service; BrAPI-native data spine with self-hosted Breedbase; PLINK 2 PGEN canonical genotype store; PHGv2 hVCF integration (consumer mode, not graph-builder mode); rrBLUP + BGLR + sommer + EnvRtype + BGGE Tier-1 prediction stack on small-N test data; Jarquín reaction-norm GBLUP harness; AlphaSimR breeding simulation harness; PyBrOpS multi-objective Pareto cross-design; FielDHub trial design; statgenSTA + statgenGxE + SpATS spatial trend correction; CROPSR + CRISPR-PLANT v2 + Cas-OFFinder + CRISPRitz + CRISPResso2 edit design and verification; off-target enumeration logic with polyploid homoeolog handling; regulatory router with full master decision matrix and Regulatory Fit Score implementation; dossier JSON-LD schema and validators (all seven blocks); falsifier registry; audit-log shape with hash chain; REST-stub adapters for GPU-bound layers; plug-replaceability test matrix; cross-model ensemble disagreement aggregator; reproducible-build audit script; license-class taint detector for model training runs; KG schema and episodic memory write path; cooling-strategy validation rig (forked from Polymath workstreams, parked as defensive carry — irrelevant here unless device-side work emerges).
- **Runpod-required**: foundation-model fine-tuning (PlantCaduceus + GPN + HyenaDNA fine-tunes for variant-effect and regulatory tasks); deep-learning prediction tracks (DNNGP / DeepGP / custom transformers) at production batch sizes; ChromaX (JAX/GPU) for ML-coupled breeding simulation at scale; large-N MET training; graph genotyping at scale (Giraffe over 10K-100K samples); protein-structure tower runs (RFdiffusion3, MACE-OFF, ESMFold) at production batch.

The cutover is a config-flag stub-swap, not a re-architecture step.

## Boundary discipline through layers

Each role inherits the prior boundary block. No role may relax the boundary. **Precision Crop Genomics' boundary explicitly excludes**: trait IP ownership; environmental release of GMO / gene-edited material by Zer0pa directly; SA deployment of gene-edited products absent GMO Act amendment; herbicide tolerance / novel insecticidal protein / pharma traits in v1; gene drives; cultivation bans; the four license traps (PLAZA, TAIR live, WorldClim 2.1, EOX cloudless) and their named alternates; APSIM commercial use; AgroNT / Nucleotide Transformer weights; AlphaFold3 / ESM3 main weights; Google Earth Engine free tier for commercial use; OpenDroneMap as hosted SaaS; Ultralytics YOLO under default license.

## Cross-machine handoff

When the next role runs on a different machine: the startup prompt for the next role gives the GitHub URL as primary path with the local fallback path on the originating machine. The next role clones (or fetches) before reading. All sub-agent work commits back to GitHub before final handoff.

## Standard repo layout

```
<workstream>/
├── README.md                              # Entry, read order
├── MODUS-OPERANDI.md                      # This pattern
├── RESISTANCE.md                          # Anti-corruption doctrine
├── HANDOFF-TO-<NEXT-ROLE>.md              # Role-specific handoff
├── <ROLE>-STARTUP-PROMPT.md               # Paste-ready startup prompt
├── source-briefs/                         # Inherited research input
├── synthesis/                             # Synthesis agent's fresh-eyes reframes
├── PRD.md                                 # Orchestrator's output
├── phases/                                # Overnight executor's output
└── runtime/                               # Runtime configs, deployment manifests
```

## Sub-agent topology (Sonnet / Opus only — operator directive 2026-05-01, carried forward)

The operator has specified that sub-agent dispatch is **Sonnet / Opus only**. No GPT-5+. The orchestrator's PRD must encode the dispatch table explicitly.

- **Strategic planner** — Claude Opus 4.7 at maximum reasoning effort.
- **Heavy code generator** — Claude Sonnet 4.x or Opus 4.7. Replaces the GPT-5+ slot from earliest workstream patterns.
- **Per-component specialists** — Sonnet sub-agents in parallel worktrees: license-stamping ETL service / BrAPI data spine / PLINK 2 + PHGv2 integration / rrBLUP + BGLR + sommer prediction stack / EnvRtype + BGGE G×E layer / AlphaSimR + PyBrOpS breeding sim / FielDHub trial design / statgen + SpATS spatial correction / CROPSR + Cas-OFFinder edit design / off-target enumeration / regulatory router / Regulatory Fit Score implementation / dossier JSON-LD schema / falsifier registry / audit-log + hash chain / REST-stub adapters for GPU-bound layers / plug-replaceability test matrix / ensemble disagreement aggregator / reproducible-build audit / KG + episodic memory.
- **Domain reasoner** — Anthropic-routed only. For Precision Crop Genomics, Opus 4.7 with paper-corpus context (CIMMYT, IRRI, AOCC, AATF publications) is the natural choice.
- **Deep-research tools** — Perplexity Pro / Gemini Advanced at engineering-blocker stuck points only. Survey lookups deferred unless they materially unblock engineering.
- **KG / episodic memory** — every decision, blocker, resolution writes a structured node.

## Acceptance gates (default + Precision-Crop-Genomics-specific)

Every PRD should pass three gates before overnight execution begins:

1. **Scientific gate** — every component has falsifier coverage, source grounding, no out-of-scope claims (no trait IP framing, no environmental release framing, no herbicide tolerance / PIP / pharma trait framing, no SA gene-edited deployment framing).
2. **Engineering gate** — local CPU build runs end-to-end with Runpod stubs; plug-replaceability test passes (the architectural invariant — swap rrBLUP for BGLR for sommer in <1 day with no downstream breakage; swap PLINK2 for PHGv2 in <1 day; swap AlphaSimR for ChromaX in <1 day; swap CROPSR for CRISPR-PLANT v2 in <1 day).
3. **Brain-functionality gate** — next-agent state is fully reconstructible from the repo plus KG plus audit log; no conversation history needed.

Stream-specific gates:

4. **ZERO-on-CPU gate** — every CPU-tractable component is 110%-complete; the cutover-to-Runpod stub-swap proves byte-identical envelopes / canonical hashes / falsifier classes / backend flags before any Runpod GPU is requested.
5. **License-class taint gate** — no class-C/D inputs contaminate any commercializable model artifact. The license-stamping ETL service emits a taint report per model training run; any taint blocks the run from being marked commercializable.
6. **Regulatory Fit Score implementation gate** — the master decision matrix (jurisdiction × trait modifier × edit type) is encoded with citations to current regulatory text; any sub-brief proposing an edit that scores below RFS 2.5 in target markets is flagged red and routed to operator review.
7. **Dossier regenerability gate** — the Crop Improvement Dossier is regenerable from inputs at any time. No implicit state, no hidden context, no untracked manual decisions. Every sub-brief that introduces state must show it survives the regenerability test.
8. **Anti-decision gate** — any sub-brief proposing one of the pre-registered anti-decisions (APSIM commercial, AgroNT, AlphaFold3 weights, WorldClim 2.1, PLAZA, TAIR live, GEE free tier, Ultralytics YOLO, OpenDroneMap as hosted, herbicide tolerance, PIP, pharma, trait IP, SA gene-edit deployment) fails brain-functionality at PRD review and must escalate to operator.

## Operator refinements (binding for all workstreams; captured 2026-05-01 + sharpened 2026-05-02)

- **Anti-MVP / anti-toy.** Target is never an MVP, never a first paying customer. **Build the most overdesigned, best-in-class system the technology landscape supports.** For Precision Crop Genomics, the success signal is **a partner-ready Crop Improvement Dossier that no incumbent currently delivers**.
- **110% pre-compute-wall sharpened: ZERO left to do on CPU before Runpod (operator directive 2026-05-02).** Strictly stronger than "do as much as you can."
- **Overnight long-horizon, autonomous, no false-flag reward hacking, no interim reporting (operator directive 2026-05-02).** Once the brief is received, the executor runs end-to-end through the night without check-ins. Every "build green" claim requires the full gate matrix.
- **GitHub + Hugging Face are the review surface.** Code, schemas, tests, audit trails, decision logs, KG nodes, and the PRD itself commit to GitHub. Large datasets and AI model artifacts go to Hugging Face under the **Architect-Prime user, not the Zer0pa org**. HF token at `~/.cache/huggingface/token` on the originating machine. HF Pro account is OAuth-authenticated on the originating machine (per Polymath Diffusion 2026-05-02 directive); streaming-corpus regime is enabled for any large dataset.
- **PRD self-contained in the repo.** Executor can and must augment the PRD as they learn.
- **Fork-and-own across workstreams.** Pipelines/projects can steal patterns freely. They cannot be runtime co-dependent.
- **RESISTANCE.md doctrine.** Every executor reads it before starting. fp-pretty-greenflag and fp-less-work-disguised-as-focus are binding additions from the prior workstreams' Zod-migration triage.
- **Operator delegates engineering / science / commercial decisions** to the synthesis and orchestrator agents. Surface only strategic decisions or boundary-evolution questions to the operator.
- **Sub-agent dispatch is Sonnet / Opus only (operator directive 2026-05-01, carried forward).** No GPT-5+ for code generation.
- **Anti-decisions pre-registered as binding falsifiers (per workstream-specific anti-decision lists).** For Precision Crop Genomics: APSIM commercial, AgroNT, AlphaFold3, ESM3 main, WorldClim 2.1, PLAZA, TAIR live, GEE free tier, Ultralytics YOLO default, OpenDroneMap as hosted, herbicide tolerance traits, PIP traits via novel insecticidal protein, pharma traits, trait IP ownership by Zer0pa, SA gene-edited product deployment, gene drives, cultivation bans.

## Beyond pipeline verticals — Precision Crop Genomics is back in pipeline-vertical territory

Health, Materials, Energy, Synthetic Biology were pipeline-vertical (L1-L7). Polymath AI was non-pipeline-vertical (on-device AR LLM training). Polymath Diffusion was non-pipeline-vertical (on-device diffusion-LM deployment). RCE was non-pipeline-vertical (bleeding-edge enhancement programme). **Precision Crop Genomics is back in pipeline-vertical territory** — six layers (L1-L6) closer in shape to the first four workstreams. The same modus operandi applies; the role chain is the same as the first four workstreams.

Future workstreams may be pipeline-vertical or non-pipeline-vertical. The same discipline carries.
