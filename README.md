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
* Inference: Here we are plotting the box plot with the help of a cat plot between the price of the flight and the destination to which the pass



