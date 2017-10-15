# DSG_Solution #

## Description ##
This is my solution to the DSG problem statement. The model has been built using the concept of ensemble stacking to make
predictions on the final test set. 

## Libraries Used ## 
* Pandas
* Numpy 
* Scikit-Learn 

## Algorithms on which the model has been built ## 
### Tier-1 algorithms ###
* Random Forest Classifier 
* ADA Boost
* Gradient Boost 
* SVM 

### Tier-2 algorithms ###
* Xtreme gradient boost

## Oveview of the approach followed ##
* First came the data exploration stage. Here I found the correlation among the various features to determine if any of the 
features were correlated . However I could not find any features which were heavily correlated so I decided to go along 
with all the features provided in the dataset.
* Now came the data processing part wherein I normalized the feature vectors with numerical values to make the algorithms 
which use gradient descent converge faster.
* Since label encoder is known to give performance issues by injecting false information into the dataset, I chose to create
dummmy variables to deal with this situation. Now this raises the problem of imbalance in the number of features in the test
and the training set whcih I rectified by initializing all the missing features to 0. 
* Now I employed K-fold classification to split the training set into 4 folds and train the algos which made up the first tier
of my model. After the training phase is over, it's predictions are then used as feature vectors to train the second tier 
of the model which then makes the final predictions.

## References ## 
* Introduction to ensemble stacking blog on kaggle 
* Analytics Vidhya 
* Offical documentation for sklearn 

