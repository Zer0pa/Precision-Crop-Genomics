# Zer0pa Precision Crop Genomics — Workstream Repository

Canonical home for the Zer0pa Precision Crop Genomics work stream. Multi-agent handoff: synthesis → orchestrator → overnight executor → Runpod migration. Repo is the source of truth across machines.

**Precision Crop Genomics is the eighth Zer0pa workstream.** It is a six-layer pipeline-vertical project to ship a license-clean, regulatorily-routed precision crop genomics platform — taking five typed inputs (crop species, agroecological zone, target trait set, breeding-or-editing constraints, regulatory route constraints) and producing a typed Crop Improvement Dossier as output. The core architectural commitment is **pangenome-aware modeling first-class for the seven Tier-1 species (maize, rice, wheat, barley, sorghum, soybean, tomato)** with graceful degradation to SNP-only for orphan crops. The Zer0pa moat is **not the model** — it is the **license-stamping ETL service plus the typed, regulatorily-routed Crop Improvement Dossier**: a partner-ready package no incumbent (Inari closed; Pairwise wet-lab licensable; Living Models foundation-only; Computomics service-based) currently delivers.

The same modus operandi as Health / Materials / Energy / Synthetic Biology / Polymath AI / Polymath Diffusion AI / RCE applies — anti-MVP, anti-toy, overdesigned best-in-class, GitHub canonical, fork-and-own across workstreams, RESISTANCE.md doctrine binding. Sub-agent dispatch is **Sonnet / Opus only** (operator directive 2026-05-01 carried forward). 110% pre-compute-wall sharpened by the operator's 2026-05-02 directive: **"ZERO left to do on CPU before they ask Runpod"** — strictly stronger than "do as much as you can." Plus: **"no false flag reward hacking or interim reporting — this is overnight execution."**

## Boundary

Research infrastructure for in silico precision crop genomics — genomic prediction, pangenome-aware genotyping, breeding simulation, edit design, regulatory routing. Outputs are research artifacts (Crop Improvement Dossiers, genomic prediction model checkpoints, breeding-cycle simulation results, edit-design proposals with off-target enumerations, regulatory route classifications). No regulatory certification claims. No clinical or human-subject use. **No trait IP** — Zer0pa is platform-only and explicitly refuses to take trait IP, which is the structural differentiator that lets Zer0pa partner with all five major seed companies simultaneously rather than picking a side. **No environmental release of GMOs or gene-edited material** by Zer0pa directly — the platform produces dossiers; physical wet-lab work is performed by partner organisations under their own biosafety regimes. **No deployment to South Africa for gene-edited products** absent GMO Act amendment (Section-19 ministerial decision January 2024 keeps gene-edited crops under full GMO Act); SA strategy defaults to MAS-and-prediction pathways. No commitment to herbicide tolerance, novel insecticidal protein traits, or pharma traits — these are pre-registered as binding falsifiers (regulatory-route-incompatible per Section 9 of the source brief).

## What is in here

