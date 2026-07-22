# Customer Churn Prediction & Business Analysis
**Tools:** Python, pandas, scikit-learn, Matplotlib  
**Dataset:** IBM Telco Customer Churn (7,032 customers, 21 features)

## Business Problem
A telecom company is losing customers but doesn't know which 
segments are at highest risk or why. This analysis identifies 
key churn drivers and delivers actionable retention 
recommendations backed by data.

## Key Findings
| Segment | Churn Rate |
|---|---|
| Month-to-month contracts | ~42% |
| Fiber optic internet users | ~41% |
| Customers in first 12 months | ~47% |
| Two-year contract customers | ~3% |

## Model Performance
| Model | Accuracy | F1 Score | ROC-AUC |
|---|---|---|---|
| Logistic Regression | 0.796 | 0.597 | 0.835 |
| Random Forest | 0.783 | 0.543 | 0.811 |

**Key insight:** Logistic Regression outperformed Random Forest 
on AUC (0.835 vs 0.811) — simpler model wins here.

## Business Recommendations
1. Offer discount to month-to-month customers at 3-month mark 
   to convert them to annual contracts
2. Investigate fiber optic service quality — high spend + 
   high churn signals a loyalty crisis
3. Implement 30-day and 90-day onboarding check-ins for 
   all new customers
4. Incentivize auto-pay to reduce electronic check churn

## Limitations
- Single company dataset — recommendations may not generalize
- No time-series data to track if interventions reduce churn
- Class imbalance (26.6% churn) affects minority class recall

## Files
- `File.ipynb` — full analysis notebook
- `churn_by_segment.png` — churn breakdown by segment
- `roc_curve.png` — model comparison
- `feature_importance.png` — top churn drivers
