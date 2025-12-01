# music-transformer-music-prediction

I'll create a short todo plan and then draft the README text for you to paste or save.

Starting: Draft README text (1/2)

Below is a ready-to-use README text. Tell me if you want me to write it to README_UPLOAD.md in the folder and/or commit & push it to GitHub.

README (draft for upload)

Project: MusicTransformer (modified copy)

Source: Based on jason9693/MusicTransformer-tensorflow2.0 (MIT License).
Copyright: Copyright (c) 2019 Kichang-Yang — retained in the LICENSE file.
What this folder contains:

A modified copy of the MusicTransformer codebase adapted to run locally and with updated defaults. It may include trained model weights and example MIDI files (see dataset).
Modifications & notes (summary)

TF/Keras imports: Uses internal TF imports like from tensorflow.python import keras and tensorflow.python.keras.optimizer_v2 to work with TF2 alpha/beta compatibility (see model.py, data.py, custom/*).
Script defaults: Changed default dataset and output paths in train.py and generate.py (e.g., dataset path set to dataset/processed, changed default --save_path and --load_path), and generate parameter defaults (beam defaulted to None).
Argument types: --beam handled as an int in generate.py (upstream used string 'None' in places).
Example inputs: generate.py uses local MIDI sample(s) by default and prints generation outputs for quick tests.
Added files/data: There are local extras not present in the original upstream (e.g., midi_processor1, additional MIDI files under dataset).
Other: Small API/signature tweaks and housekeeping changes across custom, deprecated, utils.py, preprocess.py, and params.py.
If any of these summaries are incorrect, tell me which files you changed and I’ll update the summary.

How to run (examples)

Preprocess MIDI into pickles (adjust paths as needed):
Train (example):
Generate:
Quick test (run the notebook):
Dependencies

See requirements.txt — this copy targets TensorFlow 2.x (the original used TF2 beta/nightly builds). Keep Python/TensorFlow versions compatible with the pinned requirements.
License & attribution (required)

This project is distributed under the MIT License. You must preserve the LICENSE file and the copyright notice:
Copyright (c) 2019 Kichang-Yang
If you upload this repository to GitHub, keep the LICENSE file at the repo root and do not remove or alter the original copyright attribution.
Data, privacy and redistribution notes

Some MIDI files in dataset may be copyrighted. Check dataset source terms before redistributing MIDI files or trained weights derived from copyrighted datasets.
If you plan to publish trained weights, state the license for the weights and list the datasets used to train them.
Suggested short attribution text to place at top of your GitHub README

"This repository is a modified copy of jason9693/MusicTransformer-tensorflow2.0 (MIT). I adapted the code for local TF2 compatibility, updated defaults, and trained the model on [dataset name]. Original copyright retained."
Options I can do next

Add this draft to your folder as README_UPLOAD.md (I can create and commit it).
Produce a concise NOTES.md enumerating every file that differs from upstream (I can auto-generate this from the diffs).
Provide exact git/PowerShell commands to create a new GitHub repo, add files, and push (with examples for preserving license and writing a commit message).
Would you like me to write this into README_UPLOAD.md and/or commit and push it for you?
