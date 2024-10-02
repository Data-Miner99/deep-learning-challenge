# Overview of the Analysis

 The purpose of the model was to create an algorithm to help Alphabet Soup predict whether or not applicants for funding would be successful using a CSV file with over 34000 applicants.
 The initial model was created using two hidden layers, 6 and 4 neurons, and an output layer.

 An attempt was made to optimise the model to achieve an aacuracy of over 75%. The optimized model used an additional bin, 2 hidden layers with 20 and 10 neurons each.

 What variable(s) are the target(s) for your model?
The target variable was the `IS_SUCCESSFUL` feature.

 What variable(s) are the features for your model?
The following features were chosen for the model:
`NAME`, `APPLICATION_TYPE`, `AFFILIATION`, `CLASSIFICATION`, `USE_CASE`, `ORGANIZATION`, `STATUS`, `INCOME_AMT`, `SPECIAL_CONSIDERATIONS`

What variable(s) should be removed from the input data because they are neither targets nor features?
The  variable that should be removed is `EIN` because it is an identifier for the applicant organization and has no impact on the behavior of the model.

## Compiling, Training, and Evaluating the Model

How many neurons, layers, and activation functions did you select for your neural network model, and why?
In the Optimized version of the model, 2 hidden layers were used, the first layer used 20 neurons and 10 neurons. The hidden layers used the `relu` activation function and the output layer used `sigmoid`.

Were you able to achieve the target model performance?
Yes, by optimizing the model, the accuracy increased from 72% to a little over 79%.

What steps did you take in your attempts to increase model performance?

* An additional bin was created using the name feature
* The number of neurons were increased.

## Summary

By optimizing the model, the accuracy was increased to about 79%.

This means the model is able to correctly classify each of the points in the test data 79% of the time. In other words an applicant has a close to 80% chance of being successful if they meet the following criteria:

Their NAME appears more than 5 times.
The type of APPLICATION is a T3, T4, T5, T6 or T19
The application is classified by one of the following CLASSIFICATION values : C1000, C1200, C2000, C2100 or C3000.

An alternative model to recommend is the Random Forest model as it is suited for classification problems. As can be seen, using the Random Forest model we can achieve close to 78% accuracy.
