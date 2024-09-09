# Key Components

## Dataset & Preprocessing:
- **Data Loading**: Tesla stock data is loaded, unnecessary columns removed, and Price Change Percentage (PC%) calculated.
- **RSI Calculation**: A custom RSI function creates an indicator for potential buy/sell signals.
- **Data Scaling**: MinMaxScaler scales data to a range of 0-1 for LSTM network compatibility.

## LSTM Model:
- **Architecture**: Sequential model with 4 stacked LSTM layers (50 units each) and Dropout layers to prevent overfitting.
- **Compilation**: Compiled with Adam optimizer and mean squared error loss function.
- **Training**: Trained on 60-day windows of historical data to predict future stock prices.

## Backtesting & Prediction:
- **Testing**: Model is tested on unseen data to generate predictions for Tesla’s stock prices.
- **Evaluation**: Performance is assessed using Max Error, Explained Variance Score, and R-squared metrics.

## Visualization:
- **Plotting**: Predicted vs. actual stock prices are plotted to visualize model performance.

## Techniques & Libraries:
- **Pandas & Numpy**: Data manipulation and feature engineering.
- **Seaborn & Matplotlib**: Data visualization.
- **Sklearn**: Performance evaluation metrics.
- **Keras (TensorFlow backend)**: Building and training the LSTM model.
