# Precision-Crop-Genomics · product page bundle

Portable snapshot of the Precision-Crop-Genomics product page, built against
the locked ZPE-XR / DM3 / Genesis prototype (`xr-product-page-build`).

This bundle is durability-replicated to the public Hugging Face dataset
[`Zer0pa/Precision-Crop-Genomics-lane-state`](https://huggingface.co/datasets/Zer0pa/Precision-Crop-Genomics-lane-state).
The GitHub repo (this one) is the canonical source of truth; the HF dataset is
the redundant-storage backup.

## Layout

```
product-page/
├── README.md                       — this file
├── index.html                      — the product page (self-contained, ~80 KB)
├── render.mjs                      — portable Playwright renderer
├── audit.json                      — last-render audit (pretext, console, metrics, externals)
└── screenshots/
    ├── full-1440.png               — full page at 1440 viewport
    ├── top-crop.png                — hero crop
    ├── insight-benchmark-crop.png  — 04 / 05.x / 06 / 06.1 band
    ├── possibility-crop.png        — 09 row + unlock cards
    └── mobile-414.png              — mobile fold at 414 viewport
```

## Reproduction

```bash
# Serve locally so /favicon.ico resolves cleanly:
cd product-page && python3 -m http.server 8767 &
# Then render:
PAGE_URL=http://127.0.0.1:8767/index.html node render.mjs
```

Or render directly from disk without a server:

```bash
PAGE_URL="file://$(pwd)/index.html" node render.mjs
```

`render.mjs` reads `PAGE_URL`, `OUT_DIR`, and `CHROME` from the environment;
defaults are documented inline.

## Cell-by-cell story

- **00 Hero** — `Twenty-two falsifiers, before line one of code.` (FPO advisory
  tweak adopted verbatim per Repo §B line 750).
- **04 INSIGHT** — `Twenty-two ways the system could be wrong, written first.`
  (reframes the hero into the conceptual wedge, per §A line 283).
- **05.0 / 05.1** — current-tech (emergent audit) vs our-tech (pre-registration
  discipline).
- **05.2 BENCHMARKS** — 4 mini-metrics (22 falsifiers · 5 sources · 7 dossier
  blocks · 0/1 PRD signed) + 3 mini-bars (intake committed = focus; Phase-0 +
  benchmark runs = pending).
- **06 / 06.1** — measurement surface + 4-row comparative gate panel
  (pre-registration row focus; Phase-0 / benchmark / PRD-sign-off rows pending).
- **07.1 – 07.5** — five key metrics, all values trace to FPO §A defensible
  anchors.
- **08 / 08.1 / 08.2** — determinism trio. 08.2 carries the §A non-claim
  verbatim (`No Phase-0 implementation exists.`).
- **09 / 09.1 / 09.2 / 09.3** — possibility question + ambition + live-probe +
  live-workstream status (authored per operator "complete the story"
  directive 2026-05-09).
- **09.4 – 09.8** — five unlock cards: Tier-1 pangenomes · Regulatory Fit
  Score · SE(3) protein tower (Synbio fork) · BoTorch qNEHVI six-axis Pareto
  breeding · pre-falsified-design paradigm.
- **01 / 02 / 03** — external slots (gap / markets / value) remain placeholder
  per template rules §2 (genuinely external; operator-supplied market data
  pending).
- **#2 hero diagram** — pure-black 572×534 placeholder per §C.4
  (operator-supplied asset pending; this is the contractual state, not a
  defect).

## Provenance

- **Source prototype** — `/Users/Zer0pa/Desktop/xr-product-page-build/index.html`
  (live at `http://127.0.0.1:8765/`).
- **FPO truth basis** — `reports/Precision-Crop-Genomics.md:34,42-45,58` +
  `falsification/Precision-Crop-Genomics.md:23-62`.
- **Repo §B final headline call** — ADOPT FPO advisory tweak around
  falsifiers-before-code (`LANDING_CARD_WAVE2_CENTRAL_DISPATCH_BRIEF_2026-05-08.md`
  line 750).
- **Website §C.2** — cell 04 `22 falsifiers · zero lines of code yet`; 07.1
  `22 PRE-REGISTERED FALSIFIERS`; 08.2 names "no Phase-0 implementation, PRD
  operator approval pending" plainly (line 850).

## Repo correspondence

- Hero sublabel: `A pre-PRD research-intake dossier · Precision-Crop-Genomics`
- CTA: implicit — full repo at <https://github.com/Zer0pa/Precision-Crop-Genomics>
- HEAD at bundle time: `0add531be044404c97db0d4aba536637fe1443cc` (main)
- README `Visibility` row reads `Public · research-intake dossier surface`
  (G1 closed in the cited HEAD commit).
