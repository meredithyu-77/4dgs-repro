# 4dgs-repro

Reproducing **4D Gaussian Splatting** (Wu et al., CVPR 2024) from zero background — a 19-day build log (Oct 12–30, 2026).

> Built by an Applied Math senior learning 3D vision hands-on: cloud GPU (Kaggle T4) + Colab, starting from the official `hustvl/4DGaussians` implementation.

## What this is

A working 4D reconstruction pipeline: multi-view images → trained 4D Gaussians → novel-view video renders, with measured quality metrics and one ablation study.

## Metrics

| Scene (D-NeRF) | PSNR ↑ | SSIM ↑ | LPIPS ↓ | FPS |
|---|---|---|---|---|
| Lego | — | — | — | — |
| Hook / Bouncing Balls | — | — | — | — |

*(filled in as training runs complete; evaluation protocol follows the 4DGS paper)*

## Ablation

TBD — one controlled variable change with measured effect (e.g. iteration count vs. PSNR).

## Build log

- **Day 1 (Oct 13):** Environment ready — Kaggle T4 ×2 verified via `nvidia-smi`; repo created; official 4DGaussians Colab demo ran end-to-end (Lego scene), first render video saved.
- **Day 2 (Oct 14):** PyTorch crash course (tensor / autograd / gradient descent); bouncingballs training blocked — `diff-gaussian-rasterization` failed to build on a fresh Colab runtime (environment issue, debugging after midterms).

## Papers

1. 3D Gaussian Splatting — Kerbl et al., SIGGRAPH 2023 (foundation, in reading)
2. 4D Gaussian Splatting — Wu et al., CVPR 2024, arXiv:2310.08528 (target)
3. 4C4D — CVPR 2026 (follow-up, skim)
