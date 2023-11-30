# Neural Machine Translation (French to English)

## Overview

This project focuses on developing a Neural Machine Translation (NMT) system using JoeyNMT v1 to translate French sentences into English. The model is trained on the WMT14 parallel corpus from Europarl v7 for French-English translation. Specialized corpora such as newsdev2013 and newstest2013 for French-English translation are used for development and testing.

## Model Description

The NMT model architecture is based on the Transformer framework, comprising an encoder and a decoder.

### Encoder
- Type: Transformer
- Layers: 6
- Attention Heads: 8
- Embedding Dimension: 512
- Hidden Size: 512
- Position-wise Feed-Forward Layer Size: 2048
- Dropout: 0.3

### Decoder
- Type: Transformer
- Layers: 6
- Attention Heads: 8
- Attention Mechanism: Bahdanau
- Embedding Dimension: 512
- Hidden Size: 512
- Position-wise Feed-Forward Layer Size: 2048
- Dropout: 0.3

## Training Configuration

### Training Data
- Source Language: French
- Target Language: English
- Data: Europarl v7 fr-en (WMT14 corpus)
- BPE Size: 30k

### Training Parameters
- Optimizer: Adam
- Learning Rate: 0.0005
- Batch Size: 4096
- Loss Function: Cross-Entropy
- Label Smoothing: 0.1
- Epochs: 30

## Testing and Evaluation

### Testing Configuration
- Beam Size: 5
- Length Penalty: 1.0
- Evaluation Metric: BLEU

## How to Run

1. Clone the repository.
2. Set up the required environment (Python, JoeyNMT v1).
3. Prepare datasets following the configuration guidelines.
4. Update the configuration file with desired settings.
5. Run the training script using the updated configuration.
6. Test the translation system
