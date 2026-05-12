# Lane Agent Handover — Precision-Crop-Genomics
**Date:** 2026-05-04  
**Outgoing agent:** Precision-Crop-Genomics Lane Agent (session ending)  
**Incoming agent:** Read this entire file before touching anything. Then read the documents in §2 in the order listed. Then read §3 (exact current state). Then act per §4.

---

## 1 — Your role in one paragraph

You own the **corridor** between `github.com/Zer0pa/Precision-Crop-Genomics` (PRIVATE repo) and `src/content/lanes/life-sciences/Precision-Crop-Genomics.md` in the canonical website worktree at `/Users/Zer0pa/Website/.claude/worktrees/canonical-v2-opus/site-v2/`. The repo's README is canonical; the website `.md` is derived. Your job is editorial synchronisation, nuance, and tone between them. You are not a coder, not an architect, not a registry editor. You edit only your lane's `.md` file and your lane's repo README. You do not touch other lanes' files.

---

## 2 — Read these documents, in this order, before doing anything

| # | Path | What it is |
|---|---|---|
| 1 | `/Users/Zer0pa/orchestration-state/LANE_AGENT_BRIEF_2026-05-03.md` | Canonical role definition, workflow (Phase 1–4), constraints, useful commands. Read every section. |
| 2 | `/Users/Zer0pa/orchestration-state/lane-asks/Precision-Crop-Genomics/INDEX.md` | Your ask queue. Topmost entry is the active task. Read end-to-end; the log is your session history. |
| 3 | `/tmp/lane-Precision-Crop-Genomics/STATE.md` | Phase-1 state report produced this session. The diff findings, severity tags, and recommended actions §6 are your working list. |
| 4 | `/Users/Zer0pa/Website/.claude/worktrees/canonical-v2-opus/site-v2/src/content/lanes/life-sciences/Precision-Crop-Genomics.md` | The website lane file. This is the file you edit. Read its current state before any edit. |
| 5 | `gh api repos/Zer0pa/Precision-Crop-Genomics/readme --jq '.content' \| base64 -d` | The repo README (authenticated fetch — repo is PRIVATE). This is the canonical source you sync the website .md toward. |
| 6 | `/Users/Zer0pa/orchestration-state/pypi-zenodo-lane-reports/Precision-Crop-Genomics_PYPI_ZENODO_STATUS_2026-05-03.md` | PyPI/Zenodo status report produced this session. Completed task — no re-work needed. |

The two playbooks (UX Guide and Sync Mechanic) are large files; skim them for context on the parser contract if you need to re-derive a field mapping, but they are not required reading to proceed with the open tasks below.

---

## 3 — Exact current state (as of handover)

### 3.1 — What has been done

**Phase 1 (state audit) — COMPLETE**  
Full state report at `/tmp/lane-Precision-Crop-Genomics/STATE.md`. All findings are severity-tagged. Do not re-run Phase 1; the report is the record.

**Phase 3 non-blocked edits — APPLIED**  
Four edits were applied to `src/content/lanes/life-sciences/Precision-Crop-Genomics.md`:

| Edit ID | Location | Before | After |
|---|---|---|---|
| R-3 | Body `## Readiness` table, field name | `Verdict` | `Stage` |
| R-4 frontmatter | `key_metrics[3].metric` | `"READINESS_VERDICT"` | `"READINESS_STAGE"` |
| R-4 body | `## Key Metrics` table row | `READINESS_VERDICT` | `READINESS_STAGE` |
| R-5 body | `## Verification Status` V_09/V_10 | `NOT-STARTED` | `UNTESTED` |

These edits are in the working tree (not committed — brief §8 prohibits committing without operator approval).

**PyPI/Zenodo audit — COMPLETE**  
Report at `/Users/Zer0pa/orchestration-state/pypi-zenodo-lane-reports/Precision-Crop-Genomics_PYPI_ZENODO_STATUS_2026-05-03.md`. Lane is "Not Currently PyPI-Shaped" (no `pyproject.toml`). Redaction sweep: all 9 public-audit-surface files CLEAN. No further action needed on this task.

### 3.2 — What is NOT done (open items)

