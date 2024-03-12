# MLR-Model
Built a Multiple Linear Regression model for the prediction of demand for shared bikes based upon 2 years of Data set(2018 & 2019)!!

# Introduction:-
 * A bike-sharing system is a service in which bikes are made available for shared use to individuals on a short term basis for a price or free. Many bike share systems allow people to borrow a bike from a "dock" which is usually computer-controlled 
 wherein the user enters the payment information, and the system unlocks it. This bike can then be returned to another dock belonging to the same system.
 * You are required to model the demand for shared bikes with the available independent variables. It will be used by the management to understand how exactly the demands vary with different features. They can accordingly manipulate the business 
 strategy to meet the demand levels and meet the customer's expectations. Further, the model will be a good way for management to understand the demand dynamics of a new market. 

# Steps Performed:-
> Started by understanding the data then performing EDA, after that we split the dataset into training set (which would be used to train a model) and the testing set (which would be used to check how close is our model to the predicted output).
> Further checked the collinearity of variables and then performed Recursive Feature elimination to select top ten variables.
> Finally with those ten variables started building Linear model till the VIF and p-value comes up in desired range. Lastly performed the residual analysis of the train data set and then made predictions using the choosen model.

# Model Building:-
> In the dataset provided, there are three columns named 'casual', 'registered', and 'cnt'. The variable 'casual' indicates the number casual users who have made a rental. The variable 'registered' on the other hand shows the total number of 
  registered users who have made a booking on a given day. Finally, the 'cnt' variable indicates the total number of bike rentals, including both casual and registered. The model should be built taking this 'cnt' as the target variable.

# Model Evaluation:-
> After completing model building and residual analysis and predictions on the test set, I calculated the R-squared score on the test set: where y_test is the test data set for the target variable, and y_pred is the variable containing the predicted values of the target variable on the test set.

# Findings:-
> Categorical variables in dataset are season, yr, mnth, holiday, weekday, weathersit and from the analysis, we can infer that
  • Maximum active customers is on Fall Season (September month) along with that 2019 observed more sales than 2018.
  • On Holidays the active count drops.
  • During heavy rain, there are no users whereas partly cloudy/clear sky saw the maximum count.
> By looking at the pair plot of numerical variables 'temp' and 'atemp' shows the highest correlation, along with 'cnt' and  'temp'.
> By looking at the 'error term' which corresponds as normal curve with mean zero when plotted on histogram validates the assumptions of Linear Regression.
> Based on the final model top 3 features contributing significantly towards explaining the demand of the shared bikes are 'Yr', 'temp' and 'light snowrain'.
