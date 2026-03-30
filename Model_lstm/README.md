# LSTM Model

## Model Architecture
The LSTM (Long Short-Term Memory) model is a type of Recurrent Neural Network (RNN) designed to capture sequential dependencies in text data.

Architecture:
- Embedding layer (converts words into dense vectors)
- LSTM layer (captures temporal dependencies)
- Dense output layer with sigmoid activation

## Techniques Applied
- Text tokenization using IMDB dataset built-in encoding
- Sequence padding to ensure equal input length
- Binary classification using sigmoid activation
- Loss function: binary crossentropy
- Optimizer: Adam

## Results
- Accuracy: ~85%
- The model shows good performance but slight overfitting after a few epochs, as validation loss increases while training loss decreases.
