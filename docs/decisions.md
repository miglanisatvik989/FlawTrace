# Decisions

## 2026-10-29 — approved scope and standard

- Project: FlawTrace, academic industrial surface defect detection and bounding-box localization.
- **Supersession:** the user's approved Python/PyTorch, existing-implementation, pretrained-weight approach replaces older C++ and manual-backpropagation requirements. Do not implement neural-network components from scratch.
- Adopt **SIRP 2.0**, a project-local revised Python/library-first standard retaining attribution, immutable splits, protected test evaluation, configurations/seeds, fair comparisons, honest results, and recoverable artifacts. Original older standard text is unavailable; no external accreditation is claimed.
- Baseline approach: fine-tune an established pretrained detector. Exact model, dataset, training settings, metrics, and framework versions remain undecided.
- Research direction: whole-image versus tiled inference with a higher-resolution whole-image control. No performance claim is established.
- Phase I deadline: 2026-10-31; initial setup is limited to scaffold, checks, commit, and normal push.
- Use an installable src-layout package with no runtime dependencies initially. Use available Python 3.12.14 for scaffold verification; this is not a verified PyTorch environment. No lock or reproducibility claim yet.
- Repository: clone the user-supplied empty GitHub repository into `/home/kaizen/code/FlawTrace`, establish `main`, and track `origin/main` on normal push. No prior history/files to preserve or combine.
- All run outputs go under `experiments/<run_id>/`; retain small records in Git and exclude bulk data/artifacts.
