# Length-Preserving Vessel Trajectory Simplification

Official implementation of **"Length-Preserving Vessel Trajectory Simplification With Controllable Compression–Precision Bound"** (Tu, Xie, Xu, Chen, 2026).

A dynamic-programming framework for AIS vessel trajectory simplification that explicitly optimizes **trajectory length** — a metric critical for fuel-consumption estimation, EEOI/CII carbon auditing, and voyage management — rather than only geometric shape.

---

## Overview

Existing simplifiers (RDP, ARDP, TD-TR, TDKC, SED-minimization) preserve visual shape but can silently discard large amounts of sailed distance, e.g. by collapsing out-and-back or loitering segments. This repository provides a **globally optimal, provably correct** DP formulation that directly controls the length-approximation error.

Two dual problems are solved within one unified framework:

| Mode | Given | Optimizes |
|------|-------|-----------|
| **CDS** — Compression-Driven Simplification | point budget `K` | minimizes length error `Δ(S)` |
| **PDS** — Precision-Driven Simplification | error tolerance `ε` (nmi) | minimizes number of retained points |

## Online Demo

We have implement a simple online application to demonstrate the algorithm. Please visit [http://153.92.209.120](http://153.92.209.120) 


## Citation

```bibtex
@article{TU2026128938,
title = {Length-preserving vessel trajectory simplification with controllable compression-Precision bound},
journal = {Ocean Engineering},
volume = {370},
pages = {128938},
year = {2026},
issn = {0029-8018},
doi = {https://doi.org/10.1016/j.oceaneng.2026.128938},
url = {https://www.sciencedirect.com/science/article/pii/S0029801826047724},
author = {Enmei Tu and Zhiye Xie and Xixia Xu and Shuhang Chen},
keywords = {Vessel trajectory simplification, Length preservation, Dynamic programming, AIS data}
}
```
