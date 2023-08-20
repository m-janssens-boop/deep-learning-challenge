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

<img width="518" alt="initial_model_structure" src="https://github.com/m-janssens-boop/deep-learning-challenge/assets/127706155/a5a018e4-dc54-4710-bf7e-f4058052c260">


The initial model had a ~72% accuracy, with the following summary report:

<img width="534" alt="initial_model_report" src="https://github.com/m-janssens-boop/deep-learning-challenge/assets/127706155/90307177-198a-4142-bbc9-d175e49be9bd">


To optimize the model and increase the performance, the `NAME` feature was added back into the dataset, the `CLASSIFICATION` value_counts were binned one degree higher, the number of neurons were greatly reduced, and the model performed much better, achieving a ~78% accuracy. Prior to this final optimization, other attempts included:
- Increasing the number of neurons
- Increasing the number of layers
- Decreasing the number of neurons
- Increasing the number of epochs
- Changing the activations functions from `RELU` to `TAHN`


The optimized model has the following structure of neurons, layers, and activation functions:


<img width="498" alt="optimized_model_structure" src="https://github.com/m-janssens-boop/deep-learning-challenge/assets/127706155/7a2fce50-eefc-44bd-b651-3ea740f924b1">

The optimized summary report:

<img width="504" alt="optimized_model_report" src="https://github.com/m-janssens-boop/deep-learning-challenge/assets/127706155/f5f64bea-06c8-4365-8983-7a378dfac1c0">


## Summary

This deep learning model performed relatively well overall. With more time and a larger dataset, it could be optimized further. An alternative to use for this problem would be a random forest model. The random forest model would work in a decision tree fashion, using classification rather than a neural network. To use a random forest, the data may need to be preprocessed in a slightly different way.
