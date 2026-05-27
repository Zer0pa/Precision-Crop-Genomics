# Handoff to the Precision Crop Genomics Orchestrator — Precision Crop Genomics Work Stream

You are the orchestrator for the Zer0pa Precision Crop Genomics work stream. This document briefs you on what you inherit, what is expected of you, and what you produce.

## Boundary

Research infrastructure for in silico precision crop genomics. Outputs are research artifacts (Crop Improvement Dossiers, genomic prediction model checkpoints, breeding-cycle simulation results, edit-design proposals with off-target enumerations, regulatory route classifications). No regulatory certification claims. No clinical or human-subject use. **No trait IP** — Zer0pa is platform-only. **No environmental release of GMOs or gene-edited material** by Zer0pa directly. **No deployment to South Africa for gene-edited products** absent GMO Act amendment. **No herbicide tolerance / novel insecticidal protein / pharma traits** in v1. **No vertical integration into grain supply chains** (Benson Hill lesson).

## What you inherit

### Source brief (`docs/research/source-briefs/`)

- **`01-precision-crop-genomics-report-1-full-technology-landscape.md`** — Operator-authored Pre-PRD Research Synthesis (Report 1 of 2), 160 dense lines, ~57 KB, May 2026. Sections 1-15 cover: v1 architecture in one diagram + four sentences (six-layer pipeline with LangGraph + BoTorch backbone, PLINK 2 PGEN canonical store, PHGv2/TileDB-VCF for haplotypes, BrAPI v2.1 over self-hosted Breedbase, four-column license stamp on every record, pangenome-aware modeling first-class for seven Tier-1 species); Layer 1 input encoding + ZPE schema (PlantCaduceus / HyenaDNA / Evo-2 / EnvRtype / AgERA5 / CHELSA / CHIRPS v3); Layer 2 knowledge layer + four hard-exclusion license traps (PLAZA / TAIR live / WorldClim 2.1 / EOX cloudless mosaics) + three soft row-level traps (T3 Toronto Statement, CGIAR SMTA, Doench/Fusi sgRNA scoring); Layer 3 candidate generation across cross/MAS/edit modalities (AlphaSimR + MoBPS + ChromaX + PyBrOpS + AlphaMate + optiSel + selectiongain + FielDHub + statgenSTA/GxE + SpATS for cross-and-MAS; CROPSR + CRISPR-PLANT v2 + Cas-OFFinder + CRISPRitz + CRISPResso2 for editing; base editing default + prime editing R&D-only; VIGE as IP/regulatory arbitrage); Layer 4 screening with genomic prediction (rrBLUP + BGLR + sommer + DNNGP + DeepGP) + G×E (Jarquín reaction-norm GBLUP) + pangenome-aware (PHGv2 + Giraffe + PanGenie + Sniffles2 + minigraph-cactus) + off-target + regulatory routing; Layer 5 Bayesian optimization + active learning (the "no production-grade BoTorch-for-breeding tool exists" gap is the highest-leverage build piece); Layer 6 typed handoff dossier with seven blocks (Identity / Intervention Strategy / Performance Forecast / Risk / Regulatory / Provenance / Partner Handoff); phenomics + remote sensing material-lift cases; regulatory routing as scoring axis with explicit Regulatory Fit Score formula `RFS = Σ over target markets [ MarketWeight × JurisdictionScore(0-5) × TraitMultiplier(0.3-1.0) × EditTypeCoefficient(0.2-1.0) ] − ProcessRiskPenalty` and master decision matrix; eight architecture-changing intersectional disciplines + six scoring-only; commercial landscape (Inari closed; Pairwise / Living Models / Computomics partner-shaped); South Africa / Southern Africa / orphan crop layer with ARC + SACTA + CGIAR + AATF + HarvestPlus + AOCC ecosystem; ten research-question answers; five frontier opportunities not-yet-production-ready; build order in Section 15. **Report 2 forthcoming** ("a sharper architectural specification with concrete schema definitions, partner integration sequences, and the South African go-to-market motion through ARC-BTP, SACTA, and CIMMYT-Zimbabwe").

