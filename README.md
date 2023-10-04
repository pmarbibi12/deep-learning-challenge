# deep-learning-challenge
by Panfilo Marbibi

# Contents
- AlphabetSoupCharity.ipynb
- AlphabetSoupCharity.h5
- AlphabetSoupCharity_Optimizatrion.ipynb

# Summary
- This project aims to utilize supervised machine learning to develop a predictive model for assessing the success of funding for a company.
- The Jupyter notebook, "AlphabetSoupCharity.ipynb," retrieves data from "https://static.bc-edx.com/data/dl-1-2/m21/lms/starter/charity_data.csv."
- The CSV data is imported into a Pandas dataframe for further analysis.
- The notebook proceeds to preprocess the data, which involves removing non-categorical columns, binning specific columns to reduce unique values, one-hot encoding using pd.get_dummies(), splitting the data into training and testing sets, and standardizing the features with StandardScaler.
- Utilizing TensorFlow, a neural network or deep-learning model is designed to create a binary classification model.
- The model is trained, and its performance is evaluated.

# Machine-Learning Analysis and Report
- Overview
    - Create a model that will help Alphabet Soup select applicants for funding with the best chance of success in their ventures.
- Results
    - Data Processing
        - Target for the model - "IS_SUCCESSFUL"
        - Features for the model:
            - "APPLICATION_TYPE"
            - "AFFILIATION"
            - "CLASSIFICATION"
            - "USE_CASE"
            - "ORGANIZATION"
            - "STATUS"
            - "INCOME_AMT"
            - "SPECIAL_CONSIDERATIONS"
            - "ASK_AMT"
        - Removed:
            - "NAME"
            - "EIN"
    - Compiling, Traing, and Evaluation
        - Initial Model
            - 3 Total Layers
            - 1st Layer - 80 neurons - RELU
            - 2nd Layer - 30 neurons - RELU
            - 3rd Layer - 1 neuron - SIGMOID
            - Loss: 0.559
            - Accuracy: 0.7296
        - Optimization Model
            - 3 Total Layers
            - 1st Layer - 80 neurons - RELU
            - 2nd Layer - 100 neurons - RELU
            - 3rd Layer - 1 neuron - SIGMOID
            - Loss: 0.572
            - Accuracy: 0.7278
        - Optimization Model 2
            - 3 Total Layers
            - 1st Layer - 80 neurons - RELU
            - 2nd Layer - 100 neurons - RELU
            - 3rd Layer - 30 neurons - RELU
            - 4th Layer - 1 neuron - SIGMOID
            - Loss: 0.595
            - Accuracy: 0.7266
        - Optimization Model 3
            - 3 Total Layers
            - 1st Layer - 30 neurons - RELU
            - 2nd Layer - 30 neurons - RELU
            - 3rd Layer - 30 neurons - RELU
            - 4th Layer - 30 neurons - RELU
            - 5th Layer - 1 neuron - SIGMOID
            - Loss: 0.570
            - Accuracy: 0.7279
    - Summary
        - This deep-learning model was able to achieve, at the highest, an accuracy of 73% with a loss of 56%. Running more than 100 epochs resulted in over-fitting of the training data and resulting in a lower accuracy score with the test data. More categories or meaningful features would probably have resulted in a more accurate model.