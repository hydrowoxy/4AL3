# 4AL3 - MRI Brain Tumor Segmentation

COMPSCI/SFWRENG 4AL3 | Fall 2026 | Group 30

## Project

Multiclass brain tumor segmentation using the BraTS dataset.

We are comparing a 2D U-Net against a simpler CNN-based segmentation model.

## Repository Structure

- `proposal/` - Project proposal
- `team-contract/` - Team contract
- `progress-report/` - Progress report (LaTeX)
- `src/` - Data processing, model implementations, training, and evaluation
- `results/` - Figures and experimental results

## Data

BraTS 2023 Adult Glioma (GLI) dataset.

Four MRI modalities:
- T1
- T1CE
- T2
- T2-FLAIR

Segmentation labels:
- 0: Background
- 1: Necrotic/non-enhancing tumor core
- 2: Edema
- 3: Enhancing tumor

Dataset files should be stored locally in `data/` and are not committed to Git.

## Shared Model Interface ((do we agree on this let's make sure before we do stuff))

Input image: `(4, H, W)`

Segmentation mask: `(H, W)`

Batched model output: `(B, 4, H, W)` (logits)

Train/validation/test splits must be performed at the subject level to prevent data leakage.

## Installation

```bash
pip install -r requirements.txt