# Data Policy — Precision Crop Genomics

**Status:** v0.1, drafted 2026-05-02 by orchestrator (Claude Opus 4.7, 1M context).
**Visibility:** PRIVATE repository; this policy applies regardless of future visibility flips.

## Scope

This document binds the data and artifact lifecycle for the Zer0pa Precision Crop Genomics workstream. It is consumed by the license-stamping ETL service (Phase-0 deliverable per `PRD-OUTLINE-FOR-OPERATOR-REVIEW.md`), by every sub-agent ingesting external data, and by every model training run that produces commercializable artifacts.

## License-class taxonomy

Every record ingested carries a four-column license tag (`code` / `data` / `weights` / `API`). Each column is classified into five license classes:

| Class | Meaning | Examples | Treatment |
| --- | --- | --- | --- |
| A | Fully open commercial (Apache-2.0, MIT, BSD, CC0, CC-BY) | PLINK 2 (GPL-3 code, free use), PHGv2 Apache-2.0, AlphaFold DB v4 CC-BY-4.0, AgERA5 CC-BY, CHIRPS v3 CC0, BrAPI 2.1, Crop Ontology, Plant Ontology | Default ingest; commercializable training |
| B | Attribution-required, commercially permissive (CC-BY 4.0, MPL-2.0, EPL) | UniProt CC-BY 4.0 (since 2022), InterPro CC-BY 4.0, PlantCV MPL-2.0, MicMac CECILL-B | Default ingest; auto-emit attribution per dossier; commercializable training |
| C | Non-commercial / share-alike that taints commercial outputs (CC-BY-NC, CC-BY-NC-SA, GPL-3 with linking concerns, AGPL-3.0) | WorldClim 2.1, PLAZA, EOX cloudless mosaics, AgroNT / Nucleotide Transformer weights, Ultralytics YOLO default | **Excluded from commercializable training runs**. License-stamping ETL service blocks ingest into commercializable code paths. Anti-decision falsifiers fire on attempted ingest. |
| D | Paid commercial license required, no free commercial tier | TAIR live curated data (Phoenix Bioinformatics ~$28k/yr), APSIM commercial, ASReml-R, MateSel, Google Earth Engine commercial, Corteva WUS2/BBM ag pool | **Excluded from v1 build**. Anti-decision falsifiers fire. Partner-side license procurement only — not Zer0pa-procured. |
| E | Embargoed, time-limited (Toronto Statement, JGI/Phytozome 2-year, T3 Triticeae Toolbox pre-publication) | TAIR12 GenBank releases <1 year old; Toronto-bound wheat/barley/oat data; Phytozome embargo periods | Auto-expire; per-record `embargo_expiry_timestamp` field. Once expired, reclassify to Class A or B. |

## Hard exclusions (anti-decisions; binding falsifiers)

The following data sources are explicitly excluded from any v1 build, encoded as binding falsifiers in `audit/falsifiers.yaml` (forthcoming Phase-0 Wave 0):

- **PLAZA (Ghent comparative genomics)** — CC-BY-NC-SA; explicitly excludes industrial-sponsored academic work.
- **TAIR live curated data** — Phoenix Bioinformatics paid commercial subscription required; safe path is TAIR12 from GenBank with > 1 year old releases (Class A).
- **WorldClim 2.1** — CC-BY-NC-SA despite ubiquitous academic use; CHELSA / AgERA5 / CHIRPS v3 are drop-in replacements.
- **EOX Sentinel-2 cloudless mosaics** — CC-BY-NC-SA; raw Sentinel-2 from ESA is fully open commercial.
- **JGI / Phytozome embargoed data** — 2-year redistribution restriction; Class E auto-expire.
- **APSIM commercial use** — Special Non-Commercial License; the single biggest license trap in the crop modelling stack. DSSAT-CSM (BSD-3) and AquaCrop-OSPy (GPL-3) are the open alternatives.
- **AgroNT / Nucleotide Transformer weights** — CC-BY-NC-SA; commercially unusable. PlantCaduceus (Apache-2.0) / HyenaDNA (BSD-3) / Evo-2 / GPN (MIT) / PlantRNA-FM (MIT) are the permissive alternatives.
- **AlphaFold 3 main weights / ESM 3 main weights** — non-commercial. AlphaFold DB v4 (CC-BY-4.0) plus OpenFold3 (Apache-2.0) plus ESMFold (open) are the open-weight alternatives.
- **Google Earth Engine free tier** — not commercially usable for any private company including pre-revenue Zer0pa. AWS Open Data Registry + Microsoft Planetary Computer Pro + xarray/STAC is the license-clean alternative.
- **OpenDroneMap as hosted SaaS** — AGPL-3.0 with network-use trigger forces source disclosure. Self-hosted on-premise is permitted.
- **Ultralytics YOLOv5 / v8 default license** — AGPL-3.0 with required Enterprise license. YOLOX or MMDetection are the alternatives.

