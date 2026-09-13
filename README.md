# Optimizing Deep Learning Architectures with Bio-Inspired Algorithms

A hybrid Genetic Algorithm (GA) and Particle Swarm Optimization (PSO) approach for optimizing Convolutional Neural Network (CNN) architectures for CIFAR-10 image classification.

## Overview

Designing an effective CNN architecture involves selecting hyperparameters such as the number of convolutional layers, number of filters, kernel size, dropout rate, and dense-layer units.

This project uses a hybrid GA–PSO optimization strategy to search for an effective CNN architecture based on Macro F1-score.

## Project Workflow

1. Load and preprocess the CIFAR-10 dataset
2. Train a baseline CNN model
3. Define the CNN architecture search space
4. Initialize the GA–PSO population
5. Evaluate candidate architectures using Macro F1-score
6. Perform iterative GA–PSO optimization
7. Identify the best-performing architecture
8. Retrain the optimized architecture using data augmentation
9. Evaluate the final model using accuracy, Macro F1-score, classification report, and confusion matrix

## Baseline CNN

The baseline model achieved:

| Metric | Result |
|---|---:|
| Test Accuracy | 62.71% |
| Macro F1-score | 62.92% |

## GA–PSO Optimization

The optimization searched across CNN architectural parameters including:

- Number of convolutional layers
- Number of filters
- Kernel size
- Dropout rate
- Dense-layer units

The best architecture found during the optimization was:

| Parameter | Value |
|---|---:|
| Convolutional layers | 3 |
| Filters | 128 |
| Kernel size | 3 × 3 |
| Dropout | 0.50 |
| Dense units | 256 |
| Best Macro F1-score | 77.58% |

## Final Retrained Model

The selected architecture was retrained using data augmentation and training callbacks.

Final test performance:

| Metric | Result |
|---|---:|
| Test Accuracy | 78.86% |
| Macro F1-score | 78.86% |

## Technologies

- Python
- TensorFlow / Keras
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn
- CIFAR-10
- Genetic Algorithm (GA)
- Particle Swarm Optimization (PSO)

## Repository Contents

```text
Optimizing-Deep-Learning-Architectures/
│
├── README.md
└── GA_PSO_CNN_Optimization.ipynb
