## Chicago Taxi Trips 
### Data
https://data.cityofchicago.org/Transportation/Taxi-Trips/wrvz-psew/data
### Chunk Data File

https://drive.google.com/file/d/1CKyRnKlJlPha14OeAT3HE4NY12jke0_O/view?usp=sharing

### Abstract
In our every day life we relay on Taxis for Transportation. The cost of Taxi Trips frequently increase or decrease based on factors like distance, date, time, location which cannot be predicted. In this project my target variable will be payment method. Mode of payment is also depend on various factors. My goal is to predict the payment type with the help of Chicago data. As my data is very huge I am using the chunk of it.

### Data Description
This data consist of 23 columns and 99743 rows

**Trip Id** - This is a unique code given to every trip and it's data type is object

**Taxi Id** - This is a unique code given to every vechicle and it's data type is object

**Trip Start Timestamp** - The Date and Time at Starting of a Trip and it's data type is object

**Trip End Timestamp** - The Date and Time at the end of a Trip and it's data type is object

**Trip Seconds** - Duartion of the Trip measured in Seconds and it's data type is float

**Trip Miles** - Distance of the Trip measured in Miles and it's data type is float

**Pickup Census Tract** - A unique pick up code given in each country and it's data type is float

**Dropoff Census Tract** - A unique Drop off code given in each country and it's data type is float

**Pickup Community Area** - Name of the area where the pickup has been requested and it's data type is float

**Dropoff Community Area** - Name of the are where the Dropoff has been requested and it's data type is float

**Fare** - Cost for a Trip and it's data type is float

**Tips** - Tip amount given to the driver and it's data type is float 

**Tolls** - Tolls fare it's data type is float

**Extras** - Extra amount charged and it's data type is float

**Trip Total** - sum of Fare,Tips,Tolls,Extras and it's data type is float 

**Payment Type** - Mode of payment done for a ride and it's data type is object

**Company** - Name of Taxi service provider and it's data type is object

**Pickup Centroid Latitude** - Pickup Laititue and it's data type is float

**Pickup Centroid Longitude** - Pickup Longitude and it's data type is float

**Pickup Centroid Location** - Pickup Location and it's data type is object

**Dropoff Centroid Latitude** - Dropoff Laititue and it's data type is float

**Dropoff Centroid Longitude** - Dropoff Longitude and it's data type is float

**Dropoff Centroid  Location** - Dropoff Location and it's data type is object


### Exploratory Data Analysis
I observed that Pickup Community area and Dropoff Community area seem's to be similar through visualization graphs. But when i correlate it they seem's to be normal.

I considered the trip as valid if Trip Miles is greater than zero. So,i have found Trip Miles having 0 values , so I have removed those rows and performed future analysis.   

Trip fare has more values under 100 so i have considered remaining values as an outlier and eliminated them.

I have observed the minimun fare of the trip as 0, still i considered it because their may be internal reasons like by applying coupons, or some taxis have first ride options so it might be in that case.

### Feature Selection
*  Our main goal is to predict payment method before a trip is created, so we will consider only our target variable 'Payment Type'.
*   We found some null values in census . So i will drop the columns. 
* Pickup and drop of area is easier to analyze instead of latitude and longitude so i am dropping thoes columns also.

### Results
![image](https://user-images.githubusercontent.com/92277491/167513071-091639be-bd8a-4eaf-a8ef-b8a85905927d.png)

I have considered f1-score and AUC as the metrics because, my class is imbalance so to evaluate and imbalance class f1-score is a best metrics. I also considered AUC score as a metrics because "Cash" or "Non-Cash" transcations are equally important and it depends on each individual. 

### Model Selection
 I have selected Logistic Regession as best model because it has a F1-score of 97.1% and Roc_AUC score is 97.3%
 
### Summary
* Logistic Regression performed better than decision tree and stochastic gradient descent with 97.1% of F1-score.
* For the given dataset we have seen that majority of people choose cash payments and credit card transacations.
* Most of the trips are done on Sundays in a week and on the second half in a month.
* Prices for most of trips are low below 20$.
* In a day most of trips are taken place in evening time around 6 p.m.
* I have observed that pick up and drop of community area are same , so we can say that most people are travelling for short distance.

### Future Work
* I have used chunk data for faster analysis, to improve the above models we can use more data which may leads to increase performance and score values.
* We can use more algorithms like svm,random forest, Knn, neural networks, but this may also takes more time to evaluate.
* Improving features for modeling can also give us a better performance. 
* Ensemble methods combine several models to create a better one. Using this will gives us better and less overfitting performance.



