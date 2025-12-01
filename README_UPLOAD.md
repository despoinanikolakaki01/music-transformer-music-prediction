# MusicTransformer — Modified copy (for upload)

This folder contains a modified copy of the MusicTransformer implementation originally published as `jason9693/MusicTransformer-tensorflow2.0`.

---

## Source & License

- Original project: `jason9693/MusicTransformer-tensorflow2.0` (MIT License).
- Copyright (c) 2019 Kichang-Yang — retained in the `LICENSE` file.

You must preserve the `LICENSE` file and the copyright notice when
redistributing this code.

---

## What this folder contains

- The MusicTransformer codebase adapted for local use and TF2 compatibility.
- Local additions and example files (for example, extra MIDI files under `dataset/`).
- Potentially trained model outputs or checkpoints (if present in `result*/` folders).

---

## Summary of modifications

- Reworked imports for TF2 compatibility (uses internal `tensorflow.python.keras` imports in some files).
- Adjusted script defaults and paths (`train.py`, `generate.py`, etc.).
- Changed some argument handling (e.g., `--beam` and default save/load paths).
- Added/updated local helper modules and example MIDI files.
- Minor API/signature tweaks in a few functions to suit local runtime and convenience.

Files with notable differences include: `model.py`, `data.py`, `train.py`, `generate.py`, `custom/*`, `utils.py`, `preprocess.py`, `params.py`, and documentation (`README.md`, `requirements.txt`).

If you want a precise per-file diff against the upstream source, I can generate that and include a `CHANGES.md`.

---

## How to run (examples)

Adjust these commands to match your environment and paths.

Preprocess MIDI into pickles:

```powershell
python preprocess.py dataset/midi dataset/processed
```

Train (example):

```powershell
python train.py --epochs 100 --pickle_dir dataset/processed --save_path result/dec0722 --max_seq 2048 --batch_size 2 --l_r 0.0001
```

Generate music (example):

```powershell
python generate.py --load_path result/dec0722 --length 2048 --beam 4 --save_path bin/generated.mid
```

Open the training notebook:

```powershell
jupyter notebook "music-transformer-train.ipynb"
```

---

## Dependencies

See `requirements.txt`. This fork was tested against TensorFlow 2.x family and uses some TF2 alpha/beta workarounds — ensure your Python and TensorFlow versions match the pinned dependencies for best results.

---

## Data, model weights, and redistribution notes

- Some MIDI files included may be copyrighted — check dataset terms before redistributing these files.
- If you publish trained weights, explicitly state the license under which you release them and list the datasets used to train the model.

---

## Attribution text (suggested for your GitHub README)

> Based on `jason9693/MusicTransformer-tensorflow2.0` (MIT License). Copyright (c) 2019 Kichang-Yang. Modified for TF2 compatibility and local use; trained model and changes by [Your Name].

---

If you want, I can:

- Create a `CHANGES.md` listing the exact diffs against the upstream repository.
- Insert this file into the repo and create a suggested commit message.
- Initialize a git repo and provide exact `git`/PowerShell commands to push to a new GitHub repo.

Tell me which of those you'd like next.
