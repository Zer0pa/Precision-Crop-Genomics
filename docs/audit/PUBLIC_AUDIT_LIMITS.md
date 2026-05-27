# Public Audit Limits — Precision Crop Genomics

**Status:** v0.1, drafted 2026-05-02 by orchestrator (Claude Opus 4.7, 1M context).
**Visibility:** Public repository; this document scopes the current public audit surface.

## Operator boundary

Public/internal/private state is operator-controlled. This document specifies what is and is not part of the current public audit surface.

## What IS in the public audit surface

The following structural and briefing assets constitute the public audit surface:

1. **`README.md`** — front-door spine; ≤30-word lead, Pipeline Mechanics zone-02, 4 Key Metrics rows, ≤6 Proof Anchors, Repo Shape with handoff material as support, blockers and non-claims preserved.
2. **`docs/research/RESISTANCE.md`** — anti-corruption doctrine; forbidden meta-proxies enumerated; binding for every executor agent.
3. **`docs/process/MODUS-OPERANDI.md`** — multi-agent work-stream pattern; role chain; § Operator refinements binding all workstreams 2026-05-01 + sharpened 2026-05-02; § ZERO-on-CPU before Runpod axiom; § Sub-agent topology Sonnet/Opus only; § Acceptance gates.
4. **`docs/handoffs/HANDOFF-TO-ORCHESTRATOR.md`** — orchestrator role definition; what is inherited; expected output; ten engineering-blocker deep-research lookups; three operator-engagement open questions; eighteen anti-decisions enumerated.
5. **`docs/handoffs/ORCHESTRATOR-STARTUP-PROMPT.md`** — paste-ready cross-machine handoff prompt for orchestrator role.
6. **`docs/research/source-briefs/01-precision-crop-genomics-report-1-full-technology-landscape.md`** — operator-authored Pre-PRD Research Synthesis Report 1 of 2 (160 lines, ~57 KB; full technology landscape with license decomposition, regulatory routing, intersectional science map, SA / SADC / orphan-crop strategy, ten research-question answers, frontier opportunities, build order).
7. **`docs/research/synthesis/01-fresh-eyes-on-precision-crop-genomics-report-1.md`** — synthesis fresh-eyes pass; twelve specific gaps Report 1 does not see; pressure-test points; three operator-engagement open questions; heavy fork-and-own from Synbio.
8. **`docs/planning/PRD-OUTLINE-FOR-OPERATOR-REVIEW.md`** — orchestrator's PRD outline; closes synthesis gaps + adds ten fresh-eyes additions; sub-agent dispatch table populated; ten engineering-blocker resolutions; ZERO-on-CPU binding gate; 22-falsifier registry preview.
9. **`NOTICE`** — copyright posture, license-grant timing, boundary block carried verbatim.
10. **`docs/legal/DATA_POLICY.md`** — license-class taxonomy; hard exclusions; soft row-level traps; bulk artifact placement; per-record license stamp schema; per-prediction license-class taint metric.
11. **`docs/legal/TRADEMARKS.md`** — trademark notices.
12. **`docs/audit/PUBLIC_AUDIT_LIMITS.md`** — this file.
13. **`.gitignore`** — bulk artifact exclusion enforcement.

