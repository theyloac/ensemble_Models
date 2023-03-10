# Ensemble Model Script for Text Classification
This script demonstrates how to build an ensemble model using Python and the scikit-learn library for text classification. The data used in this script consists of text articles from five different topics: business, entertainment, politics, sport, and tech. The goal is to build an ensemble model that can classify new articles into one of these topics.
## Overview
Ensemble models are machine learning models that combine the predictions of multiple individual models to create a more accurate and robust prediction. The idea behind ensemble modeling is that by combining the predictions of multiple models, we can overcome the limitations and weaknesses of any one model, and create a more accurate and reliable prediction.

There is four common ensemble methods: bagging, boosting, stacking and voting. 
1. Bagging: Bagging (Bootstrap Aggregating) is a technique used in ensemble learning where multiple models are trained on different subsets of the training data. Each model is trained independently, and the final prediction is the average of the predictions made by each individual model. Bagging helps to reduce overfitting and improve the stability and accuracy of the model.

2. Boosting: Boosting is another ensemble learning technique where multiple weak models are trained sequentially. Each subsequent model is trained on the errors of the previous model, and the final prediction is the weighted sum of the predictions made by each individual model. Boosting helps to improve the accuracy of the model and reduce bias.

3. Stacking: Stacking is an ensemble learning technique where multiple models are trained, and their predictions are used as input to a meta-model. The meta-model takes the predictions of the individual models as input and generates the final prediction. Stacking helps to reduce bias and improve the accuracy of the model.

4. Voting: Voting is an ensemble learning technique where multiple models are trained independently, and the final prediction is made by taking a simple majority vote of the predictions made by each individual model. Voting can be done with "hard" or "soft" voting, depending on whether the predictions are binary or probabilistic. Voting helps to reduce variance and improve the accuracy of the model.

In summary, bagging and boosting focus on training multiple models independently, while stacking and voting focus on combining the predictions of multiple models to improve the accuracy and stability of the final model.

In this script I will apply stacking and voting methods. To optmize the voting model we perform a for loop with two iterations: one for a "soft" voting classifier and another for a "hard" voting classifier. This will help to indentify the best hyperparamenter to be used.

In "hard" voting, the final prediction of the voting classifier is the majority vote of the individual models. That is, the prediction with the most votes is selected as the final prediction. This method is most effective when the individual models in the ensemble have high accuracy and make different types of errors.

In "soft" voting, the final prediction of the voting classifier is the weighted average of the predicted probabilities of the individual models. That is, the predicted probabilities of each class are summed across all models, and the class with the highest probability sum is selected as the final prediction. This method is most effective when the individual models in the ensemble have high accuracy and make similar types of errors.

In summary, "hard" voting is a simple method that selects the most common prediction, while "soft" voting is a more nuanced method that takes into account the confidence of each model's prediction. The choice between the two methods depends on the characteristics of the individual models and the data being used for prediction.


# Dataset
The dataset consists of text articles from five different topics: business, entertainment, politics, sport, and tech. The dataset can be found: http://mlg.ucd.ie/datasets/bbc.html.

The text data will be preprocessed to remove any stop words and non-alphabetic characters, and then converted into numerical features using scikit-learn's TfidfVectorizer.
## References
https://www.datascienceacademy.com.br/

## Contact
https://www.linkedin.com/in/theylo-antunes-chaves-6696201b6/
## I hope this helps! Let me know if you need any further assistance.
