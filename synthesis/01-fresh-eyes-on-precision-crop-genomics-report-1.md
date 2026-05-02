# Fresh-Eyes Synthesis on the Precision Crop Genomics Report 1 (Full Technology Landscape)

Synthesis-agent output. Captures the operator-read on the source brief (`source-briefs/01-precision-crop-genomics-report-1-full-technology-landscape.md`) by Claude Opus 4.7 (1M context), 2026-05-02. Read by the orchestrator as the substrate for their own fresh-eyes augmentation.

## Boundary

Research infrastructure for in silico precision crop genomics. Outputs are research artifacts. No regulatory certification claims. No clinical or human-subject use. No trait IP. No environmental release of GMOs or gene-edited material by Zer0pa directly. No deployment to South Africa for gene-edited products absent GMO Act amendment. No herbicide tolerance, novel insecticidal protein, or pharma traits in v1 scope.

## Acknowledgement

Report 1 is exceptional. It is the most architecturally and commercially complete operator-authored Pre-PRD synthesis in the Zer0pa portfolio so far — denser than Polymath AI's blueprint, denser than the Polymath Diffusion frontier brief, structurally a hybrid technology-landscape + license-decomposition + regulatory-route + competitive-landscape + intersectional-science + South-Africa-strategic + ten-research-question-answers document. The six-layer architecture (L1 ZPE → L2 license-tagged knowledge → L3 candidate generation across cross/MAS/edit modalities → L4 in silico screening with G×E and regulatory scoring → L5 Bayesian active-learning optimisation → L6 typed dossier output); the LangGraph + BoTorch backbone with PLINK 2 PGEN canonical store and PHGv2 (TileDB-VCF) for haplotypes; the BrAPI v2.1 over self-hosted Breedbase data spine; the four-column license stamp on every record; the named architecture-critical breakthroughs of the last 24 months (PHGv2 + Giraffe + PanGenie pangenome stack; PlantCaduceus / HyenaDNA / Evo-2 / GPN / PlantRNA-FM plant DNA foundation models with permissive weights; the EU NGT regulation adoption April 2026 with mid-2028 application); the four hard-exclusion license traps (PLAZA / TAIR live / WorldClim 2.1 / EOX cloudless mosaics) plus three softer row-level traps (T3 Toronto Statement, CGIAR genebank SMTA, Doench/Fusi sgRNA scoring); the Tier-1/2/3 species deployment matrix with explicit IP-encumbrance (Corteva WUS2/BBM, UC Davis GRF-GIF, Pairwise Liu/Broad sublicense for base/prime editors, ePPE/PE6c CAS-Beijing alternatives, VIGE for IP/regulatory arbitrage); the explicit empirical evidence behind base-editing-default-prime-editing-R&D-only (ABE8e 30-80% A→G in rice/wheat vs 0-25% extreme variance for prime); the Jarquín reaction-norm GBLUP best practice; the "no production-grade BoTorch-for-breeding tool exists" gap; the seven-block Crop Improvement Dossier specification (Identity / Intervention Strategy / Performance Forecast / Risk / Regulatory / Provenance / Partner Handoff); the explicit Regulatory Fit Score formula `RFS = Σ over target markets [ MarketWeight × JurisdictionScore(0–5) × TraitMultiplier(0.3–1.0) × EditTypeCoefficient(0.2–1.0) ] − ProcessRiskPenalty` with the master decision matrix; the eight architecture-changing intersectional disciplines (information theory, graph theory, control theory, SE(3)-equivariant geometry, causal inference, climate physics, active inference, systems ecology); the commercial landscape with Pairwise / Living Models / Computomics flagged as partners-not-competitors and Inari positioned as closed-flywheel non-analog; the South Africa / Southern Africa / orphan crop layer with explicit ARC + SACTA + CGIAR + AATF + HarvestPlus + AOCC ecosystem; the ten research-question answers; the five frontier opportunities not-yet-production-ready; the build order in Section 15 — every component is decisive engineering judgment that this synthesis does not repeat.

