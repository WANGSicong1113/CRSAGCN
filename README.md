# TranscircGCN
# TranscircGCN: Transformer-Enhanced Graph Convolutional Network for circRNA–Disease Association Prediction

TranscircGCN is a hybrid deep learning framework designed to predict potential associations between circRNAs and diseases.  
It integrates:

- **Deep sequence feature extraction** via a CNN-based encoder (inspired by DeepLncLoc),
- **Graph Convolutional Network (GCN)** to model the topological structure of circRNA–disease interaction networks,
- **Transformer Encoder** modules to capture deep contextual dependencies and enhance feature representations,
- **A PU (Positive-Unlabeled) learning framework** for handling the imbalanced nature of circRNA–disease data.

---

## Model Architecture

```text
      +--------------------+
      |    DeepLncLoc CNN   |   <-- circRNA sequence encoding
      +--------------------+
               |
      +--------------------+
      |        GCN         |   <-- Graph structure embedding
      +--------------------+
               |
      +----------------------------+
      |    Transformer Encoder     |   <-- Contextual feature enhancement
      +----------------------------+
               |
      +--------------------+
      |     Predictor      |   <-- circRNA-disease association score
      +--------------------+
 ```
---
##Project Structure
 ```text
TranscircGCN/
├── data/                      # Dataset files (adjacency matrices, features, sequences)
├── model.py                   # Model definitions (DeepLncLoc, GCN, Transformer, Predictor)
├── main.py                    # Training and evaluation pipeline
├── utils.py                   # Data preprocessing, metrics, helper functions
├── requirements.txt           # Dependencies
└── README.md                  # This file
 ```
