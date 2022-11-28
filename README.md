# ANN - Artificial Neural Network from scratch

**Abstract**

Implementation of a Neural Network from scratch with a customized pipeline to parameter tuning and cross validation.

The algorithm was tested in a binary problem (Breast Cancer Dataset from sklearn) and a multiclass problem (mental imagery dataset - available at https://www.bbci.de/competition/iii/desc_V.html)

The algorithm used is a single hidden layer neural network, using sigmoid activation in all neurons. The bisection algorithm was used to find the best learning rate and speed up convergence.

The pipeline used to find the best configuration considering accuracy is described in the image below.

![fluxo](https://user-images.githubusercontent.com/54689450/204160174-ea225fb6-0603-4d9f-837e-582ec4680f9e.png)

Remarks:
- The only parameter tested was the number of hidden layers
- The dataset was initally divided in training and test set (80% train and 20% test). The training was used for cross valitadion with k=5 folds (64% train cv - 16% validation cv). The best parameters selected in this phase were finally used to retrain the neural network in the entire training datatset
- The process described was repeted 5 times (results confidence)
- In the multiclass problem it was used Prinicipal Component Analysis with 30 components
- The data was normalized used z-score
