# CGRU-5mC

**CGRU-5mC** is a leakage-aware deep learning framework for predicting 5-methylcytosine (5mC) sites in human DNA promoter sequences.

## Model

- One-Hot + Nucleotide Chemical Property (NCP) encoding
- Multi-scale 1D convolution
- Dilated residual convolution
- CBAM
- BiGRU
- Multi-Head Self-Attention
- Global average and max pooling

Each input sequence contains **41 bp** and is represented as a **41 x 7** feature matrix.

## Datasets

- **Primary Dataset**
- **Secondary Dataset**

## Leakage-Aware Evaluation

For each benchmark, **20% of the data is reserved before model development as an independent test set** and is used only for the final independent evaluation. The remaining 80% is used for training and five-fold cross-validation.

Exact duplicate sequences are grouped during cross-validation, and development-test sequence overlap is explicitly audited.

## Independent-Test Performance

| Dataset | Accuracy | Sensitivity | Specificity | MCC | F1-score | AUC |
|---|---:|---:|---:|---:|---:|---:|
| Primary | 97.60% | 87.17% | 98.48% | 0.8370 | 0.8498 | 0.9936 |
| Secondary | 96.82% | 93.96% | 97.20% | 0.8582 | 0.8735 | 0.9907 |

## Additional Analysis

- Encoding analysis
- Architectural ablation
- Confusion-matrix analysis
- Two-sample nucleotide logo analysis

## Implementation

Implemented using **Python, Keras 3, and JAX**, with TPU-based training.

## Repository

https://github.com/naimulpathan99-art/CGRU-5Mc.git

## Citation

Citation details will be updated after publication.

## Research Use

CGRU-5mC is intended for research use. Computational predictions should be interpreted alongside appropriate biological or experimental validation.
