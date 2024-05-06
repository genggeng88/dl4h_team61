# Deep Learning for Healthcare - Team 61

Welcome to the public project repository for Team 61 from the Deep Learning For Healthcare course. Our project aims to reproduce the research presented in the paper titled "Prediction of drug-drug interaction events using graph neural networks based feature extraction," available at IEEE Xplore. The primary objective of our research is to construct a heterogeneous drug network by integrating drug properties across various types of drug-drug interactions (DDIs). Subsequently, we aim to predict the types of interactions between drugs.

## Project Overview

### Environments

- Python 3.6.12 :: Anaconda.
- TensorFlow 2.1
- Keras 2.3
- NumPy 1.19
- Pandas 1.1.3
- SQLite3 3.8.6
- tqdm 4.63
- Matplotlib 3.3

### Run Instructions

1. **prepare.py**: This script prepares the data and generates attributed heterogeneous networks. It involves tasks such as data preprocessing, feature extraction, and constructing the network structure based on drug properties and interactions.

2. **generate_embbeding.py**: Utilizing a Graph Neural Network (GNN) model, this script generates representation vectors for drugs. GNNs excel at learning representations from graph-structured data, making them suitable for this task. The script allows testing the model's performance with different embedding sizes to evaluate its impact on learned representations.

3. **concat.py**: After generating the embedding vectors, this script concatenates them in preparation for input into subsequent models for prediction.

4. **train.py**: This script trains models using the concatenated embedding vectors to predict drug-drug interactions (DDIs) and their types. Users have the flexibility to choose different models such as Random Forest (RF), K-Nearest Neighbors (KNN), and Logistic Regression (LR) for prediction, enabling comparison of their performance.

### How to Run

To get started with the project:

- Ensure you have the required Python and library versions installed.
- Run `prepare.py` to prepare the data and generate attributed heterogeneous networks.
- Execute `generate_embbeding.py`, possibly trying different embedding sizes to evaluate model performance.
- Run `concat.py` to concatenate the embedding vectors.
- Finally, use `train.py` to train the chosen model(s) and make predictions on drug-drug interactions and their types.
