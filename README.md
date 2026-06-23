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
