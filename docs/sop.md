# Standard Operating Procedure — Industry Magic

How to generate an EBR industry comparison table from the Industry Magic workbook.

## Before you start

- Confirm the industry average data for the target **year and quarter** has been loaded (see "Data refresh" below).
- Know the three companies you're comparing: the **Main Org** (your customer) and **two peers** (Company A and Company B).
- Decide whether the slide needs **period-over-period change** shown (deltas) or just current values.

## Step-by-step

### 1. Set the parameters (Operations tab)

On the **Operations** tab, fill in the seven selection fields:

| Field | What to enter | Notes |
|-------|---------------|-------|
| Industry | The sector to benchmark against | Drives which Industry Average is used |
| Year | Reporting year | Must have data loaded for it |
| Quarter | Q1–Q4 | The "current" period |
| Comparison Type | `Quarterly` or `Yearly` | Quarterly = vs. prior quarter; Yearly = vs. same quarter last year |
| Main Org | The customer | Select from the org list |
| Company A | First peer | Select from the org list |
| Company B | Second peer | Select from the org list |

The tool resolves each org to its stored metrics and computes the industry average for the selected sector automatically.

### 2. Select the metric rows

Tick the checkbox next to each metric you want to appear in the output. Only ticked rows are written to the Report tabs, so you can tailor the table to what matters for that customer (for example, lead with engagement rates for a mature account, or presence metrics for a newer one).

### 3. Decide on comparison (change deltas)

- If the slide should show movement over time, you'll use the **Report - Change Incl** tab. It appends a signed delta to each value, e.g. `1571 (+100)`, comparing the current period against the prior period defined by your Comparison Type.
- If you only need current values, use the **Report - No Change** tab.

### 4. Copy the generated table

Open the chosen Report tab. The table is laid out with the four comparison columns:

```
                              | Main Org | Industry Average | Company A | Company B
```

and a `Date Range: Qx, YYYY` label. Select and copy the finished table.

### 5. Format on the EBR deck

Paste into the customer's EBR slide and apply the deck's table styling (fonts, header shading, column widths). Keep the column order Main Org → Industry Average → Company A → Company B so it reads consistently across decks.

## Comparison types explained

- **Quarterly** — compares the selected quarter to the immediately preceding quarter. Example label: `Q2-2026 vs. Q1-2026`.
- **Yearly** — compares the selected quarter to the same quarter in the prior year. Example label: `Q1-2025 vs. Q1-2024`.

## Data refresh (upstream)

Each quarter, the industry-average figures are rebuilt from raw exports before Industry Magic can be used for that period:

1. Pull the required per-account reports for the industry (per-workspace breakdown, publishing/posts data, and the social-account directory) for the target quarter.
2. Aggregate them per industry to produce the Industry Average row.
3. Load the refreshed averages and any new org metrics into the workbook's backing tables.

Once the target year/quarter is loaded, the selection steps above will produce accurate comparisons.

## Tips & gotchas

- **Keep column order consistent** across decks (Main Org, Industry Average, Company A, Company B).
- **Only tick rows you'll actually show** — a shorter table is easier to read on a slide.
- **Check the period label** matches the Comparison Type before copying.
- **Don't edit the hidden tabs** (Operation Lists, Org Lists, References) unless you're maintaining the tool — the Operations tab reads from them.
