# Phase I plan

Setup date: **2026-10-29**. Phase I deadline: **2026-10-31** (Asia/Calcutta calendar dates).

## Day 1 — 2026-10-29

- Establish and verify this minimal Python research scaffold.
- Proposed next task: research a small dataset/model shortlist using primary sources; assess industrial relevance, bounding-box annotations, licenses, official implementations/pretrained weights, and feasibility on the observed RTX 5050 Laptop GPU (8151 MiB VRAM).
- Check official Python/PyTorch/torchvision/CUDA/driver/GPU compatibility before proposing exact versions. Python 3.12.14 is available for the initial package environment; system Python is 3.14.4. No training framework compatibility is established yet.

## Day 2 — 2026-10-30; review by 2026-10-31

- Propose dataset and established pretrained baseline for approval, with citations and explicit tradeoffs.
- Define immutable splits/leakage checks, protected test handling, detection metrics/IoU criteria, seeds, and artifact records.
- Specify whole-image and tiled inference plus a higher-resolution whole-image control, fair settings, tile-to-image coordinate mapping/box merging, timing protocol, and VRAM reporting.
- Prepare the Phase I problem statement, related-work notes, method proposal, comparison table template, risks, and bounded follow-up schedule.

## Exit criteria and current status

Scaffold setup ends after install/import and Git checks, diff review, commit, and normal push. Dataset/model decisions, training configuration, metric selection, downloads, training, evaluation, and results are **not started or undecided**. Phase I proposal completion is a later task; do not infer it from scaffold completion. No downloads, training, or interface work are authorized in this step.
