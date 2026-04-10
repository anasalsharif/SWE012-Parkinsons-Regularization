# Regularization Strategies for Small Biomedical Datasets
**Case Study — Parkinson's Disease Detection from Voice Measurements**

This project explores the impact of various regularization strategies on a small, high-dimensional biomedical dataset prone to severe overfitting.

## Project Overview

The Parkinson's Disease dataset (Little et al., 2008) contains 195 voice recordings defined by 22 biomedical voice features, targeting a binary classification (Healthy vs. Parkinson's). Given the high-dimensional, low-sample regime, it serves as an excellent vehicle to demonstrate regularization approaches covered in Deep Learning coursework.

### Key Research Question
> *Given a small, high-dimensional biomedical dataset where overfitting is near-certain, which regularization strategy — L2 weight decay, Dropout, L1 sparsity, or Early Stopping — provides the best generalization, and why?*

##  Repository Structure
```
├── project.ipynb        # Main Jupyter Notebook (Executed & Verified)
├── project.html         # Professional Web Report (View in Browser)
├── project_presentation.pptx # Findings Presentation (PowerPoint)
├── figures/             # Directory containing all 7 analysis plots
├── parkinsons.data      # Dataset (UCI local fallback)
├── parkinsons.names     # Dataset documentation
├── requirements.txt     # Python dependencies
├── README.md            # Project documentation (this file)
└── .gitignore           # Git ignore file
```

## Setup and Installation

1. Clone this repository:
   ```bash
   git clone <your-repo-link>
   cd DeepLearning
   ```

2. (Optional but recommended) Create a virtual environment:
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. Install requirements:
   ```bash
   pip install -r requirements.txt
   ```

4. Launch Jupyter Notebook to view or run the analysis:
   ```bash
   jupyter notebook project.ipynb
   ```

## Methodology & Technical Scope

This project implements a PyTorch-based Multilayer Perceptron (MLP) and investigates multiple strategies:
1. **Baseline** (No Regularization) — Establishing the overfitting baseline.
2. **L2 Regularization** (Weight Decay) — Shrinking weights proportionally.
3. **Dropout** — Preventing co-adaptation of neurons.
4. **Early Stopping** — Constraining the optimization trajectory based on validation loss.
5. **L1 Regularization** — Inducing sparsity (implemented manually in the PyTorch training loop).

### Evaluation Metrics
- BCE Loss tracking (Train vs. Validation)
- Test Accuracy
- Generalization Gap Analysis
- Sparsity Analysis (for L1)

## Conclusions

The notebook includes detailed explanations tying each implementation back to foundational Deep Learning literature (e.g., *Goodfellow, Bengio & Courville*). The final section compares all methods side-by-side using consolidated visualizations to determine the optimal strategy for this specific dataset profile.