| Path | Purpose | Author role |
|---|---|---|
| `MODUS-OPERANDI.md` | Reusable multi-agent pattern + parallel-exploration principle (8th instance); 110%-pre-compute-wall axiom sharpened to **ZERO left to do on CPU before Runpod**; overnight execution discipline sharpened to **no false-flag reward hacking, no interim reporting**; Sonnet/Opus-only sub-agent dispatch carried forward | Synthesis agent |
| `HANDOFF-TO-ORCHESTRATOR.md` | Precision-Crop-Genomics-specific brief for the next agent (the orchestrator) — defines what they inherit, what they must produce, the operator-policy refinements, the binding anti-decisions and license traps, the regulatory routing as first-class scoring axis | Synthesis agent |
| `ORCHESTRATOR-STARTUP-PROMPT.md` | The exact prompt the user pastes into a fresh agent session to spin up the orchestrator | Synthesis agent |
| `RESISTANCE.md` | Anti-corruption doctrine — fp-shapematchRE / fp-rushtoend / fp-NULLasout / fp-approvalseek / fp-flatteryasfreedom / efficiency-as-corner-cutting; binding for every executor before work starts. For Precision Crop Genomics specifically, the operator's "no false-flag reward hacking" directive 2026-05-02 reinforces fp-pretty-greenflag (treating "build passes" as sufficient evidence) and fp-less-work-disguised-as-focus (silently skipping call-sites under guise of scope discipline) — both surfaced in prior workstream Zod-migration triage | Imported from DM3, augmented per operator refinements |
| `source-briefs/` | Inherited research input — the operator-authored Pre-PRD Research Synthesis (`01-precision-crop-genomics-report-1-full-technology-landscape.md`, 160 dense lines, ~57 KB, May 2026). Report 1 of 2; Report 2 is forthcoming and will collapse the landscape into "a sharper architectural specification with concrete schema definitions, partner integration sequences, and the South African go-to-market motion through ARC-BTP, SACTA, and CIMMYT-Zimbabwe." | External (consumer of synthesis) |
| `synthesis/` | Fresh-eyes reading of the operator's Report 1 by the synthesis agent — what the report does not yet see when read top-to-bottom; the architectural reframe; the cross-workstream fork-and-own opportunities (especially from Synthetic Biology for protein-design tower and BoTorch optimizer); the operator's 2026-05-02 directives (ZERO-on-CPU, no-false-flag, no-interim-reporting) translated into PRD-shape implications | Synthesis agent |
| `PRD.md` (to be written) | The PRD that drives the overnight long-horizon execution by the executor agent on a Runpod-bound machine. The PRD must front-load every CPU-side build to **ZERO left** before Runpod GPU bring-up. | Orchestrator |

## Read order for the next agent

1. `RESISTANCE.md` — anti-corruption doctrine. Read first. Headspace.
2. `MODUS-OPERANDI.md` — how the role chain works; § Operator refinements (binding for all workstreams 2026-05-01 + sharpened 2026-05-02); § The 110%-pre-compute-wall axiom translated for Precision Crop Genomics as **ZERO left on CPU before Runpod**; § Sub-agent topology Sonnet/Opus only.
3. `HANDOFF-TO-ORCHESTRATOR.md` — what you (orchestrator) inherit and produce. Includes the binding anti-decisions, the four license traps, the regulatory routing as first-class scoring axis, the seven-block dossier schema requirement.
4. `source-briefs/01-precision-crop-genomics-report-1-full-technology-landscape.md` — the operator-authored Pre-PRD Research Synthesis. Sections 1-15 cover: v1 architecture in one diagram + four sentences; Layer 1 input encoding + ZPE schema; Layer 2 knowledge layer + license trap inventory; Layer 3 candidate generation across breeding/MAS/edit modalities; Layer 4 screening with genomic prediction + G×E + regulatory routing; Layer 5 Bayesian optimization + active learning + open frontier; Layer 6 typed handoff dossier; phenomics + remote sensing material-lift cases; regulatory routing as scoring axis with explicit Regulatory Fit Score formula; intersectional science map; commercial landscape and Zer0pa's defensible position; South Africa / Southern Africa / orphan crop layer; direct answers to ten required research questions; frontier opportunities not yet production-ready; conclusion with build order.
5. `synthesis/01-fresh-eyes-on-precision-crop-genomics-report-1.md` — synthesis-agent reframe; substrate for your own fresh-eyes augmentation. Surfaces the things Report 1 does not yet see, the operator's 2026-05-02 directive translation, fork-and-own opportunities from prior workstreams (especially Synthetic Biology for protein-design tower; the recurring BoTorch infrastructure pattern across workstreams), pressure-test points, anticipated Report 2 displacement.

## Provenance

- Initial commit: 2026-05-02.
- Operator (Architect Prime, Zer0pa): authored Report 1 of 2 of the Precision Crop Genomics technology landscape. This collapses the research-agent and synthesis-agent roles into a single operator-authored document.
- Synthesis agent: Claude Opus 4.7 (1M context), 2026-05-02 — applied recursive fresh-eyes pass on top of Report 1.
- Next agent: Precision Crop Genomics orchestrator (writes `PRD.md`).
- Following: overnight executor on a Runpod-bound machine — but ONLY after ZERO-on-CPU is achieved on a Mac dev machine first.

## Cross-workstream principle (deliberate)

This workstream runs in parallel with the seven prior workstreams. **No substrate is shared at runtime.** Redundancy across workstreams is a deliberate asset.

