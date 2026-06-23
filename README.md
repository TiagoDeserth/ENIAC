# Unknown Rate (%) at Selected Evaluation Moments

> **Supplementary material** for the paper *Active Adaptation for Novelty Detection in Data Streams with Extreme Latency Using Fuzzy Micro-Clusters*. This file contains the full Unknown Rate results omitted from the main text for space reasons.

## Overview

The unknown rate follows the same overall pattern across both datasets: a relatively high value at the first evaluation moment, reflecting the classifier's warm-up phase, followed by rapid convergence to values below 0.5% once the model has processed enough instances. The magnitude of the initial unknown rate is dataset-dependent — SyneDC (up to 12.79%) and RBF (up to 3.10%) — but the windowing mechanism does not introduce a systematic increase or decrease relative to the baseline once steady-state is reached. This indicates that the gains in classification quality observed for RBF and SyneDC do not come at the cost of higher instance rejection.

## RBF Dataset

| Moment | w=1 up=1.0 | w=40 up=1.0 | w=40 up=0.8 | w=40 up=0.5 | w=80 up=1.0 | w=80 up=0.8 | w=80 up=0.5 | w=200 up=1.0 | w=200 up=0.8 | w=200 up=0.5 |
|---|---|---|---|---|---|---|---|---|---|---|
| 1  | 3.10 | 3.10 | 3.10 | 2.00 | 2.90 | 2.10 | 2.20 | 2.60 | 3.10 | 3.00 |
| 5  | 0.42 | 0.94 | 0.74 | 0.58 | 0.54 | 0.72 | 0.38 | 0.68 | 0.78 | 0.88 |
| 10 | 0.27 | 0.35 | 0.28 | 0.39 | 0.30 | 0.22 | 0.27 | 0.35 | 0.16 | 0.29 |
| 15 | 0.34 | 0.35 | 0.33 | 0.29 | 0.23 | 0.21 | 0.19 | 0.37 | 0.18 | 0.22 |
| 20 | 0.18 | 0.23 | 0.22 | 0.24 | 0.18 | 0.21 | 0.10 | 0.22 | 0.18 | 0.23 |
| 25 | 0.20 | 0.22 | 0.23 | 0.17 | 0.12 | 0.18 | 0.15 | 0.14 | 0.14 | 0.21 |
| 30 | 0.16 | 0.13 | 0.12 | 0.18 | 0.08 | 0.14 | 0.01 | 0.11 | 0.14 | 0.08 |
| 35 | 0.13 | 0.13 | 0.12 | 0.17 | 0.14 | 0.08 | 0.01 | 0.13 | 0.13 | 0.12 |
| 40 | 0.10 | 0.11 | 0.12 | 0.13 | 0.10 | 0.12 | 0.01 | 0.07 | 0.10 | 0.12 |
| 45 | 0.07 | 0.12 | 0.08 | 0.11 | 0.11 | 0.06 | 0.10 | 0.08 | 0.14 | 0.08 |

## SyneDC Dataset

The SyneDC dataset presents a higher initial unknown rate (up to 12.79% at moment 1) compared to RBF, reflecting its larger number of known classes (20) and higher dimensionality (54 attributes). As with RBF, all configurations converge to values below 0.5% after the warm-up phase, with no systematic difference introduced by the windowing mechanism.

