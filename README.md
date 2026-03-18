# MNIST Hidden Layer Analysis: Neural Network Capacity & Representation Learning

## Overview
This project investigates how hidden-layer size impacts both performance and internal representations in a single-hidden-layer neural network trained on the MNIST dataset.

Rather than focusing only on accuracy, this study analyzes how neural networks learn and organize features as model capacity increases.

## Objective
- Understand how hidden neurons develop internal representations
- Analyze how model capacity affects class separability
- Evaluate the tradeoff between accuracy and interpretability

## Methodology
- Dataset: MNIST (70,000 handwritten digit images)
- Model: Fully connected neural network (1 hidden layer, ReLU, softmax output)
- Experiments: Hidden layer sizes = 1, 2, 3, 5, 20, 50, 85 neurons
- Evaluation:
  - Accuracy (train/validation/test)
  - Confusion matrices
  - Misclassification analysis
  - Hidden-layer activation visualizations

## Key Results
- Severe underfitting at low capacity:
  - 1 neuron → ~38% accuracy
- Rapid performance improvement:
  - 5 neurons → ~90% accuracy
- Diminishing returns:
  - 85 neurons → ~97% accuracy
- Larger networks improve accuracy but reduce interpretability

## Feature Engineering Experiments
- PCA (95% variance retained):
  - Maintains strong performance with reduced dimensionality
- Random Forest feature selection:
  - Reduced accuracy (~92.9%)
  - Indicates importance of full spatial context

## Insights
- Hidden layers evolve from simple stroke detectors to distributed feature representations
- Moderate model capacity provides the best balance of performance and interpretability
- Dense networks have limitations for image data
- Convolutional Neural Networks (CNNs) are better suited due to spatial structure

## Tech Stack
- Python
- TensorFlow / Keras
- NumPy / Pandas
- Matplotlib / Seaborn
- Scikit-learn

## Why This Matters
This project demonstrates a deeper understanding of:
- Model capacity vs generalization
- Neural network interpretability
- Feature representation learning

These are critical concepts for real-world ML applications where both performance and explainability matter.
