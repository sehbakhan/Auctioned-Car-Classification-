# Auctioned-Car-Classification

Dataset link: https://www.kaggle.com/competitions/DontGetKicked/data

## Introduction

One of the biggest challenges of an auto dealership purchasing a used car at an auto auction is the risk of that the vehicle might have serious issues that prevent it from being sold to customers. The auto community calls these unfortunate purchases "kicks".

Kicked cars often result when there are tampered odometers, mechanical issues the dealer is not able to address, issues with getting the vehicle title from the seller, or some other unforeseen problem. Kick cars can be very costly to dealers after transportation cost, throw-away repair work, and market losses in reselling the vehicle.

In this project we will see the cars which has higher risk of being kick, which can help real value for dealership and provide best selection for the customers,

We will take a look at real world data for 150,000 customers and use machine learning techniques to build the models.


# Data Description

**All the features in the data set are defined as follows:**

- `RefID`: Unique (sequential) number assigned to vehicles
- `IsBadBuy`: Identifies if the kicked vehicle was an avoidable purchase
- `PurchDate`: The Date the vehicle was Purchased at Auction
- `Auction`: Auction provider at which the vehicle was purchased
- `VehYear`: The manufacturer's year of the vehicle
- `VehicleAge`: The Years elapsed since the manufacturer's year
- `Make`: Vehicle Manufacturer
- `Model`: Vehicle Model
- `Trim`: Vehicle Trim Level
- `SubModel`: Vehicle Submodel
- `Color`: Vehicle Color
- `Transmission`: Vehicles transmission type (Automatic, Manual)
- `WheelTypeID`: The type id of the vehicle wheel
- `WheelType`: The vehicle wheel type description (Alloy, Covers)
- `VehOdo`: The vehicles odometer reading
- `Nationality`: The Manufacturer's country
- `Size`: The size category of the vehicle (Compact, SUV, etc.)
- `TopThreeAmericanName`: Identifies if the manufacturer is one of the top three - American manufacturers
- `MMRAcquisitionAuctionAveragePrice`: Acquisition price for this vehicle in - average condition at time of purchase
- `MMRAcquisitionAuctionCleanPrice`: Acquisition price for this vehicle in the above Average condition at time of purchase
- `MMRAcquisitionRetailAveragePrice`: Acquisition price for this vehicle in the retail market in average condition at time of purchase
- `MMRAcquisitonRetailCleanPrice`: Acquisition price for this vehicle in the retail market in above average condition at time of purchase
- `MMRCurrentAuctionAveragePrice`: Acquisition price for this vehicle in average condition as of current day
- `MMRCurrentAuctionCleanPrice`: Acquisition price for this vehicle in the above condition as of current day
- `MMRCurrentRetailAveragePrice`: Acquisition price for this vehicle in the retail market in average condition as of current day
- `MMRCurrentRetailCleanPrice`: Acquisition price for this vehicle in the retail market in above average condition as of current day
- `PRIMEUNIT`: Identifies if the vehicle would have a higher demand than a standard purchase
- `AcquisitionType`: Identifies how the vehicle was aquired (Auction buy, trade in, etc)
- `AUCGUART`: The level guarantee provided by auction for the vehicle (Green light - Guaranteed/arbitratable, Yellow Light - caution/issue, red light - sold as is)
- `KickDate`: Date the vehicle was kicked back to the auction
- `BYRNO`: Unique number assigned to the buyer that purchased the vehicle
- `VNZIP`: Zipcode where the car was purchased
- `VNST`: State where the the car was purchased
- `VehBCost`: Acquisition cost paid for the vehicle at time of purchase
- `IsOnlineSale`: Identifies if the vehicle was originally purchased online
- `WarrantyCost`: Warranty price (term=36month and millage=36K)

In this data we have 32 independent variables and we have the target variable which we have to predict is `IsBadBuy`.

Summary
We downloaded , explored , performed EDA(Exploratory Data Analysis), cleaned the data and trained few models to automate the process of identifying that the car bought at auction is a good purchase or bad purchase.

Training data & test data had approximately 73K rows and 34 columns.
Prepared the dataset and removed the data which had more categories or which had high correlations
Imputed the missing values in both categorical columns and numeric columns.
Encoded the categorical columns with Label encoding & One hot encoding and scaled the numerical values using MinMaxScaler.
Then split the data into train data and validation data and trained the dumb model to get the baseline for our models.
Dataset was Imbalance , its important to balance the dataset first we applied `class_weights' parameter for balancing the data.
Trained four models: LogisticRegression,KNNClassifier DecissionTree and RandomForest. Among these RandomForest performed better and applied hyperparameter tuning onto it so that it gave the accuracy of 89% on the validation set.
Possible Future Work:

Performing better feature engineering.
Tuning the Hyperparameter.
performing cross-validation like k_fold.
