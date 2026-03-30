# IMDB Sentiment Analysis — Model Comparison

## Overview
This project focuses on sentiment classification of IMDB movie reviews using both deep learning and traditional machine learning models.

The main objective is to compare model performance, training behavior, and generalization ability across different approaches.

Models implemented:
- 1D Convolutional Neural Network (1D-CNN)
- Long Short-Term Memory (LSTM)
- Baseline Machine Learning Model (TF-IDF + classifier)

---

## Data Preprocessing

All models use a consistent preprocessing pipeline:

- Lowercasing text
- Removing non-alphabetic characters
- Tokenization using IMDB dataset encoding
- Sequence padding (fixed length)
- Train / validation / test split

---

## Models

### 1D-CNN Model

#### Architecture
- Embedding layer (128 dimensions)
- Conv1D layer (filters = 128, kernel size = 5)
- Global Max Pooling layer
- Dense layer (ReLU)
- Output layer (Sigmoid)

#### Strengths
- Fast training
- Captures local textual patterns (key phrases)
- Strong generalization performance

---

### LSTM Model

#### Architecture
- Embedding layer (128 dimensions)
- LSTM layer (128 units)
- Dense output layer (Sigmoid)

#### Strengths
- Captures sequential dependencies in text
- Learns contextual relationships

#### Limitations
- Slower training compared to CNN
- Shows signs of overfitting after a few epochs

---

### Baseline Machine Learning Model

#### Architecture
- TF-IDF Vectorization
- Classification model (e.g., Logistic Regression or Naive Bayes)

#### Strengths
- Fast and simple
- Provides a baseline for comparison

#### Limitations
- Lower performance compared to deep learning models

---

## Training Settings

| Parameter        | Value                  |
|-----------------|------------------------|
| Optimizer       | Adam                   |
| Loss Function   | Binary Crossentropy    |
| Batch Size      | 64                     |
| Epochs          | 5                      |

---

## Performance Comparison

| Model         | Accuracy | Notes                          |
|--------------|---------|--------------------------------|
| 1D CNN       | ~0.87   | Best overall performance       |
| LSTM         | ~0.85   | Slight overfitting observed    |
| Baseline ML  | Lower   | Fast but less accurate         |

---

## Observations

- Both deep learning models achieved strong performance.
- CNN outperformed LSTM on validation and test data.
- LSTM shows early signs of overfitting (validation loss increases).
- CNN maintains more stable validation performance.
- Baseline model is useful but clearly less powerful.

---

## Interpretation

Sentiment in IMDB reviews is often expressed through short phrases such as:
- "not good"
- "very boring"
- "absolutely amazing"

The 1D CNN model is effective at detecting these local patterns using convolutional filters, which explains its superior performance.

LSTM models are better suited for capturing long-term dependencies, but this advantage is less relevant for this dataset.

---

## Conclusion

- The **1D CNN model is the best-performing model** for this task.
- LSTM provides good results but is slower and slightly less stable.
- The baseline model offers a useful reference but is outperformed by deep learning approaches.

---

## Project Structure
IMDB-SENTIMENT-ANALYSIS/
│
├── Model_cnn/
│ └── results/
│
├── Model_lstm/
│ └── results/
│
├── Model_mlpBaseline/
│
├── comparison.ipynb
├── IMDB Dataset.csv
├── submission.csv


---

## Final Note

This project highlights the importance of selecting the appropriate model for text classification tasks. In this case, convolutional approaches proved more effective than recurrent models due to the nature of the data.
