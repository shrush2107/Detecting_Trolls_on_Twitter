# Bot Detection Using NLP

## Overview

This project aims to detect bots on the internet by analyzing tweets. It combines various datasets, processes the data, and employs machine learning techniques to classify tweets as either from bots or humans. The project consists of several Jupyter Notebooks and a Flask deployment for the final model.

## Project Structure

The project is structured into multiple components:

1. **Dataset Collection and Preprocessing**:
   - `Dataset1(Trolls).ipynb`: Collects and processes a 3 million Russian troll tweets dataset, extracting only English language tweets.
   - `Dataset2(Humans).ipynb`: Converts the `humansraw.txt` file into a CSV format for human tweets.

2. **Dataset Combination**:
   - `FinalDataset.ipynb`: Combines the output from the first two notebooks and labels the dataset as 'bot' (1) or 'human' (0).

3. **Text Processing**:
   - `Bot_in_Net1.ipynb`: Performs text processing on the combined dataset. Steps include converting text to lowercase, removing non-alphabetic characters, tokenization, stopword removal, and lemmatization.

4. **Model Building**:
   - `Model.ipynb`: The core of the project where machine learning models are trained and evaluated. It converts words into feature vectors using different techniques such as Count Vectorization, TF-IDF, and word embeddings. The following models are trained: Logistic Regression (LR), Naive Bayes (NB), Support Vector Machine (SVM), Random Forest (RF), and Long Short-Term Memory (LSTM) for sequence modeling.


## Getting Started

To get started with this project, follow these steps:

1. Clone this repository to your local machine:

   ```bash
   git clone <repository-url>
   cd <repository-directory>
   ```

2. Install the required dependencies. You may need to create a virtual environment first:

   ```bash
   pip install -r requirements.txt
   ```

3. Run the notebooks in the following order:
   - `Dataset1(Trolls).ipynb`
   - `Dataset2(Humans).ipynb`
   - `FinalDataset.ipynb`
   - `Bot_in_Net1.ipynb`
   - `Model.ipynb`

4. After running the notebooks, you can deploy the final model using the Flask application.

## Data Sources

- Russian Troll Tweets Dataset: [Link](https://www.kaggle.com/fivethirtyeight/russian-troll-tweets)