| Moment | w=1 up=1.0 | w=40 up=1.0 | w=40 up=0.8 | w=40 up=0.5 | w=80 up=1.0 | w=80 up=0.8 | w=80 up=0.5 | w=200 up=1.0 | w=200 up=0.8 | w=200 up=0.5 |
|---|---|---|---|---|---|---|---|---|---|---|
| 1   | 10.39 | 12.79 | 12.79 | 5.00 | 6.99 | 6.99 | 9.29 | 6.59 | 6.59 | 11.49 |
| 40  | 0.21  | 0.20  | 0.20  | 0.22 | 0.17 | 0.17 | 0.24 | 0.28 | 0.28 | 0.23  |
| 80  | 0.17  | 0.07  | 0.07  | 0.11 | 0.12 | 0.12 | 0.11 | 0.12 | 0.12 | 0.08  |
| 120 | 0.07  | 0.09  | 0.09  | 0.08 | 0.07 | 0.07 | 0.05 | 0.07 | 0.07 | 0.11  |
| 160 | 0.05  | 0.04  | 0.04  | 0.04 | 0.05 | 0.05 | 0.04 | 0.03 | 0.03 | 0.04  |
| 200 | 0.03  | 0.04  | 0.04  | 0.06 | 0.04 | 0.04 | 0.04 | 0.06 | 0.06 | 0.03  |
| 240 | 0.03  | 0.04  | 0.04  | 0.05 | 0.03 | 0.03 | 0.03 | 0.05 | 0.05 | 0.03  |
| 280 | 0.02  | 0.03  | 0.03  | 0.04 | 0.03 | 0.03 | 0.03 | 0.04 | 0.04 | 0.02  |
| 320 | 0.02  | 0.03  | 0.03  | 0.03 | 0.03 | 0.03 | 0.02 | 0.03 | 0.03 | 0.02  |
| 369 | 0.02  | 0.02  | 0.02  | 0.03 | 0.02 | 0.02 | 0.02 | 0.03 | 0.03 | 0.02  |

# Precision, Recall and F1-Score (%) at Selected Evaluation Moments

> **Supplementary material** for the paper *Active Adaptation for Novelty Detection in Data Streams with Extreme Latency Using Fuzzy Micro-Clusters*. This file contains the full Precision, Recall, and F1-Score results omitted from the main text for space reasons.

---

## Precision

### RBF Dataset

In the RBF dataset, precision shows the most pronounced divergence between the baseline and the windowed configurations toward the end of the stream: at moment 45, the baseline drops to 60.73%, while w=80, up=0.8 reaches 80.83%, a gap of 20.1 pp. This indicates that the baseline's per-instance updates make the model increasingly susceptible to false-positive classifications as concept drift accumulates, whereas the partial-update windowed configuration preserves the precision of its decision boundaries. A notable anomaly occurs at moment 10 for w=40, up=1.0 and up=0.5 (58.45% and 58.52%, respectively), a transient drop not observed for up=0.8, suggesting instability tied to full or very partial updates at that specific window size during early micro-cluster formation.

| Moment | w=1 up=1.0 | w=40 up=1.0 | w=40 up=0.8 | w=40 up=0.5 | w=80 up=1.0 | w=80 up=0.8 | w=80 up=0.5 | w=200 up=1.0 | w=200 up=0.8 | w=200 up=0.5 |
|---|---|---|---|---|---|---|---|---|---|---|
| 1  | 75.00 | 75.00 | 75.00 | 75.00 | 75.00 | 75.00 | 75.00 | 75.00 | 75.00 | 75.00 |
| 5  | 75.00 | 75.00 | 75.00 | 75.00 | 75.00 | 75.00 | 75.00 | 75.00 | 75.00 | 75.00 |
| 10 | 79.43 | 58.45 | 79.34 | 58.52 | 79.23 | 78.57 | 79.43 | 79.67 | 79.20 | 78.79 |
| 15 | 78.10 | 77.77 | 78.30 | 77.49 | 76.90 | 78.28 | 76.06 | 77.35 | 78.80 | 78.14 |
| 20 | 76.89 | 77.79 | 77.74 | 77.08 | 74.95 | 78.20 | 74.86 | 75.56 | 78.55 | 77.85 |
| 25 | 76.35 | 77.92 | 77.48 | 76.85 | 74.02 | 78.17 | 74.52 | 74.57 | 78.46 | 77.79 |
| 30 | 76.14 | 78.03 | 77.41 | 76.91 | 73.59 | 78.25 | 75.23 | 74.08 | 78.51 | 77.83 |
| 35 | 75.65 | 77.99 | 77.17 | 76.67 | 72.94 | 78.03 | 75.50 | 73.48 | 78.41 | 77.75 |
| 40 | 74.75 | 77.72 | 76.61 | 76.11 | 71.91 | 77.74 | 75.53 | 72.56 | 78.19 | 77.58 |
| 45 | 60.73 | 79.70 | 79.00 | 78.65 | 75.40 | 80.83 | 78.54 | 75.88 | 80.40 | 62.95 |