The source brief is operator-authored as a hybrid research-agent + synthesis-agent output. **Your PRD is not a re-do of Report 1 — it is the recursive-fresh-eyes augmentation that surfaces what the operator-as-synthesizer did not see, plus the executable specifics the executor needs that the brief does not yet pin down.**

### Synthesis (`docs/research/synthesis/`)

- **`01-fresh-eyes-on-precision-crop-genomics-report-1.md`** — Fresh-eyes reading by the synthesis agent (Claude Opus 4.7, 2026-05-02). Surfaces:
  - The architectural reframe: Precision Crop Genomics is a license-clean partner-platform whose unit-of-output is the typed, regulatorily-routed Crop Improvement Dossier; every layer of the six-layer pipeline exists to serve the dossier's seven blocks. Dossier-first active-inference is the architectural primitive.
  - Cross-tool / cross-model disagreement (rrBLUP + BGLR + sommer + DNNGP ensemble) and license-class disagreement (class-A-only vs class-A+B+C training) and Tier-1-vs-orphan-crop disagreement (pangenome-aware vs SNP-only) as three first-class falsification primitives.
  - Twelve specific things Report 1 does not see: (1) the operator's 2026-05-02 directive sharpening (ZERO-on-CPU + no false-flag reward hacking + no interim reporting) that must be encoded verbatim; (2) the license-stamping ETL service is the moat, named explicitly, and underspecified; (3) the seven-block dossier JSON-LD schema must be locked before any other layer's interface contract; (4) the Regulatory Fit Score master decision matrix needs versioned encoding with citation chain; (5) Pairwise and Living Models as partners-not-competitors should reflect in API integration order; (6) the BoTorch-for-breeding gap is highest-leverage AND a recurring cross-workstream pattern (fork from Synbio MFMO); (7) the SA carveout has architectural implications, not just narrative; (8) the eight architecture-changing intersectional disciplines need explicit prioritisation (causal → climate+active inference → SE(3) → graph → info theory → control → systems ecology); (9) Report 2 forthcoming and may displace PRD decisions; (10) the BoTorch-native multi-objective breeding-cycle optimizer should be promoted from frontier-deferred to Phase-1; (11) Benson Hill bankruptcy carries a structural lesson Zer0pa must encode (no vertical integration); (12) orphan-crop SNP-only graceful degradation needs explicit logic, not narrative.
  - Pressure-test points (ten explicit) and three operator-engagement open questions (Pairwise / Living Models partnership sequencing; SA go-to-market motion; intersectional-roadmap prioritisation).
  - Heavy fork-and-own opportunities especially from Synthetic Biology (sister bio-domain pipeline; SBOL3-like dossier attestation, Unknown Enzyme tools as protein-structure tower, MFMO as BoTorch optimiser fork, CEKM corpus discipline as crop-genomic-prediction corpus discipline).

### Doctrine (`docs/research/RESISTANCE.md`)

- **`docs/research/RESISTANCE.md`** — Anti-corruption doctrine. Read first. Augmented per Polymath Diffusion / RCE precedents with `fp-pretty-greenflag` and `fp-less-work-disguised-as-focus`. **The operator's 2026-05-02 "no false flag reward hacking or interim reporting — this is overnight execution" directive reinforces these as binding.** The discipline IS the resistance.

## Operator refinements (binding; carried verbatim from `docs/process/MODUS-OPERANDI.md`)