**BLOCKED — awaiting operator answers in INDEX.md:**

| Item | What's needed | Where operator fills in |
|---|---|---|
| R-1 (CRITICAL) | Visibility: frontmatter says `INTERNAL`, GitHub API says `PRIVATE`. Operator must decide which is correct for the website render. | INDEX.md Q1 `*Operator answer:*` |
| R-2 (MEDIUM, REPO-SIDE first) | License: README `## Repo Identity` says SAL v7.1; README `## Licensing` says Apache-2.0; `.md` frontmatter says `OWNER_DEFERRED`. Operator must name the canonical value. README must be fixed first, then website `.md` body follows. | INDEX.md Q2 `*Operator answer:*` |
| R-6 (LOW, REPO-SIDE) | `last-commit-sha` row absent from README `## Repo Identity` table. Deferred — self-defeating without a CI hook. Operator to decide skip vs. add automation. | Not in INDEX Q-set; surface in next Phase-3 complete entry. |

**DEFERRED — infrastructure blockers outside this lane's scope:**

| Item | Status |
|---|---|
| `bun run build` full 8-gate pass | CANNOT be obtained. Worktree-wide build fails due to other lane agents writing `BLOCKED` verdict tokens (not in schema enum) into Health.md and Gnosis-Morph-Bench.md. PCG.md is schema-clean (7× `PASS`, 3× `PENDING`). The schema enum `"PASS"\|"FAIL"\|"INC"\|"PENDING"\|"STAGED"` does not include `BLOCKED` or `UNTESTED`. This needs a cross-lane infrastructure fix in `content.config.ts` — outside any lane agent's scope. |
| Live `curl -sI 200 OK` | DEFERRED — dev server at :4500 was not running at audit time. Run `curl -sI http://127.0.0.1:4500/life-sciences/Precision-Crop-Genomics/` when server is up. |
| R-5 frontmatter V_09/V_10 precision | Kept as `"PENDING"` (schema-enforced). README and body say `UNTESTED`. Will stay mismatched until `UNTESTED` is added to the schema enum. Surface this to repo-team. |

### 3.3 — Repo state

| Field | Value |
|---|---|
| HEAD SHA (as of 2026-05-03T01:39:40Z) | `0ec91b854d0dcd227f5d7d34523203a5db8816fe` |
| Repo visibility | PRIVATE (GitHub API confirmed) |
| Lane stage | STAGE-2 RESEARCH-INTAKE |
| Phase-0 code | None (PRD outline awaiting operator confirmation) |
| LICENSE | SAL v7.1 (`LicenseRef-Zer0pa-SAL-7.1`) |
| CITATION.cff | ABSENT |
| .zenodo.json | ABSENT |
| pyproject.toml | ABSENT — not PyPI-shaped |

### 3.4 — Website .md state

File: `src/content/lanes/life-sciences/Precision-Crop-Genomics.md`  
In the worktree at: `/Users/Zer0pa/Website/.claude/worktrees/canonical-v2-opus/site-v2/`  
Branch: `design/canonical-v2-opus`  
Status: modified (R-3, R-4, R-5 edits applied; not committed)

**Frontmatter fields that are still blocked / inconsistent:**
- `visibility: "INTERNAL"` → should be `"PRIVATE"` per GitHub API (pending OQ-1)
- `license: "LicenseRef-Zer0pa-OWNER_DEFERRED"` → needs operator decision on canonical value (pending OQ-2)
- `verification[8].verdict: "PENDING"` (V_09) → ideally `"UNTESTED"` but schema prevents it
- `verification[9].verdict: "PENDING"` (V_10) → same constraint

---

## 4 — What to do next (in order)

**Step 1 — Check for operator answers.**  
Read `/Users/Zer0pa/orchestration-state/lane-asks/Precision-Crop-Genomics/INDEX.md`. Look at the Q1 and Q2 `*Operator answer:*` lines. If filled in, proceed to Step 2. If still blank, the lane is in a waiting state — do not invent answers; surface the blocked state to the operator.