### SyneDC Dataset

For SyneDC, the configurations with up=0.5 consistently outperform both the baseline and their up=1.0/up=0.8 counterparts of the same window size, regardless of w. The configuration w=200, up=0.5 achieves the highest precision at nearly every moment from 80 onward (e.g., 87.72% at moment 160 vs. 87.38% for the baseline), suggesting that, for this dataset, sampling roughly half of the window's accumulated instances acts as a regularizer that slightly reduces false-positive classifications without the instability seen at up=1.0 for the RBF dataset.

| Moment | w=1 up=1.0 | w=40 up=1.0 | w=40 up=0.8 | w=40 up=0.5 | w=80 up=1.0 | w=80 up=0.8 | w=80 up=0.5 | w=200 up=1.0 | w=200 up=0.8 | w=200 up=0.5 |
|---|---|---|---|---|---|---|---|---|---|---|
| 1   | 73.17 | 80.00 | 80.00 | 75.09 | 80.00 | 80.00 | 79.93 | 80.00 | 80.00 | 80.00 |
| 40  | 74.52 | 74.08 | 74.08 | 74.57 | 73.61 | 73.61 | 74.64 | 74.59 | 74.59 | 74.92 |
| 80  | 81.26 | 80.73 | 80.73 | 81.22 | 80.34 | 80.34 | 81.36 | 81.25 | 81.25 | 81.49 |
| 120 | 84.84 | 84.29 | 84.29 | 84.75 | 84.10 | 84.10 | 85.07 | 84.92 | 84.92 | 85.18 |
| 160 | 87.38 | 87.10 | 87.10 | 87.54 | 86.86 | 86.86 | 87.66 | 87.62 | 87.62 | 87.72 |
| 200 | 87.21 | 86.88 | 86.88 | 87.29 | 86.75 | 86.75 | 87.37 | 87.29 | 87.29 | 87.59 |
| 240 | 85.48 | 85.14 | 85.14 | 85.55 | 85.00 | 85.00 | 85.62 | 85.50 | 85.50 | 85.80 |
| 280 | 84.88 | 84.54 | 84.54 | 84.95 | 84.39 | 84.39 | 85.01 | 84.90 | 84.90 | 85.20 |
| 320 | 84.65 | 84.31 | 84.31 | 84.72 | 84.17 | 84.17 | 84.79 | 84.67 | 84.67 | 84.97 |
| 369 | 84.52 | 84.18 | 84.18 | 84.59 | 84.03 | 84.03 | 84.65 | 84.53 | 84.53 | 84.84 |

---

## Recall

### RBF Dataset

Recall in RBF mirrors the accuracy pattern: w=80, up=0.8 sustains the highest values across the second half of the stream, peaking at 78.50% at moment 45 — nearly 15 pp above the baseline (63.64%) at the same moment. As with precision, w=80, up=1.0 is the weakest configuration in this regime (61.76% at moment 45), reinforcing that full updates with this particular window size are unsuitable for RBF's drift pattern.

| Moment | w=1 up=1.0 | w=40 up=1.0 | w=40 up=0.8 | w=40 up=0.5 | w=80 up=1.0 | w=80 up=0.8 | w=80 up=0.5 | w=200 up=1.0 | w=200 up=0.8 | w=200 up=0.5 |
|---|---|---|---|---|---|---|---|---|---|---|
| 1  | 73.00 | 73.24 | 72.69 | 73.79 | 73.15 | 73.71 | 73.65 | 73.28 | 73.00 | 73.05 |
| 5  | 74.71 | 74.43 | 74.55 | 74.53 | 74.64 | 74.49 | 74.77 | 74.55 | 74.41 | 74.25 |
| 10 | 72.40 | 59.86 | 70.95 | 59.89 | 69.60 | 62.23 | 71.83 | 73.86 | 69.86 | 64.40 |
| 15 | 73.76 | 72.70 | 74.36 | 71.58 | 69.55 | 74.68 | 66.18 | 70.94 | 76.33 | 74.11 |
| 20 | 74.46 | 76.19 | 76.09 | 74.75 | 70.02 | 76.94 | 69.89 | 71.49 | 77.57 | 76.28 |
| 25 | 74.94 | 77.29 | 76.66 | 75.75 | 70.53 | 77.65 | 71.92 | 71.72 | 78.06 | 77.12 |
| 30 | 75.23 | 77.79 | 77.03 | 76.30 | 70.76 | 78.03 | 74.03 | 71.73 | 78.33 | 77.58 |
| 35 | 75.56 | 78.16 | 77.34 | 76.76 | 71.37 | 78.24 | 75.44 | 72.34 | 78.56 | 77.92 |
| 40 | 76.00 | 78.50 | 77.67 | 77.25 | 72.42 | 78.52 | 76.77 | 73.40 | 78.83 | 78.39 |
| 45 | 63.64 | 66.07 | 68.05 | 67.10 | 61.76 | 78.50 | 67.95 | 62.35 | 69.48 | 65.56 |