## Soft row-level traps (per-record handling)

Three softer traps require row-level handling (not hard exclusion):

- **T3 (Triticeae Toolbox) Toronto Statement** — pre-publication restrictions on some wheat / barley / oat data; per-record `toronto_embargo_expiry_timestamp` field; auto-expire Class E → Class A or B.
- **CGIAR genebank physical seed (ITPGRFA Annex 1)** — moves under SMTA; per-record `smta_flag` field linked to ITPGRFA Annex 1 jurisdiction table.
- **Doench / Fusi sgRNA scoring weights** — Microsoft Research redistribution constraints bundled into many CRISPR design tools. Per-record `microsoft_research_redistribution_flag`; the Zer0pa-owned `cropsr_scoring_substitute` module is the safe path for commercial pipelines.

## Bulk artifact placement

No bulk genomic, phenotypic, satellite, or model artifacts are vendored in this repository. The `.gitignore` enforces:

- VCF / BCF / PGEN / PVAR / PSAM / BED / BIM / FAM / GFA / TileDB / hVCF — excluded from git
- Parquet / HDF5 / Feather — excluded from git
- Safetensors / .bin / .pt / .pth / .onnx model checkpoints — excluded from git
- TIFF phenomics image stacks — excluded from git

Bulk artifacts go to **private Hugging Face under the Architect-Prime user (NOT the Zer0pa org)**. HF token at `~/.cache/huggingface/token` on the originating machine. HF Pro account is OAuth-authenticated; streaming-corpus regime is enabled per Polymath Diffusion 2026-05-02 directive. Per-corpus repo naming follows: `Architect-Prime/pcg-<corpus>-v<version>`.

## Per-record license stamp schema (v0.1; Phase-0 Wave-1 deliverable)

The license-stamping ETL service emits a per-record JSON-LD stamp:

```json
{
  "@context": "https://zer0pa.ai/pcg/license-stamp/v0.1",
  "record_id": "sha256:...",
  "source_url": "https://...",
  "code_license": {"class": "A", "spdx": "Apache-2.0", "url": "..."},
  "data_license": {"class": "B", "spdx": "CC-BY-4.0", "url": "..."},
  "weights_license": {"class": "A", "spdx": "Apache-2.0", "url": "..."},
  "api_license": {"class": "B", "spdx": "CC-BY-4.0", "url": "..."},
  "toronto_embargo_expiry_timestamp": null,
  "smta_flag": false,
  "microsoft_research_redistribution_flag": false,
  "ingest_timestamp": "2026-05-02T...",
  "downstream_taint_filter_verdict": "commercializable"
}
```

Every prediction emitted by the platform carries the aggregate license stamp through the audit-log sha256 hash chain into the dossier's Provenance Block. Downstream taint filter blocks any model training run that mixes Class A inputs with Class C/D inputs into a commercializable artifact (binding falsifier `f009`).

## Per-prediction license-class taint metric

Every prediction the platform emits carries a `license_class_taint_metric` quantifying the marginal effect of Class B (attribution-required) and Class C/D (excluded) inputs on the prediction. Computed by re-running the prediction with the Class-A-only training set vs the full training set; metric is the L2 distance in prediction space normalised by prediction magnitude. The audit log captures this metric per prediction. High-taint predictions are flagged in the dossier's Risk Block.

## Scheduled refresh

Every Class A / B / C / D / E classification carries a `last_verified_date` timestamp. A scheduled refresh sub-brief (run quarterly) re-fetches each cited license text and updates `last_verified_date` if no change, or flags for human review if change detected. License drift triggers binding falsifier `f019`.

## Cross-machine handoff

When the next role (overnight executor) runs on a different machine, it inherits this policy via repo clone. No data moves between machines except through HF Pro under Architect-Prime authentication. AWS af-south-1 (Cape Town) is the preferred satellite-compute region for SA-residency operations.
