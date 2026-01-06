🇬🇧 English | [🇷🇺 Русская версия](README.md)



## 🇬🇧 English Version

# A/B Test Analysis: Cookie Cats Retention

## Project Overview
This project analyzes an A/B test in the mobile game **Cookie Cats**, where the product team tested a gameplay change and evaluated its impact on user retention.



## Hypothesis

The change in user experience impacts player retention.



## Metrics

**Primary Metric:**
- `retention_7` — 7-day user retention

**Secondary Metrics:**
- `retention_1` — 1-day retention
- `sum_gamerounds` — player engagement



## Data Summary
- **Total players:** 90,189  
- **Groups:**  
  - `gate_30` — control  
  - `gate_40` — test  
- Source: public Cookie Cats A/B dataset



## Analysis Steps

1. Data check (unique users, no missing/duplicates)
2. Group balance check
3. Compute retention and effect sizes
4. Chi-square significance testing
5. Bootstrap confidence intervals
6. Outlier trimming for robustness checks



## Key Results

| Metric | Control | Test | Absolute Diff | Relative Diff |
|--------|---------|------|---------------|----------------|
| retention_1 | 44.82% | 44.23% | -0.59 pp | -1.32% |
| retention_7 | 19.02% | 18.20% | -0.82 pp | -4.31% |

**Statistical significance:**  
- `retention_7`: p = 0.00160 (significant)  
- `retention_1`: p = 0.07550 (not significant)

**Bootstrap 95% CI for difference:** [-1.33 pp, -0.32 pp]

**Robustness:** Results hold after trimming top 1% of gamers.



## Conclusion

The test version negatively affects 7-day retention.  
Recommendation: **do not roll out the change as is.**



## Tools
- Python, Pandas, NumPy, SciPy, Seaborn/Matplotlib
- Jupyter Notebook
