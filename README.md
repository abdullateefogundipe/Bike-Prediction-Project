# bike-pred-project
# Report: Predict Bike Sharing Demand with AutoGluon Solution
#### OGUNDPE ABDULLATEEF

## Initial Training
### What did you realize when you tried to submit your predictions? What changes were needed to the output of the predictor to submit your results?
TODO: Add your explanation
I noticed that the predictions are float and some are non-positive values which was not accepted for submission. 
The changesI made was to round up all predictions to whole number and equate all negative numbers to zero

### What was the top ranked model that performed?
TODO: Add your explanation
The top ranked that performed was weIghted ensemble model

## Exploratory data analysis and feature creation
### What did the exploratory analysis find and how did you add additional features?
TODO: Add your explanation
1.The exploratory analysis that I did was to check the columns of the train and test set. With this, I noticed there are two columns that are in the train dataset but not
in the test set which are (casual and registered). So I had to remove them from the train data before fitting.
2.I converted the date feature in the test and train dataset to be a timestamp and extracted year, month, date, hour as additional feature for training.
3.I change the datatype of season and weather to category

### How much better did your model preform after adding additional features and why do you think that is?
TODO: Add your explanation
After added additional feature, my scoregreatly improved from 1.28838 to 0.49727. I think ths improvement happened due to model having much features to consider before arrivng at a final predicton, thereby increasing accuracy.
## Hyper parameter tuning
### How much better did your model preform after trying different hyper parameters?
TODO: Add your explanation
My model pefromed didn't perform better after trying the first hyperparameter tuning from a score of 0.49727 to 0.50834.
it later performed better in the third hyper paprameter tuning from a score of 0.49727 to 0.49107.

### If you were given more time with this dataset, where do you think you would spend more time?
TODO: Add your explanation
1.I will create more features
2.I will ty more hyperparameter tuning
3.I will find correlation between the features and the target. This will enable me to train my model with necessary and important features.


### Create a table with the models you ran, the hyperparameters modified, and the kaggle score.
|model|hpo1|hpo2|hpo3|score|
|--|--|--|--|--|
|initial|?|?|?|?|
|add_features|?|?|?|?|
|hpo|?|?|?|?|
 
Answer:

	model			sample_weight	time_limit	eval_metric		score
0	predictor_new_hpo	none		10mins		mean absolute error	0.50834
1	predictor_new_hpo2	auto_weight	10mins		root mean squared error	4.76188
2	predictor_new_hpo3	balance_weight	5mins		mean squared error	0.49170



### Create a line plot showing the top model score for the three (or more) training runs during the project.
The picture has been attached to the file 

TODO: Replace the image below with your own.
(C:\Users\drogu\Downloads\PROJECT 1 CORRECTION 2/model_train_score.png)

### Create a line plot showing the top kaggle score for the three (or more) prediction submissions during the project.
The picture has been attached to the file 

TODO: Replace the image below with your own.
(C:\Users\drogu\Downloads\PROJECT 1 CORRECTION 2/model_test_score.png)

## Summary
TODO: Add your explanation
The project examines the performance of a training work. The first set of training that was done involves using the raw data given to fit the TabularPredictor.
The result from this was alittle bit poor. Then the data was cleaned and new features was generated. This imporved the accuracy. Lastly, several hyperparameter tuning 
was carried out to see its effect. The project was an eye opener to vaious ways to increase the accuracy of a model



