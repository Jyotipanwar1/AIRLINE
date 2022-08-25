# AIRLINE
Airline Price Prediction

# Problem Statement
 the problen statement of the given dataset is to  analyzing the flight fare prediction using Machine Learning dataset using essential exploratory data analysis techniques then will draw some predictions about the price of the flight based on some features such as what type of airline it is, what is the arrival time, what is the departure time, what is the duration of the flight, source, destination and more.
 
 # about dataset
 
* Airline: So this column will have all the types of airlines like Indigo, Jet Airways, Air India and many more.
* Date_of_Journey: This column will let us know about the date on which the passenger’s journey will start.
* Source: This column holds the name of the place from where the passenger’s journey will start.
* Destination: This column holds the name of the place to where passengers wanted to travel.
 * Route: Here we can know about that what is the route through which passengers have opted to travel from his/her source to their destination.
 * Arrival_Time: Arrival time is when the passenger will reach his/her destination
 * Duration:Duration is the whole period that flight will take to complete its journey from source to destination 
 * Total_Stops: This will let us know  how many places flights will stop there for the flight in the whole journey
 * Additional_Info: In this column, we will get information about food, kind of food, and other ame
* Price: Price of the flight for a complete journey including all the expenses before onboarding.

# Data Preprocessing and EDA

Our data had significant no. of missing values in it,mainly 
40% of the data as null or missing.
We could not think of dropping the null values because of the percentage of total data it
beared, so we thought about mean, median imputation but it would create so many
similar data points i.e around 40% of the total data would have the same value of
certain columns.we will be removing those repeated values from the dataset and keeping the in-place attribute to be true so that there will be no changes.
Checking the Additional_info column and having the count of unique types of values

# data Visualization 
* Plotting Price vs Airline plot
* Inference: with the help of the cat plot we are trying to plot the boxplot between the price of the flight and airline and we can conclude that Jet Airways has the most outliers in terms of price.
* Plotting Violin plot for Price vs Source
* Inference: Now with the help of cat plot only we are plotting a box plot between the price of the flight and
the source place i.e. the place from where passengers will travel to the destination and we can see that Banglore as the source location has the most outliers while Chennai has the least.
* Plotting Box plot for Price vs Destination
* Inference: Here we are plotting the box plot with the help of a cat plot between the price of the flight and the destination to which the pass.
* Plotting Bar chart for Months (Duration) vs Number of Flights
: in graph we have plotted the count plot for journey in a month vs several flights
and got to see that May has the most number of flights.

Plotting Bar chart for Types of Airline vs Number of Flights
e: after plotting  graph we can see that between the type of airline and count of flights we
can see that Jet Airways has the most flight boarded.
we also visualize ticket price and Airlines .


# Feature Engineering
first we are dividing the features and labels and then converting the hours in minutes.
Date_of_Journey: Here we are organizing the format of the date of journey in our dataset for better preprocessing in the model stage.
Dep_Time: Here we are converting departure time into hours and minutes
Arrival_Time: Similarly we are converting the arrival time into hours and minutes.
Now after final preprocessing let’s see our dataset.
Correlation between all Features
Dropping the Price column as it is of no use
data = train_df.drop(["Price"], axis=1)
Dealing with Categorical Data and Numerical Data
Label Encode and Hot Encode for Categorical Columns.
After the feature engineering ,Concatenating both Categorical Data and Numerical Data
conclusion: So as we saw that we have done a complete EDA process, getting data insights, feature engineering, and data visualization as well so after all these steps one can go for the prediction using machine learning model-making steps.

# Model Selection
We apply random forest regressor it it would give r2score 0.87 then we apply rfe to select best feature for our model and help us to eliminate redundant features total_stops,Journey_day,Airline_jet_airways ,Journey_month came out to be a best features. 
and features like additional_info_charges_airports,Airline_Vistara Premium economy
,Additional_Info_No check-in baggage included came out to be most redundant features.
after eliminating these features we made a function linear regression in which we fit lasso,ridge,elastic net and it will give not so much good prediction. after that we craete a function for bagging boosting models and xgb give best r2score 94 across all other models.




