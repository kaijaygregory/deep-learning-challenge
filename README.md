# __deep-learning-challenge__

# __Alphabet Soup Charity Deep Learning Project__

## __Background__
Alphabet Soup, a nonprofit foundation, seeks a predictive tool to assist in selecting funding applicants likely to succeed in their ventures. Utilizing machine learning and neural networks, this project aims to create a binary classifier predicting the success of Alphabet Soup-funded organizations based on provided dataset features.

The dataset comprises over 34,000 organizations that received Alphabet Soup funding, containing columns capturing metadata, such as:

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

## __Setup and Preprocessing Instructions__ 

Follow Google Colab Instructions

## __Project Workflow__

__Step 1: Preprocessed the Data__

-Read charity_data.csv into a Pandas DataFrame.
-Identified target and feature variables.
-Dropped EIN and NAME columns.
-Determined unique values and data point counts for columns.
-Binned rare categorical variables.
-Encoded categorical variables using pd.get_dummies().
-Split data into features (X) and target (y) arrays.
-Split preprocessed data into training and testing datasets.
-Scaled training and testing features using StandardScaler.

__Step 2: Compiled, Trained, and Evaluated the Model__
-Designed neural network model with appropriate layers and activations.
-Compiled, trained, and evaluated the model.
-Saved the model's weights every five epochs.
-Evaluated the model's performance using test data.
-Exported results to AlphabetSoupCharity.h5.

__Step 3: Optimize the Model__
-Created a new Google Colab file for optimization.
-Repeated preprocessing steps.
-Implemented model optimization methods.
-Saved optimized model as AlphabetSoupCharity_Optimization.h5.()

__Step 4: Composed a Report on the Neural Network Model That Provides the Following:
- An overview of the analysis.
- Addresses questions on Data Preprocessing and Model Compilation, Training, and Evaluation.
- Summarizes overall model results and suggests alternative approaches.
