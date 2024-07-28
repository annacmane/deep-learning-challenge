# Overview of the Analysis
The objective of this analysis was to create a tool that can help the nonprofit foundation Alphabet Soup to select applicants for funding with the best chance of success in their ventures. Using a CSV that contains more than 34,000 organizations that Alphabet Soup has funded over the years, we will use the features in the provded dataset to create a binary classifier that can predict whether applicants will be successful if funded by Alphabet Soup.

# Results
* Data Processing:
    * Target Variable(s): The target variable for the model is the "IS_SUCCESSFUL" column, which indicates whether the funding was used effectively (1) or not (0).
    * Feature Variable(s): The model includes the following columns:
    EIN and NAME—Identification columns
    APPLICATION_TYPE—Alphabet Soup application type
    AFFILIATION—Affiliated sector of industry
    CLASSIFICATION—Government organization classification
    USE_CASE—Use case for funding
    ORGANIZATION—Organization type
    STATUS—Active status
    INCOME_AMT—Income classification
    SPECIAL_CONSIDERATIONS—Special considerations for application
    ASK_AMT—Funding amount requested
    IS_SUCCESSFUL—Was the money used effectively
    * Excluded Variables: 
    "EIN" and "NAME" removed from 1st, 2nd, and 3rd attempt as not directly linked to the probability of success. "STATUS" and "SPECIAL_CONSIDERATIONS" removed from the 2nd and 3rd attempt as they did not improve accuracy of the model.

# Compiling, Training, and Evaluating the Model
First Attempt: (Starter_Code.ipynb)
* Number of Neurons:8 nodes in layer 1, 5 nodes in layer 2
* Number of Layers: 2
* Number of Activation Functions: 100

Second Attempt: (AlphabetSoupCharity_Optimization.ipynb)
* Number of Neurons:13 nodes in layer 1, 10 nodes in layer 2
* Number of Layers: 2
* Number of Activation Functions: 100

Second Attempt: (AlphabetSoupCharity_Optimization.ipynb)
* Number of Neurons:117 nodes in layer 1, 178 nodes in layer 2, and 39 in layer 3
* Number of Layers: 3
* Number of Activation Functions: 150

Out of all 3 attempts, I was not able to reach the targeted 75% accuracy. First attempt showed an accuracy of 72.69%. After the slight changes to the number of nuerons in the layers, it increased by 0.17%. On the third attempt, I checked to see the shape of the X_train (39) and changed the number of neurons in each layer while adding a third layer. Additionally, the activation functions were increased by 50 which resulted in an accuracy of 73.03%.

Overall, I believe the model can acheive a 75% accuracy by increasing the number of neurons, having around 3-6 layers and increasing the number of activiation functions. 

