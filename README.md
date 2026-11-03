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
@article{tu2025length,
  title   = {Length-Preserving Vessel Trajectory Simplification With
             Controllable Compression-Precision Bound},
  author  = {Tu, Enmei and Xie, Zhiye and Xu, Xixia and Chen, Shuhang},
  year    = {2025},
  note    = {Preprint / manuscript}
}
```
