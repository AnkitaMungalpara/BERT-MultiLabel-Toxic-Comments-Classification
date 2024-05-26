# Multi-Label Text Classification with BERT

## Overview

This project utilizes BERT for multi-label text classification, specifically for the Toxic Comments Challenge on Kaggle. The dataset consists of user comments from Wikipedia edit pages labeled across multiple categories such as toxic, severe_toxic, obscene, threat, insult, and identity_hate.

## Dataset

The dataset used is from the Toxic Comments Challenge on Kaggle. It contains the following labels:

- **toxic**: 15,294 samples
- **severe_toxic**: 1,595 samples
- **obscene**: 8,449 samples
- **threat**: 478 samples
- **insult**: 7,877 samples
- **identity_hate**: 1,405 samples

## Model

I used BERT (Bidirectional Encoder Representations from Transformers) for the task of multi-label classification. The model architecture includes:

- BERT model for feature extraction.
- Dropout layer for regularization.
- Fully connected layer for classification.

## Data Preparation

The text data is tokenized using `BertTokenizer`. Labels are encoded appropriately for multi-label classification. Padding and truncation are applied to ensure uniform input sizes.

## Training

The model is trained using the `AdamW` optimizer. Key training configurations include:

- Batch size: 32
- Learning rate: 2e-5
- Number of epochs: 3
- Gradient clipping to handle exploding gradients.

GPU acceleration is utilized to speed up the training process.

## Results

The model achieved strong performance, demonstrating the effectiveness of BERT for this task. Detailed training and validation statistics are recorded and analyzed.
