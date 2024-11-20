# credit-risk-classification

Overview of the Analysis

This analysis evaluates the performance of a logistic regression model in predicting loan statuses, specifically distinguishing between healthy loans (0) and high-risk loans (1). The analysis used financial data provided in lending_data.csv, which includes various features describing the loans and their associated risk status.

Key Steps:

	1.	Data Preparation:
		Loaded the data into a Pandas DataFrame.
		Split the data into labels (y, the loan_status column) and features (X, the remaining columns).
		Used train_test_split to divide the data into training and testing sets.
	2.	Model Development:
		Created a logistic regression model using the training data (X_train and y_train).
		Used the fitted model to generate predictions for the testing dataset (X_test).
	3.	Evaluation:
		Evaluated model performance using a confusion matrix and a classification report.
		Analyzed the accuracy, precision, recall, and F1-score to determine the model’s effectiveness.

Results

Logistic Regression Model

	•	Accuracy: 99%
	•	The model correctly classified 99% of loans overall.
	•	Precision:
	•	Healthy Loans (0): 100%		
		(All predicted healthy loans are truly healthy.)
	•	High-Risk Loans (1): 84%
		(16% of loans predicted as high-risk are misclassified.)
	•	Recall:
	•	Healthy Loans (0): 99%
		(1% of actual healthy loans were misclassified.)
	•	High-Risk Loans (1): 94%
		(6% of actual high-risk loans were missed.)

### Confusion Matrix:
The confusion matrix highlights the model’s performance:

- **True Positives (`1` correctly identified):** High.
- **False Positives (`0` incorrectly predicted as `1`):** Some misclassification.
- **True Negatives (`0` correctly identified):** Very high.
- **False Negatives (`1` incorrectly predicted as `0`):** Minimal.

Summary

The logistic regression model demonstrates strong performance:
	•	Strengths: Near-perfect predictions for healthy loans (0) with a precision of 100% and recall of 99%.
	•	Limitations: While the model performs well for high-risk loans (1), it occasionally misclassifies healthy loans as high-risk, indicated by a precision of 84%.

Recommendation:
This model is recommended for use due to its overall high accuracy and reliability. However, since the identification of high-risk loans (1) is critical, further refinement is advised. Techniques such as addressing class imbalance or adjusting the decision threshold could reduce false positives, improving the model’s performance for high-risk loans while maintaining its strength in identifying healthy loans.