**Fork-and-own is explicitly permitted (operator clarification 2026-05-01).** The orchestrator may copy any implementation pattern, falsifier-registry shape, audit-log schema, plug-replaceability harness, code structure, test pattern, or architectural detail from a sibling workstream and reimplement it inside Precision Crop Genomics. **What is rejected is runtime co-dependency.**

**For Precision Crop Genomics specifically, the highest-value forks are:**

- **From Synthetic Biology**: the SBOL3-attested audit-trail with sha256 hash chain shape (forked as JSON-LD-attested dossier with sha256 hash chain); the four-column license decomposition pattern (already mirrored in Report 1's "every record gets a four-column license stamp"); the Unknown Enzyme Generative Sub-Pipeline tools (RFdiffusion3, MACE-OFF, ProteinMPNN, AlphaFold DB) reusable as the protein-structure tower for NLR receptor / photosynthetic enzyme / transporter / TF DBD trait engineering.
- **From Health**: the TxGemma reasoner-tuple discipline (forked as dossier-tuple discipline — every (input, dossier, gate-result, falsifier-judgment) writes to a private dataset that compounds the moat); the audit-log shape with hash chain across all 12 audit tables; the cross-model disagreement primitive (forked as ensemble disagreement: rrBLUP + BGLR + sommer + DNNGP at evaluation).
- **From Materials**: the falsifier-registry-first build discipline (write the registry + audit-log shape + back-edge router *first*, then plug adapters into it); the cross-model ensemble disagreement aggregator code structure.
- **From Energy**: the same-shape Runpod cutover with `httpx.MockTransport` golden-fixture invariance — Mac-CPU-vs-Runpod-GPU equivalence test.
- **From Polymath AI / Polymath Diffusion AI**: the Sonnet/Opus-only sub-agent dispatch directive; the RESISTANCE.md augmentation with fp-pretty-greenflag and fp-less-work-disguised-as-focus.
- **From RCE**: the surgical-sub-brief shape for any specific schema-locking task (e.g., "lock the Crop Improvement Dossier JSON-LD schema" as a tightly scoped sub-brief mirroring the operator's Zod migration brief).
- **A cross-workstream pattern visible at the orchestrator level**: every workstream needs a BoTorch multi-objective optimizer (Synbio MFMO, Polymath AI BoTorch loops, Materials BoTorch acquisition, Energy qMFKG, Polymath Diffusion AFP-controlled scheduler — and now Precision Crop Genomics qNEHVI Pareto over yield × resilience × nutrition × input efficiency × regulatory friction). The synthesis agent surfaces this as a fork-and-own pattern: the orchestrator should fork-and-own the BoTorch shape from whichever sibling workstream has the closest fit to the breeding-cycle-simulator-as-black-box use case. **No runtime co-dependency** — Precision Crop Genomics carries its own BoTorch deployment. But the *shape* of the optimizer can be standardised across forks.

All forks; no runtime co-dependency. Precision Crop Genomics carries its own copy of every fork.

## Anti-decisions pre-registered as binding falsifiers

The source brief names specific tools, datasets, and architectural choices that are **off-limits** for any v1 build. The orchestrator's PRD must encode these as binding falsifiers — any sub-brief proposing one of these fails the brain-functionality gate and must escalate to the operator.

- **APSIM** — Special Non-Commercial License; the single biggest license trap in the crop modeling stack; treat as proprietary.
- **ASReml-R, BLUPF90** — proprietary; replaced by sommer + statgenSTA + statgenGxE + SpATS open stack.
- **OpenDroneMap as hosted SaaS** — AGPL-3.0 with network-use trigger; forces source disclosure for any hosted Zer0pa SaaS. (Self-hosted on-premise OK; hosted is not.)
- **Ultralytics YOLOv5/v8** — AGPL-3.0 with required Enterprise license; substitute YOLOX or MMDetection.
- **Google Earth Engine free tier** — not commercially usable for any private company including pre-revenue Zer0pa; license-clean alternative is AWS Open Data Registry + Microsoft Planetary Computer Pro + xarray/STAC.
- **AgroNT, Nucleotide Transformer weights** — CC-BY-NC-SA; commercially unusable. PlantCaduceus / HyenaDNA / Evo-2 / GPN / PlantRNA-FM are the permissive alternatives.
- **AlphaFold3 weights, ESM3 main weights** — non-commercial. Use AlphaFold DB v4 (CC-BY 4.0) plus OpenFold3 (Apache-2.0).
- **WorldClim 2.1** — CC-BY-NC-SA despite ubiquitous academic use. CHELSA / AgERA5 / CHIRPS v3 are drop-in replacements.
- **PLAZA (Ghent comparative genomics)** — CC-BY-NC-SA; explicitly excludes industrial-sponsored academic work.
- **TAIR live curated data** — paid Phoenix Bioinformatics commercial subscription required (~$28k/yr large company); only public release >1 year old is CC-BY 4.0; safe path is TAIR12 from GenBank.
- **EOX Sentinel-2 cloudless mosaics** — CC-BY-NC-SA; raw Sentinel-2 from ESA is fully open commercial.
- **JGI/Phytozome embargoed data** — 2-year redistribution restriction.
- **Herbicide tolerance traits** — automatic NGT-2 in EU regardless of edit size; kills EU access; pre-registered as edit-design exclusion unless EU and SA markets are explicitly out of scope.
- **PIP-equivalent insect resistance via novel insecticidal protein** — EPA PIP registration trigger plus EU NGT-1 exclusion. Loss-of-function susceptibility-gene knockouts are the architecturally cleaner path.
- **Pharma traits** — TraitMultiplier 0.30 in the Regulatory Fit Score; deeply penalised; pre-registered as scope exclusion.
- **Trait IP ownership** — Zer0pa is platform-only and explicitly refuses to take trait IP. Any sub-brief proposing Zer0pa take trait IP fails the brain-functionality gate.
- **Gene drives, cultivation bans** — JurisdictionScore 0; pre-registered as scope exclusion.
- **Refrigeration of any device** — carryover from Polymath Diffusion (irrelevant here; defensive carry).

## Architecture commitments locked in Report 1

The source brief names specific architectural commitments that the orchestrator's PRD must respect (not re-derive):

- **L1 ZPE encoding**: PlantCaduceus (Apache-2.0) primary; HyenaDNA-large-1m (BSD-3) for long-range; Evo-2 (Apache-2.0) cross-domain; EnvRtype + AgERA5 + CHELSA + CHIRPS v3 for environment.
- **L2 knowledge stack**: Ensembl Plants + NCBI RefSeq + UniProt + InterPro + Gramene + OBO Foundry suite + Breedbase (BrAPI 2.1) + GRIN-Global + Genesys + AgERA5 + ERA5-Land + SoilGrids 2.0 + CHIRPS v3 + TerraClimate. **License-stamping ETL** is the Zer0pa-built primitive.
- **L3 candidate generation**: AlphaSimR + MoBPS + ChromaX + PyBrOpS + AlphaMate + optiSel + selectiongain + FielDHub + statgenSTA + statgenGxE + SpATS for cross-and-MAS; CROPSR + CRISPR-PLANT v2 + Cas-OFFinder + CRISPRitz + Variant-aware Cas-OFFinder + CRISPResso2 for editing. **Base editing default; prime editing R&D-only** (per Report 1 §4 empirical evidence). **VIGE as IP/regulatory arbitrage** for Tier-3 species.
- **L4 screening**: rrBLUP + BGLR + sommer baseline; Jarquín reaction-norm GBLUP for G×E; PHGv2 + vg/Giraffe + PanGenie + Sniffles2 + minigraph-cactus for pangenome-aware genotyping; off-target layer with polyploid homoeolog handling; **Regulatory Fit Score as first-class Pareto axis**.
- **L5 optimization**: BoTorch qNEHVI multi-objective with AlphaSimR or ChromaX as black-box simulator; Pareto front over (yield gain, drought resilience, nutrient efficiency, nutritional quality, regulatory friction, deployment ROI).
- **L6 dossier**: typed JSON-LD with seven blocks (Identity, Intervention Strategy, Performance Forecast, Risk, Regulatory, Provenance, Partner Handoff). **Regenerable from inputs at any time** — no implicit state.

The orchestrator may pressure-test these commitments but must surface override reasoning explicitly per RESISTANCE.md doctrine.
