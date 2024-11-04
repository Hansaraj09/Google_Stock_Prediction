**Welcome to Google Stock Price Prediction Model Repository!!!**

This repository leverages the LSTM model for predicting Google stock prices.

Let's have a brief walk through this!

1. First of all, we download the dataset from **Yahoo Finance** having all the values from high, low, open, and close, and save them in a CSV file.

2. Then after data cleaning and pre-processing, we obtain only **Date** and **Close** values of the stocks

3. Then we visualize the data by plotting it to see its trends.

![image](https://github.com/user-attachments/assets/4974b9d5-44ef-4e19-865c-da8e8dd634f0)

4. Then, we convert the data into a supervised learning framework for the LSTM model, which has stock prices up to 3 previous dates.

5. We should remember that it is necessary in a time series forecasting model as the current values depend on previous values.

6. Then we call the LSTM model, compile it, and fit the model with a suitable number of epochs over the dataset.

7. We monitor the **mean_absolute_error**.

8. After fitting the model we visualize the plot from which we can see that the **Validation Observation** and **Validation Predictions** are diverging. Also, the **validation_mean_absolute_error** value is high.

9. So to reduce it we adjust the date window and finally obtain

![image](https://github.com/user-attachments/assets/8b438631-bf61-4873-b5bd-f123f3439469)

10. After that, we recursively predict the prices and obtain

![image](https://github.com/user-attachments/assets/9e45feee-e62f-498f-8e84-3c4bb7156f13)

**Note**: From the plot above we can see that the recursive line is flat stating that the model has no idea of how to predict the future. This is kind of funny!! However, this approach represents a reasonable method of prediction, acknowledging the inherent challenges associated with forecasting stock prices.
Also from the curve trend plot above it is safe to say that it is a good stock.
