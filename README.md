# bike-sharing-demand-prediction
# Project Type - EDA/Regression
# project summary
-Currently Rental bikes are introduced in many urban cities for the enhancement of mobility comfort. It is important to make the rental bike available and accessible to the public at the right time as it lessens the waiting time. Eventually, providing the city with a stable supply of rental bikes becomes a major concern. The crucial part is the prediction of bike count required at each hour for the stable supply of rental bikes.

# columns in the dataset
The dataset contains weather information (Temperature, Humidity, Windspeed, Visibility, Dewpoint, Solar radiation, Snowfall, Rainfall), the number of bikes rented per hour and date information.

Attribute Information:

Date : year-month-day.

Rented Bike count - Count of bikes rented at each hour.

Hour - Hour of he day.

Temperature-Temperature in Celsius.

Humidity - %.

Windspeed - m/.

Visibility - 10m.

Dew point temperature - Celsius

Solar radiation - MJ/m2

Rainfall - mm

Snowfall - cm

Seasons - Winter, Spring, Summer, Autumn

Holiday - Holiday/No holiday

Functional Day - NoFunc(Non Functional Hours), Fun(Functional hours)


-By seeing into the Data I came to know that it is consisted of[8760 rows x 14 columns] and there are no duplicate and missing values

# Data Wrangling
-I changed the date column into day,month,year column
-I used one hot encoding to all the categorical variables
-for linear regression assumption is that the data should be normal distribution so i checked it and then i transformed using transformation techniques
-The target variable is left skewed so i applied transformation techniques in that square root transformation gave good result
# machine learning model implementation
# Linear Regression
-Mean Absolute Error: 5.7135227078889095
-Mean Squared Error: 54.53469891362764
-Root Mean Squared Error: 7.384761263143694
-r2: 0.653717728193994
-trained r2: 0.6527765844128129
# Ridge Regression
-Mean Absolute Error: 5.713522717198201
-Mean Squared Error: 54.534698988850046
-Root Mean Squared Error: 7.384761268236777
-r2: 0.6537177277163497
-trained r2: 0.6527765844128127
# Lasso regression
 - Mean Absolute Error: 5.713548645953172
  -Mean Squared Error: 54.53490268027101
-Root Mean Squared Error: 7.384775059558078
 - r2: 0.6537164343246302
  -trained r2: 0.6527765826839536
# Descision Tree Regressor
 - Mean Absolute Error: 3.091613218736375
-Mean Squared Error: 20.358306543325387
-Root Mean Squared Error: 4.512018012300636
-r2: 0.8707296312186269

# conclusion
In this project, I tackled a regression problem in which I had to predict the bike sharing count to match increasing popularity of bike rentals in metropolitan areas to enhance mobility and convenience for the public. It emphasizes the importance of providing timely access to rental bikes to reduce wait times for users, making a steady supply of rental bikes a key factor.

I began our analysis by performing EDA on all of our datasets. First, I looked at our dependent variable, "Rental Bike Count." After that, I looked at categorical variables and numerical variables and discovered their correlation, distribution, and connection to the dependent variable. Additionally, I hot-encoded the categorical variables and removed some numerical features which are used only for EDA purposes and have multi-collinearity. Following that, I examine several well-known individual models, ranging from straightforward Linear Regression and Regularization Models (Ridge, Lasso)to more complex and ensemble models like Random Forest

1.The majority of rentals are for daily commutes to workplaces and colleges. While planning for extra bikes to stations the peak rental hours must be considered, i.e. 7–9 am and 5–6 pm.

2.Season: I see the highest number of bike rentals in the Spring (July to September) and Summer (April to June) Seasons and the lowest in the Winter (January to March) season.

3.i came to know that a low no of bookings done on non functioning day only 295

4.I have chosen the Decision tree regressor which is above all else I want better expectations for the rented_bike_count and time isn't compelling here. I compared R2 metrics to choose a model.
 
   