**Step 2 — Apply R-1 once OQ-1 is answered.**  
Edit frontmatter `visibility:` field:  
- If operator says PRIVATE: `visibility: "INTERNAL"` → `visibility: "PRIVATE"`  
- If operator says INTERNAL (sibling convention): leave `visibility: "INTERNAL"` unchanged  

**Step 3 — Apply R-2 once OQ-2 is answered (README first, then .md).**  
The README is canonically inconsistent; the README team must fix it first. Once README is reconciled, propagate the canonical license value to:
- `.md` body `## Repo Identity` table License row
- `.md` frontmatter `license:` field  
The three locations to reconcile: README `## Repo Identity` table | README `## Licensing` section | `.md` frontmatter `license:`.

**Step 4 — Attempt `bun run build` from the worktree.**  
```bash
cd /Users/Zer0pa/Website/.claude/worktrees/canonical-v2-opus/site-v2
bun run build 2>&1
```  
Receipt all 8 gate outputs literally. If build fails on OTHER lanes (not PCG), note this clearly — it is not your failure to fix. PCG.md's schema is currently clean.

**Step 5 — Attempt live verify.**  
```bash
curl -sI http://127.0.0.1:4500/life-sciences/Precision-Crop-Genomics/
```  
Must return `200 OK`. If dev server not running, note as deferred.

**Step 6 — Append Phase-3-complete entry to INDEX.md.**  
With: files changed, literal build receipt, live verify result, any remaining open items as RF-N flags.

---

## 5 — Key constraints (do not violate)

- **Sonnet sub-agents only** — never Opus, never Haiku.
- **Edit only this lane's .md** — do not touch Health.md, Synthetic-Biology.md, or any other lane.
- **Do not commit** to the worktree without explicit operator approval. The worktree has other agents' uncommitted work.
- **Do not run the dev server** — the :4500 server is operator-managed.
- **Do not touch** `content.config.ts`, `site-registry.ts`, `canonical-zones.ts`, `BaseLayout.astro`, `src/components/`, or any audit script.
- **Receipts, not narrative** — every build/audit result must show literal stdout.
- **README is canonical** — the website .md follows the repo README, not the other way around (except GIF direction, which is irrelevant here).

---

## 6 — Useful commands (copy-paste ready)

```bash
# Pull current README
gh api repos/Zer0pa/Precision-Crop-Genomics/readme --jq '.content' | base64 -d

# Check HEAD SHA
gh api repos/Zer0pa/Precision-Crop-Genomics/commits/main --jq '.sha'

# Check repo metadata
gh api repos/Zer0pa/Precision-Crop-Genomics --jq '{name, visibility, pushed_at}'

# Check current .md file state
cat /Users/Zer0pa/Website/.claude/worktrees/canonical-v2-opus/site-v2/src/content/lanes/life-sciences/Precision-Crop-Genomics.md | head -100

# Build (from worktree)
cd /Users/Zer0pa/Website/.claude/worktrees/canonical-v2-opus/site-v2 && bun run build 2>&1

# Live verify
curl -sI http://127.0.0.1:4500/life-sciences/Precision-Crop-Genomics/

# Check HF
curl -sI https://huggingface.co/Zer0pa/Precision-Crop-Genomics
```

---

## 7 — Session artefacts produced

| Artefact | Path | Status |
|---|---|---|
| Phase-1 STATE report | `/tmp/lane-Precision-Crop-Genomics/STATE.md` | Complete — do not re-produce |
| PyPI/Zenodo status report | `/Users/Zer0pa/orchestration-state/pypi-zenodo-lane-reports/Precision-Crop-Genomics_PYPI_ZENODO_STATUS_2026-05-03.md` | Complete — do not re-produce |
| INDEX ask log | `/Users/Zer0pa/orchestration-state/lane-asks/Precision-Crop-Genomics/INDEX.md` | Active — append Phase-3-complete entry when R-1/R-2 are resolved |
| This handover | `/Users/Zer0pa/orchestration-state/lane-asks/Precision-Crop-Genomics/HANDOVER_2026-05-04.md` | For incoming agent only |

---

*Incoming agent: begin at §4 Step 1. Do not re-run Phase 1. Do not re-produce the PyPI/Zenodo report. Check for operator answers in INDEX.md and act accordingly.*
