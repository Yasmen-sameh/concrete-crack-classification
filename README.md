# Concrete Crack Classification with Deep Learning

A binary image-classification project that detects whether a concrete-surface image contains a crack.

## Project Overview

This project uses a custom Convolutional Neural Network (CNN) built with TensorFlow/Keras to classify concrete images into:

- **Negative** — no visible crack
- **Positive** — crack present

The dataset contains **40,000 RGB images** at 227×227 resolution, evenly distributed between the two classes.

## Dataset Split

The full dataset was retained and split using stratified sampling:

| Split | Images |
|---|---:|
| Train | 24,000 |
| Validation | 8,000 |
| Test | 8,000 |
| **Total** | **40,000** |

## Model

The model is a custom CNN with:

- Image rescaling
- Convolutional blocks
- Batch Normalization
- ReLU activation
- Max Pooling
- Global Average Pooling
- Dropout regularization
- Dense layer
- Sigmoid output for binary classification

Training used:

- Adam optimizer
- Binary Cross-Entropy loss
- Early Stopping
- ReduceLROnPlateau
- Model Checkpointing

## Test Results

Evaluation was performed on the held-out **8,000-image test set**.

| Metric | Result |
|---|---:|
| Accuracy | **99.72%** |
| Precision | **99.73%** |
| Recall | **99.72%** |
| F1-score | **99.72%** |

### Per-class results

| Class | Precision | Recall | F1-score |
|---|---:|---:|---:|
| Negative | 99.68% | 99.78% | 99.73% |
| Positive | 99.77% | 99.68% | 99.72% |

### Confusion Matrix

```text
                 Predicted
               Negative Positive
Actual Negative   3991      9
       Positive     13    3987
```

## Technologies

- Python
- TensorFlow / Keras
- NumPy
- Pandas
- Matplotlib
- Scikit-learn

## Repository Structure

```text
concrete-crack-classification/
├── concrete_crack_classification.ipynb
├── README.md
├── requirements.txt
└── assets/
```

## How to Run

1. Download the dataset from Kaggle.
2. Update `DATA_DIR` in the notebook to match your local/Kaggle dataset path.
3. Install the required packages.
4. Run the notebook cells in order.

> The reported metrics above are the results recorded from the submitted notebook on the held-out test set.

## Important Note

This is an academic/computer-vision project for image classification. It is not a certified structural-safety inspection system and should not be used as a substitute for professional engineering inspection.

## Author

**Yasmen Sameh**  
Computer Science + AI Student  
AI / Machine Learning Track
