# 2025-sharpe-ratio — Agent Index

## Repo Purpose
Sharpe Ratio Inference library from the paper "Sharpe Ratio Inference: A New Standard" (SSRN 5520741). Statistical backbone for performance measurement across the Newton pipeline.

## Key Functions (in functions.py)
| Function | What It Does |
|----------|-------------|
| probabilistic_sharpe_ratio() | Is this Sharpe statistically significant? |
| minimum_track_record_length() | How many months to trust this? |
| critical_sharpe_ratio() | What Sharpe beats luck given K trials? |
| sharpe_ratio_variance() | Confidence interval (accounts for skew/kurtosis) |
| expected_maximum_sharpe_ratio() | Max Sharpe from luck alone |
| effective_rank() | True independent strategy count from correlation matrix |
| number_of_clusters() | Optimal clustering for multiple testing correction |
| control_for_FDR() | FDR-controlled strategy selection gate |

## Quick Usage
```python
from functions import probabilistic_sharpe_ratio, minimum_track_record_length
psr = probabilistic_sharpe_ratio(SR=0.5, SR0=0, T=252, gamma3=-0.5, gamma4=4.0)
```