This synthesis augments where Report 1 does not yet see when read top-to-bottom as a unified specification, plus folds in the operator's 2026-05-02 directive sharpening (ZERO-on-CPU before Runpod; no false-flag reward hacking; no interim reporting).

## The architectural reframe — Precision Crop Genomics is a license-clean partner-platform that hands off typed dossiers, not a model-research project

Report 1's stated framing is "the real Zer0pa moat is not modeling — it is the typed, license-aware, regulatory-routed handoff dossier." Correct; but the architectural primitive that subsumes the entire pipeline is sharper:

**Precision Crop Genomics is a license-clean partner-platform whose unit-of-output is the typed, regulatorily-routed Crop Improvement Dossier. Every layer of the six-layer pipeline exists to serve the dossier's seven blocks.** The stated framing positions the dossier as the moat; the architectural reframe makes the dossier the *agent's policy output*, with the six layers as the agent's perception-action factorisation.

Stated precisely:

- **Hidden state the platform infers about**: the optimal intervention strategy across (cross design / MAS / edit / VIGE / cisgenic) modalities for the input (crop × zone × trait set × constraints × regulatory route).
- **Generative model**: the composition of L1 ZPE encoding ∘ L2 knowledge layer ∘ L3 candidate generation ∘ L4 screening ∘ L5 BoTorch optimisation ∘ L6 dossier output — a probabilistic mapping from inputs to a Pareto-front of typed candidate interventions with full provenance.
- **Free energy F(θ) the platform minimises**: predictive loss on (genotype × environment × trait) outcomes, regularised by the license-class taint penalty (any class-C/D contamination in commercializable predictions is infinity-cost), the regulatory friction penalty (any sub-2.5 RFS market is high-cost), and the IP-encumbrance penalty (any encumbered transformation/regeneration target without licensing path is high-cost).
- **Expected free energy G(π) the platform uses to choose actions**: BoTorch qNEHVI multi-objective acquisition over the six-axis Pareto front (yield gain, drought resilience, nutrient efficiency, nutritional quality, regulatory friction, deployment ROI). The "Pareto-front-rather-than-scalar-output" design choice is the active-inference policy commitment; it is structural, not a tuning parameter.
- **Actions the platform recommends**: the typed Intervention Strategy block of the dossier — ranked candidates each tagged as `cross_design`, `mas_marker_set`, `crispr_edit`, `base_edit`, `prime_edit`, `vige_edit`, or `cisgenic_insertion` with full execution specifications.
- **Observations from partners**: which dossier candidates led to actual cultivar releases, which edits regenerated, which traits cleared regulatory review — feeding the partner-handoff-outcome corpus that compounds the moat.

This reframe matters for the orchestrator's PRD because **every layer's interface contract should be designed dossier-first, not model-first**. The L6 dossier JSON-LD schema must be locked first; everything else conforms to it. This mirrors the operator's "the handoff schema must be designed before the pipeline is built, because every other layer's output type contract depends on it" (Report 1 Section 7) — but elevates it from an implementation note to the architectural primitive.

Within the Zer0pa portfolio, this is the same pattern Health applied (falsification-engine subsumes the forward chain), Materials applied (variational unification subsumes the seven layers), Energy applied (information-theoretic channels subsume the dual sub-verticals), Synthetic Biology applied (active-inference loop subsumes L1-L7), Polymath AI / Polymath Diffusion AI applied (multi-compute-wall integration subsumes the three walls), RCE applied (market-signal-as-infrastructure subsumes the §A/§B/§C/§D inventory). For Precision Crop Genomics, **dossier-first active-inference is the architectural primitive**.

## Cross-tool / cross-model disagreement is the universal falsification primitive — applied to genomic prediction

Every prior workstream surfaced cross-model disagreement as the universal falsification primitive. Report 1 implies this without making it structural — Section 5 names rrBLUP / BGLR / sommer / DNNGP / DeepGP as parallel prediction tracks but does not specify ensemble-disagreement-as-falsifier.

