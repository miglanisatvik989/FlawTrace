# Run artifacts

`experiments/<run_id>/` is the single location for all run outputs. No runs exist yet. Use a unique descriptive ID, for example `YYYYMMDDTHHMMSSZ_wholeimage_seedN`.

Git retains only deliberately small top-level run records named `config.yaml`, `config.json`, `manifest.json`, `metadata.json`, `summary.md`, or `summary.json`. Review their size and contents before staging. All other run contents are ignored, including checkpoints, generated predictions, logs, visualizations, and large evaluation outputs. Small reusable dataset manifests live in `data/manifests/`; reusable experiment configurations live in `configs/`.

For each run, record the source commit/dirty state, resolved settings, relevant seeds, dataset and split identities, model implementation/weights, actual environment and hardware, timestamps, status, metrics and limitations. Store generated files in appropriate subdirectories of the same run. Record checksums and durable storage/retrieval locations for excluded artifacts in `manifest.json`; validate recovery before claiming it. Never include credentials in these records. Follow the protected-test policy in SIRP 2.0.
