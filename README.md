# SurfNet-NEU Surface Defect Classification

A PyTorch-based implementation of a lightweight CNN approach inspired by the SurfNet research work for multi-class surface defect classification.

## 📌 Project Overview

This project implements a surface defect classification system using a convolutional neural network based on the SurfNet architecture described in the research paper:

**"Surface Defect Classification in Real-Time Using Convolutional Neural Networks"**

The publicly available NEU surface defect dataset is used for reproducible experimentation.

## 📄 Reference Paper

S. Arikan, K. Varanasi, and D. Stricker,  
"Surface Defect Classification in Real-Time Using Convolutional Neural Networks,"  
arXiv:1904.04671, 2019.

Paper: https://arxiv.org/abs/1904.04671

## 📊 Dataset

The NEU surface defect dataset contains:

- 1,800 grayscale images
- 6 defect categories
- 300 images per class

### Classes

1. Crazing
2. Inclusion
3. Patches
4. Pitted Surface
5. Rolled-in Scale
6. Scratches

The dataset itself is not included in this repository.

## 🧠 Model

The implementation follows the documented SurfNet design principles, including:

- 5×5 convolutional processing
- Batch Normalization
- PReLU activation
- Residual processing
- Stride-based downsampling
- Global Average Pooling
- Fully connected classification layer

The implementation is evaluated as a multi-class classification problem with six output classes.

## ⚙️ Training Configuration

| Parameter | Value |
|---|---|
| Framework | PyTorch |
| Input Size | 128 × 128 |
| Number of Classes | 6 |
| Batch Size | 10 |
| Optimizer | RMSProp |
| Learning Rate | 0.0001 |
| Weight Decay | 0.1 |
| Loss Function | NLLLoss |
| LR Scheduler | StepLR |
| LR Reduction | 0.8 |
| Scheduler Step | 3 epochs |
| Maximum Epochs | 100 |
| Cross Validation | 10-Fold Stratified |

## 🔬 Methodology

The overall workflow is:

Dataset
→ Preprocessing
→ SurfNet Model
→ Training
→ 10-Fold Cross Validation
→ Performance Evaluation
→ Final Model
→ Single Image Prediction

## 📈 Evaluation

The implementation includes:

- 10-fold cross-validation
- Accuracy
- Precision
- Recall
- F1-score
- Confusion matrix
- Training loss graph
- Training accuracy graph
- Learning-rate graph
- Single-image prediction

## 🛠️ Technologies

- Python
- PyTorch
- Torchvision
- NumPy
- Pandas
- Scikit-learn
- Matplotlib
- Seaborn
- Pillow
- Google Colab

## 📁 Repository Structure

```text
SurfNet-NEU-Surface-Defect-Classification/
│
├── SurfNet_NEU.ipynb
├── requirements.txt
├── README.md
│
└── results/
    ├── cv_results.csv
    ├── confusion_matrix.png
    ├── training_loss.png
    ├── training_accuracy.png
    └── learning_rate.png