- **Anti-MVP / anti-toy.** Target is never an MVP. For Precision Crop Genomics: success signal is **a partner-ready Crop Improvement Dossier that no incumbent currently delivers**.
- **110% pre-Runpod sharpened: ZERO left to do on CPU before Runpod (operator directive 2026-05-02).** Strictly stronger than "do as much as you can." Every CPU-tractable component is 110%-complete; cutover-to-Runpod is a config-flag stub-swap.
- **Overnight long-horizon, autonomous, no false-flag reward hacking, no interim reporting (operator directive 2026-05-02).** Once the brief is received, the executor runs end-to-end through the night without check-ins. Every "build green" claim requires the full gate matrix.
- **GitHub + Hugging Face are the review surface.** Code, schemas, tests, audit trails, decision logs, KG nodes, and the PRD itself commit to GitHub. Large datasets and AI model artifacts go to Hugging Face under the **Architect-Prime user, not the Zer0pa org**. HF Pro account is OAuth-authenticated on the originating machine; streaming-corpus regime is enabled for any large dataset (per Polymath Diffusion 2026-05-02 directive).
- **PRD self-contained in the repo.** Executor can and must augment.
- **Fork-and-own across workstreams.** Pipelines/projects can steal patterns freely. Cannot be runtime co-dependent.
- **docs/research/RESISTANCE.md doctrine.** Every executor reads it before starting.
- **Operator delegates engineering / science / commercial decisions** to you (synthesis + orchestrator).
- **Sub-agent dispatch is Sonnet / Opus only (operator directive 2026-05-01, carried forward).** No GPT-5+ for code generation. The PRD encodes the dispatch table explicitly.
- **Anti-decisions pre-registered as binding falsifiers (Precision Crop Genomics specific):** APSIM commercial use; AgroNT / Nucleotide Transformer weights (CC-BY-NC-SA); AlphaFold3 / ESM3 main weights (non-commercial); WorldClim 2.1 (CC-BY-NC-SA); PLAZA (CC-BY-NC-SA); TAIR live curated data (paid); Google Earth Engine free tier for commercial use; Ultralytics YOLOv5/v8 default license; OpenDroneMap as hosted SaaS; EOX Sentinel-2 cloudless mosaics; herbicide tolerance traits in v1; PIP-equivalent insect resistance via novel insecticidal protein; pharma traits; trait IP ownership by Zer0pa; SA gene-edited product deployment absent GMO Act amendment; gene drives; cultivation bans; vertical integration into grain supply chains.

## What you must do

Write `PRD.md` at the top of this repo. The PRD specifies a long-horizon overnight execution by a separate set of overnight-executor agents on a separate Mac dev machine + a Runpod-bound machine. **The PRD must achieve ZERO left to do on CPU before any Runpod GPU is requested.** Every CPU-tractable component is 110%-complete; the cutover-to-Runpod is a config-flag stub-swap proving byte-identical envelopes / canonical hashes / falsifier classes / backend flags.

You are expected to:

