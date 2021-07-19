# Neural_Network_Charity_Analysis

## Overview
Alphabet Soup is a philanthroic organization dedicated to helping the environment and improving people's wellbeing. They have fundraised and donated over 10 billion dollars in the past 20 years. This money has been used to invest in life-saving technologies and organize reforestation groups around the world. They provided a CSV dataset of more than 34,000 organizations that have received funding from Alphabet Soup over the years. The objective of this project was to create a binary classifier machine learning model capable of predicting whether applicants will be successful if funded by Alphabet Soup. 


### Tools
* Python
* Pandas
* Matplotlib
* SkLearn
* Tensorflow
* Google Colab

## Results
### Data Preprocessing
#### Raw data DataFrame
{INSERT DATA FRAME SCREENSHOT}

* Target: Is_Successful
* Features:
    * APPLICATION_TYPE
    * AFFILIATION
    * CLASSIFICATION
    * USE_CASE
    * ORGANIZATION	
    * STATUS
    * INCOME_AMT
    * SPECIAL_CONSIDERATIONS
    * ASK_AMT
* Variables to be removed: 
    * EIN
    * Name

The categorical variables were transformed using the OneHotEncoder in order to be in proper format for the machine learning model. The one-hot-encoded data was then merged with the original data frame, and the original categorical values were dropped.  The data was then split in to training and testing groups and scaled. 

#### Merged DataFrame
{INSERT merged DATA FRAME SCREENSHOT}

### Compiling, Training, and Evaluating the Model
The initial instance of the model had 8 nodes in the first layer, and 5 in the second. The sigmoid activation function was used at all layers since it is logistic regression. As well, the model was fit in 50 epochs. This resulted in an accuracy rate of 73.08%. 

{insert results screenshot}


In an attempt to increased the accuracy of the model, the ASK_AMT variable was place in to bins then converted to objects. This adds another dimension to the data which is meant to increase its accuracy. Various changes to the model were applied in addition - such as decreasing and increasing the hidden layers, increasing the number of neurons, using different activation functions, and decreasing the number of epochs to the training regiment. Despite different attempts to increase the accuracy of the model, the highest accuracy score achieved was the first attempt of 73.08%. More experimentation is required to increase the accuracy of the model. 


