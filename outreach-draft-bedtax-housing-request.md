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
> **2. Pre-Ian vs current housing data (RPCRA / SWFL MLS), split by property type.**
> The dashboard's Housing Market section has been rebuilt to mirror the format Sanibel uses on its recovery dashboard — current-month value vs same-month-2022 (pre-Ian) baseline, split by property type. Five cards in the grid: Residential Home Sales, Residential Listings, Condo Sales, Condo Listings, Vacant Lot Sales. Any month before October 2022 is a clean pre-Ian baseline because Ian made landfall September 28, 2022.
>
> The full-year context is already populated from Beach Talk Radio News (Jorge Barrera at Premiere Plus Realty, sourcing SWFL MLS) — for example, single-family closings went 192 (2021) → 179 (2023) → 70 (2024); condos went 401 (2021) → 232 (2022) → 197 (2023) → 166 (2024). What we still need are the **single-month figures** to populate the actual current-vs-pre-Ian comparisons:
>
>   - **Single-family closings**: most-recent-month (April or May 2026) AND the same month in 2022.
>   - **Single-family active listings**: most recent count (refresh of the May 2025 number of ~201) AND the same month in 2022.
>   - **Condo/villa/townhouse closings**: same — most-recent-month + same-month-2022.
>   - **Condo/villa/townhouse active listings**: same — refresh of May 2025 count (~316) + same-month-2022.
>   - **Vacant lot closings**: same — most-recent-month + same-month-2022.
>   - **Median sale price (YTD or current month)**: by property type if separable. Sanibel's analogous cards show median price YTD as the trend line.
>
> Even a partial pull (just the same-month-2022 baselines, since we have most current-side numbers) would let us complete every recovery percentage on the cards. The dashboard's "Data Decisions" page documents every pending request, so anything received is properly sourced.
>
> **Alternate channel — Jorge Barrera (Premiere Plus Realty):** If the RPCRA path is slow, Jorge Barrera at Premiere Plus Realty is the source the dashboard already cites — he compiles the SWFL MLS pulls that Beach Talk Radio News publishes. A direct ask to Barrera for the single-month figures above would close most of the gap without waiting on RPCRA. Happy to reach out to him directly if that helps.
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
  - The five housing cards (Residential Home Sales, Residential Listings, Condo Sales, Condo Listings, Vacant Lot Sales) — pre-Ian baseline and current-month values fill in the recovery percentages
  - The annual median sale price by type can fold into each sales card as the trend line (matches the Sanibel format)

## Alternative contacts if Jacki can't deliver

- **Jorge Barrera, Premiere Plus Realty:** 239-791-9893. Compiles the SWFL MLS pulls already published in Beach Talk Radio News. Most direct path to single-month closings + active listings by type.
- **Lee County Clerk of Court Inspector General Department:** 239-533-2190 (cited in their TDT FAQ as the contact for non-public data inquiries) — for bed tax only.
- **Lee County Property Appraiser** (Matthew H. Caldwell): for closed-sales data (deed transfers); does NOT have active MLS listings.
- **Royal Palm Coast Realtor Association (RPCRA):** publishes Lee County housing reports but FMB-specific cuts likely require direct request to marketing@rpcra.org.
