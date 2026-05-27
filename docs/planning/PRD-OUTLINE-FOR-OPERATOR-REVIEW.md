# PRD Outline for Operator Review — Precision Crop Genomics

**Status:** DRAFT for operator review BEFORE committing full PRD.md (binding gate per `docs/handoffs/HANDOFF-TO-ORCHESTRATOR.md`).
**Author:** PCG orchestrator (Claude Opus 4.7, 1M context), 2026-05-02.
**Purpose:** Surface the structural decisions and substantive resolutions so the operator can intervene before the full PRD is written.

---

## 0. What the operator should sign off on before I write the full PRD

This outline is not the PRD. It is the architectural commitment summary — the points the operator most likely wants to override before I write 1,200+ lines of binding spec. If you disagree with any of these, push back here and I'll revise. If you sign off, I'll write the full PRD without further interim reporting (per operator directive 2026-05-02), commit and push, then write `HANDOFF-TO-OVERNIGHT-EXECUTOR.md`.

**Three things you should know up front:**
1. I am committing to the synthesis's **dossier-first active-inference architectural reframe** as the primitive. Every layer's interface contract is designed dossier-first.
2. I am **challenging the synthesis's intersectional-roadmap ranking** — promoting SE(3)-equivariant geometry from v1.5 to Phase-1 (fork from Synbio's Unknown Enzyme tower is ready), and I'm explaining why.
3. I am **challenging Report 1's deferral of the BoTorch-for-breeding qNEHVI optimiser to frontier-v2** — promoting it to Phase-0 deliverable, with the six-axis Pareto front demonstrated on AlphaSimR test corpus before any Runpod is requested. The synthesis already proposed this; I'm locking it.

ZERO-on-CPU before Runpod is the binding Phase-0 acceptance gate. No exceptions.

---

## 1. PRD section structure (mirrors Synbio's 27-section template, adapted for PCG)

