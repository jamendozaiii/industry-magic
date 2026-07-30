# Industry Magic

A Google Sheets–based tool for generating **industry benchmark comparisons** used in Executive Business Reviews (EBRs). Given a company, an industry, and a time period, it produces a formatted comparison table — the customer vs. the industry average vs. two peer companies — ready to drop into an EBR deck.

> **Note on data:** This repository documents the *methodology and structure* only. All company names, account IDs, and figures in the examples are fictional. No customer data or internal file links are included.

## What it does

The tool turns raw quarterly social/digital-presence metrics into a single, decision-ready comparison table. For a chosen **Main Org** (the customer), it shows how they stack up against:

- the **Industry Average** for their sector,
- **Company A** and **Company B** (two named peers), and
- optionally, the **change vs. a prior period** (quarter-over-quarter or year-over-year).

The output is a clean table an account team copies straight into the customer's EBR slide.

## How it's structured

The workbook has six tabs:

| Tab | Visibility | Purpose |
|-----|-----------|---------|
| **Operations** | Editable | The control panel — pick parameters and tick which metric rows you want. |
| **Report - Change Incl** | Output | Comparison table *with* period-over-period change deltas (Option 1). |
| **Report - No Change** | Output | Comparison table *without* deltas (Option 2). |
| **Operation Lists** | Hidden | Backing lists for the Operations dropdowns. |
| **Org Lists** | Hidden | Master list of orgs/accounts available for selection. |
| **References** | Hidden | Lookup tables that drive the calculations. |

## Parameters

Set these on the **Operations** tab:

1. **Industry** — sector to benchmark against (e.g. Life, Wealth, B2B, P&C, Asset Management, Commercial Banking, Retail Banking, Mortgage, Recruiting, and regional variants).
2. **Year** — reporting year (kept current each quarter).
3. **Quarter** — Q1–Q4.
4. **Comparison Type** — `Quarterly` (vs. the previous quarter) or `Yearly` (vs. the same quarter last year).
5. **Main Org** — the customer being reviewed.
6. **Company A** — first peer to compare against.
7. **Company B** — second peer to compare against.

## Metrics

Metrics are grouped into three themes. Tick the rows you want on the Operations tab.

**Strengthening Presence**
- Workspaces
- Social Accounts per workspace
- Connections per workspace
- Average Facebook / Instagram / LinkedIn / Twitter Connections

**Publishes and Engagements**
- Quarterly Publishes per workspace
- Monthly Publishes per workspace
- % of original publishes per workspace
- Overall engagement rate
- Facebook / Instagram / LinkedIn / Twitter engagement rate

**Creating Touchpoint Opportunities**
- Received Private Messages per Workspace
- Sent Private Messages per Workspace

## Quick start

1. Open the **Operations** tab.
2. Choose the seven parameters above.
3. Tick the checkbox for each metric row you need.
4. Decide whether you want change deltas — use **Report - Change Incl** if yes, **Report - No Change** if not.
5. Copy the generated table from the chosen Report tab.
6. Paste and format it on the EBR deck.

See [`docs/sop.md`](docs/sop.md) for the full step-by-step and [`docs/example-output.md`](docs/example-output.md) for a worked example. For how it was done manually — with a sanitized sample workbook and a sample output slide — see [`docs/source-spreadsheet.md`](docs/source-spreadsheet.md).

## Background

Industry averages are produced upstream from raw quarterly exports (per-workspace breakdowns, publishing data, and social-account directories) that are aggregated per industry. Industry Magic consumes those aggregates and handles the selection, comparison, and formatting for EBRs.

## License

[MIT](./LICENSE)
