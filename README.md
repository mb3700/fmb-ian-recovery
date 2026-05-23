# Fort Myers Beach Hurricane Ian Recovery Dashboard

Tracks the measurable signals of Fort Myers Beach's recovery from Hurricane Ian, with transparent methodology and sourced pre-Ian baselines. Built in the framework first developed for the Sanibel Solutions recovery dashboard.

**Live site:** https://fmb-ian-recovery.vercel.app
**Methodology:** [methodology.html](methodology.html)

> **Refresh in progress (requested May 23, 2026):** FMB-specific FY26 Q1 (Oct–Dec 2025) bed tax data has been requested from the Lee County Clerk of Court via the FMB Chamber of Commerce. Dashboard will be updated when figures are received. Current bed-tax data is FY25 YTD through August 2025.

## Snapshot (Q1 2026)

- **Lodging capacity: 66% recovered** (4,159 of 6,263 pre-Ian rooms — FMB Chamber, March 2026)
- **Bed tax revenue: 48% recovered** (FY25 YTD vs FY22 YTD — Lee County Clerk of Court)
- **877 lodging units in development** across 9 confirmed projects (665 hotel + 212 VR); 2 projects pending plans; 15 residential units tracked in a separate housing pipeline (verified May 23, 2026)
- **816 rooms permanently lost** (17 destroyed hotels + 226 VR rooms)
- **Watchlist:** 160 delinquent VR licenses, 3 of 7 cafés temporarily closed

## What's in the repo

```
.
├── index.html             — main dashboard
├── methodology.html       — methodology and data sources (linked from dashboard)
├── styles.css             — visual styling
├── data/
│   └── metrics.json       — single source of truth for all metric values
├── recovery-summary.md    — methodology in markdown form
└── images/                — placeholder for hero image
```

Pure static HTML/CSS — no build step, no JavaScript framework. Deploys cleanly to any static host (Vercel, Netlify, GitHub Pages).

## Data sources

1. **Lodging capacity (primary):** Fort Myers Beach Chamber of Commerce, Accommodations file (March 18, 2026)
2. **Bed tax revenue:** Lee County Clerk of Court, Tourist Development Tax breakdown by municipality (FY22–FY25 YTD)
3. **Business inventory:** FMB Chamber Community Dashboard project Q1 2026 business database
4. **Population:** US Census Bureau QuickFacts + 2024 American Community Survey

## Methodology

Adapted from the Sanibel Solutions recovery framework. Five rules:

1. Compare each metric to its pre-Ian baseline where verifiable.
2. Cap recovery at 100% — exceeding baseline counts as fully recovered.
3. Mark "baseline pending" when data is unverified; don't fabricate.
4. Exclude inverse indicators (e.g., real-estate listing volume).
5. Surface leading indicators (delinquent VR licenses, café closures) as watchlist, not headline.

Full methodology details: [methodology.html](methodology.html)

## Update cadence

Quarterly. Each update refreshes current values and revises pre-Ian baselines as Lee County and Town of FMB data becomes available.

## License

Data is sourced from public records and reproduced under fair-use for civic transparency. Visual framework and methodology adapted from Sanibel Solutions with attribution.

## Contact

Prepared by Mark Bole · FGCU Ain Technology and Design Hub
