# Bike-Sharing-Demand-Prediction

Currently Rental bikes are introduced in many urban cities for the enhancement of mobility comfort. It is important to make the rental bike available and accessible to the public at the right time as it lessens the waiting time. Eventually, providing the city with a stable supply of rental bikes becomes a major concern. The crucial part is the prediction of bike count required at each hour for the stable supply of rental bikes.

![image](https://user-images.githubusercontent.com/57758182/211597037-6d313240-685e-41d7-918d-161b3d8b4f08.png)


Considering the "SeoulBikeData" dataset, the exploratory and predictive analysis has been carried out, and the following conclusions can be made:

● The dataset with 10 numerical features and 4 categorical features very well explains the bike
rental count in the city and is further explored and analyzed to draw some meaningful
predictions/insights.

● The outliers in the features have been handled by robust scaling.

● The exploratory data analysis gives insights into the dependency between features, their
relationship with the target variable, and various trends.

  > Bike rental count is seen to follow a certain trend to grow high during peak hours of
favorable seasons, and functioning hours.

  > Bike rental count tends to increase with the increase in temperature, indicating that
people tend to avoid bikes during low temperatures.

● Various models have been fitted onto the prepared dataset and the following comparisons
can be made:

  > Linear Regression model fails to capture the details in the data and the extreme high
coefficients of certain features can bias the model towards the same. Hence looking for regularization. It also suffers from heteroscedasticity.

  > Regularization helped in regularizing the model coefficients and smoothening the
coefficients plot. Though no prominent improvements in the performance are seen
after regularization.

  > Non-linear model- Decision Tree succeeded in capturing the non-linearities in the
data that the linear model couldn't capture, hence leading to the improved
performance, which was further improved by hyperparameter tuning but led to an
overfitting model.

  > Random forest model got further improvement in the performance but was still
overfit, which was further improved by hyperparameter tuning to obtain the results
[Random Forest GridSearchCV: 0.9597(train), 0.8892(test)]. The residual plot exhibits
homoscedasticity.

  > Started off boosting ensemble models with the 'Gradient Boosting' algorithm that
performed comparatively weaker than previous non-linear models. The performance
improved highly on hyperparameter tuning and obtained an optimally fit model with
high performance of [GBM: 0.9174(train), 0.8703(test)]
Further carried on with 'LGB' model and 'CatBoost' model resulting in the most
optimally fit models with adjusted r2 score of [LGBM: 0.9613(train), 0.9008(test)] and
[CatBoost: 0.9523(train) and 0.9025(test)].

● It is safe to conclude that models namely 'Random Forest GridSearchCV', 'Gradient Boosting
GridsearchCV', 'Light Gradient Boosting', and 'CatBoost' are fit to be considered for
application/implementation purposes.

● Temperature and Humidity remain the most important features in ensemble predictive
models [Random Forest, Gradient Boosting, Light GBM, CatBoost]. This implies that
temperature and humidity are the most crucial features in deciding the bike rental count. The
higher the temperature and the lower the humidity, the more the number of bike rents.

● Functioning Day, Solar radiation, Rainfall, and Hour_18 are the others among the most
important features in most of the optimally performing models.

> This implies the fact that the prediction of bike count is high during functioning hours
and least during non-functioning hours.
> The higher the rainfall, the lesser the bike rents (negative correlation).
> Higher the solar radiation, the more the bike rents (positive correlation).
> And 6:00 pm being one of the peak hours is one among the most important factors in
prediction.
