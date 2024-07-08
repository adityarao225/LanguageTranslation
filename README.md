# Language Translation Project

## Overview

This project focuses on building a transformer-based model for translating text between languages. The primary datasets used are Italian to English and Hindi to English translations, sourced from Kaggle. The project includes data preprocessing, model training, and evaluation, all implemented in a Google Colab notebook using PyTorch.

## Datasets

- **Italian to English**: Available as a text file (`.txt`).
- **Hindi to English**: Available as a CSV file (`.csv`).

Both datasets are stored in the `Dataset` directory.

## Project Structure

- `model.py`: Contains the implementation of the transformer model, including embedding layers, positional encoding, multi-head attention, feed-forward networks, and residual connections.
- `Dataset/`: Contains the translation datasets.
- `notebook.ipynb`: Google Colab notebook with code for data preprocessing, model training, and evaluation.

## Transformer Model

The transformer model is built using PyTorch and includes the following components:

1. **InputEmbeddings**: Converts token indices to embeddings and scales them.
2. **PositionalEncoding**: Adds positional information to the embeddings.
3. **LayerNormalization**: Normalizes the input across features.
4. **FeedForwardBlock**: Two linear layers with ReLU activation and dropout.
5. **ResidualConnection**: Adds residual connections with layer normalization.
6. **MultiHeadAttentionBlock**: Implements multi-head attention mechanism.
7. **EncoderBlock**: Combines self-attention and feed-forward blocks with residual connections.
8. **Encoder**: Stacks multiple encoder blocks.
9. **DecoderBlock**: Combines self-attention, cross-attention, and feed-forward blocks with residual connections.
10. **Decoder**: Stacks multiple decoder blocks.
11. **ProjectionLayer**: Projects the decoder output to the target vocabulary size.
12. **Transformer**: Combines encoder, decoder, embedding layers, positional encoding, and projection layer.

## Getting Started

### Prerequisites

- Python 3.8+
- PyTorch
- Google Colab

### Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/adityarao225/LanguageTranslation.git
    cd LanguageTranslation
    ```

2. Upload the `notebook.ipynb` to your Google Drive and open it with Google Colab.

### Running the Project

1. Open the Google Colab notebook (`notebook.ipynb`).
2. Follow the instructions in the notebook to preprocess the data, train the model, and evaluate the results.

## Usage

To use the transformer model for translation, you can import the `build_transformer` function from `model.py` and initialize the model with the desired parameters.

## Acknowledgments

- This project utilizes the transformer architecture as described in the paper "Attention is All You Need" by Vaswani et al.
- The datasets are sourced from Kaggle.

## License

This project is licensed under the MIT License.
