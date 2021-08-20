# Predicting airbnb monthly business

## Problem Statement

Can landlords predict the monthly bookings of their listed properties? What differentiates a property with high volume vs low volume?

## Data

The data was obtained from : https://www.kaggle.com/airbnb/seattle. It consists of 92 parameters for airbnb properties in Seattle.
Since the actual booking numbers were not available, I have used 'reviews per month' as a proxy relative measure.

## Approach

1. Since it is a regresson problem, I first ran the data through some models to get a sense of the performance : Linear Regression, Decision Tree, Random Forest & Gradient Boost. The model performance was evaluated on 3 parameters : MAE, RMSE & MAPE.

2. Using the prominent features from Linear Regression, Decision Tree and Gradient Boost, 3 new datasets were created and trained on the 4 models again.

3. Gradient Boost was found to have the best performance across all other models, and hence tuned further using GridSearch cross-validation and Random Search cross-vlaidation.

## Final Model Performance

The Gradient Boost model hypertuned via Grid Search CV had the following results :

R-squared of training data : 0.897

R-squared of test data : 0.698

MAE : 0.697

RMSE : 0.994

MAPE : 0.625

## Conclusion

![airbnb explainability](https://user-images.githubusercontent.com/40080277/130167104-49dd19fb-65fc-474a-9f6a-f79338b763ee.png)

### Existing hosts
The important things is to maintain a high response rate and maintain their verified status, in order to ensure good business.
### New hosts
The time of listing unfortunately cannot be controlled, and is the biggest factor for getting bookings. However, they can still improve their business by responding to booking requests quickly. They should also try to get their identity verified and reach a Superhost status as quickly as possible.
