# Investor Conviction Radar & Investment Intelligence (v3.0 Institutional)

An institutional-grade, zero-dependency financial web terminal that tracks recent investments made by notable investors and U.S. government officials, normalizes transaction sizes relative to estimated net worth into a **Conviction Ratio**, and provides real-time deal scanning.

---

## Visual Design Architecture (v3.0)

Designed specifically for fintech professionals and quantitative research analysts:
* **Predominantly Greyscale / Monochrome Foundation**: Engineered around matte charcoal (`#090a0d`), deep slate (`#111317`), hairline zinc borders (`#20242c`), and high-contrast typography (`Inter` + `JetBrains Mono` with `tabular-nums` for numeric alignment).
* **Elimination of "AI Artifacts"**: Zero rainbow gradients, neon glow drop-shadows, blurred glass card clutter, or cartoon emojis. All components use crisp, purposeful SVG micro-icons.
* **Semantic Color Signposting**: Colors are reserved exclusively to signpost high-priority analytical signals and common use patterns:

### 1. Conviction & Sizing Signals
* <span style="color:#34d399">■</span> **High Conviction ($\ge 5.0\%$) — Financial Emerald**: Signposts outsized portfolio concentration where the investor puts substantial capital on the line (e.g. Ackman's Uber position, Pelosi's call options, Crenshaw's Amazon allocation). High-conviction rows are emphasized with a discrete left green indicator.
* <span style="color:#38bdf8">■</span> **Strategic Allocation ($1.0\% - 4.99\%$) — Steel / Cobalt Blue**: Standard institutional core position sizing.
* <span style="color:#fbbf24">■</span> **Standard Position ($0.2\% - 0.99\%$) — Muted Amber**: Broad baseline holding or diversification stake.
* <span style="color:#71717a">■</span> **Toehold / Minor Stake ($< 0.2\%$) — Zinc Grey**: Exploratory or low-impact allocation.

### 2. Regulatory Channel Signposting
* **Congressional STOCK Act Filings**: Distinct Slate-Indigo tag (`STOCK Act PTR` with landmark icon) to immediately differentiate legally mandated legislative disclosures from Wall Street funds.
* **Institutional 13F / 13D**: Discrete zinc tag (`SEC 13F` with document icon).
* **Private / Growth Rounds**: Discrete dark slate tag.

### 3. Instrument & Structural Flags
* **Call Options & Leverage**: Amber badge (`CALL LEVERAGE`) alerting the user to derivative leverage vs direct equity holdings.

---

## Formula

$$\text{Conviction Ratio} = \left(\frac{\text{Disclosed Nominal Investment Amount}}{\text{Estimated Investor Net Worth}}\right) \times 100\%$$

---

## How to Run

Simply double-click `index.html` or run in PowerShell:
```powershell
Start-Process "C:\Users\morgh\.gemini\antigravity\scratch\investor-radar\index.html"
```

*(Note: Previous legacy version is preserved at `index_v2_legacy.html`)*.

---

## Core Capabilities

1. **Live Internet & Wire Scanner**: Scans open financial wire and news APIs to extract and normalize disclosed transactions for tracked entities.
2. **Entity Ingestion & Tracking**: Track custom investors, family offices, or politicians with automated profile lookups and net worth heuristics.
3. **Institutional Telemetry Strip**: High-density financial metrics including Active Capital Monitored, Mean Conviction Index, and Peak Concentration Bet.
4. **Sizing & Allocation Simulator**: Benchmark hypothetical trade sizes against notable investors.
5. **Data Export**: 1-click export to formatted CSV for Excel, Python/pandas, or R workflows.
6. **Zero Dependencies & Local Persistence**: Self-contained single file that runs in any browser without Node, npm, build steps, or external servers.
