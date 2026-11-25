# SMS Spam Detection Under Misspellings

## Project Overview

This project inspect SMS spam detection using Natural Language Processing (NLP). The goal is to classify English SMS messages as Spam or Ham and examine how spelling variations affect classification performance.

## Experimental Question

Which method is more effective at detecting spam messages that contain misspellings?

## Dataset

UCI SMS Spam Collection Dataset

https://archive.ics.uci.edu/dataset/228/sms+spam+collection

After cleaning and duplicate removal (preprocessing), the dataset was divided into training, development, and testing subsets using stratified sampling.

## Methods

### Method 1
TF-IDF + Logistic Regression

### Method 2
all-MiniLM-L6-v2 Sentence Embeddings + Logistic Regression

Both methods use the same training, development, and test splits to ensure a fair comparison.

## Challenge

To evaluate robustness against misspellings, a modified version of the test set was created. Selected words in spam messages were altered using character substitutions while preserving their intended meaning.

Example:

free → fr33

offer → 0ffer

The models were not trained on these modified messages.

## Notebook Structure

- Setup
- Data
- Method 1
- Method 2
- Results
- Try It
- Conclusion
- Sources

## Running the Notebook

1. Open the notebook in Google Colab.
2. Select Runtime > Run All.
3. Wait for both models to train.
4. Review the generated evaluation results.
5. Use the **Try It** section to enter a new SMS message and receive a prediction.

## Requirements

- Python 3
- pandas
- scikit-learn
- sentence-transformers
- joblib

## Authors

Group 1 - NLP Course

Lina Mushabeb Alqahtani - Imam Abdulrahman Bin Faisal University (Computer Engineering department - AI)

Nabaa Nabeeh Alaswad - Imam Abdulrahman Bin Faisal University (Computer Engineering department - AI)

Shahad Saeed Alshahrani - Imam Abdulrahman Bin Faisal University (Computer Engineering department - AI)
