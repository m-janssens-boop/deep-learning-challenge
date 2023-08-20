# deep-learning-challenge

Overview
------------------
The nonprofit foundation Alphabet Soup wants a tool that can help it select the applicants for funding with the best chance of success in their ventures. Using machine learning and neural networks, use the features in the provided dataset to create a binary classifier that can predict whether applicants will be successful if funded by Alphabet Soup.

Results
-------------------

### Data Preprocessing
The target variable for both the initial and the optimized models is the `IS_SUCCESSFUL` column of the data, which denotes whether a venture that was funded was successful or not.


Because some of the feature variables were categorical variables, the `pd.get_dummies()` function was used to convert them to numerical features. The features variables for the optimized model include:
- NAME
- APPLICATION_TYPE
- AFFILIATION
- CLASSIFICATION
- USE_CASE 5 ORGANIZATION
- STATUS
- INCOME_AMT
- SPECIAL_CONSIDERATIONS
- ASK_AMT


The `EIN` variable was removed from the dataset because it is a redundant variable.


### Compiling, Training, and Evaluating the Model


The initial model did not include `NAME` as a feature variable and had the following structure of neurons, layers, and activation functions:

INCLUDE PHOTO HERE

The initial model had a ~72% accuracy, with the following summary report:

INCLUDE PHOTO HERE

To optimize the model and increase the performance, the `NAME` feature was added back into the dataset, the `CLASSIFICATION` value_counts were binned one degree higher, the number of neurons were greatly reduced, and the model performed much better, achieving a ~78% accuracy. Prior to this final optimization, other attempts included:
- Increasing the number of neurons
- Increasing the number of layers
- Decreasing the number of neurons
- Increasing the number of epochs
- Changing the activations functions from `RELU` to `TAHN`


The optimized model has the following structure of neurons, layers, and activation functions:


INCLUDE PHOTO HERE


The optimized summary report:


INCLUDE PHOTO HERE


## Summary