**The synthesis recommendation: every prediction the platform emits carries a cross-model disagreement metric across at least three of {rrBLUP, BGLR, sommer, DNNGP}, computed on the same fold.** High agreement = high confidence; high disagreement = predictions whose model-dependence flags them for a falsifier in the dossier's Risk Block.

The Materials DPA-3 + MACE / Energy TGLF + CGYRO + GACODE / Synbio cross-kinetics ensemble / Polymath AI Qwen + SmolLM3 / Polymath Diffusion four-axis disagreement are all prior-workstream patterns. Precision Crop Genomics should fork the disagreement-aggregator code structure from Materials (it has the most mature implementation per the Wave A-E execution).

A second layer of disagreement, structurally important for Precision Crop Genomics specifically: **license-class disagreement** — when the same prediction is generated using a class-A-only training set vs a class-A+B+C training set, the disagreement signal is the upper bound on how much "academic-only" data is moving the prediction. The license-stamping ETL service (Report 1 Section 3) is the substrate for this; the orchestrator's PRD should specify the per-prediction license-class taint metric as a first-class quantity flowing through the audit log alongside primary outputs.

A third layer: **Tier-1-vs-orphan-crop disagreement** — pangenome-aware prediction vs SNP-only prediction on the same Tier-1 species should agree closely; on orphan crops, the SNP-only prediction is the only available signal but the platform should explicitly flag the absence of pangenome coverage as a falsifier (the Risk Block carries an "orphan-crop-pangenome-unavailable" flag).

## Twelve specific things Report 1 does not see when read top-to-bottom as a unified specification

### 1. The operator's 2026-05-02 directive sharpens the 110% axiom and the overnight discipline; the orchestrator's PRD must encode the new wording, not paraphrase from prior turns

Operator directive 2026-05-02: **"there must be ZERO left to do on CPU before they ask Runpod"** plus **"no false flag reward hacking or interim reporting — this is overnight execution."** Both are strictly stronger than the prior 110% / overnight phrasings. The orchestrator must encode them verbatim and gate the Runpod cutover on them. The PRD's engineering gate is **failed** if any sub-brief reaches Runpod with CPU-tractable work outstanding, OR if any sub-brief claims "build green" without the full gate matrix.

### 2. The license-stamping ETL service is the moat, named explicitly, and underspecified

Report 1 Section 3 states: "The Zer0pa-built piece in the knowledge layer is the license-stamping ETL service: every record ingested gets a four-column license tag, a Toronto-embargo expiry timestamp where applicable, an SMTA flag for physical material, and a downstream filter that prevents any model training run from mixing class-A and class-C/D inputs into a commercializable artifact. No upstream tool does this — it is a Zer0pa-owned data primitive."

This is the most concrete moat statement in any prior workstream. **The orchestrator's PRD must treat the license-stamping ETL service as the architectural primitive, not just one feature.** Every other layer consumes its output. Every model artifact carries its taint metric. Every dossier emits its attribution chain. The PRD should specify:

