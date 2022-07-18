# An Analysis of Charities Using a Neural Network
## Overview
### Using machine learning and neural networks, I created a binary classifier in order to be able to predict whether applicants will be successful in utilizing their funding from Alphabet Soup.
## Results
### Data Preprocessing
* Target variable is IS_SUCCESSFUL
* The features of this model are APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMT
* The variables that are neither targets or features are EIN and NAME and were removed
### Compiling, Training and Evaluating the Model
* 2 hidden layers were selected for this model
* 80 neurons for the first hidden layer and 30 neurons for the second hidden layer were selected
* Relu activation function was used for the hidden layers and sigmoid activation function was used for the output layer
* These were all selected in order to achieve a high degree of accuracy
![First Model](https://github.com/NickBaldassarre/Neural_Network_Charity_Analysis/blob/e465c8fe9fe94ad84bd53c908e2ab2d61ad8140b/Resources/Model_1st.png)
![First Model Accuracy](https://github.com/NickBaldassarre/Neural_Network_Charity_Analysis/blob/e465c8fe9fe94ad84bd53c908e2ab2d61ad8140b/Resources/Accuracy_1st.png)
### Optimization
* I removed the STATUS variable which only very slightly improved the model
* I added neurons to both hidden layers, with 100 in the first and 40 in the second, again with only a slight improvement
* I added 2 additional hidden layers with 20 neurons and 10, again with only a slight improvement
* I experimented with multiple combinations of activation functions and ended up using a combination of relu and tanh functions in the hidden layers, and kept the sigmoid function for the output layer.
* I increased the epochs to 40
![Optimized Model](https://github.com/NickBaldassarre/Neural_Network_Charity_Analysis/blob/e465c8fe9fe94ad84bd53c908e2ab2d61ad8140b/Resources/Model_2nd.png)
![Optimized Model Accuracy](https://github.com/NickBaldassarre/Neural_Network_Charity_Analysis/blob/e465c8fe9fe94ad84bd53c908e2ab2d61ad8140b/Resources/Accuracy_2nd.png)
## Summary
After many attemps with different neural network models, I was not able to achieve an accuracy above 75%. I did find it interesting that when I reduced the number of neurons by a factor of 10, the overall accuracy was not very much affected. Adding addtional hidden layers had a negligible impact on accuracy. The sigmoid function did seem to be the most effective output function, while tanh seemed to work best for the hidden layers. I tried removing almost every column one at a time, to little effect. Ultimately, I don't believe that a neural network is the best model for this data. I reccoemend attempting with a supervised machine learning model such as the EasyEnsembleClassifier.
