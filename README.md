# music-transformer-music-prediction
# Music Generation for [Your Thesis Topic]

Based on the [Music Transformer implementation](https://github.com/jason9693/MusicTransformer-tensorflow2.0) by jason9693.

## Training Configuration

### Dataset
The model was trained on the MAESTRO (MIDI and Audio Edited for Synchronous TRacks and Organization) dataset, comprising 1,600 classical piano performances. The dataset was partitioned following standard machine learning practices:
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

$$\text{lr} = d_{model}^{-0.5} \cdot \min(\text{step}^{-0.5}, \text{step} \cdot \text{warmup\_steps}^{-1.5})$$

where $d_{model} = 256$ (embedding dimension) and warmup steps were set according to the original Music Transformer implementation. This adaptive learning rate strategy prevents gradient instability during early training phases while maintaining efficient convergence in later epochs.

### Computational Resources
The training process completed in approximately 13 hours.

## Generated Samples
[Link to samples folder or audio player]

## Pretrained Weights
Available at: [link if hosted externally]

## Citation
[Your thesis citation]
