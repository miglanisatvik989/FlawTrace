# FlawTrace

Academic research on industrial surface defect detection and bounding-box localization using Python/PyTorch, existing model implementations, and pretrained weights.

Phase I is due **2026-10-31** (two days from project setup on 2026-10-29). This scaffold establishes the research workflow; it contains no training or evaluation implementation.

## Status and direction

- Dataset and exact detector: **undecided**.
- Baseline: an established pretrained detector, fine-tuned on the selected industrial dataset.
- Research question: how do whole-image and tiled inference compare, including a higher-resolution whole-image control?
- Training settings: **undecided**. Training, evaluation, and results: **not started**.
- Python and libraries supersede earlier C++ and manual-backpropagation requirements; see [decisions](docs/decisions.md).

Read [SIRP 2.0](RESEARCH_STANDARD.md), the [charter](docs/project_charter.md), [Phase I plan](docs/phase1_plan.md), and [current progress](docs/progress.md).

## Local setup

Available at setup: system Python **3.14.4**, alternative Python **3.12.14**, Git **2.53.0**, uv **0.12.5**. The intended scaffold environment uses Python **3.12.14**:

```sh
uv venv --python python3.12 .venv
uv pip install --python .venv/bin/python -e .
.venv/bin/python -c "import flawtrace; print(flawtrace.__file__)"
```

The package has no runtime dependencies yet. Installation uses setuptools as its build backend. No environment lock exists, and end-to-end reproducibility has not been verified.

Hardware observed through `nvidia-smi`: NVIDIA GeForce RTX 5050 Laptop GPU, **8151 MiB** reported VRAM, driver **610.74**. PyTorch/CUDA are not installed by this project. Before choosing their versions, verify official compatibility across the chosen detector, Python, torch/torchvision, driver, CUDA runtime, and GPU architecture, then validate an actual GPU operation. Driver visibility alone does not prove framework compatibility.

## Repository layout

- `src/flawtrace/`: installable Python package; no model implementation yet.
- `configs/`: small, versioned experiment configurations once decisions are approved.
- `data/`: dataset documentation and small manifests; raw data stays untracked.
- `experiments/<run_id>/`: **single location for all run outputs**, including predictions, checkpoints, logs, summaries, and recovered artifacts. See [artifact policy](experiments/README.md).
- `docs/`: scope, plans, progress, decisions, and source attribution.

Do not download datasets, train, or build an interface during scaffold setup. The next task is evidence-based dataset and pretrained-detector selection.