- The four-column license tag schema (code / data / weights / API license each with class A/B/C/D/E classification).
- The Toronto-embargo expiry timestamp shape (per-record; auto-expires at the 1-year mark for TAIR-style embargoes).
- The SMTA flag for physical material with link to the ITPGRFA Annex 1 jurisdiction table.
- The downstream taint filter as a hard gate at the boundary between knowledge layer and model training (any class-C/D input forced into a commercializable artifact triggers a falsifier).
- The attribution emitter that writes CC-BY citations per dossier for every contributing data source.
- The license-class disagreement metric (synthesis recommendation #2 above).

### 3. The seven-block dossier JSON-LD schema must be locked before any other layer's interface contract

Report 1 Section 7 says the dossier "must be designed before the pipeline is built, because every other layer's output type contract depends on it." **The orchestrator's PRD must lock the JSON Schema for each of the seven blocks (Identity / Intervention Strategy / Performance Forecast / Risk / Regulatory / Provenance / Partner Handoff) BEFORE any code is written for L1-L5.** This is the dossier-first architectural primitive.

The orchestrator should specify the schema-locking sub-brief as the first sub-brief, mirroring the operator's canonical Zod migration brief shape from RCE (Context / Why / Scope / Acceptance Gates / Falsification Loop / Resistance Self-Check / Deliverables / Success). Falsification loop: deliberately corrupt one block's required field; confirm the validator rejects it; revert.

### 4. The Regulatory Fit Score formula is explicit but the master decision matrix needs versioned encoding with citation chain

Report 1 Section 9 states the RFS formula: `RFS = Σ over target markets [ MarketWeight × JurisdictionScore(0-5) × TraitMultiplier(0.3-1.0) × EditTypeCoefficient(0.2-1.0) ] − ProcessRiskPenalty`. The jurisdiction scores, trait multipliers, and edit type coefficients are listed but the master decision matrix is not delivered as a structured artifact.

**The orchestrator's PRD must specify the master decision matrix as a versioned JSON artifact** committed to the repo, with: per-jurisdiction score (with regulation citation, effective date, sunset date if known); per-trait multiplier (with regulatory text citation); per-edit-type coefficient (with empirical efficiency citation); a regenerable derivation showing how an input (crop × trait × jurisdiction × edit type) produces an RFS. The matrix must be falsifiable: deliberately update one regulatory text reference; confirm the RFS recomputes; revert. Versioning matters because regulations change — the matrix is dated, with a "sunset / next-review" timestamp per row.

### 5. Pairwise and Living Models as partners is a strategic claim; the API integration order should reflect it

Report 1 Section 11 explicitly positions: "Pairwise [...] is the most aggressive licensor: their Fulcrum platform is sub-licensed to Bayer, Corteva [...], Tropic, CIMMYT, Enza Zaden, Genus, and academic partners — making Pairwise the most likely strategic partner for Zer0pa rather than competitor." And: "Living Models released BOTANIC (open weights on Hugging Face) in March 2026 [...] this is the closest direct technical peer and warrants close watching, possibly partnership rather than competition."

**The orchestrator's PRD should encode the partner-shaped vs competitor-shaped distinction in the integration order.** Specifically:

- Pairwise Fulcrum API integration spec is a Phase-2 deliverable (after v1 dossier shape is stable), not a competitor-deliberate-incompatibility play.
- Living Models BOTANIC weights consumption is a Phase-1 deliverable — fine-tune BOTANIC on Zer0pa's license-clean training set as one of the foundation-model paths.
- Syngenta Cropwise Open Platform (opened to third-party developers November 2025; ~70M ha; 30+ countries) is a Phase-2 distribution-channel integration.
- Corteva Genlytix is a long-run exit-partner relationship; v1 does not integrate with Genlytix directly.

### 6. The "no production-grade BoTorch-for-breeding tool exists" gap is the highest-leverage build piece — and it is also a cross-workstream pattern

Report 1 Section 6: "No production-grade BoTorch-for-breeding tool exists as of May 2026 [...]. The clean architecture is to wrap AlphaSimR or ChromaX as a black-box simulator behind a BoTorch GP surrogate with qNEHVI multi-objective acquisition; this is the highest-impact piece Zer0pa can build itself."

**This is the highest-leverage build piece for Precision Crop Genomics, AND it is a cross-workstream pattern that has appeared in every prior pipeline-vertical workstream.** Synbio MFMO, Materials BoTorch acquisition, Energy qMFKG, Polymath Diffusion AFP-controlled scheduler — all are BoTorch multi-objective optimisers wrapped around a black-box simulator. **Fork-and-own from Synbio's MFMO is the natural starting point** if Synbio's MFMO is far enough along; reimplement inside Precision Crop Genomics. No runtime co-dependency.

The synthesis recommendation: the orchestrator's PRD specifies the BoTorch optimiser sub-brief as a Phase-1 deliverable (not Phase-2 frontier), forking the shape from Synbio MFMO with breeding-cycle-simulator (AlphaSimR or ChromaX) replacing the metabolic-engineering-simulator. Acceptance criterion: the optimiser produces a six-axis Pareto front on a small AlphaSimR test corpus before any Runpod is touched (per ZERO-on-CPU directive).

### 7. The South Africa carveout has architectural implications that need explicit routing logic, not just narrative

Report 1 Section 9: "South Africa's January 2024 Section-19 ministerial decision keeps gene-edited crops under the GMO Act 1997 [...] The structural workaround is to perform CRISPR work in Kenya/Nigeria/Mauritius, complete non-GMO determination in the origin jurisdiction, and import the resulting trait into SA via conventional crossing under SACTA-recognized cultivar registration."

**This is operational, not narrative. The dossier's Regulatory Block must encode the SA-specific routing.** Concretely:

- The Intervention Strategy block carries an `origin_jurisdiction` field per edit candidate (where the wet-lab work happens — Kenya / Nigeria / Mauritius / etc.).
- The Regulatory Block carries the per-jurisdiction route classification with explicit handling of the SA-import-via-conventional-crossing path.
- The Partner Handoff block for SA seed companies carries the SACTA-compatible cultivar registration documentation chain — distinct from the Kenya/Nigeria/Mauritius wet-lab partner handoff.
- The Performance Forecast block carries SA-specific predictions from the imported trait at SACTA-compatible trial sites.

The orchestrator's PRD must specify this as a first-class routing logic in L4/L6, not a narrative caveat.

### 8. The eight architecture-changing intersectional disciplines are listed but not prioritised; v1.5/v2 roadmap needs explicit ordering

Report 1 Section 10 lists eight architecture-changing disciplines (information theory, graph theory, control theory, SE(3)-equivariant geometry, causal inference, climate physics, active inference, systems ecology) and six scoring-only disciplines (statistical mechanics, evolutionary biology, signal processing, computer vision, optimization theory, economics). The architecture-changing list is "also the prioritized v1.5/v2 development roadmap" — but the prioritisation within the list of eight is not specified.

**The synthesis recommendation: the orchestrator's PRD ranks the architecture-changing list in priority order based on (a) cross-workstream fork-and-own availability, (b) operator-strategic-value, (c) implementation cost.** Suggested ranking:

1. **Causal inference** — high cross-workstream fork-and-own (Synbio's GO-CBED is far enough along; CI-GWAS demonstrated multi-trait causal graphs); replaces correlational GWAS with do-calculus. Highest leverage because it reframes the entire L4 layer.
2. **Climate physics + active inference (joint)** — climate physics adds the learned environment encoder branch; active inference turns the breeding pipeline into a POMDP. These two compose: G×E-VAE with sequential intervention selection. Polymath Diffusion's three-wall integration pattern provides a fork.
3. **SE(3)-equivariant geometry** — fork from Synbio's Unknown Enzyme Generative Sub-Pipeline; protein-structure tower for NLR receptor / photosynthetic enzyme / TF DBD trait engineering.
4. **Graph theory** — GNN message-passing over the heterogeneous knowledge graph; centrality priors on marker effect.
5. **Information theory** — Tishby-style bottleneck encoder; useful but lower marginal lift than the above.
6. **Control theory** — ODE/PDE dynamics layer; useful for time-varying traits but high implementation cost.
7. **Systems ecology** — holobiont rather than genotype; long-term value but data substrate is thin.

This is a synthesis recommendation; the orchestrator can take, refine, or override.

### 9. Report 2 is forthcoming and may displace some PRD decisions — the orchestrator should design for that

Report 1 Section 15: "Report 2 will collapse this landscape into a sharper architectural specification with concrete schema definitions, partner integration sequences, and the South African go-to-market motion through ARC-BTP, SACTA, and CIMMYT-Zimbabwe."

**The orchestrator should design the PRD with explicit Report-2-displacement points.** Specifically:

- The dossier JSON-LD schema is locked Phase-1 from Report 1 alone, but the orchestrator should mark which schema fields are Report-2-pending (e.g., concrete partner integration sequence fields in the Partner Handoff block).
- The South African go-to-market motion is Phase-2; v1 covers the architectural carveout but defers the SACTA / ARC-BTP / CIMMYT-Zimbabwe execution detail.
- The orchestrator's PRD should include a "Report 2 reconciliation" sub-brief that runs once Report 2 lands, comparing Report 2's recommendations against the v1 PRD and surfacing any displacement.

### 10. Five frontier opportunities are explicitly v1.5/v2-deferred but the BoTorch-native multi-objective breeding-cycle optimizer is recurring across workstreams

Report 1 Section 14 names five frontier opportunities not-yet-production-ready: BoTorch-native multi-objective breeding-cycle optimizer; causal-inference-for-trait-discovery layer; plant image foundation model; ImageNet-for-crop-GSxE benchmark; reinforcement-learning-distilled breeding policy. Plus a frontier-most-likely-to-change-v1-architecture: plant single-cell foundation model (scPlantLLM / scGPT-fine-tune / Geneformer-fine-tune on Plant Cell Atlas).

**The synthesis flags the BoTorch-native multi-objective breeding-cycle optimizer as recurring across workstreams (synthesis observation #6 above) — promote from frontier-deferred to Phase-1 deliverable via fork-and-own.** The other four frontiers stay v1.5/v2.

The plant-single-cell-FM frontier is the one most likely to change architecture during 2026; the orchestrator should pre-architect a model branch interface that can absorb a commercial-licensed plant scFM if one emerges.

### 11. The competitive landscape suggests Inari is closed-flywheel non-analog but Benson Hill's Chapter 11 + Chapter 7 carries a structural lesson Zer0pa must encode

Report 1 Section 11: "Benson Hill filed Chapter 11 in March 2025 and Chapter 7 in September 2025 [...] the lesson is that vertically-integrated grain supply chains paired with computational platforms are capital-fragile."

**The orchestrator's PRD must encode this as a binding architectural constraint: Zer0pa is platform-only and explicitly refuses to take trait IP, vertical integration, or grain supply chain ownership.** The anti-decision pre-registration in `MODUS-OPERANDI.md` § Acceptance Gates and `HANDOFF-TO-ORCHESTRATOR.md` § Anti-decisions already captures "no trait IP"; the synthesis reinforces this with the Benson-Hill lesson explicitly cited.

### 12. The orphan crop layer has architectural implications for SNP-only graceful degradation, not just narrative

Report 1 Section 12: "The orphan-crop layer is advancing rapidly even where Zer0pa's narrative center stays on Tier-1 cereals. [...] Most African indigenous crops still lack curated reference genomes beyond AOCC publications, meaning Zer0pa would need to handle de novo assembly and annotation in many cases — but the rails are laid."

**The orchestrator's PRD must specify the SNP-only-graceful-degradation logic explicitly.** Concretely:

- L1 input encoding gracefully accepts SNP-only when no pangenome exists for the target species.
- L4 screening explicitly flags "orphan-crop-pangenome-unavailable" in the dossier's Risk Block.
- The Performance Forecast block carries a different uncertainty model when pangenome coverage is absent (wider credible intervals; explicit caveat in the partner-handoff narrative).
- The Bayesian active-learning loop (L5) adjusts acquisition function weights when operating in SNP-only mode — orphan-crop work prioritises information-gain over yield-gain because the prior is weaker.

This is one of the architectural commitments most likely to differentiate Zer0pa for NARES / AOCC partners; it is implicit in Report 1 and should be made explicit in the PRD.

## A non-cross-workstream substrate proposal — heavy fork-and-own from Synthetic Biology and Materials

Precision Crop Genomics does not have a Materials / Energy-shaped cross-workstream substrate-sharing recommendation, because Report 1 was disciplined about it.

That said, the synthesis surfaces specific fork-and-own opportunities:

**From Synthetic Biology (highest-value source — both are bio-domain pipelines):**
- The four-column license decomposition pattern (already mirrored in Report 1; verbatim fork at the implementation level).
- The SBOL3-attested audit-trail with sha256 hash chain → JSON-LD-attested dossier with sha256 hash chain. Forked structure.
- The Unknown Enzyme Generative Sub-Pipeline tools (RFdiffusion3, MACE-OFF, ProteinMPNN, AlphaFold DB v4, OpenFold3, ESMFold) reusable as the SE(3)-equivariant protein-structure tower for trait engineering. Synbio-fork-and-own.
- The Synbio MFMO multi-fidelity BoTorch optimiser shape forked as the qNEHVI breeding-cycle optimiser shape.
- The CEKM training corpus discipline (BRENDA CC BY 4.0 + EnzyExtract MIT + GotEnzymes2 CC BY 4.0; synthetic negatives via active-site distance gates; held-out partition for blind eval; calibration-curve audit) → translates to crop-genomic-prediction corpus discipline (G2F + CIMMYT + 3K Rice + AgERA5 + SoilGrids; synthetic negatives via cross-population permutation; held-out leave-one-environment-out / leave-one-year-out partitions; calibration-curve audit per prediction model).

**From Health (TxGemma reasoner-tuple discipline):**
- Every (input, dossier, gate-result, falsifier-judgment) writes to a private dataset that compounds the moat. Forked structure. The dossier-tuple discipline is the substrate for the partner-handoff-outcome corpus that Report 1 Section 13 names as one of the three substrates that compound.

**From Materials (DPA-3 + MACE ensemble disagreement):**
- Cross-model disagreement aggregator code structure (the most mature implementation across the prior workstreams; Wave A-E execution-hardened). Fork directly for the rrBLUP / BGLR / sommer / DNNGP ensemble.

**From Energy (same-shape Runpod cutover with `httpx.MockTransport` golden-fixture invariance):**
- Mac-CPU-vs-Runpod-GPU equivalence test pattern. Forked for the Precision Crop Genomics CPU-vs-Runpod cutover gate.

**From Polymath Diffusion / Polymath AI (RESISTANCE.md augmentation + Sonnet/Opus-only sub-agent dispatch + HF Pro streaming-corpus regime):**
- fp-pretty-greenflag and fp-less-work-disguised-as-focus added to RESISTANCE.md.
- Sonnet / Opus only sub-agent dispatch.
- HF Pro OAuth-authenticated session for streaming large datasets to/from training (relevant for foundation-model fine-tuning corpus and large MET training data).

**From RCE (surgical-sub-brief shape):**
- The operator's canonical Zod v3 → v4 migration brief shape (Context / Why / Scope (Authorised + Not Authorised) / Acceptance Gates / Falsification Loop / Resistance Self-Check / Deliverables / Success) for any specific schema-locking task — the Crop Improvement Dossier schema-locking sub-brief is the natural first application.

All forks; no runtime co-dependency. Precision Crop Genomics carries its own copy.

## What the orchestrator should pressure-test before locking the PRD

Same shape as prior workstreams — pressure-test points, not pre-baked answers:

- **Is the dossier-first active-inference reframe the right architectural primitive for Precision Crop Genomics?** The synthesis argues yes. You may have a stronger frame.
- **Should the BoTorch-for-breeding optimiser be Phase-1 (per synthesis recommendation, forking Synbio MFMO) or Phase-2 frontier-deferred (per Report 1 Section 14)?** The synthesis argues Phase-1 because the gap is the highest-leverage build piece and Synbio MFMO provides a fork-and-own starting point.
- **Should the v1.5/v2 architecture-changing intersectional roadmap be ranked as the synthesis suggests (causal inference → climate-physics+active-inference → SE(3) → graph → information theory → control theory → systems ecology), or differently?** Operator engagement.
- **Are the four hard-exclusion license traps (PLAZA / TAIR live / WorldClim 2.1 / EOX cloudless) and three soft traps (T3 Toronto, CGIAR SMTA, Doench/Fusi) the complete set?** The orchestrator's PRD should re-verify against current 2026 license states; some may have changed.
- **Is base-editing-default-prime-editing-R&D-only the correct empirical commitment?** Report 1 Section 4 says yes (ABE8e 30-80% A→G in rice/wheat vs 0-25% extreme variance for prime). Re-check against any 2026 publications.
- **Is the master decision matrix in Section 9 complete and current?** Re-verify against EU NGT regulation final OJEU text (publication during 2026); US APHIS replacement rule RIN 0579-AE84 expected 2026; any 2026 jurisdiction updates.
- **Is the Tier-1 species deployment matrix (Arabidopsis / *Nicotiana* / tomato / rice japonica / potato / lettuce / Camelina; Tier-2 wheat-with-GRF-GIF / barley / triticale / citrus; Tier-3 maize-elite / sorghum / sugarcane via Corteva WUS2/BBM) correctly framed?** Re-verify Corteva licensing terms; re-verify UC Davis GRF-GIF non-exclusive availability.
- **Is VIGE the right IP/regulatory arbitrage move for Tier-3 species in 2026?** Report 1 says yes. Re-verify BSMV / FoMV / TRV / PVX viral vector availability and current academic IP positions.
- **Should the SA strategy include direct ARC-BTP / SACTA partnerships in v1, or defer to Phase 2?** Operator engagement (Report 2 will displace).
- **What is the cross-machine artifact-exfiltration plan from the Mac dev machine + Runpod machine to GitHub + HF for review?** Synthesis recommends fork from prior workstream patterns; orchestrator commits.

These are pressure-test points. Take them or override them with reasoning.

## What the synthesis agent recommends and the operator should weigh in on

Three points warrant operator engagement before the orchestrator locks the PRD:

1. **The Pairwise / Living Models partnership integration sequencing.** Should v1 start outreach to Pairwise for Fulcrum platform sub-licensing? Living Models BOTANIC fine-tuning is technically Phase-1 but the partnership conversation is operator-strategic.
2. **The South African go-to-market motion through ARC-BTP / SACTA / CIMMYT-Zimbabwe.** Report 2 will cover this; operator may want to pre-decide whether v1 includes any SA partnership outreach or defers entirely.
3. **The intersectional-roadmap prioritisation.** The synthesis suggests an ordering; the operator may have a stronger preference based on existing Zer0pa research (e.g., active inference is also central to Polymath Diffusion AI, so co-developing the active-inference layer across workstreams via fork-and-own is operator-strategic).

All other open questions are within the orchestrator's delegated authority per the operator's 2026-05-01 refinement.

## Provenance

- Synthesis agent: Claude Opus 4.7 (1M context).
- Source: `source-briefs/01-precision-crop-genomics-report-1-full-technology-landscape.md` (operator-authored Pre-PRD Research Synthesis Report 1 of 2, 160 dense lines, ~57 KB, May 2026). Report 2 forthcoming.
- Reference reading of sibling repos `Zer0pa/Health`, `Zer0pa/Materials`, `Zer0pa/Energy`, `Zer0pa/Synthetic-Biology`, `Zer0pa/Polymath-AI`, `Zer0pa/Polymath-Diffusion-AI`, and `Zer0pa/RCE` permitted at the orchestrator level for cross-workstream pattern observation only (read for fork-and-own; no runtime co-dependency).
- Date: 2026-05-02.
- Operator refinements (binding for all workstreams) as captured in `MODUS-OPERANDI.md` § Operator refinements 2026-05-01 + sharpened 2026-05-02 (ZERO-on-CPU before Runpod; no false-flag reward hacking; no interim reporting).
- Operator directive (carried forward from Polymath Diffusion 2026-05-01): sub-agent dispatch is **Sonnet / Opus only**.
- Next role: Precision Crop Genomics orchestrator (writes `PRD.md`).
