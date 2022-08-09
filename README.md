# Lead Scoring Case Study Summary Report
Steps Involved in Solving the Case Study:
1. Importing and reading the dataset. <br>
•	Importing the “Leads.csv” dataset into python.<br> 
2. Inspecting the dataset. <br>
•	We looked into the shape, info, and statistical aspects of the dataset. <br>
3. Data Preparation. <br>
•	Checked for missing values. <br>
•	Dropped columns having more than 40% missing values.<br> 
•	Replacing NaN values with mode/new category values.<br> 
•	Checked for outliers and treated them using capping and flooring method.<br>
4. EDA. <br>
•	Created Univariate analysis plots.<br>
•	Created plots with hue = target variable. <br>
•	Created Correlation heatmap and pairplot.<br>
5. Dummy Variable Creation.<br>
•	Created dummy variables for categorical variables.<br>
6. Train-Test Split. <br>
•	We Put all feature variables in X and Target variable in y. <br>
•	We Split the dataset into train and test set in the ratio of 70:30. <br>
7. Feature Scaling. <br>
•	Standard scaler scales the features so that the predictors have a mean of 0 and standard deviation of 1.<br>
8. Model Building:<br>
•	Using RFE (recursive feature elimination) to select top 15 variables for our model. <br>
•	We built a model with the features selected by RFE using StatsModels. <br>
•	Dropped Insignificant features having high p-value and High VIF value. <br>
•	We repeated the model building process till we arrived to a model with features having normal p-value and VIF values. <br>
•	We then predicted the values on train set. <br>
•	Created a confusion matrix and checked the accuracy, sensitivity and specificity of our model.<br>
9. Plotting ROC Curve(Receiver operating characteristic):<br>
•	We then plotted a ROC curve, higher the area under the ROC curve the better is your model. The value of ROC curve should be closer to 1, we have the area under ROC curve = 0.96.<br>
10. Finding Optimal Cutoff Point. <br>
•	From the plot we decided to take the cutoff point of 0.2. <br>
•	After taking the cutoff point of 0.2 we created a confusion matrix and checked the accuracy, sensitivity and specificity. <br>
•	The accuracy, sensitivity and specificity for train set are 90%, 89%, 90% respectively. <br>
•	We also checked for precision and recall scores.<br>
11. Making Predications on the Test set. <br>
•	We scaled the variables in the test set. <br>
•	We predicted the values on the test set.<br>
•	We created a confusion matrix for test set and checked the accuracy, sensitivity and specificity.<br>
•	Accuracy, sensitivity and specificity for test set are 91%, 86%, 94% respectively.<br>
