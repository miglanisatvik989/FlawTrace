# Working on FlawTrace

Before work, read `RESEARCH_STANDARD.md`, `docs/progress.md`, `docs/decisions.md`, and any instructions in the affected directories. Follow the approved Python/PyTorch, existing-implementation, pretrained-weight approach. Earlier C++ or manual-backpropagation instructions are superseded by SIRP 2.0.

Make bounded changes tied to the current task and two-day Phase I scope. Preserve existing files and uncommitted work. Do not implement neural-network components from scratch. Do not add speculative abstractions, placeholder training/evaluation code, meaningless tests, Docker, databases, tracking servers, web frameworks, or CI workflows.

Check framework, model, Python, CUDA, and GPU compatibility before choosing dependencies or installing PyTorch/CUDA. Never invent locks, results, citations, or reproducibility claims. Dataset, detector, and training settings remain undecided until recorded decisions establish them.

Follow SIRP 2.0 for attribution, immutable splits, protected test evaluation, seeds/configurations, fair comparisons, honest reporting, and recoverable artifacts. All run outputs belong under `experiments/<run_id>/`. Keep small configurations, manifests, summaries, and metadata version-controlled; keep raw data, weights, predictions, and large outputs out of Git.

Run checks relevant to each change, review the diff and ignored paths, and update `docs/progress.md` with changes, exact checks/outcomes, limitations, and the next task. Update `docs/decisions.md` and `docs/sources.csv` when decisions or sources change. Do not start downloads, training, or interface work without a task authorizing them.

Inspect remote history before connecting or combining repositories. Reuse authentication; never request credentials in chat. Never force-push, overwrite a different remote, or automatically merge unrelated histories. Commit only authorized task changes.