| § | Section | PCG-specific content |
|---|---|---|
| 0 | Boundary | Verbatim research-only block + 18 anti-decisions enumerated |
| 1 | Operator mandate (binding, verbatim) | Anti-MVP/anti-toy/overdesigned best-in-class; ZERO-on-CPU before Runpod; no false-flag reward hacking; no interim reporting; GitHub canonical + HF Pro under Architect-Prime; Sonnet/Opus only sub-agent dispatch; fork-and-own across workstreams; docs/research/RESISTANCE.md doctrine binding |
| 2 | Source basis (read order) | docs/research/RESISTANCE.md → PRD.md → HANDOFF-TO-OVERNIGHT-EXECUTOR.md → docs/process/MODUS-OPERANDI.md → docs/handoffs/HANDOFF-TO-ORCHESTRATOR.md → docs/research/synthesis/01 → docs/research/source-briefs/01 + Report 2 reconciliation pointer → sibling repos for fork-and-own |
| 3 | Scope and Tier-1/2/3 species validation triple | **PCG validation triple** (analog to Synbio HMO seed): Seed 1 known-good (maize G2F yield); Seed 2 known-borderline (wheat Ug99 SrxLr base-edit); Seed 3 novel (bambara groundnut SADC drought × yield, orphan-crop SNP-only mode) |
| 4 | Architecture invariants | UniversalLayerEnvelope (PCG-shaped, forked from Synbio); plug-replaceability invariant; six-layer factorisation L1-L6; dossier-first active-inference primitive |
| 5 | Falsification framework | Three-tier falsifier hierarchy (Fast / Medium / Heavy) forked from Synbio; **22 named falsifiers** committed in `audit/falsifiers.yaml` BEFORE any layer code; cross-model disagreement + license-class disagreement + Tier-1-vs-orphan-crop disagreement as three first-class falsification primitives |
| 6 | Layer contracts | L1 ZPE encoding; L2 license-stamping ETL service + knowledge layer; L3 candidate generation (cross/MAS/edit/VIGE/cisgenic); L4 in silico screening (genomic prediction stack + G×E + pangenome-aware + off-target + RFS); L5 BoTorch qNEHVI multi-objective optimisation + active inference; L6 Crop Improvement Dossier with seven blocks; **L4.5 SE(3) protein-structure tower** (forked from Synbio Unknown Enzyme tools — Phase-1 promoted from frontier) |
| 7 | Repository outcome | Standard layout: `src/zer0pa_pcg/` with adapters/{l1_zpe, l2_etl, l2_knowledge, l3_cross_mas, l3_edit, l4_5_protein_tower, l4_prediction, l4_gxe, l4_pangenome, l4_offtarget, l4_rfs, l5_botorch, l6_dossier}/; falsifiers/; disagreement/; gpsm/ (the Zer0pa-owned Genomic Prediction Stack Model); audit/; kg/; rest/; plug_replaceability/; cli/ |
| 8 | Agent topology + sub-agent dispatch table | Per-component dispatch (Sonnet 4.6 / Opus 4.7); spawn-vs-serialise rationale; prompt template; success criterion; hand-back protocol; expected wall-clock; expected token budget |
| 9 | Audit trail and KG — **Zer0pa Crop Improvement Dossier Audit-Trail Specification v0.1** | JSON-LD + PROV-O extension forked from Synbio SBOL3+PROV-O; sha256 hash chain across all dossier blocks + all model artifacts + all license stamps; campaign-grade per-dossier provenance |
| 10 | Data sovereignty (three tiers) | Tier-1 (license class A, fully open commercial); Tier-2 (license class B, attribution required); Tier-3 (class C/D, excluded from commercializable artifacts via taint detector); Tier-E (embargoed, auto-expires per Toronto rule) |
| 11 | Self-bootstrapping reasoner — **Crop Dossier Tuple Flywheel** | (input, dossier, gate-result, falsifier-judgment, partner-outcome) tuples → private dataset compounding the moat; structure mirrors Health reasoner_queue/runs/<rid>/tuples.jsonl forked; partner-handoff-outcome corpus per Report 1 §13 |
| 12 | GPSM training corpus design | License-clean composite: G2F + CIMMYT panels (599-wheat, 2K, Iranian) + 3K Rice + 1001 Genomes + TERRA-REF + GWHD + AgERA5 + SoilGrids 2.0 + CHIRPS v3 + Sentinel-2/Landsat/HLS; synthetic negatives via cross-population permutation; held-out leave-one-environment-out / leave-one-year-out partitions; calibration-curve audit per prediction model |
| 13 | Partner integration adapter plan (replaces Synbio's cell-free TX-TL adapter) | BrAPI v2.1 adapter (consumer + provider); Pairwise Fulcrum REST stub adapter (Phase-1 scaffold; Phase-2 partnership conversation operator-deferred); Living Models BOTANIC fine-tune adapter (Phase-1 conditional on license verification); Syngenta Cropwise Open Platform adapter (Phase-2); NRGene GenoMAGIC consumer adapter (Phase-2); Hiphen Cloverfield phenotyping API consumer (Phase-2) |
| 14 | Hugging Face storage plan | Architect-Prime user (NOT Zer0pa org); HF Pro OAuth-authenticated streaming-corpus regime; bulk slices > 5 GB to HF; manifests + metadata only on Mac; per-corpus repo: `Architect-Prime/pcg-g2f-met-v0.1`, `Architect-Prime/pcg-cimmyt-wheat-v0.1`, `Architect-Prime/pcg-3k-rice-v0.1`, `Architect-Prime/pcg-pangenome-tier1-v0.1`, `Architect-Prime/pcg-aocc-orphan-v0.1`, `Architect-Prime/pcg-fixtures-bootstrap-v0.1` |
| 15 | CPU-first build sequence — **overnight execution waves** | Wave 0 (boundary + falsifier registry + KG schema + dossier audit-trail spec + license stamp schema); Wave 1 (license-stamping ETL service + dossier JSON-LD all-seven-blocks-locked + RFS master decision matrix as versioned JSON); Wave 2 (BrAPI/Breedbase data spine + PLINK 2 + PHGv2 consumer + canonical genotype store); Wave 3 (rrBLUP + BGLR + sommer prediction stack + cross-model disagreement aggregator + EnvRtype + BGGE G×E); Wave 4 (AlphaSimR + PyBrOpS breeding sim + FielDHub trial design + statgen + SpATS); Wave 5 (CROPSR + Cas-OFFinder + CRISPRitz + CRISPResso2 edit design + off-target enumeration + polyploid handling); Wave 6 (regulatory router + Regulatory Fit Score + jurisdiction × trait × edit-type matrix); Wave 7 (BoTorch qNEHVI optimiser wrapping AlphaSimR + six-axis Pareto front demonstration); Wave 8 (SE(3) protein-structure tower CPU-side stub adapters + REST-stub for Runpod swap); Wave 9 (KG + episodic memory + reasoner_queue + dossier-tuple discipline); Wave 10 (plug-replaceability test matrix + license-class taint detector + reproducible-build audit + cutover golden-fixture invariance test); Wave 11 (PCG validation triple end-to-end: seed 1 + seed 2 + seed 3 dossiers emit; ZERO-on-CPU gate verified) |
| 16 | Core config flags | `PCG_<LAYER>_BACKEND=stub|local_cpu|gpu_rest_stub|runpod_rest`; `PCG_LICENSE_CLASS_FILTER=A|A_PLUS_B|ALL`; `PCG_PANGENOME_MODE=tier1_aware|snp_only|auto`; `PCG_REGULATORY_ROUTE=v1_eu_pre_2028|v1_eu_post_2028|v1_us_pre_secure|v1_us_post_replacement` etc. |
| 17 | REST stub surface | Every GPU-bound layer has a REST stub returning shape-correct canned outputs validated against the same envelope schema as production endpoint; Runpod cutover is config-flag stub-swap; `httpx.MockTransport` golden-fixture invariance test (forked from Energy Wave 4) |
| 18 | Frontier slots — three concrete BlockedSourceManifest entries | (a) Plant single-cell foundation model fine-tune on Plant Cell Atlas — pending commercial-licensed plant scFM emergence; (b) Closed-loop active-inference policy distillation with audit-friendly rule extraction (Younis et al. 2024 RL frontier; not yet packaged); (c) ImageNet-for-crop-GSxE benchmark public release (frontier; v2 community contribution) |
| 19 | Runpod migration plan | Config-flag stub-swap; byte-identical envelopes verified by golden fixture; foundation-model fine-tuning (PlantCaduceus + GPN + HyenaDNA + BOTANIC); deep-learning prediction tracks (DNNGP / DeepGP / custom transformers) at production batch; ChromaX (JAX/GPU) ML-coupled breeding sim at scale; large-N MET training; graph genotyping at scale (Giraffe over 10K-100K samples); SE(3) protein-structure tower runs (RFdiffusion3, MACE-OFF, ESMFold) at production batch; AWS af-south-1 satellite compute for SA residency |
| 20 | Acceptance gates | Scientific gate; engineering gate (plug-replaceability test passes); brain-functionality gate; **ZERO-on-CPU gate** (binding); license-class taint gate; **Regulatory Fit Score implementation gate** (master decision matrix + citation chain encoded; falsifier-loop verified); **dossier regenerability gate** (regenerable from inputs at any time); **anti-decision gate** (any sub-brief proposing one of the 18 anti-decisions fails brain-functionality at PRD review and escalates to operator) |
| 21 | Productisation framing — partner-shaped not customer-shaped | Pairwise / Living Models / Computomics / Syngenta Cropwise / Corteva Genlytix integration order; mid-tier seed companies + CGIAR + NARES + specialty-crop programs + SA/SADC under-filled niche; no vertical integration; no trait IP; Benson Hill Chapter 11 lesson encoded |
| 22 | License and status findings (the 10-item resolution table) | EU NGT; US APHIS; PHGv2; PlantCaduceus/HyenaDNA/Evo-2/GPN/PlantRNA-FM; AlphaFold DB v4; Living Models BOTANIC; UC Davis GRF-GIF; Corteva WUS2/BBM; Pairwise Fulcrum; BrAPI v2.1 — each with current state (May 2026) and PRD-binding action |
| 23 | Open questions resolved by orchestrator (no operator round-trip) | Resolution of synthesis pressure-test points + license-trap completeness re-verification + base-editing-default empirical commitment + Tier-1/2/3 species deployment matrix + VIGE viral vector availability + cross-machine artifact-exfiltration plan |
| 24 | Open questions remaining for operator | (a) Direct SA partnership outreach to ARC-BTP / SACTA / CIMMYT-Zimbabwe in v1, or defer to Report 2 + Phase 2 outreach plan? (b) Pre-emptive partnership outreach to Pairwise for Fulcrum sub-licensing v1 conversation, or defer? (c) Report 2 reconciliation sub-brief trigger — when Report 2 lands, run reconciliation pass against v1 PRD to surface displacement |
| 25 | Final output required from overnight executor | Phase 0 ZERO-on-CPU complete with all 11 waves green; Phase 1 Runpod cutover green with byte-identical envelopes; PCG validation triple seeds 1, 2, 3 emit valid dossiers with cross-model disagreement, license stamps, RFS scores, and partner-handoff blocks |
| 26 | Agent's standing instruction | The agent decides every contested call autonomously using the discipline in this PRD; updates GitHub continuously; HF Pro for bulk artifacts; does not interim-report; does not engage operator until end-to-end completion or genuine boundary blocker |
| 27 | DRIFT DELETED card | Per Synbio convention — explicit list of patterns / framings / scope creeps the agent must NOT do |

---

## 2. Where I am applying fresh eyes that the synthesis agent missed

The synthesis identified twelve specific gaps. I am closing all twelve and adding the following that the synthesis missed:

**(13) The dossier-first active-inference reframe collapses the L4-L5 boundary, but the synthesis does not name the operational consequence: the active-inference loop must be implemented in v1, not v1.5/v2.** Specifically, the (input → dossier → partner outcome → next dossier with refined ranking) feedback loop is the active-inference closure; without it, dossier-first is just dossier-shaped. The PRD must specify closed-loop dossier mode as a Phase-1 deliverable (mirroring Synbio's closed-loop completion). Round-N dossier emits → partner reports outcomes via BrAPI hook or manual JSON-LD post-back → BoTorch GP surrogate updates → round-(N+1) dossier emits with refined ranking and new validation sequence.

**(14) The license-class taint detector is named in the synthesis but the *cross-class metric* is not specified.** I am specifying it: every prediction carries a `license_class_taint_metric` quantifying the marginal effect of class-B (attribution-required) and class-C/D (excluded) inputs on the prediction. Computed by re-running the prediction with class-A-only training set vs full training set; metric is the L2 distance in prediction space normalised by prediction magnitude. The audit log captures this metric per prediction. This is not a synthesis recommendation — it is a fresh-eyes addition.

**(15) The seven-block dossier JSON-LD schema needs Pydantic + JSON Schema dual encoding.** The synthesis says "JSON-LD with explicit JSON Schema." I am specifying Pydantic models as the source of truth (because the runtime validation lives there) plus auto-generated JSON Schema for external partner consumption plus auto-generated TypeScript types for partner web UIs. The Pydantic-first approach is forked from Synbio L7 dossier (Pydantic dossier factory).

**(16) The Regulatory Fit Score formula in Report 1 is a static computation; the synthesis names the master decision matrix as versioned JSON but doesn't specify the *regulatory-text-staleness* falsifier.** I am adding falsifier `f_regulatory_route_citation_stale`: every row in the master decision matrix carries `regulation_text_url` + `regulation_text_last_verified_date`; if `last_verified_date < (today - 90 days)` for any row used in an active dossier computation, the dossier emits with a yellow flag. The PRD includes a scheduled refresh sub-brief (run quarterly) that re-fetches each cited regulatory text and updates `last_verified_date` if no change, or flags for human review if change detected. This addresses the "regulations change" concern operationally.

**(17) The orphan-crop SNP-only graceful degradation is named but the *prior-strength differential* is not specified.** The synthesis says "wider credible intervals" and "explicit caveat in partner-handoff narrative." I am specifying the operational consequence: the BoTorch qNEHVI acquisition function is reweighted in SNP-only mode to prefer information-gain-rich regions (high posterior variance × high marginal utility) over yield-gain-rich regions (high posterior mean × medium marginal utility). The breeding sim runs with explicit "prior-strength=0.3" knob in SNP-only mode vs "prior-strength=0.9" in Tier-1 pangenome-aware mode. This is encoded in the L5 BoTorch adapter, not the dossier narrative.

**(18) The Benson Hill Chapter 11 lesson is encoded as "no vertical integration / no trait IP" — but the *capital-fragility implication* is also that Zer0pa platform must be partner-revenue-sustaining at sub-$10M ARR.** I am encoding this as a productisation constraint: the platform must be operable at the cost basis of a 5-person engineering team for partner-revenue runway purposes. The PRD productisation section (§21) names this explicitly so the overnight executor doesn't accidentally introduce dependencies that would push the cost basis up (e.g., an exotic SaaS integration that requires a vendor license >$50k/year).

**(19) The Tier-1 species deployment matrix lists seven species but the *graph-pangenome-readiness* state varies across them.** Maize, rice, soybean, tomato have public graph pangenomes ready for PHGv2 consumer mode. Wheat has PHGv2 deployment per April 2026 (Buckler Lab six-species line). Barley has the wheat-pattern. Sorghum has limited graph pangenome. The PRD encodes per-species pangenome-readiness in a versioned JSON file (`src/zer0pa_pcg/refs/tier1_pangenome_readiness.json`) with `pangenome_url`, `pgsn_naming_convention`, `last_verified_date`, and `phgv2_compatible` flag. Falsifier `f_pangenome_aware_claim_without_coverage` triggers when a dossier emits "pangenome-aware prediction" for a species whose `phgv2_compatible == false`.

**(20) The "no production-grade BoTorch-for-breeding tool exists" gap (Report 1 §6) needs the *six-axis Pareto front demonstration* specified as a Phase-0 acceptance test.** Synthesis says "produces a six-axis Pareto front on a small AlphaSimR test corpus before any Runpod is touched." I am specifying the test corpus: 100-genotype × 5-environment AlphaSimR simulation with seven trait classes (yield, drought tolerance, N-use efficiency, P-use efficiency, protein content, pest resistance, abiotic stress); BoTorch qNEHVI runs 50 acquisition iterations; resulting Pareto front must (a) span ≥10 distinct candidate strategies, (b) include at least one MAS-only candidate, one base-edit candidate, one VIGE candidate, (c) compute correctly under SNP-only and pangenome-aware modes, (d) emit a six-axis Pareto front visualisation (PCA-projected for human readability). Acceptance test committed as `tests/integration/test_phase0_botorch_six_axis_pareto.py`.

**(21) The Synbio fork-and-own from Unknown Enzyme tools lifts to PCG NLR receptor / photosynthetic enzyme / TF DBD trait engineering, but the *protein-structure-aware-trait-engineering* use cases are not enumerated.** I am specifying four concrete use cases for the SE(3) tower: (a) NLR receptor diversification for resistance breeding (LRR domain redesign for novel effector recognition), (b) photosynthetic enzyme efficiency (Rubisco, FBPase, transporters; CC-BY AlphaFold DB v4 substrate ready), (c) seed storage protein redesign for nutritional quality (gluten avenin sub-units, lectin removal), (d) TF DBD specificity engineering for cis-regulatory rewriting (consistent with Phytoform's cis-regulatory frame). Each use case has a Phase-1 acceptance test in the SE(3) tower adapter.

**(22) The 18 anti-decisions enumerated in `docs/process/MODUS-OPERANDI.md` need to be encoded as falsifier IDs in `audit/falsifiers.yaml`, not just narrative.** I am specifying that each anti-decision becomes a falsifier with `tier=Heavy`, `gate_action=block_pr`, and an `evidence_schema` that names the specific input that would trigger the violation. E.g., `f_anti_decision_apsim_commercial`: triggers when `pcg_apsim_adapter` is imported by any commercial code path; evidence schema is the import statement.

---

## 3. Engineering-blocker deep-research lookup results (10 items resolved)

| # | Lookup | Status (May 2026) | PRD-binding action |
|---|---|---|---|
| 1 | EU NGT regulation OJEU final text | Council adopted **21 April 2026 (CONFIRMED)**; Parliament plenary tentatively **18 May 2026 (scheduled, future)**; OJEU publication 20 days post-Parliament; **mid-2028 application after 24-month transition** | Master decision matrix encodes per-row `expected_application_date` field; rows for EU NGT-1 / NGT-2 carry `effective_from=2028-mid-or-later`; pre-2028 EU jurisdiction score remains 1 (full GMO Act applies) |
| 2 | US APHIS replacement rule RIN 0579-AE84 | **Spring 2025 Unified Agenda listed**; publication projected 2026 but **not yet delivered**; **pre-SECURE regime in effect** since 16 June 2025 (vacatur 2 December 2024) | Master decision matrix encodes US jurisdiction score 5 for "SDN-1, no plant pest, no Agrobacterium" under pre-SECURE regime; falsifier `f_us_post_replacement_rule_pending` triggers if the replacement rule publishes during execution |
| 3 | PHGv2 release status | **Apache-2.0 confirmed**; last update **12 March 2026**; six species deployed; v2.5+ production-ready | PRD encodes PHGv2 as Phase-0 binding consumer-mode dependency; `phgv2_compatible` flag in `tier1_pangenome_readiness.json` per-species |
| 4 | Plant DNA foundation model weights | PlantCaduceus **Apache-2.0 (CONFIRMED)**; HyenaDNA **BSD-3 (CONFIRMED)**; PlantRNA-FM **MIT (CONFIRMED)**; GPN **MIT (CONFIRMED)**; Evo-2 Arc Institute / NVIDIA BioNeMo (license needs final HF model card check; PRD treats as Apache-2.0 pending verification with falsifier `f_evo2_license_class_c_or_d` as guard) | All five plant DNA FMs cleared for Phase-1 fine-tune; AgroNT / Nucleotide Transformer remain anti-decisioned (CC-BY-NC-SA) |
| 5 | AlphaFold DB v4 license | **CC-BY 4.0 confirmed** (since January 2022; commercial use permitted with attribution) | PRD encodes AlphaFold DB v4 as Phase-1 SE(3) tower input; AlphaFold 3 weights remain anti-decisioned (separate non-commercial terms); OpenFold3 (Apache-2.0) + ESMFold add the open-weight folding stack |
| 6 | Living Models BOTANIC weights | **Released 11 March 2026 with $7M seed**; available on `huggingface.co/living-models` as Botanic0-S / Botanic0-M / Botanic0-L; license **not displayed on org page** — needs check on individual model card; commercialization model is "licensing for fine-tuning in customer secure environment" | PRD encodes BOTANIC fine-tune as **Phase-1 conditional** on per-model-card license verification; if class-A or class-B (Apache/MIT/CC-BY): proceed with fine-tune in Zer0pa-secure HF Pro environment; if class-C/D: BOTANIC anti-decisioned via falsifier `f_living_models_botanic_license_class_c_or_d`; partnership conversation operator-deferred to v2 |
| 7 | UC Davis GRF-GIF licensing | Vectors **free for research**; commercial requires **paid non-exclusive license** (UC Davis tech transfer ID 31641); patent app 62/873,123; specific pricing not public | PRD encodes Tier-2 species (wheat / barley / triticale / citrus) transformation as GRF-GIF-license-required; commercial deployment is partner-side license procurement (Zer0pa platform-only); license-cost-line-item flagged in dossier Risk Block |
| 8 | Corteva WUS2/BBM ag pool | **Patent estate confirmed** (US7256322 et seq.); technology spans maize/sorghum/sugarcane/four grass subfamilies; **no public "ag pool 2026" terms found** | PRD encodes Tier-3 species (maize-elite / sorghum / sugarcane) commercial regeneration as Corteva-license-required; **VIGE remains primary IP-arbitrage path** (Phase-0 binding); operator-deferred decision: pre-emptive Corteva partnership outreach for license terms (carry-forward to operator open question) |
| 9 | Pairwise Fulcrum sub-licensing | **CIMMYT June 2025 license confirmed** (maize/wheat/sorghum/pearl millet/finger millet/pigeon pea/groundnut for NARS partners across 20 countries); Tropic / Solis / Bayer / Corteva sub-licensee list confirmed; **specific sub-licensing terms not public** | PRD encodes Phase-1 technical scaffold (Fulcrum REST stub adapter + interface contract); Phase-2 partnership conversation **operator-deferred** to v2 (carry-forward open question) |
| 10 | BrAPI v2.1 | **v2.1 released 1 July 2022; current stable**; no v2.2 publicly announced | PRD encodes BrAPI v2.1 as Phase-0 binding spec for the data spine; falsifier `f_brapi_version_drift` triggers if v2.2 lands during execution and Zer0pa adapters need update |

---

## 4. Sub-agent dispatch table (concrete, populated, ready for execution)

Every sub-agent is **Sonnet 4.6 or Opus 4.7** (operator directive 2026-05-01 binding). Wave assignment follows §15.

| Wave | Component | Owner-agent | Spawn-vs-serialise | Success criterion | Wall-clock | Token budget |
|---|---|---|---|---|---|---|
| 0 | Boundary block + falsifier registry skeleton | Sonnet 4.6 | Serial (foundational) | `audit/falsifiers.yaml` committed with 22 named falsifiers; boundary block in golden-fixture test passes | 1.5h | 80k |
| 0 | KG schema + dossier audit-trail spec v0.1 | Sonnet 4.6 | Parallel with falsifier registry | `kg/schema.yaml` committed; `docs/CIDA-TS-v0.1.md` (Crop Improvement Dossier Audit-Trail Spec) committed | 2h | 100k |
| 1 | License-stamping ETL service | Opus 4.7 | Serial (moat-critical, complex) | License-class-A-only training run vs class-A+B+C training run produces measurable disagreement metric; downstream taint filter blocks class-C/D contamination of commercializable artifact in golden-fixture test | 4h | 250k |
| 1 | Crop Improvement Dossier JSON-LD schema lock — all 7 blocks | Opus 4.7 | Serial (foundational; everything depends on it) | All 7 Pydantic models pass round-trip JSON-LD ↔ Pydantic ↔ JSON Schema validation; deliberate corruption of one required field rejected by validator | 3h | 200k |
| 1 | Regulatory Fit Score master decision matrix | Sonnet 4.6 | Parallel with dossier schema lock | `regulatory/master_matrix_v0.1.yaml` committed with per-row regulation citation chain + last_verified_date; RFS computation for (crop=wheat, trait=Sr-locus-base-edit, jurisdiction=US-EU-SA) emits expected score | 2.5h | 130k |
| 2 | BrAPI v2.1 data spine adapter | Sonnet 4.6 | Parallel | Self-hosted Breedbase smoke-test passes; consumer + provider endpoints work; MIAPPE 1.1 round-trip | 3h | 150k |
| 2 | PLINK 2 PGEN canonical store + PHGv2 hVCF consumer | Sonnet 4.6 | Parallel | VCF→PGEN→hVCF round-trip preserves byte-identical genotype; `f_invalid_vcf` and `f_pgen_signature_mismatch` falsifiers trigger correctly | 3h | 150k |
| 3 | rrBLUP + BGLR + sommer prediction stack | Sonnet 4.6 | Parallel — three sub-agents (one per package) | Each runs on G2F maize subset; cross-model disagreement aggregator computes pairwise + ensemble metrics | 5h (parallel) | 350k total |
| 3 | EnvRtype + BGGE Jarquín reaction-norm G×E | Sonnet 4.6 | Parallel | G×E variance components (G, E, GxE) recovered on G2F subset within ±10% of literature | 3h | 180k |
| 3 | Cross-model disagreement aggregator | Opus 4.7 | Serial after rrBLUP/BGLR/sommer stand up | Aggregates predictions, computes pairwise disagreement, ensemble disagreement, license-class disagreement, Tier-1-vs-orphan-crop disagreement; falsifier `f_cross_model_disagreement_above_threshold` triggers correctly | 3h | 200k |
| 4 | AlphaSimR + PyBrOpS breeding sim | Sonnet 4.6 | Parallel | 100-genotype × 5-env AlphaSimR sim runs; PyBrOpS Pareto cross-design produces ≥10 candidates | 3h | 150k |
| 4 | FielDHub trial design + statgen + SpATS | Sonnet 4.6 | Parallel | Row-column design generated for 100-plot 4-rep trial; SpATS spatial trend correction recovers planted G×E within ±10% | 2.5h | 130k |
| 5 | CROPSR + Cas-OFFinder + CRISPRitz + CRISPResso2 edit design | Sonnet 4.6 | Parallel — four sub-agents (one per package) | sgRNA design for wheat Sr-locus base-edit produces ≥3 candidates; off-target enumeration with polyploid homoeolog handling correct; CRISPResso2 edit verification round-trip works | 4h (parallel) | 280k total |
| 5 | Off-target enumeration with polyploid handling | Opus 4.7 | Serial after edit-design stack | Wheat Sr-locus base-edit off-target enumeration treats homoeologs as target group not off-targets; falsifier `f_offtarget_above_threshold` triggers correctly; falsifier `f_polyploid_homoeolog_misclassified` triggers correctly | 3h | 200k |
| 6 | Regulatory router + Regulatory Fit Score implementation | Opus 4.7 | Serial after master matrix | RFS computation for (crop, trait, edit, jurisdictions) tuple emits per-target-market score; threshold gates (4.0 green / 2.5 yellow / <2.5 red) routing decisions; `f_regulatory_route_citation_stale` triggers when matrix row last_verified_date older than 90 days | 4h | 250k |
| 7 | BoTorch qNEHVI multi-objective optimiser | Opus 4.7 | Serial — highest-leverage build piece | Six-axis Pareto front demonstrated on AlphaSimR 100-genotype × 5-env corpus with 50 acquisition iterations; ≥10 distinct candidate strategies; SNP-only and pangenome-aware modes both work | 5h | 300k |
| 7 | Active-inference closed-loop dossier mode | Opus 4.7 | Serial after BoTorch | Round-N dossier → simulated partner outcome JSON-LD post-back → BoTorch GP surrogate updates → round-(N+1) dossier emits with refined ranking; closed-loop test passes | 3h | 200k |
| 8 | SE(3) protein-structure tower CPU-side stub adapters | Opus 4.7 | Serial — forked from Synbio | RFdiffusion3 + MACE-OFF + ProteinMPNN + AlphaFold DB v4 + OpenFold3 + ESMFold REST stubs return shape-correct canned outputs; envelope schema unchanged; four use-case acceptance tests pass (NLR LRR / Rubisco / seed protein / TF DBD) | 4h | 280k |
| 9 | KG + episodic memory + reasoner_queue | Sonnet 4.6 | Parallel | KG nodes (Run / Phase / Sub-agent / Component / Dossier / DossierBlock / Decision / Falsifier / DispatchRecord / EvalArtifact / RegulatoryReference / LicenseStamp) + edges; episodic memory write path; `runs/<rid>/tuples.jsonl` shape forked from Health | 3h | 180k |
| 10 | Plug-replaceability test matrix | Sonnet 4.6 | Parallel | Swap rrBLUP for BGLR — envelope schema unchanged; swap PLINK2 for PHGv2 — envelope unchanged; swap AlphaSimR for ChromaX — envelope unchanged; swap CROPSR for CRISPR-PLANT v2 — envelope unchanged | 3h | 180k |
| 10 | License-class taint detector + reproducible-build audit | Opus 4.7 | Serial | Detector emits taint metric per training run; reproducible-build audit re-runs Phase-0 from cold start and produces byte-identical outputs except for runtime/provenance fields | 3h | 200k |
| 10 | Runpod cutover golden-fixture invariance test | Sonnet 4.6 | Serial after taint detector | `httpx.MockTransport` test passes with `gpu_rest_stub` backend; same fixture passes with `runpod_rest` backend (mocked); byte-identical envelopes verified | 2h | 120k |
| 11 | PCG validation triple end-to-end | Opus 4.7 | Serial — final acceptance gate | Seed 1 (maize G2F yield) dossier emits with cross-model disagreement, license stamps, RFS for US/EU/SA; Seed 2 (wheat Ug99 base-edit) emits with off-target enumeration, polyploid handling, regulatory route SDN-1; Seed 3 (bambara groundnut SADC orphan-crop) emits with SNP-only mode, wider credible intervals, SACTA-compatible partner-handoff | 6h | 400k |

**Total estimated wall-clock for Phase-0 (CPU-only):** ~70 sub-agent-hours, parallelised across waves. With 4 sub-agents in parallel maximum at any wave, real wall-clock is ~12-16 hours of overnight execution.
**Total estimated token budget for Phase-0:** ~4.5M tokens.

---

## 5. Three operator-engagement open questions — my resolution + remaining carry-forwards

### (a) Pairwise / Living Models partnership integration sequencing

**My resolution:**
- **Living Models BOTANIC** is **Phase-1 conditional** on per-model-card license verification. If license is class-A/B (Apache/MIT/CC-BY): BOTANIC fine-tune deliverable in Phase-1, performed in Zer0pa-secure HF Pro environment per Living Models' partner pattern. If license is class-C/D: anti-decision via falsifier `f_living_models_botanic_license_class_c_or_d`, BOTANIC excluded. The license check is the first thing the BOTANIC sub-agent does.
- **Pairwise Fulcrum** is **Phase-1 technical scaffold** (Fulcrum REST stub adapter with interface contract; the dossier's Intervention Strategy block flags candidates that would benefit from Fulcrum integration). **Phase-2 partnership conversation operator-deferred.**

**Remaining operator open question (carry-forward):** Should v1 include pre-emptive Pairwise partnership outreach for sub-licensing terms, or defer entirely to v2? My recommendation is **defer to v2** — the technical scaffold is ready, the partnership conversation is operator-strategic and Report 2 will likely sharpen the partner integration sequence. Operator override welcome.

### (b) South Africa go-to-market motion through ARC-BTP / SACTA / CIMMYT-Zimbabwe

**My resolution:**
- **Phase-1**: Architectural carveout encoded in dossier Regulatory Block (`origin_jurisdiction` field per edit candidate; SA-import-via-conventional-crossing routing; SACTA-compatible cultivar registration documentation in Partner Handoff block; SA-specific Performance Forecast at SACTA-compatible trial sites). This is the technical substrate; no partnership conversations required to build it.

**Remaining operator open question (carry-forward):** Should v1 include direct ARC-BTP / SACTA / CIMMYT-Zimbabwe partnership outreach, or defer to Report 2 + Phase 2 outreach plan? My recommendation is **defer to Report 2** — Report 2 explicitly covers SA go-to-market motion, and the carveout architecture stands independent of the partnership decisions. Operator override welcome.

### (c) Intersectional-roadmap prioritisation

**My resolution (challenging the synthesis):** The synthesis suggested causal inference → climate-physics+active-inference → SE(3) → graph theory → information theory → control theory → systems ecology. I am promoting **SE(3)-equivariant geometry from v1.5 to Phase-1** for these reasons:

1. The fork-and-own from Synbio's Unknown Enzyme Generative Sub-Pipeline is the most mature cross-workstream pattern (RFdiffusion3 + MACE-OFF + ProteinMPNN + AlphaFold DB v4 + OpenFold3 + ESMFold).
2. AlphaFold DB v4 (CC-BY 4.0) is the substrate, and it is ready.
3. The four concrete use cases (NLR LRR / Rubisco / seed protein / TF DBD) are real PCG trait engineering needs, not academic exploration.
4. The cost of including the SE(3) tower in Phase-1 is low (CPU-side stub adapters + REST stubs for Runpod swap), but the architectural value is high — it eliminates "v1.5 add-on" risk where the SE(3) tower gets deferred indefinitely.

I am also promoting **active inference from v1.5 to architectural primitive**:
- The synthesis already named active inference as the dossier-first reframe — I am locking it as Phase-0 architectural primitive (not v1.5 add-on).
- The closed-loop dossier mode (round-N dossier → partner outcome → BoTorch surrogate update → round-(N+1) dossier) is the active-inference completion. v1 ships with closed-loop, not single-shot.

The remaining intersectional-roadmap items keep roughly synthesis ranking:
1. ✅ **Active inference** — Phase-0 architectural primitive (locked).
2. ✅ **SE(3)-equivariant geometry** — Phase-1 deliverable (challenging synthesis; promoting from v1.5).
3. **Causal inference** — Phase-2 first frontier (highest cross-workstream fork-and-own; reframes L4).
4. **Climate physics + active inference (joint G×E-VAE)** — Phase-2 second frontier (forking Polymath three-wall integration).
5. **Graph theory (GNN over heterogeneous KG)** — Phase-2 third frontier (KG substrate built Phase-0; GNN layered on top in Phase-2).
6. **Information theory (Tishby bottleneck)** — Phase-3 v2 (lower marginal lift).
7. **Control theory (ODE/PDE for time-varying traits)** — Phase-3 v2 (high implementation cost).
8. **Systems ecology (holobiont)** — Phase-3 v2 (microbiome data substrate thin).

**Remaining operator open question (carry-forward):** Operator strategic preference on whether causal inference and climate-physics+active-inference (Phase-2 first/second frontiers) should be co-developed across workstreams (e.g., Polymath Diffusion AI also has active-inference substrate; cross-workstream fork-and-own at the Phase-2 layer)? My recommendation is **yes** — the BoTorch pattern is already cross-workstream, the active-inference pattern can follow the same fork-and-own discipline at the Phase-2 boundary. Operator override welcome.

---

## 6. ZERO-on-CPU before Runpod — explicit binding gate

The PRD's binding Phase-0 acceptance gate: **every CPU-tractable component is 110% complete; cutover-to-Runpod is a config-flag stub-swap proving byte-identical envelopes / canonical hashes / falsifier classes / backend flags.** Cutover gate verified by the Runpod golden-fixture invariance test (forked from Energy Wave 4 `httpx.MockTransport` pattern).

**CPU-tractable (must be 110% complete before Runpod):**
- License-stamping ETL service
- BrAPI-native data spine + self-hosted Breedbase
- PLINK 2 PGEN canonical store
- PHGv2 hVCF integration (consumer mode only — graph-builder mode is GPU-bound)
- rrBLUP + BGLR + sommer + EnvRtype + BGGE Tier-1 prediction stack on small-N test data
- Jarquín reaction-norm GBLUP harness
- Cross-model disagreement aggregator
- AlphaSimR + PyBrOpS breeding simulation
- FielDHub trial design + statgenSTA + statgenGxE + SpATS
- CROPSR + Cas-OFFinder + CRISPRitz + CRISPResso2 edit design
- Off-target enumeration with polyploid handling
- Regulatory router + Regulatory Fit Score with full master decision matrix
- Crop Improvement Dossier JSON-LD schema with all seven blocks locked
- Falsifier registry (22 named falsifiers committed)
- Audit-log + sha256 hash chain
- REST-stub adapters for GPU-bound layers
- Plug-replaceability test matrix
- License-class taint detector
- Reproducible-build audit
- KG + episodic memory + reasoner_queue
- BoTorch-for-breeding qNEHVI optimiser with six-axis Pareto front demonstration on AlphaSimR 100-genotype × 5-env test corpus
- Active-inference closed-loop dossier mode (CPU-side closed-loop test)
- SE(3) protein-structure tower CPU-side stub adapters
- PCG validation triple end-to-end (seeds 1, 2, 3 all emit valid dossiers)

**Runpod-required (Phase-1; only after Phase-0 ZERO-on-CPU verified):**
- Foundation-model fine-tuning (PlantCaduceus + GPN + HyenaDNA + BOTANIC conditional + PlantRNA-FM)
- Deep-learning prediction tracks (DNNGP / DeepGP / custom transformers) at production batch
- ChromaX (JAX/GPU) ML-coupled breeding simulation at scale
- Large-N MET training (G2F + CIMMYT scale)
- Graph genotyping at scale (Giraffe over 10K-100K samples)
- SE(3) protein-structure tower runs at production batch (RFdiffusion3, MACE-OFF, ESMFold)
- AWS af-south-1 satellite compute for SA residency

---

## 7. Falsifier registry preview (22 named falsifiers, committed in `audit/falsifiers.yaml`)

Preview — full registry committed Wave 0:

| ID | Tier | Description | Gate action |
|---|---|---|---|
| f001 | Fast | Invalid VCF format | Block PR |
| f002 | Fast | PGEN signature mismatch | Block PR |
| f003 | Fast | Boundary block missing or modified in any artifact | Block PR |
| f004 | Fast | Dossier block missing required field | Block PR |
| f005 | Medium | Mass-balance violation (genotype+env input vs prediction) | Yellow flag |
| f006 | Medium | Off-target above threshold (≤4 mismatches + 1 bulge plus base-editor window) | Yellow flag |
| f007 | Medium | Polyploid homoeolog misclassified as off-target | Block PR |
| f008 | Heavy | RFS below 2.5 in any active target market | Red gate; route to operator |
| f009 | Heavy | Class-C/D input contamination of commercializable artifact | Block PR; license-class taint detector |
| f010 | Heavy | Pangenome-aware-claim without pangenome coverage | Block PR |
| f011 | Heavy | Predicted-yield without G×E environment | Block PR |
| f012 | Medium | Regulatory-route citation stale (>90 days since last_verified_date) | Yellow flag |
| f013 | Heavy | Partner-handoff block not emitted | Block PR |
| f014 | Heavy | SA-deployment without SACTA-compatible cultivar registration documentation | Block PR |
| f015 | Heavy | Cross-model ensemble disagreement above threshold | Yellow flag |
| f016 | Medium | License-class disagreement metric above threshold | Yellow flag |
| f017 | Heavy | Tier-1-vs-orphan-crop disagreement on Tier-1 species (SNP-only fallback when pangenome available) | Block PR |
| f018 | Heavy | Anti-decision triggered (any of 18 enumerated) | Block PR; route to operator |
| f019 | Heavy | License drift (model artifact license class change between training and serving) | Block PR |
| f020 | Heavy | Reproducible-build audit failure | Block PR |
| f021 | Medium | BrAPI version drift (v2.1 → v2.2 if released) | Yellow flag |
| f022 | Heavy | Living Models BOTANIC license class C or D detected on individual model card | Block BOTANIC fine-tune |

---

## 8. Final operator decision points before I commit the full PRD

Please confirm or override before I write the full document:

1. **Confirm: dossier-first active-inference architectural reframe locked as primitive.** ☐
2. **Confirm: SE(3)-equivariant protein-structure tower promoted from synthesis-v1.5 to Phase-1 deliverable** (forked from Synbio Unknown Enzyme tools; four use cases NLR LRR / Rubisco / seed protein / TF DBD). ☐
3. **Confirm: BoTorch qNEHVI six-axis Pareto front on AlphaSimR test corpus is Phase-0 binding** (not Phase-2 frontier). ☐
4. **Confirm: closed-loop dossier mode (round-N dossier → partner outcome → BoTorch update → round-(N+1) dossier) is Phase-1 deliverable.** ☐
5. **Confirm: 22 named falsifiers committed Wave-0 BEFORE any layer code; full registry preview in §7 above.** ☐
6. **Confirm: Pairwise Fulcrum partnership outreach deferred to v2** (technical scaffold Phase-1, partnership conversation operator-deferred). ☐
7. **Confirm: Direct SA partnership outreach to ARC-BTP / SACTA / CIMMYT-Zimbabwe deferred to Report 2 reconciliation sub-brief** (carveout architecture Phase-1). ☐
8. **Confirm: 18 anti-decisions enumerated in docs/process/MODUS-OPERANDI.md encoded as falsifier IDs in audit/falsifiers.yaml** (not just narrative). ☐
9. **Confirm: Phase-0 ZERO-on-CPU acceptance gate is binding** (no Runpod request until 11 waves green + golden-fixture invariance test passes). ☐
10. **Confirm: Sub-agent dispatch is Sonnet 4.6 / Opus 4.7 only** (no GPT-5+; per operator directive 2026-05-01). ☐

If you sign off on these (or override with reasoning), I will write the full PRD.md (~1,200-1,500 lines), commit and push to GitHub, then write `HANDOFF-TO-OVERNIGHT-EXECUTOR.md`. No further interim reporting per operator directive 2026-05-02.

If you want any specific reconsideration before I commit, name it and I'll revise this outline first.

---

## 9. What this outline closes vs what remains

**Closed at outline level (will be expanded into full PRD):**
- All 12 synthesis-identified gaps + 10 fresh-eyes additions (§2)
- All 10 engineering-blocker deep-research lookups (§3)
- Sub-agent dispatch table populated with concrete component ownership, success criteria, wall-clock estimates, token budgets (§4)
- Three operator-engagement open questions resolved with reasoning (§5)
- ZERO-on-CPU binding gate explicit (§6)
- 22 named falsifiers preview (§7)

**Remaining as operator-engagement open questions:**
- Pre-emptive Pairwise partnership outreach v1 vs defer to v2 (my recommendation: defer)
- Direct SA partnership outreach v1 vs defer to Report 2 (my recommendation: defer)
- Cross-workstream Phase-2 active-inference fork-and-own coordination with Polymath Diffusion AI (my recommendation: yes, coordinate at the pattern level, no runtime co-dependency)

**Carried forward as Report-2-displacement reconciliation sub-brief:**
- When Report 2 lands, the orchestrator runs a one-pass reconciliation against this PRD; surfaces displacement; updates v1 PRD or commits to v2 follow-on as appropriate.

---

**Signed:** PCG orchestrator (Claude Opus 4.7, 1M context), 2026-05-02.
**Awaiting operator review.** No commit to PRD.md until operator confirms or overrides §8.
