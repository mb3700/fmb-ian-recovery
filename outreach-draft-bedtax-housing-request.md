# Outreach Draft — Bed Tax + Housing Data Request

**To:** Jacki Liszak, President — Fort Myers Beach Chamber of Commerce
**CC (suggested):** Lee County Clerk of Court contact; RPCRA contact (if known)
**From:** Mark Bole, FGCU Ain Technology and Design Hub
**Subject:** Two data requests for the FMB Recovery Dashboard (Q2 2026 refresh)
**Date drafted:** May 23, 2026

---

## Suggested email body

> Hi Jacki,
>
> Thanks for the accommodations file you shared in March — the Chamber's hotel and VR room counts are now the primary lodging source on the [FMB Recovery Dashboard](https://fmb-ian-recovery.vercel.app). I'd like to refresh it ahead of any wider Chamber discussions.
>
> Two specific data refreshes would tighten the dashboard substantially:
>
> **1. Bed tax — FMB-specific FY26 Q1 (October–December 2025).**
> The dashboard currently shows FY25 YTD-through-August data from the file you provided. The Lee County Clerk's publicly-published TDC reports contain only county aggregates (which makes sense given the statutory confidentiality of TDT returns). To extend the 4-year recovery trajectory — 15% → 37% → 48% — into FY26, we'd need the FMB-specific Oct, Nov, Dec 2025 collections in the same format as the spreadsheet you sent through August. The format I'm working from is *Tourist Tax Breakdown - Add'l needed - Data through August 2025.xlsx.*
>
> **2. Pre-Ian vs current housing data (RPCRA / Lee County Property Appraiser).**
> The dashboard's Housing Market section currently shows year-over-year growth from Redfin — Feb 2026 closings (44) were up 69% over Feb 2025 (26); December 2025 (37) was up 68% over December 2024 (22). YoY change tells direction, not recovery. To follow the Sanibel framework properly — pre-Ian (2022) vs current (2026) on both listings and sales — we'd need an FMB-specific MLS pull from RPCRA (or whoever your contact is at Lee County Property Appraiser). Specifically:
>
>   - **Active listings:** total active FMB residential listings on a representative pre-Ian date (e.g., June 2022) and on a current date (e.g., end of Q1 2026).
>   - **Annual sales:** 2022 monthly closing counts for FMB (pre-Ian full-year baseline), and a trailing-12-month total for the current period.
>   - **Median price + days on market:** 2022 annual averages on FMB to compare to the Feb 2026 Redfin values ($580K median, 134 DOM).
>
> Even a partial pull (e.g., just the 2022 monthly closings) would let us populate the most important card. The dashboard's "Data Decisions" page documents every override and pending request, so anything received is properly sourced.
>
> No rush on either — the dashboard is explicitly flagged "refresh in progress" until the data arrives. Sharing now so the request is queued.
>
> Happy to take a phone call if it's easier than email exchanges. And thanks for everything you've done to make the Chamber's data the spine of this dashboard.
>
> Mark
> Mark Bole · FGCU Ain Technology and Design Hub
> Live dashboard: https://fmb-ian-recovery.vercel.app
> Methodology: https://fmb-ian-recovery.vercel.app/methodology.html

---

## Notes for sending

- **Tone:** collegial, not transactional. Jacki has already shared two non-public data pulls — this is a follow-up, not a cold ask.
- **Volume:** two requests in one email is fine because they share a recipient and channel. If she has different contacts at the Clerk vs. RPCRA, she'll naturally split the asks downstream.
- **Timing:** sending mid-week (Tuesday–Thursday) tends to get faster responses on data requests like this.
- **Follow-up cadence:** if no response in 7–10 business days, a single short bump email referencing the original. Don't over-press; she's busy and the value of the data improves as it accumulates anyway.

## When the data comes back

- Drop the spreadsheet (or numbers) into the conversation. ~5 minutes to update `metrics.json`, replace the refresh-status flags, and push.
- Vercel auto-deploys; live within ~30 seconds.
- New numbers will populate:
  - The bed-tax trajectory chart (FY26 Q1 added as a 5th bar) and the sister-city comparison table
  - The two housing placeholder cards (Active Listings and Annual Sales Volume) currently showing "— / —"
  - The pre-Ian columns on the Median Price + DOM card
  - A new top-level "Housing Recovery %" computation in the Housing Market section once both pre-Ian and current values are in

## Alternative contacts if Jacki can't deliver

- **Lee County Clerk of Court Inspector General Department:** 239-533-2190 (cited in their TDT FAQ as the contact for non-public data inquiries).
- **Lee County Property Appraiser** (Matthew H. Caldwell): for housing data and parcel-level FMB residential statistics.
- **Royal Palm Coast Realtor Association (RPCRA):** publishes Lee County housing reports but FMB-specific cuts likely require direct request.
