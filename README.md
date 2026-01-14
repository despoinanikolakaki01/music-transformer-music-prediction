# music-transformer-music-prediction
# Music Generation for [Music prediction and creation with using Deep Learning]

Based on the [Music Transformer implementation](https://github.com/jason9693/MusicTransformer-tensorflow2.0) by jason9693.

## About This Project

This folder contains a modified copy of the MusicTransformer implementation from `jason9693/MusicTransformer-tensorflow2.0` (MIT License), adapted for TensorFlow 2.x compatibility and local use with custom adjustments to imports, paths, and argument handling. The codebase includes preprocessed MIDI files, training scripts, and example utilities tailored for music generation tasks. All modifications preserve the original copyright (c) 2019 Kichang-Yang as specified in the LICENSE file. When redistributing this code, ensure proper attribution and preservation of the original license terms.

## Training Configuration

### Dataset
The model was trained on a subsest of the MAESTRO (MIDI and Audio Edited for Synchronous TRacks and Organization) dataset, comprising 1,600 classical piano performances. The dataset was partitioned following standard machine learning practices:
- **Training set**: 1,280 pieces (80%)
- **Validation set**: 160 pieces (10%)
- **Testing set**: 160 pieces (10%)

### Hyperparameters
| Parameter | Value |
|-----------|-------|
| Epochs | 300 |
| Batch Size | 2 |
| Optimizer | Adam |
| Learning Rate | Scheduled (warmup + decay) |
| Training Duration | ~13 hours |

### Learning Rate Schedule
A custom learning rate schedule was implemented to enhance training stability and convergence. The schedule employs a warmup phase followed by inverse square root decay, mathematically defined as:

```math
lr = d_{model}^{-0.5} \cdot \min(step^{-0.5}, step \cdot warmup\_steps^{-1.5})
```

## Generated Samples


## Pretrained Weights
Available at: results folder


