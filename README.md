# An Analysis of Charities Using a Neural Network
## Overview
### In order to determine the best machine learning model to use when trying to predict credit risk, 6 different models were applied to the data. As credit risk data is inherently imbalanced, models were specifically chosen to address this.
## Results
### RandomOverSampler
* Balanced accuracy score of 0.65
* Average precision of 0.99
* Average recall of 0.59
![RandomOverSampler](https://github.com/NickBaldassarre/Credit_Risk_Analysis/blob/71e39cafddc87e1148ac12806955288ed2ffda36/Resources/RandomOverSampler.png)
### SMOTE
* Balanced accuracy score of 0.66
* Average precision of 0.99
* Average recall of 0.69
![SMOTE](https://github.com/NickBaldassarre/Credit_Risk_Analysis/blob/71e39cafddc87e1148ac12806955288ed2ffda36/Resources/SMOTE.png)
### ClusterCentroids
* Balanced accuracy score of 0.54
* Average precision of 0.99
* Average recall of 0.40
![ClusterCentroids](https://github.com/NickBaldassarre/Credit_Risk_Analysis/blob/71e39cafddc87e1148ac12806955288ed2ffda36/Resources/ClusterCentroids.png)
### SMOTEEN
* Balanced accuracy score of 0.64
* Average precision of 0.99
* Average recall of 0.57
![SMOTEEN](https://github.com/NickBaldassarre/Credit_Risk_Analysis/blob/71e39cafddc87e1148ac12806955288ed2ffda36/Resources/SMOTEEN.png)
### BalancedRandomForestClassifier
* Balanced accuracy score of 0.79
* Average precision of 0.99
* Average recall of 0.87
![BalancedRandomForestClassifier](https://github.com/NickBaldassarre/Credit_Risk_Analysis/blob/71e39cafddc87e1148ac12806955288ed2ffda36/Resources/BalancedRandomForestClassifier.png)
### EasyEnsembleClassifier
* Balanced accuracy score of 0.93
* Average precision of 0.99
* Average recall of 0.94
![EasyEnsembleClassifier](https://github.com/NickBaldassarre/Credit_Risk_Analysis/blob/71e39cafddc87e1148ac12806955288ed2ffda36/Resources/EasyEnsembleClassifier.png)
## Summary
There are certainly machine learning models that are better suited to analyzing this dataset than others. Undersampling is the least successful in providing the most accurate predictions, with the lowest scores in balanced accuracy and average recall. Oversampling methods fared a little bit better, but not enough to make them viable options. The BalancedRandomForestClassifier saw a significant improvement over undersampling and oversampling methods, with a balanced accuracy score of 0.79 and average recall of 0.87. The EasyEnsembleClassifier however was far and above the best performing model, with a balanced accuracy score of 0.93 and average recall of 0.94. The average F1 score of 0.97 solidifies that this model will be effective in predicting credit risk.

My recommendation is to use the EasyEnsembleClassifier to predict credit risk. 
