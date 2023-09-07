# Stock_Prediction
Description of the provided code for stock price prediction using an LSTM model:

1. **Data Retrieval**:
   - The code begins by importing the necessary libraries, including yfinance for fetching stock data.
   - The stock symbol, in this case, 'GAIL.NS' (GAIL India Limited), is specified.
   - Historical stock data for the last 5 years with a daily interval is downloaded and stored in the 'data' variable.

2. **Data Preprocessing**:
   - The 'Open' prices from the downloaded data are selected and plotted to visualize the stock's price trends.
   - Min-max scaling is applied to normalize the stock prices between 0 and 1.
   - The dataset is split into training and testing sets.

3. **Data Preparation for LSTM**:
   - A function 'create_ds' is defined to create sequences of 100 days as input data (X) and the next day's price as the output (Y).
   - The dataset is divided into training and testing sequences.

4. **LSTM Model Creation**:
   - A Sequential LSTM model is defined with three LSTM layers and a final dense layer.
   - The model is compiled using the mean squared error loss function and the Adam optimizer.
   - The model is trained on the training data for 100 epochs.

5. **Model Evaluation**:
   - The loss during training is plotted to assess the model's performance.
   - Root Mean Squared Error (RMSE) is calculated for both training and testing data to evaluate the model's accuracy.

6. **Visualization**:
   - Predictions are made on both training and testing data and inverse transformed to the original scale.
   - A visualization of the actual and predicted stock prices is created.

7. **Future Price Prediction**:
   - Predictions for the stock price for the next 30 days are made in a sliding window manner.
   - The code iterates through each day, using past predictions as input to forecast the next day's price.

8. **Final Visualization**:
   - A graph is plotted with both the actual and predicted stock prices.
   - A horizontal red line is added to mark the predicted stock price for the 30th day.
   - The final graph provides a visual representation of the stock price prediction for the next month.

In summary, this code uses LSTM neural networks to predict stock prices based on historical data, evaluates the model's performance, and provides a visualization of the predictions. It also extends predictions into the future for the next 30 days, allowing users to assess potential stock price trends.