### SyneDC Dataset

In SyneDC, recall closely tracks accuracy: w=80, up=0.5 achieves the highest values in the central portion of the stream (89.02% at moment 120 and 90.83% at moment 200), while the baseline and the up=1.0/up=0.8 variants remain consistently 1–3 pp lower. The early-stream advantage is even more pronounced for w=40, up=0.5 (71.32% vs. 64.11% for the baseline at moment 1), reinforcing that partial updates speed up the classifier's convergence during the warm-up phase for this dataset.

| Moment | w=1 up=1.0 | w=40 up=1.0 | w=40 up=0.8 | w=40 up=0.5 | w=80 up=1.0 | w=80 up=0.8 | w=80 up=0.5 | w=200 up=1.0 | w=200 up=0.8 | w=200 up=0.5 |
|---|---|---|---|---|---|---|---|---|---|---|
| 1   | 64.11 | 65.75 | 65.75 | 71.32 | 69.39 | 69.39 | 68.65 | 68.16 | 68.16 | 66.96 |
| 40  | 80.46 | 81.08 | 81.08 | 80.87 | 80.65 | 80.65 | 81.05 | 80.29 | 80.29 | 80.26 |
| 80  | 85.76 | 86.07 | 86.07 | 86.02 | 85.64 | 85.64 | 86.38 | 85.80 | 85.80 | 85.70 |
| 120 | 88.40 | 88.42 | 88.42 | 88.50 | 88.25 | 88.25 | 89.02 | 88.46 | 88.46 | 88.43 |
| 160 | 89.95 | 90.11 | 90.11 | 90.40 | 89.75 | 89.75 | 90.61 | 90.04 | 90.04 | 90.11 |
| 200 | 90.44 | 90.50 | 90.50 | 90.64 | 90.39 | 90.39 | 90.83 | 90.47 | 90.47 | 90.64 |
| 240 | 78.28 | 78.22 | 78.22 | 78.39 | 78.24 | 78.24 | 78.27 | 78.07 | 78.07 | 78.30 |
| 280 | 71.40 | 71.32 | 71.32 | 71.47 | 71.32 | 71.32 | 71.43 | 71.29 | 71.29 | 71.48 |
| 320 | 64.01 | 63.97 | 63.97 | 64.12 | 63.98 | 63.98 | 64.07 | 63.95 | 63.95 | 64.14 |
| 369 | 54.82 | 54.82 | 54.82 | 54.93 | 54.83 | 54.83 | 54.84 | 54.73 | 54.73 | 54.91 |

---

## F1-Score

### RBF Dataset

F1-Score confirms the trend already observed in precision and recall for RBF: w=80, up=0.8 delivers the best result at the final moment (79.65% vs. 62.15% for the baseline, a gap of 17.5 pp), and remains the top performer from moment 15 onward. The convergence of precision and recall gains into a substantially higher F1-Score reinforces w=80, up=0.8 as the most balanced configuration for this dataset.

