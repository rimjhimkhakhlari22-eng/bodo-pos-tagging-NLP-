# bodo-pos-tagging-NLP-
NLP-based POS tagging for the low-resource Bodo language using BiLSTM-CRF and IndicBERT v2.

## Overview

This project focuses on Part-of-Speech (POS) tagging for the low-resource Bodo language. Two approaches are implemented and compared: BiLSTM-CRF as the baseline model and IndicBERT v2 as a transformer-based model.

## Objectives
1. To develop an automated Part-of-Speech (POS) tagging system for the Bodo language using
deep learning techniques.
2. To implement a BiLSTM-CRF model as the baseline approach for Bodo POS tagging.
3. To fine-tune IndicBERT v2 for the Bodo POS tagging task using the same annotated dataset.
4. To compare the performance of the BiLSTM-CRF and IndicBERT v2 models using standard
evaluation metrics such as Accuracy, Precision, Recall, and F1-score.
5. To analyze the strengths and limitations of both models in handling POS tagging for a low-
resource language.
6. To investigate whether a pretrained transformer-based model (IndicBERT v2) provides
better performance than the baseline BiLSTM-CRF model for Bodo POS tagging.
7. To contribute towards the development of NLP resources and benchmark results for the
Bodo language, thereby supporting future research on low-resource Indic languages.

## Dataset

The project uses an annotated Bodo language dataset containing **35 unique POS tags**.

The dataset was preprocessed and tokenized before training the models.

## Models

### 1. BiLSTM-CRF

BiLSTM is used to capture contextual information from both directions, while the CRF layer models the relationships between consecutive POS tags.

### 2. IndicBERT v2

IndicBERT v2 is a pretrained multilingual/Indic language transformer model used for contextual token classification.

## Workflow

Bodo Dataset
↓
Data Preprocessing
↓
Tokenization
↓
BiLSTM-CRF / IndicBERT v2
↓
POS Prediction
↓
Evaluation

<img width="2324" height="3604" alt="image" src="https://github.com/user-attachments/assets/022c7a87-adde-4e88-a2e4-d1b46148424e" />


## Results

| Model | Accuracy | Precision | Recall | F1-Score |
|---|---:|---:|---:|---:|
| BiLSTM-CRF | 82.95% | 82.62% | 82.95% | 82.38% |
| IndicBERT v2 | 85.51% | 85.36% | 85.51% | 85.31%|

IndicBERT v2 outperformed the BiLSTM-CRF baseline across all primary evaluation metrics, demonstrating the advantage of pretrained transformer-based representations for Bodo POS tagging. The lower macro F1-score indicates comparatively lower performance on rare POS tags due to class imbalance in the dataset.

## Project Structure

```text
Bodo-POS-Tagging/
│
├── README.md
├── requirements.txt
│
├── data/
│   └── Bodo11_dataset.csv
│
├── notebooks/
│   ├── BiLSTM-CRF.ipynb
│   └── IndicBERT-v2.ipynb
│
├── results/
│   ├── model_comparison.png
│   └── metrics.txt
│
└── models/
    └── README.md
