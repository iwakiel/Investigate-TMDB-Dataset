# Investigate: TMDB Movie Dataset

Exploratory data analysis of ~10k movies from The Movie Database (TMDB):
data cleaning, transformation, and trend analysis with pandas in Jupyter.

## Questions investigated

- Which genres are associated with higher revenue and popularity?
- How have production volume and budgets shifted over the decades?
- Do bigger budgets actually predict bigger returns?

## Approach

1. **Cleaning** — dropped duplicates, handled zero-budget/zero-revenue rows
   (recorded as 0 rather than NaN in the source — silently poisonous for
   averages if left in), parsed multi-value genre fields.
2. **Transformation** — inflation-adjusted budget/revenue columns, decade
   bucketing, genre explosion for per-genre aggregates.
3. **Analysis** — grouped aggregations and visualizations (matplotlib) per
   question, with the reasoning written inline in the notebook.

## Files

| File | Purpose |
|---|---|
| `P1 - investigate-a-dataset.ipynb` | Main analysis notebook |
| `P1 - investigate-a-dataset.html` | Rendered read-only version |
| `tmdb-movies.csv` | Source dataset |

## Honest limitations

Correlation-only analysis (no causal claims), the zero-revenue handling
discards rather than imputes, and popularity is TMDB's opaque metric — noted
in the notebook where it matters. An early project, kept public as the
starting point of the arc; my current data-engineering work is in my newer
repositories.
