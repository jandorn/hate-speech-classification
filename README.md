Hate Speech Classification / Twitter Sentiment Classification

We developed a tweet hate speech classification pipeline including preprocessing steps, data set splitting, and three methods of classifying a tweet that includes a _Naive Bayes_, a _Support Vector Machine_ and a _Neural Network_. Hyperparameter tuning methods were used to maximize the precision of each method. The best and final model was obtained with the SVM.

For the classification, we used a python-notebook (.ipynb). This way we could easily and quickly access various python libraries while maintaining a clear structure. In addition, the format is very suitable for working in a group via Google Colab.

# Structure

## Jupyter Notebook

1. **_Imports & read data:_** Data for training are uploaded, Python libraries are imported
2. Basic inspection of dataset
3. **_Preprocessing:_**
   1. „@USER, RT and {{URL}}" are removed
   2. Stemming and Lemmatization
   3. Everything in lowercase
4. Train/test split: Division into train (80%) and test-set (20%)
5. **_Naïve Bayes_**
   1. Train model incl. hyperparameter tuning
   2. Evaluation (classification_report, ConfusionMatrixDisplay.from_estimator)
   3. Apply to test set
6. **_SVM_**
   1. Train model incl. hyperparameter tuning
   2. Evaluation (classification_report, ConfusionMatrixDisplay.from_estimator)
   3. Apply to test set
7. **_Neural Network_**
   1. Train model incl. hyperparameter tuning
   2. Evaluation (classification_report, ConfusionMatrixDisplay.from_estimator)
   3. Apply to test set
8. Export results: Export of the classification result with the highest accuracy (in our case, the SVM)

## Dataset

### train.tsv

The `train.tsv` file is our dataset used for training. It has a collection of over **18.000 labeled tweets** in a convenient tsv format.

### test.tsv.dist

The `test.tsv.dist` file is our evaluation or testing set. These tweets consisting of almost **5000 tweets** are not labeled and are to be predicted by our different trained models. Unfortunately we dont have access to the corresponding dataset with the actual labels. We do know, that our SVM labeled them correctly with a success rate of about _~94%_.

## Authors
