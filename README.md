# Neural_Network_Charity_Analysis-

## Overview of the analysis

The purpose of this analysis is to deisgn a neural network to help the foundation predict where to make investments. The model will create a binary classifier that is capable of predicting whether loan applicants will be successful if funded by Alphabet Soup.

## Results: Using bulleted lists and images to support your answers, address the following questions.

1.  Data Preprocessing

- The column IS_SUCCESSFUL contains binary data refering to weither or not the charity donation was used effectively. Therefore this variable is considered as the target of the model.
- The categorical or feature columns were:  APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMT. 
- Two columns were removed from the input data, the columns EIN and NAME. 
- For the optimized version, I removed special_considerations and status. This with the purpose to see if the model worked better using less features. 

2. Compiling, Training, and Evaluating the Model

- This deep-learning neural network model is made of two hidden layers with 80 and 30 neurons respectively.
The input data has 43 features and 25,724 samples.
The output layer is made of a unique neuron as it is a binary classification.
To speed up the training process, we are using the activation function ReLU for the hidden layers. As our output is a binary classification, Sigmoid is used on the output layer.
For the compilation, the optimizer is adam and the loss function is binary_crossentropy.
- The model accuracy is under 75%. This is not a satisfying performance to help predict the outcome of the charity donations.
- To increase the performance of the model, we applied bucketing to the feature ASK_AMT and organized the different values by intervals. We increased the number of neurons on one of the hidden layers, then we used a model with three hidden layers. We also tried a different activation function (tanh) but none of these steps helped improve the model's performance. Finally we considered using the SVM (support vector machine) model, but this one didn't perform well either. 

## Summary: Summarize the overall results of the deep learning model. Include a recommendation for how a different model could solve this classification problem, and explain your recommendation.

Overall, it could be stated that none of the models that we implemented have a high accuracy. We tried both a deep learning model and a Support Vector MAchine to solve this classification problem. However, it seems that this problem requieres a different model. A colleage mentioned Random Forest Classifier because it's a more accurate decision tree algorithm and work. 
For example, in this scenario the Random Forest Classifier would work as follow. The root node and decision nodes represent the features of the organization asking for the loan. The leaf node represents the final output, whether the organization was succesful or not. The main features that determine the sucess include the application type, the use case, the income amount, the ask amount, the organization type, and so on. 
It would be interesting to design this model and run it to see its accuracy level. Specially since it seems that it would be a good fit. 