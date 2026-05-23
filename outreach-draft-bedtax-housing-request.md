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
> Thanks for the accommodations file you shared in March — the Chamber's hotel and VR room counts are now the primary lodging source on the [FMB Recovery Dashboard](https://fmb-ian-recovery.vercel.app), which I've shared with London Bay for review and want to refresh ahead of any wider Chamber discussions.
>
> Two specific data refreshes would tighten the dashboard substantially:
>
> **1. Bed tax — FMB-specific FY26 Q1 (October–December 2025).**
> The dashboard currently shows FY25 YTD-through-August data from the file you provided. The Lee County Clerk's publicly-published TDC reports contain only county aggregates (which makes sense given the statutory confidentiality of TDT returns). To extend the 4-year recovery trajectory — 15% → 37% → 48% — into FY26, we'd need the FMB-specific Oct, Nov, Dec 2025 collections in the same format as the spreadsheet you sent through August. The format I'm working from is *Tourist Tax Breakdown - Add'l needed - Data through August 2025.xlsx.*
>
> **2. Pre-Ian housing baseline (2022 monthly residential closing counts on FMB).**
> The dashboard's Housing Market section currently shows year-over-year growth — Feb 2026 closings (44) were up 69% over Feb 2025 (26); December 2025 (37) was up 68% over December 2024 (22). These come from Redfin's FMB-specific reporting. To compute a Sanibel-style "Housing Recovery %" against the right baseline, we'd need 2022 (pre-Ian) monthly closing counts for FMB residential properties. RPCRA or the Lee County Property Appraiser is presumably the right source. If there's a member of your team or a board contact who pulls that, even a single year of 2022 monthly counts would be enough.
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
- New numbers will go into the bed-tax trajectory chart, the sister-city comparison table, and (for housing) a new "FMB Housing Recovery %" computation in the Housing Market section.

## Alternative contacts if Jacki can't deliver

- **Lee County Clerk of Court Inspector General Department:** 239-533-2190 (cited in their TDT FAQ as the contact for non-public data inquiries).
- **Lee County Property Appraiser** (Matthew H. Caldwell): for housing data and parcel-level FMB residential statistics.
- **Royal Palm Coast Realtor Association (RPCRA):** publishes Lee County housing reports but FMB-specific cuts likely require direct request.
