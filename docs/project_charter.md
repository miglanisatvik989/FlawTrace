# Project charter

FlawTrace is an academic research project for industrial surface defect detection and bounding-box localization using Python/PyTorch and existing model implementations with pretrained weights.

The baseline will fine-tune an established pretrained detector on a selected industrial dataset. Dataset, model, training settings, and evaluation metrics remain undecided. No training, evaluation, or results exist.

The research direction compares whole-image versus tiled inference, including a higher-resolution whole-image control. The hypothesis is that tiling may improve localization of small defects at a resource/latency cost; this is untested. Freeze the comparison protocol and protected test procedure before evaluation, accounting for compute, input resolution, tile boundaries, and box merging.

Phase I is due 2026-10-31, two days after setup. Its scope is a credible proposal: problem framing, attributed dataset/model shortlist, environment compatibility assessment, and a bounded experiment protocol. Deliver evidence and unresolved questions; do not promise experimental results within the scaffold step.

Use SIRP 2.0. Earlier C++ and manual-backpropagation requirements are explicitly superseded by the approved Python/library-first direction. Do not build neural-network components from scratch. Interfaces, infrastructure expansion, dataset downloads, and training are outside initial setup.
