# __Neural Network Model Report__

## __Overview of the analysis:__

Alphabet Soup, a nonprofit foundation, seeks a predictive tool to assist in selecting funding applicants likely to succeed in their ventures. Utilizing machine learning and neural networks, this project aims to create a binary classifier predicting the success of Alphabet Soup-funded organizations based on provided dataset features.

## __Results:__ 

__Data Preprocessing__

__What variable(s) are the target(s) for your model?__

The target variable is "IS_SUCCESSFUL". This column represents whether the funding allocated was effectively used.

__What variable(s) are the features for your model?__

All columns except "IS_SUCCESSFUL" are features for the model. These columns provide various metadata about the organizations:
-__EIN and NAME:__  Identification columns
-__APPLICATION_TYPE:__  Alphabet Soup application type
-__AFFILIATION:__ Affiliated sector of industry
-__CLASSIFICATION:__ Government organization classification
-__USE_CASE:__ Use case for funding
-__ORGANIZATION:__ Organization type
-__STATUS:__ Active status
-__INCOME_AMT:__ Income classification
-__SPECIAL_CONSIDERATIONS:__ Special considerations for application
-__ASK_AMT:__ Funding amount requested
-__IS_SUCCESSFUL:__ Money utilization effectiveness indicator


__What variable(s) should be removed from the input data because they are neither targets nor features?__
The "EIN" and "NAME" columns are removed, as they are non-beneficial identification columns for predicting success.

## __Compiling, Training, and Evaluating the Model__

__How many neurons, layers, and activation functions did you select for your neural network model, and why?__

__The model comprises:__

Input layer: 43 input features.
First hidden layer: 80 neurons with ReLU activation.
Second hidden layer: 30 neurons with ReLU activation.
Output layer: 1 neuron with sigmoid activation for binary classification.

__Reasoning for the Model's Architecture:__

The choice of 80 neurons in the first hidden layer and 30 neurons in the second hidden layer might have been based on the complexity of the dataset and experimentation.
ReLU activation is commonly used for hidden layers to introduce non-linearity, and sigmoid activation in the output layer is appropriate for binary classification tasks.

__Were you able to achieve the target model performance?__


The model's performance after training for 100 epochs is as follows:

Loss: 0.561

Accuracy: 72.61%

The model achieved an accuracy of approximately 72.61% on the test dataset. While it's a decent accuracy, it might not meet the target threshold of over 75%. Consider further optimizing the model to improve its performance.

__What steps did you take in your attempts to increase model performance?__

The steps taken to enhance the model's performance involved a systematic approach. Initially, additional non-beneficial columns ('SPECIAL_CONSIDERATIONS' and 'USE_CASE') were removed from the dataset to streamline the feature set for the model. Subsequently, adjustments were made to the neural network's architecture. The input dimension was modified from 43 to 36 after dropping these columns. In the hidden layers, modifications included reducing the number of units in each layer: the first hidden layer was adjusted to 50 units with ReLU activation, the second to 40 units with tanh activation, the third to 30 units with sigmoid activation, and the fourth to 20 units with ReLU activation. The output layer retained 1 unit with sigmoid activation for binary classification. The changes were carefully designed to fine-tune the model's architecture, aiming to improve its capacity to recognize patterns and optimize predictive performance. Despite the adjustments made to the model's architecture, the accuracy remains around 72.23%. While there was a marginal change in accuracy, it's still below the 75% threshold. Further optimization or exploration of different model architectures or hyperparameters may be considered to achieve the target performance.



__Summary:__ 

The deep learning model developed for the classification problem of predicting success in Alphabet Soup's funding achieved an accuracy of approximately 72.23% after extensive adjustments to its architecture. Despite these efforts, the model fell short of the target accuracy threshold of 75%. The model underwent various modifications, including feature selection, altering the neural network architecture by adjusting layers, units, and activation functions, aiming to enhance predictive capability. However, these alterations yielded only marginal improvements.

![Removig Additional Columns](https://github.com/kaijaygregory/deep-learning-challenge/blob/main/Images/Removing%20Additional%20Columns.png)

![Adjusting Architecture](https://github.com/kaijaygregory/deep-learning-challenge/blob/main/Images/Adjusting%20Architecture.png)

![Updated Accuracy](https://github.com/kaijaygregory/deep-learning-challenge/blob/main/Images/Updated%20Accuracy.png)

A different approach to address this classification problem could involve utilizing an ensemble learning technique, specifically a Random Forest or Gradient Boosting model. Ensemble methods combine predictions from multiple models to improve accuracy and robustness. In the case of Random Forest, it builds numerous decision trees and aggregates their outputs, making it less prone to overfitting. Gradient Boosting, on the other hand, builds trees sequentially, learning from the errors of the previous trees, and can be optimized for better performance.

Ensemble methods often perform well in scenarios where single models struggle, such as when dealing with noisy or complex datasets. Incorporating an ensemble approach like Random Forest or Gradient Boosting could potentially improve classification accuracy by leveraging the strengths of multiple models, thereby enhancing the prediction of successful funding outcomes for Alphabet Soup.

