# Music Transformer – Music Generation and Prediction

This repository contains the experimental results and training configuration used in my master's thesis on music generation and prediction using deep learning.

The implementation is based on the Music Transformer model provided by
[jason9693/MusicTransformer-tensorflow2.0](https://github.com/jason9693/MusicTransformer-tensorflow2.0),
licensed under the MIT License.

---

## Training Configuration

### Dataset
The model was trained on a subset of the **MAESTRO (MIDI and Audio Edited for Synchronous Tracks and Organization)** dataset, consisting of 1,600 classical piano performances. The dataset was split as follows:

- **Training set**: 1,280 pieces (80%)
- **Validation set**: 160 pieces (10%)
- **Testing set**: 160 pieces (10%)

---

### Hyperparameters

| Parameter | Value |
|----------|-------|
| Epochs | 300 |
| Batch Size | 2 |
| Optimizer | Adam |
| Learning Rate | Scheduled (warmup + decay) |
| Training Duration | ~13 hours |

---

### Learning Rate Schedule
A custom learning rate schedule was employed to improve training stability and convergence. The schedule consists of a warmup phase followed by inverse square root decay, defined as:

```math
lr = d_{model}^{-0.5} \cdot \min(step^{-0.5}, step \cdot warmup\_steps^{-1.5})
```

### Generated Samples
Generated MIDI samples can be found in the audio results/ directory.
Corresponding piano roll visualizations can be found in the `piano_rolls/` directory.

## Trained Model Weights
The trained model weights obtained from the experiments conducted for this thesis are available in the weights/ directory.
