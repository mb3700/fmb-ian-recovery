# Handoff — FMB Recovery Dashboard

**Read this first.** Captures where the project stands at the end of the May 23, 2026 build sessions and what the next session needs to know.

---

## Current state

- **Live:** https://fmb-ian-recovery.vercel.app
- **Repo:** https://github.com/mb3700/fmb-ian-recovery
- **Local working copy:** `/Users/markbole/Documents/fort myers beach/recovery-dashboard/`
- **Most recent commit at handoff:** `438b555` — Sister-City scale-context note
- **Deploy:** Vercel auto-deploys from `main` within ~30 seconds of push

The dashboard is content-complete and editorially ready. It has NOT been shared with FMB stakeholders (Chamber, town staff, London Bay, press) yet. Until that first share, treat pre-publication correction rules (clean cleanup, no withdrawn markers) — see editorial standards below.

---

## Pre-share checklist

Mark's plan is to share with stakeholders in this order: Jacki Lysak (Chamber, primary data source) → London Bay's Mark Wilson → town staff → broader audience. Each round of feedback before broader exposure reduces correction cost.

Do these before the first stakeholder share:

1. **Final read-through, top to bottom on the live deploy.** Look for stale claims, broken cross-references, lingering wrong-narrative bits. We caught 3 in one session (Sandpiper override, Lodging Mix causal claim, Sister-City causal claim) — assume more may exist.
2. **Click every link.** Every override chip on every card. Sticky nav. Footer. Flip buttons on both `index.html` and `data-decisions.html`. Confirm nothing 404s or lands on a raw `.md` file.
3. **Send the outreach to Jacki.** Draft at `outreach-draft-bedtax-housing-request.md`. Sending it unblocks the FY26 Q1 bed tax refresh AND the housing pre-Ian baselines (RPCRA). The freshness banner's "requested from Lee County" claim needs an actual request behind it.
4. **Mobile check.** Deferred during the build. Open the URL on a phone. Verify nav doesn't break, cards stack cleanly, flip buttons are tappable, tables scroll horizontally OK.
5. **Validate the JSON one more time.** `python3 -c "import json; json.load(open('data/metrics.json'))"` from the project root.

---

## Pending data refreshes (already flagged in the dashboard)

