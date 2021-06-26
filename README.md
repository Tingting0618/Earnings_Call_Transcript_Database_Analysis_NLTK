# Hotel Demand Forecast - Machine Learning

## The goal/inspiration

In the project, we are going to forecast hotel occupancy 4 days out (e.g., Today is Monday, and we will be forecasting this Friday's occupancy.)

### Results

Mean Absolute Error (MAE) on a hold-out set = 4.9%. In other words, on average, we are <5% off when forecasting a hotel's occupancy. As a comparison, when there is no model (i.e., directly use last year's occupancy as this year's occupancy on a same weekday), we are on average 8% occupancy points off.

### Methods used

0) Cross-fold validation
1) Same Day Last Year
2) Random Forest
3) Ridge Regression
4) Lasso Regression
5) Multiple Regression
6) Grid Search for hyperparameter tuning

### Technologies used

Python (scikit-learn, SHAP, pandas), SQL

### Data source

Historical and forward-looking, property-level hotel demand data is provided by STR SHARE Center. STR is the leading provider of premium global data benchmarking, analytics, and marketplace insights. The STR SHARE Center provides hotel and tourism data to professors for research, student projects, and use in the classroom.

### Demo/details

**Data preview:**

In the holdout set, we have occupancy information: 
- occ_x: Last year, same day's occupancy
- ADR: Average Daily Rate of a room
- 4W: 4 weeks away from the target predicting date, the % of hotel rooms that have been booked.
- 3w: 3 weeks away from the target predicting date, the % of hotel rooms that have been booked.
- class: the dummy variable describes a hotel's class (e.g., luxury vs economy) 

![Holdoutset](https://user-images.githubusercontent.com/44503223/123178699-5b0bc380-d44d-11eb-9c76-c2b592b9ffc3.png)

**Train/Test/Holdout Split Procedures**

![traintest](https://user-images.githubusercontent.com/44503223/123180423-d9b63000-d450-11eb-91a7-1d4400fb7269.png)

**Demo:**

For the fifth hotel, it has 93.7% occupancy the same weekday last year, and 4 weeks prior to the target predicting date, this hotel has 39.9% booked. In addition, this is an Upscale Class hotel (e.g., Doubletree, Crowne Plaza, etc.) The prediction is 88% for this Friday, and the actual occupancy is 90%. (This prediction is from the trained Random Forest model.)

![first instance](https://user-images.githubusercontent.com/44503223/123179333-c6a26080-d44e-11eb-807c-9e7502c764f3.png)

**Understand the black box:**

![model interpretation](https://user-images.githubusercontent.com/44503223/123179469-13863700-d44f-11eb-868f-0fe297030c15.png)

In this example, since the hotel has a relatively high price ($233 per room night!), the predicted demand was reduced a little bit. Also, since this hotel was popular last year same weekday, and also was pretty full 4 days and 1 week prior to the target prediction date, the predicted occupancy was increased a little bit. 

**Most important factors that impact hotel demand this year**

![factors](https://user-images.githubusercontent.com/44503223/123179919-ef772580-d44f-11eb-8083-3b89f5d93a01.png)

Based on SHAP value, the occupancy last year and booked room 4 days prior to the target prediction date are most important. 

**Lastly, what's the full picture?**

![image](https://user-images.githubusercontent.com/44503223/123180188-68767d00-d450-11eb-82b8-ee9258598797.png)

Mean Absolute Error: 4.9%. On average, the model is off by 4.9% in hotel occupancy. For example: Forecasted Occupancy: 90%; Actual Occupancy: 85.1%

Without any modeling (i.e., merely using the same-day last year’s data), the model is off by 8% in hotel occupancy. The model improved the accuracy by **37.5%** [(5% - 8%)/8%]



## Learn More

You can learn more in the [Tingting Duan's Project Portfolio](https://tingting0618.github.io).

