# Neural_Network_Charity_Analysis

## Project Overview

Using Machine learning and neural networks to create a binary classifier cabpable of predicting whether applicants will be successful if funded by Alphabet Soup.

## Resources

- Applications\Software: Jupyter Notebook 6.1.4
- Languages\Libraries: Python 3.8.5, pandas, scikit-learn, tensorflow
- Data: [Charity Data](charity_data.csv)

## Results

### Data Preprocessing

#### 1. Target Variable for the model

- **IS_SUCCESSFUL** will be the target variable for this model

<img src="Resources/target_variable.PNG"/>

#### 2. Feature Variables for the model

- **APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, INCOME_AMT, SPECIAL_CONSIDERATIONS** will be the features for this model

<img src="Resources/feature_variables.PNG"/> 

#### 3. Variables to be removed

- Non-beneficial variables of **NAME** and **EIN** will be removed from this model

<img src="Resources/removed_variables.PNG"/> 

### Compiling, Training, and Evaluating the Model

#### Original Model

- Hidden Layers: 2
- Layer 1 Nodes/Activation Feature: 90/ReLU
- Layer 2 Nodes/Activation Feature: 30/ReLU
- Output Layer Activation Feature: Sigmoid
- Epochs = 100

<img src="Resources/original.PNG"/>
<img src="Resources/summary_original.PNG"/>

- The original model was not able to achieve the target model **75%** accuracy.

The following attempts were made to increase model performance: 

#### 1. Optimized Model - Attempt 1

- Change activation features for hidden layers, decrease node count, decrease epochs:
	- Hidden Layers: 2
	- Layer 1 Nodes/Activation Feature: 40/Sigmoid
	- Layer 2 Nodes/Activation Feature: 20/Sigmoid
	- Output Layer Activation Feature: Sigmoid
	- Epochs = 10

<img src="Resources/attempt_1.PNG"/>
<img src="Resources/attempt_1_summary.PNG"/>

#### 2. Optimized Model - Attempt 2

- Add hidden layer, decrease node count, decrease epochs:
	- Hidden Layers: 3
	- Layer 1 Nodes/Activation Feature: 40/ReLU
	- Layer 2 Nodes/Activation Feature: 20/ReLU
	- Layer 3 Nodes/Activation Feature: 10/ReLU
	- Output Layer Activation Feature: Sigmoid
	- Epochs = 15

<img src="Resources/attempt_2.PNG"/>
<img src="Resources/attempt_2_summary.PNG"/>

#### 3. Optimized Model - Attempt 3

- Add hidden layer, decrease node count, decrease epochs:
	- Hidden Layers: 4
	- Layer 1 Nodes/Activation Feature: 100/ReLU
	- Layer 2 Nodes/Activation Feature: 80/ReLU
	- Layer 3 Nodes/Activation Feature: 60/ReLU
	- Layer 4 Nodes/Activation Feature: 10/ReLU
	- Output Layer Activation Feature: Sigmoid
	- Epochs = 20

<img src="Resources/attempt_3.PNG"/>
<img src="Resources/attempt_3_summary.PNG"/>

## Summary

- The original model achieved **70%** accuracy which does not meet the targeted accuracy of **75%**
- After 3 attempts to optimize the original model, the model was still unable to achieve the desired accuracy.
- The closest result was **73%** on **Attempt 2**, by reducing the epochs to 15, adding an additional third hidden layer, and reducing the node count for each hidden layer.

#### Recommendations to achieve the 75% accuracy for future models:
- Adjust the source data to remove outliers or variables that are confusing the model.
- Create additional bins for rare occurrences in columns.
- Increase or decrease the value for each bin.
- Remove additional unnecessary columns.


