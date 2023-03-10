# Neural_Network_Charity_Analysis

## Overview of the analysis: 
Beks has come a long way since her first day at that boot camp five years ago—and since earlier this week, when she started learning about neural networks! Now, she is finally ready to put her skills to work to help the foundation predict where to make investments.<br/>
With the knowledge of machine learning and neural networks, this analysis will help Beks create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup.<br/>
From Alphabet Soup’s business team, Beks received a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years. Within this dataset are a number of columns that capture metadata about each organization, such as the following:<br/>
* EIN and NAME—Identification columns
* APPLICATION_TYPE—Alphabet Soup application type
* AFFILIATION—Affiliated sector of industry
* CLASSIFICATION—Government organization classification
* USE_CASE—Use case for funding
* ORGANIZATION—Organization type
* STATUS—Active status
* INCOME_AMT—Income classification
* SPECIAL_CONSIDERATIONS—Special consideration for application
* ASK_AMT—Funding amount requested
* IS_SUCCESSFUL—Was the money used effectively

### Objectives:
* Deliverable 1: Preprocessing Data for a Neural Network Model
* Deliverable 2: Compile, Train, and Evaluate the Model
* Deliverable 3: Optimize the Model
* Deliverable 4: A Written Report on the Neural Network Model (README.md)



## Results: 
### Data Preprocessing

#### What variable(s) are considered the target(s) for your model?
The target variable for the model is 'IS_SUCCESSFUL'.

#### What variable(s) are considered to be the features for your model?
The feature variable for the model are:
* APPLICATION_TYPE
* AFFILIATION
* CLASSIFICATION
* USE_CASE
* ORGANIZATION
* STATUS
* INCOME_AMT
* SPECIAL_CONSIDERATIONS
* ASK_AMT

#### What variable(s) are neither targets nor features, and should be removed from the input data?
The variable 'EIN' and 'NAME' are removed from the dataset. Thus, these are neither the targets nor features.


### Compiling, Training, and Evaluating the Model
#### How many neurons, layers, and activation functions did you select for your neural network model, and why?
My neural network model had 2 hidden layers. The first hidden layer had 80 neurons and the second layer had 30 neurons. The activation function selected for input layers was 'relu' and for the output layer was 'sigmoid'. The reason for selecting 'relu' for the input layer is that the model trained with it converges quickly and take much lesser time as compared to other activation functions. For the Output layer, it is good to have 'sigmoid' activation function, as the range of output given by it is 0 and 1, which is best for our model here.

<img width="962" alt="Screen Shot 2023-01-18 at 11 47 34 PM" src="https://user-images.githubusercontent.com/111387025/213262310-507e541e-7dad-4951-876f-3bb4ff5d16cd.png">


#### Were you able to achieve the target model performance?
The accuracy of my model was 69% which was lower than the target performance of 75%.

<img width="791" alt="Screen Shot 2023-01-19 at 12 45 54 PM" src="https://user-images.githubusercontent.com/111387025/213379415-59228057-0bcf-41cf-a638-695f006091c5.png">


#### What steps did you take to try and increase model performance?
#### Attempt 1: Dropping more columns:
* By dropping additional 2 columns in the data set - 'SPECIAL_CONSIDERATIONS','USE_CASE', the accuracy remained **69%**. Thus, the model performance showed an improvement.

<img width="699" alt="Screen Shot 2023-01-19 at 12 00 13 PM" src="https://user-images.githubusercontent.com/111387025/213371705-1f1e10bd-11c0-4699-ba30-e6e991ce2a18.png">

#### Attempt 2: Adding more hidden layers and hidden nodes for each layer.
In the second attempt, one additional hidden layer was added and 100 neurons for first hidden layer, 50 for second and 30 for the third layer. The accuracy dropped to **61%**.

<img width="699" alt="Screen Shot 2023-01-19 at 12 02 36 PM" src="https://user-images.githubusercontent.com/111387025/213372097-e2c8528f-3d24-44c7-a9ba-806eb5fb1bdc.png">

#### Attempt 3: Reducing the number of epochs to the training regimen.
In the third attempt, the number of epochs were reduced to 50. It turned out to be best out of all the attempts and increased the accuracy to **71%**.

<img width="706" alt="Screen Shot 2023-01-19 at 12 04 02 PM" src="https://user-images.githubusercontent.com/111387025/213372290-b1f2d316-5144-47e4-9ef4-a927cc86f041.png">

#### Attempt 4: Changing the acivation function for hidden layers and reducing number of epochs.
The accuracy plunged to **47%**, after changing the activation function of input layers from 'relu' to 'tanh'.

<img width="767" alt="Screen Shot 2023-01-19 at 1 03 40 PM" src="https://user-images.githubusercontent.com/111387025/213382506-4f2302d4-68e4-466d-9528-280589fa636f.png">

## Summary: 
* The initial neural network model gave the accuracy of 69%. 
* In attempts to increase the model performance, various measures were taken such as dropping more columns, adding more layers, reducing number of epochs. 
* The attempts to optimize the models were successful, as the third attempt was able to raise the accuracy to **71%**. However, the accuracy score was still not up to the target performance. 
* Using a larger dataset and adding more hidden layers accordingly can certainly help to improve the model performance.
* Random forest classifier is another great choice, as they are faster and helps to avoid overfitting as well.
* Another way of optimization can be by using keras tuner, as by running the model with it and dropping fewer columns, the accuracy increased to **76%**, as shown below.

<img width="914" alt="Screen Shot 2023-01-19 at 12 39 01 PM" src="https://user-images.githubusercontent.com/111387025/213377982-bf1c766a-2d37-4d9f-bd95-e09d53e0c2a5.png">

<img width="741" alt="Screen Shot 2023-01-19 at 10 18 55 AM" src="https://user-images.githubusercontent.com/111387025/213357903-d62f567b-fc7f-44af-b96d-939b7dcffb82.png">
