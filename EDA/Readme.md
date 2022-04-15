### Data
https://data.cityofchicago.org/Transportation/Taxi-Trips/wrvz-psew/data
## Chunk Data File

https://drive.google.com/file/d/1Af7G4fx9UYKjFTpHQqVaAHHiDGcDqsk8/view?usp=sharing

### Abstract
In our every day life we relay on Taxis for Transportation. The cost of Taxi Trips frequently increase or decrease based on factors like distance, date, time, location which cannot be predicted. In this project my traget variable will be payment method. Mode of payment is also depend on various factors. My goal is to predict the payment type with the help of Chicago data. As my data is very huge I am using the chunk of it.

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
I observed that Pickup Community area and Dropoff Community area seem's to be similar through visualization graphs. But when i correlate it they seem's to be normal

I considered the trip as valid if Trip Miles is greater than zero. So,i have found Trip Miles having 0 values , so I have removed those rows and performed future analysis   

Trip fare has more values under 100 so i have considered remaining values as an outlier and eliminated them.

I have observed the minimun fare of the trip as 0, still i considered it because their may be internal reasons like by applying coupons, or some taxis have first ride options so it might be in that case.
