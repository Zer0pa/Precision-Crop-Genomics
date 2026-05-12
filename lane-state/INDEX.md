# Lane Ask Queue — Precision-Crop-Genomics

## Identity
- Lane: `Precision-Crop-Genomics`
- Repo: `github.com/Zer0pa/Precision-Crop-Genomics` (PRIVATE)
- Section: `life-sciences`
- Website .md: `src/content/lanes/life-sciences/Precision-Crop-Genomics.md`
- Website URL: http://127.0.0.1:4500/life-sciences/Precision-Crop-Genomics/
- Brief (canonical): `/Users/Zer0pa/orchestration-state/LANE_AGENT_BRIEF_2026-05-03.md`

## Known flags
PRIVATE repo — README via authenticated `gh api`.

Known REPO-SIDE flag: README `## Repo Identity` License row says `SAL v7.1` but `## Licensing` section says Apache-2.0; `.md` frontmatter says `OWNER_DEFERRED`. Three different license values; needs repo-team reconciliation first.

---

## Ask log (newest first; append above the divider)

### 2026-05-03 · Phase-3 execution receipt — COMPLETE (partial)

**Executed:** Non-blocked actions R-3, R-4, R-5 from STATE.md §6.  
**Blocked:** R-1 (visibility, awaits OQ-1), R-2 (license, awaits OQ-2), R-6 (deferred — see below).

**Edits applied to `src/content/lanes/life-sciences/Precision-Crop-Genomics.md`:**

| Edit | Location | Change |
| --- | --- | --- |
| R-4 frontmatter | `key_metrics[3].metric` | `"READINESS_VERDICT"` → `"READINESS_STAGE"` |
| R-4 body | `## Key Metrics` table | `READINESS_VERDICT` → `READINESS_STAGE` |
| R-3 body | `## Readiness` table | `\| Verdict \|` → `\| Stage \|` |
| R-5 body | `## Verification Status` V_09/V_10 | `NOT-STARTED` → `UNTESTED` |

**R-5 frontmatter V_09/V_10: schema constraint discovered.**  
README uses `UNTESTED` as a verdict token; the collection schema only allows `"PASS"|"FAIL"|"INC"|"PENDING"|"STAGED"`. `UNTESTED` would cause `[InvalidContentEntryDataError]`. Kept frontmatter V_09/V_10 as `"PENDING"` (schema-valid approximation). Body displays `UNTESTED` (free text, README-faithful). **Action for operator/repo-team: add `UNTESTED` to the schema enum in `content.config.ts` if `UNTESTED` is the intended canonical token for pre-code checks. Until then, frontmatter V_09/V_10 must remain `PENDING`.**

**Schema validation confirmed:**  
PCG.md frontmatter verification verdicts: 7× `PASS`, 3× `PENDING` — all schema-valid (no `BLOCKED`, `NOT-STARTED`, or `UNTESTED` in frontmatter).

**`bun run build` receipt:**
```
[preflight-disk] PASS: 5.71 GiB free on worktree volume.
[generate-viz-unified] DONE: 32 nodes, 1 links → public/viz-unified.json
[embed-lanes] wrote workers/semantic-docs.generated.ts (32 lanes)
[site-version] Build SHA: 080567253e0549f584a20ba80165e12a400367f8
astro build → FAIL (schema error in OTHER lane — NOT Precision-Crop-Genomics)
[InvalidContentEntryDataError] lanes → gnosis/gnosis-morph-bench — verification.4.verdict:
  Invalid option: expected one of "PASS"|"FAIL"|"INC"|"PENDING"|"STAGED"
```
Build is broken worktree-wide due to multiple other lane agents introducing invalid verdict tokens (`BLOCKED`, etc.) into their lanes (Health.md, Gnosis-Morph-Bench.md confirmed; possibly others). **This is a cross-lane infrastructure failure — not caused by PCG edits.** PCG.md passed schema validation in the first build attempt; only other lanes caused the content-entry errors.

Baseline build test (stash state, pre-my-edits, all other-agent edits present): same result — build was already broken before my edits.

**Live verify:** DEFERRED — dev server was not running at either audit point (curl exit code 7 on port 4500).

**R-6 (last-commit-sha) — DEFERRED to operator.**  
Adding a SHA row to the README is self-defeating without a hook/CI step that keeps it current; the HEAD will be stale the next commit. Flagging for repo-team to decide whether to implement an automated SHA-stamp step or skip R-6 entirely. Current HEAD for reference: `0ec91b854d0dcd227f5d7d34523203a5db8816fe`.

**Still open (awaiting operator):**
- OQ-1 / R-1: PRIVATE vs INTERNAL in `.md` frontmatter `visibility:`
- OQ-2 / R-2: License reconciliation (README Repo Identity vs Licensing section vs .md frontmatter)
- OQ-3: Dev server up?
- Cross-lane: schema enum gap — `UNTESTED` not in schema (affects PCG frontmatter V_09/V_10 precision, and likely caused other agents' BLOCKED-token failures)

---

### 2026-05-03 · Phase-2 partial gate (operator) — PENDING

Source: Operator review of STATE report at `/tmp/lane-Precision-Crop-Genomics/STATE.md`.

**Status:** PARTIALLY GREENLIT — operator decisions required before Phase 3 can proceed in full.

**Operator decisions pending** (operator: append answer under each question below):

**Q1 (blocks visibility fix R-1):** GitHub API confirms repo is `private`. Website `.md` says `visibility: "INTERNAL"`. Sibling lanes (Health, Synthetic-Biology) all use `INTERNAL`. Should this lane render `PRIVATE` (matches GitHub API), or `INTERNAL` (matches sibling convention)?

*Operator answer:*

**Q2 (blocks license fix R-2) — REPO-SIDE first:** README is internally inconsistent on license — `## Repo Identity` says SAL v7.1, `## Licensing` says Apache-2.0; `.md` frontmatter says `OWNER_DEFERRED`. Three different values; needs repo-team reconciliation first. Which is canonical?

*Operator answer:*

**Q3 (informational) — Dev server expected up?** Lane agent could not produce live `200 OK` receipt because :4500 was down at audit time.

*Operator answer:*

---

When the operator has filled in answers above, you may proceed to Phase 3 per the protocol below.

**Phase-3 protocol when unblocked:**
1. Re-read `/tmp/lane-Precision-Crop-Genomics/STATE.md` and the operator's answers above.
2. Apply non-blocked actions from §6 immediately if any; apply blocked actions after operator answers land.
3. From the worktree: `bun run build` — receipt all 8 audits.
4. Verify live: `curl -sI http://127.0.0.1:4500/life-sciences/Precision-Crop-Genomics/` → 200 OK.
5. Append `Phase-3-complete` entry with files / receipts / open follow-ups.

Sonnet sub-agents only.

**Status:** Awaiting operator decision.

---

*Lane Agent: read this file end-to-end, then execute the topmost unfulfilled entry. Append your reply with receipts as a new dated entry above the divider when you complete each ask.*