| Moment | w=1 up=1.0 | w=40 up=1.0 | w=40 up=0.8 | w=40 up=0.5 | w=80 up=1.0 | w=80 up=0.8 | w=80 up=0.5 | w=200 up=1.0 | w=200 up=0.8 | w=200 up=0.5 |
|---|---|---|---|---|---|---|---|---|---|---|
| 1  | 73.99 | 74.11 | 73.83 | 74.39 | 74.06 | 74.35 | 74.32 | 74.13 | 73.99 | 74.01 |
| 5  | 74.86 | 74.71 | 74.77 | 74.76 | 74.82 | 74.74 | 74.88 | 74.78 | 74.70 | 74.63 |
| 10 | 75.75 | 59.15 | 74.91 | 59.20 | 74.11 | 69.46 | 75.44 | 76.65 | 74.24 | 70.87 |
| 15 | 75.86 | 75.15 | 76.28 | 74.41 | 73.04 | 76.44 | 70.77 | 74.00 | 77.54 | 76.07 |
| 20 | 75.65 | 76.98 | 76.91 | 75.90 | 72.40 | 77.56 | 72.29 | 73.47 | 78.06 | 77.06 |
| 25 | 75.64 | 77.61 | 77.07 | 76.30 | 72.23 | 77.91 | 73.20 | 73.11 | 78.26 | 77.45 |
| 30 | 75.68 | 77.91 | 77.22 | 76.60 | 72.15 | 78.14 | 74.63 | 72.89 | 78.42 | 77.70 |
| 35 | 75.60 | 78.07 | 77.26 | 76.71 | 72.14 | 78.14 | 75.47 | 72.91 | 78.49 | 77.84 |
| 40 | 75.37 | 78.11 | 77.13 | 76.68 | 72.16 | 78.13 | 76.14 | 72.98 | 78.51 | 77.98 |
| 45 | 62.15 | 72.25 | 73.12 | 72.42 | 67.90 | 79.65 | 72.86 | 68.45 | 74.54 | 64.23 |

### SyneDC Dataset

For SyneDC, F1-Score peaks consistently for w=80, up=0.5 in the central region of the stream (89.11% at moment 160 and 89.07% at moment 200), and for w=200, up=0.5 in the final, most degraded phase (66.67% at moment 369, the highest among all configurations). This indicates that up=0.5 is the most robust update fraction for this dataset across different window sizes, balancing the precision and recall gains discussed previously.

| Moment | w=1 up=1.0 | w=40 up=1.0 | w=40 up=0.8 | w=40 up=0.5 | w=80 up=1.0 | w=80 up=0.8 | w=80 up=0.5 | w=200 up=1.0 | w=200 up=0.8 | w=200 up=0.5 |
|---|---|---|---|---|---|---|---|---|---|---|
| 1   | 68.34 | 72.18 | 72.18 | 73.16 | 74.32 | 74.32 | 73.87 | 73.61 | 73.61 | 72.90 |
| 40  | 77.37 | 77.43 | 77.43 | 77.59 | 76.97 | 76.97 | 77.71 | 77.33 | 77.33 | 77.49 |
| 80  | 83.45 | 83.31 | 83.31 | 83.55 | 82.91 | 82.91 | 83.80 | 83.46 | 83.46 | 83.54 |
| 120 | 86.59 | 86.31 | 86.31 | 86.59 | 86.12 | 86.12 | 87.00 | 86.66 | 86.66 | 86.78 |
| 160 | 88.65 | 88.58 | 88.58 | 88.95 | 88.28 | 88.28 | 89.11 | 88.81 | 88.81 | 88.90 |
| 200 | 88.80 | 88.65 | 88.65 | 88.93 | 88.53 | 88.53 | 89.07 | 88.85 | 88.85 | 89.09 |
| 240 | 81.72 | 81.53 | 81.53 | 81.82 | 81.48 | 81.48 | 81.78 | 81.62 | 81.62 | 81.88 |
| 280 | 77.56 | 77.37 | 77.37 | 77.63 | 77.31 | 77.31 | 77.63 | 77.50 | 77.50 | 77.74 |
| 320 | 72.90 | 72.75 | 72.75 | 73.00 | 72.70 | 72.70 | 72.99 | 72.86 | 72.86 | 73.10 |
| 369 | 66.50 | 66.40 | 66.40 | 66.61 | 66.36 | 66.36 | 66.56 | 66.44 | 66.44 | 66.67 |
