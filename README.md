# IMDB-Movie-rating-classification
## 1. Dataset
This dataset has been split into train and test set. The IMDB Movie ratings are discretised into 5 bins, with 0 as lowest and 4 as highest rating
## 2. Preprocess ‘title_year’
The number of years of every movie’s released year from the median is calculated so we can have the ‘years’ feature in a Gaussian distribution
## 3. Visualising features and classes
Class distribution is visualised through a pie and bar chart to check for class imbalance
## 4. Preprocessing
### Scaling continuous features
Any redundant features that were observed from the visualisation of data are removed. The remaining continuous features are standardised so that their ranges are consistent
### Categorical features
One Hot Encoding is used to represent categorical features in a continuous space. This step is done in a pipeline to ensure that the encoding scheme used for the testing data is consistent with that of the training data. This also allows better handling of new categorical attributes in the testing instances.
## 5. Building the classifiers
For all of the following models, the accuracy for testing instances and an average accuracy of 5-fold cross validation are used as the evaluation metric. The training and prediction runtime are also recorded to compare the models’ complexity. The following classifiers are built:
- 0R as baseline model
- Random Forest
- Bagging ensemble of Decision Trees
- Logistic Regression
