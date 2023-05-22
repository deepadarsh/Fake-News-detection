# Fake-News-detection

[![MasterHead](https://www.analyticssteps.com/backend/media/thumbnail/6298822/1830215_1576840364_tittle-banner-of-fakenews.jpg)]


This repository contains code for classifying news articles as true or fake based on their titles and content. The code uses a logistic regression model and text preprocessing techniques to train and evaluate the classification performance.

## Dataset

The dataset used for training and testing the model is the "Fake and Real News Dataset" available on Kaggle. It consists of two CSV files: "True.csv" containing true news articles and "Fake.csv" containing fake news articles.

## Code Overview

The main steps performed in the code are as follows:

1. Loading and Concatenating the Dataset:
   - The true and fake news datasets are loaded using pandas and concatenated into a single dataframe.
   - A target column is added to indicate whether the news is true or fake.

2. Preprocessing:
   - The title and text columns are preprocessed by removing stopwords, converting to lowercase, and tokenizing the text.
   - The preprocessed tokens are joined back into cleaned title and cleaned text columns.

3. Data Visualization:
   - Bar plots are created to visualize the distribution of true and fake news articles and the count of articles by subject.
   - Word clouds are generated to visualize the most frequent words in true and fake news titles.

4. Fake News Classification Based on Title:
   - The dataset is split into training and test sets.
   - The titles are transformed into vectors using CountVectorizer.
   - A logistic regression model is trained on the training set and evaluated on the test set.
   - The accuracy of the predictions is calculated using ROC AUC score.
   - A confusion matrix is generated to evaluate the performance of the model.

5. Fake News Classification Based on Content:
   - The text of the news articles is preprocessed and transformed into vectors using CountVectorizer.
   - A logistic regression model is trained and evaluated on the cleaned joined text.
   - The accuracy of the predictions is calculated using ROC AUC score.
   - A confusion matrix is generated to evaluate the performance of the model.

## Results

- Classification Based on Title: 
- Accuracy: [0.9504329471767458] (ROC AUC score).
- Confusion Matrix: <img align="right" alt="Coding" width="400" src="https://github.com/deepadarsh/Fake-News-detection/assets/77419863/d9b197fd-1a92-4132-984e-c96719686b1f"> 
 

- Classification Based on Content:
- Accuracy: [0.9972045456669588] (ROC AUC score).
- Confusion Matrix: [link to the confusion matrix heatmap image]

## Conclusion

- Predicting the truthfulness of news articles based solely on their titles is not very accurate. The titles can be misleading.

- Considering the content of the news articles significantly improves the accuracy of the classification model.

- By combining both the title and the content, the highest accuracy percentages are achieved.
