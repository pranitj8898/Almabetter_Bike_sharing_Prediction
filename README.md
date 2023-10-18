# Almabetter_Bike_sharing_Prediction

In many urban areas, rental bikes have been introduced to improve transportation convenience. Ensuring these bikes are available and easily accessible when needed is essential to reduce wait times for users. Thus, a key challenge is forecasting the number of bikes needed hourly to ensure a consistent availability for residents.




Data Description
The dataset contains weather information (Temperature, Humidity, Windspeed, Visibility, Dewpoint, Solar radiation, Snowfall, Rainfall), the number of bikes rented per hour and date information.


Attribute Information:

* Date : year-month-day

* Rented Bike count - Count of bikes rented at each hour

* Hour - Hour of he day

* Temperature-Temperature in Celsius

* Humidity - %

* Windspeed - m/s

* Visibility - 10m

* Dew point temperature - Celsius

* Solar radiation - MJ/m2

* Rainfall - mm

* Snowfall - cm



**Conclusion**:

* We have computed the MAE, MSE, RMSE, and R^2 scores for each model. We'll determine the model's performance based on the R^2 score.

* If the difference in R2 scores between the training data and test data exceeds 5%, we would regard the model as overfitting.


1. Linear,Lasso,Ridge and ElasticNet.

From the provided data frame, it's evident that the linear, Lasso, Ridge, and Elastic regression models yield comparable R2 scores (around 61%) for both training and test datasets. This observation remains consistent even after employing GridSearchCV, yielding results akin to the base models.

2. Decision Tree Regressiom:

In the initial Decision Tree regressor model, without hyperparameter adjustments, we achieved a 100% r2 score on the training data but a significantly lower score on the test data. This indicates that the model overfitted and essentially memorized the training dataset.
However, after fine-tuning the hyperparameters, the model's r2 score on the training data was 88%, and it achieved an 83% score on the test data, which is a satisfactory result for us.

3. Random Forest:

On Random Forest regressor model, without hyperparameter tuning we got r2 score as 98% on training data and 90% on test data. Thus our model memorised the data.So it was a overfitted model, as per our assumption After hyperparameter tuning we got r2 score as 90% on training data and 87% on test data which is very good for us.

4. Gradient Boosting Regression:
Using the Random Forest regressor model without any hyperparameter adjustments, we achieved an r2 score of 86% on the training data and 85% on the test data, indicating a good performance by default.
However, after fine-tuning the hyperparameters, our performance significantly improved, reaching an r2 score of 96% on the training data and 91% on the test data. This underscores the benefits of hyperparameter optimization in enhancing our model's performance.