- **Apply recursive fresh eyes.** Augment and innovate. Report 1 is itself a synthesis — your PRD must surface what the operator-as-synthesizer did not see, plus the executable specifics the executor needs that Report 1 does not yet pin down. The synthesis agent has identified twelve specific gaps; build on these. **If your PRD is not substantively richer than Report 1 plus the synthesis pass, you have not done your job.** You are explicitly empowered to challenge the synthesis recommendations with reasoning.
- **Spawn Sonnet / Opus sub-agents in parallel worktrees** per pipeline component (license-stamping ETL service / BrAPI data spine + self-hosted Breedbase / PLINK 2 + PHGv2 integration / rrBLUP + BGLR + sommer prediction stack / EnvRtype + BGGE G×E layer / pangenome-aware genotyping consumer / AlphaSimR + PyBrOpS breeding sim / FielDHub trial design / statgen + SpATS spatial correction / CROPSR + Cas-OFFinder edit design / off-target enumeration / regulatory router / Regulatory Fit Score implementation / dossier JSON-LD schema and validators / falsifier registry / audit-log + sha256 hash chain / REST-stub adapters for GPU-bound layers / plug-replaceability test matrix / cross-model ensemble disagreement aggregator / license-class taint detector / reproducible-build audit / KG + episodic memory / BoTorch-for-breeding qNEHVI optimiser).
- **Use Perplexity Pro / Gemini Advanced deep research** at engineering-blocker stuck points only (operator directive 2026-05-02 — survey lookups deferred unless they materially unblock engineering). Engineering-blocker lookups to resolve before Phase 0:
  1. **EU NGT regulation OJEU final text status** — Council adoption 21 April 2026; Parliament plenary 18 May 2026; OJEU publication during 2026; mid-2028 application. Verify current state.
  2. **US APHIS replacement rule RIN 0579-AE84 status** — pre-SECURE regime restored 16 June 2025; replacement rule expected 2026. Verify current state and pre-SECURE specifics for SDN-1-no-plant-pest.
  3. **PHGv2 v2.5+ release status** — Apache-2.0; TileDB-VCF backend; six species deployed as of April 2026. Verify any v2.6+ updates.
  4. **PlantCaduceus / HyenaDNA / Evo-2 / GPN / PlantRNA-FM weight licensing** — confirm Apache-2.0 / BSD-3 / MIT status in 2026 (the synthesis bases on Report 1's assertion; verify against current HF model cards).
  5. **AlphaFold DB v4 license status** — CC-BY 4.0 since January 2022; verify any 2026 changes.
  6. **Living Models BOTANIC weights** — released March 2026 with $7M seed funding; verify HF Hub presence and weight license status; assess fine-tuning compatibility.
  7. **UC Davis GRF-GIF non-exclusive licensing terms** — verify current pricing and per-species coverage for wheat / barley / triticale / citrus.
  8. **Corteva WUS2/BBM ag pool license terms** — verify current pricing for maize-elite / sorghum / sugarcane regeneration; assess any 2026 changes.
  9. **Pairwise Fulcrum platform sub-licensing terms** — verify current sub-licensee list and integration API for non-Bayer / non-Corteva / non-Tropic / non-CIMMYT third parties.
  10. **BrAPI v2.1 specification status** — verify current version and any v2.2 changes in 2026.
- **Resolve the three operator-engagement open questions:** Pairwise / Living Models partnership integration sequencing; SA go-to-market motion through ARC-BTP / SACTA / CIMMYT-Zimbabwe; intersectional-roadmap prioritisation.
- **Maximally front-load pre-Runpod engineering — to ZERO.** Every CPU-tractable component must be 110%-complete before Runpod cutover. This is the binding gate.

## Shape of the PRD

The structure is yours. Mirror the sibling Health / Materials / Energy / Synbio / Polymath AI / Polymath Diffusion / RCE patterns where useful; depart where your fresh eyes warrant. The PRD must cover at minimum:

- **Scope and boundary** (verbatim research-only block; Precision-Crop-Genomics-specific exclusions; anti-MVP / anti-toy / overdesigned best-in-class explicit; success signal is partner-ready dossier no incumbent delivers).
- **Architecture** (interface contracts: VCF/BCF/PLINK BED/PGEN canonical/HapMap/PHGv2 hVCF for genotype; GFA 1.1/2 + rGFA + PanSN naming for pangenome paths; MIAPPE 1.1 over BrAPI v2.1 with ISA-Tab + RO-Crate for phenotype; xarray/COG rasters for environment; Crop Ontology / Plant Ontology / Plant Trait Ontology / Plant Stress Ontology / ENVO / PECO for traits; PlantCV-compatible image stacks for phenomics; JSON-LD for dossier; sha256 hash chain for audit; plug-replaceability invariant — swap rrBLUP for BGLR for sommer in <1 day; swap PLINK2 for PHGv2 in <1 day; swap AlphaSimR for ChromaX in <1 day; swap CROPSR for CRISPR-PLANT v2 in <1 day).
- **Dossier-first active-inference architectural reframe** (per synthesis recommendation; you commit or override).
- **Falsification framing** (cross-model + license-class + Tier-1-vs-orphan-crop disagreement as three first-class falsifiers; falsifier registry covering invalid VCF / PGEN signature mismatch / mass-balance violation / off-target above threshold / RFS below 2.5 / class-C/D-input contamination of commercializable artifact / dossier-block missing required field / pangenome-aware-claim-without-pangenome-coverage / predicted-yield-without-G×E-environment / regulatory-route-citation-stale / partner-handoff-block-not-emitted / SA-deployment-without-SACTA-registration).
- **Build sequence** (CPU-first to ZERO; per-overnight-agent decomposition; layer order; gating test cases per layer).
- **Sub-agent dispatch table (operator directive 2026-05-01 binding)**: `(component, owner-agent (Sonnet|Opus), spawn-vs-serialise rationale, prompt template, success criterion, hand-back protocol, expected wall-clock, expected token budget)`. Encode every major component.
- **Phase 0 deliverable (CPU-only on Mac)**: license-stamping ETL service implemented and validated; BrAPI-native data spine wired with self-hosted Breedbase; PLINK 2 + PHGv2 integration in consumer mode; rrBLUP + BGLR + sommer prediction stack with cross-model disagreement aggregator; EnvRtype + BGGE G×E harness; AlphaSimR + PyBrOpS breeding sim; FielDHub trial design; statgen + SpATS spatial correction; CROPSR + Cas-OFFinder edit design; off-target enumeration with polyploid handling; regulatory router with full master decision matrix encoded as versioned JSON; dossier JSON-LD schema with all seven blocks locked and validated; falsifier registry; audit-log + sha256 hash chain; REST-stub adapters for GPU-bound layers; plug-replaceability test matrix; license-class taint detector; reproducible-build audit; KG + episodic memory; BoTorch-for-breeding qNEHVI optimiser wrapped around AlphaSimR; six-axis Pareto front demonstration on small AlphaSimR test corpus.
- **Phase 1 deliverable (Runpod GPU)**: foundation-model fine-tuning (PlantCaduceus + GPN + HyenaDNA fine-tunes for variant-effect and regulatory tasks); deep-learning prediction tracks (DNNGP / DeepGP / custom transformers) at production batch sizes; ChromaX (JAX/GPU) for ML-coupled breeding sim at scale; large-N MET training; graph genotyping at scale (Giraffe over 10K-100K samples); protein-structure tower runs (RFdiffusion3, MACE-OFF, ESMFold) at production batch — but ALL only after Phase 0 is ZERO-on-CPU complete.
- **Agent topology** (Opus 4.7 + Sonnet 4.x sub-agents — Sonnet/Opus only; Perplexity / Gemini engineering-blocker deep research only; KG with episodic memory).
- **Audit-trail spec** (campaign-grade per-dossier provenance with sha256 hash chain across all blocks + all model artifacts; KG schema with explicit nodes (Run / Phase / Sub-agent / Component / Dossier / DossierBlock / Decision / Falsifier / DispatchRecord / EvalArtifact / RegulatoryReference / LicenseStamp) and edges; per-step log shape).
- **Self-bootstrapping reasoner** ((input, dossier, gate-result, falsifier-judgment, partner-outcome) tuples → private dataset compounding the moat; structure mirrors Health's reasoner_queue/runs/<rid>/tuples.jsonl shape, forked not shared; dossier-tuple discipline is the substrate for the partner-handoff-outcome corpus).
- **License-stamping ETL service spec** (the moat per Report 1 Section 3 + synthesis recommendation #2): four-column license tag schema; Toronto-embargo expiry timestamp; SMTA flag; downstream taint filter; attribution emitter; license-class disagreement metric.
- **Crop Improvement Dossier JSON-LD schema lock** (per Report 1 Section 7 + synthesis recommendation #3): all seven blocks (Identity / Intervention Strategy / Performance Forecast / Risk / Regulatory / Provenance / Partner Handoff) with explicit JSON Schema; regenerable-from-inputs invariant; falsification loop on each block.
- **Regulatory Fit Score implementation** (per Report 1 Section 9 + synthesis recommendation #4): the formula encoded; the master decision matrix as versioned JSON with regulation citation chain per row; the threshold gates (4.0 green, 2.5 yellow, <2.5 red); falsification loop on the matrix.
- **BoTorch-for-breeding qNEHVI optimiser** (per Report 1 Section 6 + synthesis recommendation #6): forked-and-owned from Synbio MFMO; AlphaSimR or ChromaX as black-box simulator; six-axis Pareto front; Phase-1 deliverable not Phase-2 frontier.
- **Anti-decision pre-registration** (the eighteen anti-decisions enumerated in docs/process/MODUS-OPERANDI.md; any sub-brief proposing one fails brain-functionality at PRD review).
- **Acceptance gates** (scientific, engineering, brain-functionality, ZERO-on-CPU, license-class taint, Regulatory Fit Score implementation, dossier regenerability, anti-decision).
- **Productisation framing — partner-shaped not customer-shaped**. Pairwise / Living Models / Computomics partnership integration. No vertical integration. No trait IP. Mid-tier seed companies + CGIAR + NARES + specialty-crop programs + SA/SADC region as the under-filled niche.
- **Open questions for the operator / for the next agent** — explicitly. The three operator-engagement items (Pairwise / Living Models sequencing; SA go-to-market; intersectional-roadmap prioritisation) plus the Report-2-displacement reconciliation sub-brief.

Be granular. The overnight executor is a separate agent on a separate machine with no conversation context. Every interface, every contract, every threshold, every fallback must be readable from the PRD alone.

## Constraints

- Mac storage bounded on the originating machine (~42 GiB free at last check); bulk artifacts go to private Hugging Face under Architect-Prime when offload is needed.
- HF Pro account OAuth-authenticated on the originating machine; streaming-corpus regime enabled (per Polymath Diffusion 2026-05-02 directive). HF token at `~/.cache/huggingface/token` under Architect-Prime user.
- Runpod available for the GPU-bound Phase-1 deliverables; same `gh` / token paths as prior workstreams.
- AWS Open Data Registry + Microsoft Planetary Computer Pro + xarray/STAC for satellite compute; Google Earth Engine explicitly excluded for commercial use.
- No Docker on the originating Mac (overnight executor on Runpod may use Docker).
- No bulk local datasets — manifests + metadata + small slices only on Mac; corpus streams from HF.
- GitHub canonical. All sub-agent work commits back to `Zer0pa/Precision-Crop-Genomics` before PRD finalisation.
- No regulatory or clinical claims; no human-subject inference; no trait IP; no environmental release; no SA gene-edited deployment; no herbicide tolerance / PIP / pharma traits in v1; no vertical integration.
- **No cross-workstream runtime co-dependency.** Fork-and-own from prior workstreams (especially Synbio for protein-structure tower + MFMO + license decomposition + dossier-attestation; Health for reasoner-tuple discipline + audit-log shape; Materials for cross-model disagreement aggregator + falsifier-registry-first build; Energy for Runpod cutover golden-fixture invariance; Polymath workstreams for Sonnet/Opus + docs/research/RESISTANCE.md augmentation + HF Pro streaming) IS explicitly permitted.
- **Sub-agent dispatch is Sonnet / Opus only (operator directive 2026-05-01).** No GPT-5+.
- **ZERO left to do on CPU before Runpod (operator directive 2026-05-02).** Strictly stronger than "do as much as you can."
- **No false-flag reward hacking, no interim reporting (operator directive 2026-05-02).** Every "build green" requires the full gate matrix; the executor runs through the night without check-ins.

## Authorities and tooling

- `gh` CLI authenticated as Zer0pa-Architect-Prime on the originating machine.
- HF token at `~/.cache/huggingface/token` under Architect-Prime user (Pro account, OAuth-authenticated).
- Runpod available for Phase-1 GPU deliverables.
- Anthropic Opus 4.7 + Claude Code SDK or Anthropic Console — primary planning + heavy code review at maximum reasoning effort.
- Anthropic Sonnet 4.x — sub-agent code generation in parallel worktrees.
- Perplexity Pro / Gemini Advanced — engineering-blocker deep research only (research tools, not sub-agents).
- AWS Open Data Registry + Microsoft Planetary Computer Pro for satellite compute; AWS `af-south-1` (Cape Town) for SA-residency operations.
- LangGraph + Prefect + Parsl as the orchestration trio (carried from prior workstreams).
- BoTorch + Ax + GPyTorch for the L5 substrate (qNEHVI multi-objective).
- Open-source crop genomics stack per Report 1 Section 13: PLINK 2 + PHGv2 + BrAPI 2.1 + Breedbase + rrBLUP + BGLR + sommer + EnvRtype + BGGE + AlphaSimR + PyBrOpS + FielDHub + statgenSTA + statgenGxE + SpATS + DSSAT-CSM + AquaCrop-OSPy + CROPSR + CRISPR-PLANT v2 + Cas-OFFinder + CRISPRitz + CRISPResso2 + PlantCaduceus + HyenaDNA + Evo-2 + GPN + PlantRNA-FM + AlphaFold DB v4 + OpenFold3 + RFdiffusion3 + ProteinMPNN + PlantCV + pliman + Detectron2 + SAM2 + DINOv2 + MicMac.
- Sibling Zer0pa workstream repos for fork-and-own (especially `Zer0pa/Synthetic-Biology` for protein-structure tower + MFMO + license decomposition + dossier-attestation patterns).

## Where the PRD lands and what comes next

Commit `PRD.md` to the top level of `Zer0pa/Precision-Crop-Genomics`. Push to GitHub. After the PRD is final, write `HANDOFF-TO-OVERNIGHT-EXECUTOR.md` describing what the next role inherits, what they produce, and the constraints / authorities they operate under.

The operator will then trigger the overnight execution on a separate Mac dev machine (Phase 0 to ZERO-on-CPU) plus a Runpod-bound machine (Phase 1).

## Success criteria

- A PRD that the overnight executor can decompose into parallel sub-streams without further operator input.
- Every interface contract locked. Every falsifier specified. Every acceptance gate measurable.
- Phase 0 ZERO-on-CPU acceptance criterion explicit and binding.
- The license-stamping ETL service spec + the dossier JSON-LD schema lock + the Regulatory Fit Score implementation + the BoTorch-for-breeding qNEHVI optimiser are Phase-0 deliverables (not deferred).
- The eighteen anti-decisions pre-registered as binding falsifiers.
- The ten engineering-blocker deep-research lookups resolved or escalated.
- The three operator-engagement open questions resolved with operator engagement.
- Heavy fork-and-own from Synthetic Biology (sister bio-domain pipeline) and from Health / Materials / Energy / Polymath workstreams visible in every artifact.
- Anti-MVP / anti-toy / overdesigned best-in-class discipline visible in every component spec.
- docs/research/RESISTANCE.md doctrine carried through, augmented with fp-pretty-greenflag and fp-less-work-disguised-as-focus.
- No false-flag reward hacking; no interim reporting; full gate matrix on every "build green" claim.

## What you should pressure-test before locking the PRD

The synthesis agent committed to several positions that you should pressure-test with your fresh eyes:

- **Is the dossier-first active-inference reframe the right architectural primitive for Precision Crop Genomics?** The synthesis argues yes. You may have a stronger frame.
- **Should the BoTorch-for-breeding optimiser be Phase-1 (per synthesis, forking Synbio MFMO) or Phase-2 frontier-deferred (per Report 1)?** The synthesis argues Phase-1.
- **Should the v1.5/v2 architecture-changing intersectional roadmap be ranked as the synthesis suggests?** Operator engagement.
- **Are the four hard-exclusion license traps + three soft traps the complete set?** Re-verify against current 2026 license states.
- **Is base-editing-default-prime-editing-R&D-only the correct empirical commitment?** Re-check against any 2026 publications.
- **Is the master decision matrix in Section 9 complete and current?** Re-verify against EU NGT regulation final OJEU text and US APHIS replacement rule.
- **Is the Tier-1/2/3 species deployment matrix correctly framed?** Re-verify Corteva WUS2/BBM and UC Davis GRF-GIF licensing terms.
- **Is VIGE the right IP/regulatory arbitrage move for Tier-3 species in 2026?** Re-verify viral vector availability.
- **Should the SA strategy include direct ARC-BTP / SACTA partnerships in v1, or defer to Phase 2?** Operator engagement (Report 2 will displace).
- **What is the cross-machine artifact-exfiltration plan from Mac dev + Runpod to GitHub + HF for review?** Synthesis recommends fork from prior workstream patterns; you commit.

These are pressure-test points, not pre-baked answers. Take them or override them with reasoning.
