# Used-car-Price-Prediction
Build an machine learning model to predict the price of used car.

IDEA: I have found out that during and after the pandemic a large monetary crisis was seen among the common populace. Some people were forced to sell their possessions and some had to buy used and second-hand product at a cheap price.  When I saw the process of buying and selling used vehicles, I also saw the problem of people not getting proper value for their money. To make the exchange fair I thought of an idea and developed this project. To observe the buying and selling of used cars I had to look through many websites and applications. The problem was that they didn't consider all the relevant factors of a car while setting a price tag for said car. Then I thought of a way to improve the prediction by taking into consideration all relevant factors and then setting a price tag for said car. That was how I came up with the idea for this project.

OVERVIEW OF THE DATASET:This dataset consists information about used car listed on cardekho.com. It has 9 columns each columns consists information about specific features like Car_Name gives information about car company .which Year the brand new car has been purchased.selling_price the price at which car is being sold this will be target label for further prediction of price.km_driven number of kilometre car has been driven.fuel this feature the fuel type of car (CNG , petrol,diesel etc).seller_type tells whether the seller is individual or a dealer. transmission gives information about the whether the car is automatic and manual.owner number of previous owner of the car. Present_price what is the current showroom price of the car.

DATA COLLECTION:I have taken data set from here
https://www.kaggle.com/nehalbirla/vehicle-dataset-from-cardekho?select=car+data.csv
The data set is in csv format.Now i will import all the essential library that will be needed for this project.

DATA PREPROCESSING:

Here we have cars of 98 different companies and name of companies won’t affect car’s price ,price depends upon how many year it’s been used ,fuel type etc,.so i will drop the column car_name from original dataframe.

Now we will check the data type of each column if the data type is numerical then we have no such issue but if datatype is categorical then we need to convert all those categorical features into numerical values.

Now we will make the categorical dataframe with all the features having categorical variables, and will drop all the categorical features from original dataframe.

Year represent the year in which car have been purchased so how we can estimate the number of year car has been used ?

So as we are in 2021 and car is of 2014 then number of years it’s been used will be :- number of year car has been used=2021–2014=7 to print number of year car has been used we need to add a column which represent current year.
We have successfully added the current_ year now we will add number_of_years column and drop Year and Current _year column.

PRE MODELING:
Splitting dataset into dependent and independent variable.
split the dataset into train and test set

Feature Importance :- checking which all features are important for output features out of all the given features.

ALGORITHM:By using the gradient boosting regressor i got the accuracy of 96%.
