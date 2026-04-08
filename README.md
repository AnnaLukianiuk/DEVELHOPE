# 📊 Superstore Sales Analysis

## Dataset

**File:** `Sample_-_Superstore.csv`  
**Source:** https://www.kaggle.com/datasets/vivek468/superstore-dataset-final  
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

1. **Discounts are the #1 profit killer.** The correlation heatmap confirms a strong negative relationship between discount rates and profit margins. This data suggests that the current discount policy is unsustainable and should be revisited urgently to protect the company's bottom line.

2. **The West region is the most profitable.** The West is the most profitable region overall, driven by its dominance in the Consumer and Corporate segments. While the East generates comparable revenue and leads in the Home Office segment, the West's superior performance in the larger segments ensures its position as the top profit contributor.

3. **The Central region underperforms.** Central shows the lowest total profit and may benefit from targeted promotions, pricing adjustments, or a review of the product mix.

4. **Technology has the best profit margin.** While Furniture and Office Supplies generate significant revenue, Technology products produce the highest absolute profit. Investing in Technology inventory and marketing is likely to yield the best ROI.

5. **Furniture is consistently loss-prone.** Several Furniture sub-categories (notably Tables and Bookcases) generate significant losses. The combination of high discounts on Furniture items is a key driver.

6. **Revenue is highly seasonal.** There is a clear spike in Q4 (November–December) every year. The company should plan inventory, logistics, and staffing to meet this seasonal demand.

7. **Sales distribution is heavily right-skewed.** The median order value is significantly lower than the mean, confirming a heavily right-skewed distribution. A small fraction of high-value orders drives a disproportionate share of total revenue, making the retention of top-tier customers a strategic priority.

8. **Consumer segment drives the most orders.** Consumers represent the largest order volume, but Corporate customers tend to have higher average order values - a useful segmentation for targeted sales efforts.

9. **18.7% of all transactions are loss-making.** Nearly 1 in 5 orders generates a negative profit, often correlated with high discount rates. Identifying and managing these orders could immediately improve overall profitability.

10. **Quantity alone does not predict profit.** The near-zero correlation between Quantity and Profit indicates that selling more units per order does not reliably increase profit - product mix and discount rate matter far more.

---

## Libraries Used

| Library | Purpose |
|---|---|
| `pandas` | Data loading, cleaning, grouping, aggregation |
| `numpy` | Numerical operations, correlation, regression line |
| `matplotlib` | Base plotting (histograms, bar charts, line charts, scatter) |
| `seaborn` | Correlation heatmap and theme styling |

---
