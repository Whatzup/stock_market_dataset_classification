Problem Statement:
	You are expected to pre-process/transform data, perform exploratory analysis/visualization build classifier(s)  and provide evaluation matrix.
		No. records - 50,000
		No. of features - 63 (Numerical as well as categorical)
	Target variable marked as Y (Binary classification)

Data Overview:
	The dataset contains an anonymized set of variables, each representing a random feature.
	Target: The ground truth is labelled ‘Y’ and represents the categorical output.

Mapping the Business problem to a Machine Learning problem
	This is a classification problem to predict the Y. This solution includes three classification algorithms:
		1. Logistic Regression.
		2. Decision Tree Classifier.
		3. Random Forest Classifier.
	This addresses the challenge of the business problem.

Performance Metric
	Just as exams are conducted to evaluate our knowledge in the subject, performance metric is an exam that a 
	trained ML model has to pass with flying colours. Performance metrics help us evaluate the performance of 
	our models on train(seen) and test(unseen) data. 
	The performance metric used in this case study are:
		Accuracy
		Precision
		Recall
		F1 score
		Confusion Matrix

1. Load required libraries

2. Load and explore dataset.
	We start with loading the downloaded train & test csv files into the jupyter notebook environment using pandas.

3. Remove nulls if any.
	This step involves checking for Not a number(NaN)/missing values. In case you encounter NaN’s then data imputation.
	(like mean,median or mode replacement) techniques can help mitigate this problem.

4. See if dataset is balanced or imbalanced.
	Draw countplot to check balance of the data.

5. Convert text columns into numerical columns using dummy variables

6. Find correlation among feature in original dataset.

7. Use PCA for dimensionality reduction.
	This stage involves removing duplicate features and features having very low variance. 
	Low variance implies that a particular column is dominated with a particular value and that there is no diversity among values.

8. Divide the data into training set and testing set
	Once the final data is prepared, now let us randomly split the train data into X_train and X_test in 80:20 ratio where 80% 
	of train data goes to X_train & the rest 20% goes to X_test. Here X_test represents the cross validation set which is used 
	to assess the model performance on unseen data. Also the test data here is untouched and will only be used for 
	predictions by a final trained model.
9. Models
	Let us try out various linear and non-linear regression algorithms and check the performance.
10. Use Logistic regression for classification
	Calculate performance matrices (Accuracy, precision, recall, F1 score)
	Calculate confusion matrix.
11. Use Decision Tree classifier.
	Calculate performance matrices (Accuracy, precision, recall, F1 score)
	Calculate confusion matrix.
12. Use Random Forest classifier.
	Calculate performance matrices (Accuracy, precision, recall, F1 score)
	Calculate confusion matrix.