# 📊 Superstore Sales Analysis — Project README

## Dataset

**File:** `Sample_-_Superstore.csv`  
**Source:** Tableau Sample Superstore (widely used public analytics training dataset)  
**Size:** 9,994 rows × 21 columns  
**Coverage:** US retail orders across 4 regions, 3 product categories, multiple years

### Columns included
| Column | Description |
|---|---|
| Order ID / Order Date | Unique order identifier and date placed |
| Ship Date / Ship Mode | Fulfilment details |
| Customer ID / Name / Segment | Customer identity and market segment |
| Region / State / City | Geographic information |
| Category / Sub-Category / Product Name | Product hierarchy |
| Sales | Revenue for the line item ($) |
| Quantity | Units ordered |
| Discount | Discount rate applied (0–1) |
| Profit | Profit for the line item ($) |

---

## How to Run the Notebook

### Prerequisites
Make sure the following Python libraries are installed:

```bash
pip install pandas numpy matplotlib seaborn
```

### Steps

1. Place both files in the same directory:
   - `analysis.ipynb`
   - `Sample_-_Superstore.csv`

2. Launch Jupyter:
   ```bash
   jupyter notebook
   # or
   jupyter lab
   ```

3. Open `analysis.ipynb` and run all cells top-to-bottom:
   - **Kernel → Restart & Run All** (recommended for a clean run)

> ⚠️ The CSV must be in the same folder as the notebook, or update the path in the `pd.read_csv(...)` call in Section 1.

---

## Notebook Structure

| Section | Description |
|---|---|
| 1. Data Loading | Load CSV, display head, dtypes, missing value summary |
| 2. Data Cleaning | Parse dates, fix Postal Code type, derive Profit Margin |
| 3. KPI Calculation | Revenue, profit, margins, regional stats, monthly trend |
| 4. Data Visualization | 6 plots covering distributions, comparisons, correlations, trends |
| 5. Insights | 10 key findings and actionable recommendations |

---

## Main Insights

1. **Discounts destroy profit** — orders with >20% discount are frequently loss-making. Discount policy needs immediate review.
2. **West is the top-performing region** — highest profits across all customer segments.
3. **Central region underperforms** — lowest profitability; warrants strategic attention.
4. **Technology = best margin** — highest profit-to-revenue ratio among all categories.
5. **Furniture is loss-prone** — Tables and Bookcases regularly generate negative profit.
6. **Strong Q4 seasonality** — November–December revenue spikes every year; plan inventory accordingly.
7. **Sales are right-skewed** — median order ≈ $54 vs mean ≈ $230; a few large orders dominate revenue.
8. **~18% of orders are loss-making** — nearly 1 in 5 transactions generates negative profit.
9. **Corporate customers have higher average order values** — a priority segment for B2B sales strategy.
10. **Quantity ≠ Profit** — selling more units per order does not reliably increase profitability; product mix matters more.

---

## Libraries Used

| Library | Purpose |
|---|---|
| `pandas` | Data loading, cleaning, grouping, aggregation |
| `numpy` | Numerical operations, correlation, regression line |
| `matplotlib` | Base plotting (histograms, bar charts, line charts, scatter) |
| `seaborn` | Correlation heatmap and theme styling |

---

*Project completed as part of a Python & Data Analysis assignment.*