| Pending item | Channel | Where it surfaces today |
|---|---|---|
| FMB-specific FY26 Q1 (Oct–Dec 2025) bed tax | Lee County Clerk of Court via FMB Chamber | Freshness banner; bed tax card refresh-status; Sister-City; methodology |
| Pre-Ian (2022) vs current housing — single-family residential + condo, split: active listings, annual closings, median price + DOM | RPCRA / Lee County Property Appraiser via FMB Chamber | All four Housing placeholder cards; methodology; outreach draft section 2 |
| Sandcastle Beach Club status (Chamber's own "20 or 53 rooms?" flag) | Direct ask to Chamber | Data Decisions → Pending Chamber Clarification panel |
| Compass Rose project — verify if active or dormant | Direct ask to Chamber | Data Decisions → Pending Chamber Clarification panel |

When any of these arrive, the corresponding cards / banners just need values plugged in. The "refresh in progress" framing already in place handles the wait.

---

## Editorial standards (memory)

Four memory files capture the standards established this session. The next session should read them before making content changes:

- `~/.claude/projects/-Users-markbole-Documents-analytics-display/memory/feedback_fmb_sourcing.md` — Chamber is source of truth; only override with sourced post-March 2026 facts or pre-March official records; booking-platform listings are NOT evidence of current operation; pre- vs post-publication correction protocol
- `feedback_fmb_london_bay_objectivity.md` — Mark must read as independent; no cosmetic couplings to London Bay; factual pipeline + audit entries OK
- `feedback_fmb_no_sanibel_methodology.md` — Strip methodology attribution to Sanibel; bed-tax cross-municipality comparison (including Sanibel) is fine
- `feedback_fmb_editorial_tone.md` — No self-asserting language ("analytically correct," "most credible," "deliberately strict to keep credible"); describe what the dashboard shows; let readers judge

Plan file with this session's running plan: `~/.claude/plans/no-the-chamber-doesn-t-mighty-petal.md`

---

## Source files on disk

| File | Use |
|---|---|
| `/Users/markbole/Downloads/Accommodations as ofMarch 18,, 2026.xlsx` | **Source of truth.** FMB Chamber's published lodging baseline + pipeline. All dashboard lodging numbers and the destroyed-hotels list trace back to this. |
| `/Users/markbole/Documents/fort myers beach/Tourist Tax Breakdown - Add'l needed - Data through August 2025.xlsx` | Lee County Clerk bed-tax data by municipality, FY22–FY25 YTD. Source for the 48% headline and Sister-City comparison. |
| `/Users/markbole/Documents/fort myers beach/fmb-baseline-report-march-2026.xlsx` | FMB business database (Google-Places-verified). Used for non-lodging categories and the delinquent VR license signal. |
| `/Users/markbole/Documents/fort myers beach/fmb-system-of-record-lodging.xlsx` | Mark's verification work file. Use as a cross-check, NOT as a source — Chamber is canonical. |
| `/Users/markbole/Documents/analytics display/sanibel-ref/dashboard/scorecard.ts` | Sanibel comparison data (tourism metrics, housing metrics) — for sister-city comparisons only |

---

## Open questions

- **Sandcastle Beach Club:** Chamber's own "20 or 53 rooms?" uncertainty. Currently kept at Chamber's 53 in the destroyed list. Needs direct Chamber clarification.
- **Compass Rose project (140 rooms in pipeline):** Chamber lists "permanent holding pattern" — no corroborating public reporting. Needs direct Chamber clarification.
- **London Bay project status post-June Council hearing:** The dashboard currently says "LPA recommended denial May 2026; Town Council hearing June 2026." When the Council vote happens (June 2026), update the status. Use the neutral phrasing pattern Mark already approved.
- **Beach Baptist Phase 2 (10 rooms in Chamber file marked "need update"):** Chamber's own flag. Whether it's a real Phase 2 or a duplicate of the 12-home sell-land project needs Chamber confirmation.

---

## Post-publication correction protocol

Once the dashboard has been shared with any external stakeholder, the cleanup rules change:

- **Pre-publication:** if you find a wrong override or claim, just correct it as if it never happened. Delete the row, renumber, cascade the numbers.
- **Post-publication:** leave the wrong override in the Override Log marked **WITHDRAWN** with the correction date, the source that authorized the withdrawal, and the cascade effects. This is the transparency signal — the dashboard catches and publicly corrects its own mistakes.

(Full pattern documented in `feedback_fmb_sourcing.md`.)

---

## Architectural notes (for code-level work)

- **Dashboard pages are static HTML.** No build step. Edit `index.html` directly; `cp index.html dashboard.html` to sync (they're maintained as identical copies because Vercel's default route serves both).
- **`data-decisions.html`** is the standalone audit-trail page. Its sticky nav points back to `index.html` sections; its own "Data Decisions" link is styled `class="active"`.
- **`data/metrics.json`** is the underlying data; the HTML is hand-written to match. They must stay in sync manually. When pipeline numbers change in metrics.json, update the corresponding HTML.
- **Card-flip mechanic** is JS-augmented (script at the bottom of `index.html`). Each `.metric-card` with prose elements (`.metric-note`, `.metric-source`, `.refresh-status`) auto-gets a flip button at page load. Cards without prose are skipped. To remove the flip, just delete the script — no markup changes needed.
- **Scroll-spy** highlights the active nav section using IntersectionObserver. Also script-augmented at the bottom of `index.html`.
- **Icons** on metric cards are inline `data:image/svg+xml` backgrounds defined in `styles.css` (no font dependency). 17-icon library; add new ones by extending the `.metric-icon.NAME` pattern.

---

## How to resume in a new session

First message can be:

> *"Read /Users/markbole/Documents/fort myers beach/recovery-dashboard/HANDOFF.md to ground yourself in where the FMB Recovery Dashboard stands, then [specific ask]."*

That loads this doc + the relevant memory files via reference. The next session should be productive within the first turn.
