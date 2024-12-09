# Enhancer Classification Project
Project for university course in bioinformatics
## Objective
The goal of this project is to train a classifier capable of predicting enhancer sequences from DNA data using the frequency of k-mers.

## Datasets
Two datasets were used to train and evaluate the model:

1. **Dataset 1**: Sequences from the **Vista database**, labeled with 1 (enhancer) or 0 (non-enhancer).
2. **Dataset 2**: A combination of **Vista database** enhancers and randomly sampled non-enhancer sequences from the **GRCh38 human genome**.

## Methods
### Data Preprocessing
The frequency of each k-mer in sequences was calculated and used as input features for the classifier.

### Classifier
A logistic regression classifier was selected for its simplicity and low training time. Grid search with 10-fold cross-validation was used to find the best coefficients for L2 regularization.

## Results
The classifier was tested on both datasets with k-values of 3, 4, and 5. Performance metrics such as accuracy, precision, recall, AUC-ROC, and F1-score were calculated for each k. Confusion matrices were also analyzed.

- **Dataset 1**: The model performed poorly with low accuracy and high recall, suggesting it was classifying non-enhancers as enhancers more frequently.
- **Dataset 2**: The model performed significantly better, with balanced precision and recall.