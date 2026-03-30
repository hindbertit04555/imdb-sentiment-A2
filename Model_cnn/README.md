# 1D CNN Model

## Model Architecture
The 1D Convolutional Neural Network (CNN) is used to extract local features from text sequences.

Architecture:
- Embedding layer
- Conv1D layer (detects important patterns in text)
- Global Max Pooling layer (reduces dimensionality)
- Dense output layer with sigmoid activation

## Techniques Applied
- Text vectorization using IMDB dataset encoding
- Sequence padding
- Convolutional filters to capture key phrases
- Binary classification using sigmoid activation
- Loss function: binary crossentropy
- Optimizer: Adam

## Results
- Accuracy: ~87%
- The model performs better than LSTM due to its ability to detect important phrases in text.
- Shows stable validation performance.
