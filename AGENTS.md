# Project guidance

This repository is data only: datasets. Do not add code, tests, CI or servers here.

New data files are JSONL. Keep synthetic/AI-drafted content explicitly marked
(`verified: false`, `source`) and distinct from human-verified data. Data
goes under `data/` by layer: `layer_1_specialist`, `layer_2_everyday`, `layer_3_synthetic`.
Earlier material and history are in `gee842/aceh-nlp-dataset` at tag `evidence-20261103`.
Never commit secrets, personal data, raw ratings or uploaded user datasets.
