### Data
https://data.cityofchicago.org/Transportation/Taxi-Trips/wrvz-psew/data

###Abstract
In our every day life we relay on Taxis for Transportation. The cost of Taxi Trips frequently increase or decrease based on factors like distance, date, time, location which cannot be predicted. In this project my traget variable will be payment method. Mode of payment is also depend on various factors. My goal is to predict the payment type with the help of Chicago data. As my data is very huge I am using the chunk of it.


### Data Description
This data consist of 23 columns and 99743 rows

Trip Id - This is a code given to every trip and it is represented as an object
Taxi Id - This is a code given to every vechicle and it is represented as an object
Trip Start Timestamp - The Date and Time at Starting of a Trip and it is represented as an object
Trip End Timestamp - The Date and Time at the end of a Trip and it is represented as an object
Trip Seconds - Duartion of the Trip measured in Seconds and it is represented as a float
Trip Miles - Distance of the Trip measured in Miles and it is represented as a float
Pickup Census Tract - A unique pick up code given in each country and it is represented as a float
Dropoff Census Tract - A unique Drop off code given in each country and it is represented as a float
Pickup Community Area - Name of the area where the pickup has been requested and it is a float datatype
Dropoff Community Area - Name of the are where the Dropoff has been requested and it is a float datatype
Fare - Cost for a Trip and it is float datatype

Tips - Tip amount given to the driver and it is a float 
Tolls - Tolls fare represented as float datatype
Extras - Extra amount charged and it is repsented as a float
Trip Total - sum of Fare,Tips,Tolls,Extras and it is float 
Payment Type - Mode of payment done for a ride and it is an object
Company - Name of Taxi service provider and it is an object
Pickup Centroid Latitude - Pickup Laititue and it is an float
Pickup Centroid Longitude - Pickup Longitude and it is an float
Pickup Centroid Location - Pickup Location and it is an object
Dropoff Centroid Latitude - Dropoff Laititue and it is an float
Dropoff Centroid Longitude - Dropoff Longitude and it is an float
Dropoff Centroid  Location - Dropoff Location and it is an object