When Phase-0 code lands (per `docs/planning/PRD-OUTLINE-FOR-OPERATOR-REVIEW.md`), the audit surface extends to:
- `src/zer0pa_pcg/` — Python source for layer adapters, license-stamping ETL, falsifier registry, dossier validators, KG schema, REST stubs, plug-replaceability test matrix.
- `audit/falsifiers.yaml` — 22+ named falsifiers with id / tier / description / severity / gate_action / evidence_schema.
- `audit/runtime/` — runtime audit logs (excluded from git per `.gitignore`; produced during execution).
- `kg/schema.yaml` — KG node and edge taxonomy.
- `regulatory/master_matrix_v0.1.yaml` — Regulatory Fit Score master decision matrix with per-row regulation citation chain.
- `tests/` — unit, integration, golden-fixture invariance tests.
- `docs/CIDA-TS-v0.1.md` — Crop Improvement Dossier Audit-Trail Specification (forked-pattern from Synbio's SBOL3+PROV-O).
- `fixtures/` — small (< 5 GB) test fixtures for golden-fixture invariance testing.

## What is NOT in the public audit surface

The following are **excluded** from the public audit surface regardless of repository visibility:

1. **Partner data** — no seed company genotype / phenotype data, no NARES germplasm material data, no SACTA cultivar registration data, no Pairwise Fulcrum design output, no Living Models BOTANIC fine-tune corpus partner data. These are partner-private under their own data-use agreements.
2. **Field trial data** — no operator's own field trial yield / disease / agronomic data. The platform is research infrastructure, not an in-house breeding programme.
3. **Off-the-shelf licensed regulatory text bodies** — EU NGT regulation full OJEU text, US APHIS RIN 0579-AE84 full rule text, SA GMO Act 1997 text, Cartagena / Nagoya / SMTA legal text bodies. The repository carries citations and `last_verified_date` per row in the master decision matrix; the legal text bodies themselves are not vendored. Where Class-A copies exist (US public-domain regulatory text), they may be vendored under explicit `regulatory/regulatory_text/` with per-file source attribution.
4. **Model fine-tune weights** — PlantCaduceus / GPN / HyenaDNA / Evo-2 / PlantRNA-FM / Living Models BOTANIC fine-tune checkpoints go to private Hugging Face under Architect-Prime, not into this repository. The `.gitignore` enforces.
5. **HF token / API credentials** — `~/.cache/huggingface/token` and any API credentials are never vendored. `.gitignore` enforces `.env*` exclusion.
6. **Endpoint logs and operational transcripts** — runtime audit logs, dossier production logs, and partner-handoff outcome corpus tuples are produced during execution and stored under `audit/runtime/` and `runs/<rid>/tuples.jsonl`; these directories are excluded from git per `.gitignore`. Aggregate audit summaries may be committed via explicit operator-authorised exfiltration only.
7. **Sub-agent prompts and conversation transcripts** — internal sub-agent dispatch is logged structurally (Run / Phase / Sub-agent / Component / Decision / DispatchRecord nodes in the KG) but full prompt-and-response transcripts are not part of the public audit surface.
8. **Architect-Prime HF Pro account credentials and OAuth state** — operator-controlled; not part of any audit surface.

## Audit boundary preservation rules

When the operator authorizes external review, the following rules are enforced:

- The Boundary block (carried verbatim across every artifact) is non-negotiable. No external auditor request to relax the boundary is honoured.
- The 18 anti-decisions are non-negotiable. They are encoded as binding falsifiers in `audit/falsifiers.yaml` (Phase-0 Wave-0 deliverable).
- The `What We Don't Claim` section in `README.md` is the canonical anti-overclaim posture.
- Honest blockers are visibly preserved. WIP is not framed as finished product.
- Cross-workstream fork-and-own is acknowledged at the pattern level; no runtime co-dependency exists between this workstream and any sibling Zer0pa workstream.

## Cross-workstream alignment

This audit-limit posture mirrors the Zer0pa Lane Agent Front Door standard applied to:
- `Zer0pa/DM3` (PUBLIC; READY; System Mechanics zone-02)
- `Zer0pa/Glyph-Engine` (PUBLIC; READY; Method Mechanics zone-02)
- `Zer0pa/Indus-Valley` (PUBLIC; READY; Method Mechanics zone-02; Traditional-Knowledge / non-decipherment posture preserved)
- `Zer0pa/Morph-Bench` (PUBLIC; READY; Method Mechanics zone-02)

Sibling workstreams in the live workstream tier (`Zer0pa/Polymath-AI`, `Zer0pa/Health`, `Zer0pa/Materials`, `Zer0pa/Synthetic-Biology`, `Zer0pa/Energy`) are at the same prep-for-front-door stage as this repository and will follow the same posture when their lane agents align them.

## Honest scoping

This repository is at STAGE-2 RESEARCH-INTAKE. There is no Phase-0 code yet. The "audit surface" at present is briefing assets and orchestrator-authored handoff and PRD-outline materials only. When Phase-0 code lands, the audit surface extends as described above. External reviewers should not expect runtime claims, performance numbers, or deployable system surfaces from this repository at present.
