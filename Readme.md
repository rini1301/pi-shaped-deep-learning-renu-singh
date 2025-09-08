# Stock Price Prediction with RNN/LSTM  

This project demonstrates how to build and train a **Recurrent Neural Network (SimpleRNN or LSTM)** to predict **Tesla stock opening prices** using a publicly available Kaggle dataset.  

---

## Project Workflow  
1. **Dataset Loading** – Tesla stock price dataset is loaded from Kaggle CSV.  
2. **Preprocessing** – Includes scaling, sequence framing (input windows), and train-test split.  
3. **Modeling** – An LSTM (or SimpleRNN) model is built to predict the next-day opening price.  
4. **Training** – Model is trained with multiple epochs and early stopping.  
5. **Evaluation** – Performance measured with regression metrics (MAE, RMSE, MAPE).  
6. **Visualization** – Predictions are plotted against actual values for interpretation.  

---

## Core Concept Questions  

### 1. What is the benefit of using RNNs (or LSTMs) over traditional feedforward networks for time-series data?  
- **RNNs** process sequential data by maintaining memory of past inputs, unlike feedforward networks which treat each input independently.  
- **LSTMs** improve upon RNNs by using gates (input, forget, output) to capture **long-term dependencies** and reduce the vanishing gradient problem.  

---

### 2. Why is sequence framing (input windows) important in time series forecasting?  
- Stock prices depend on previous days’ values.  
- Sequence framing converts raw time-series data into **sliding windows of past observations** (e.g., past 60 days → next day).  
- Without it, the model cannot learn temporal relationships.  

---

### 3. How does feature scaling impact training of RNN/LSTM models?  
- Scaling (e.g., MinMaxScaler or StandardScaler) ensures all features have comparable ranges.  
- Prevents dominance of large-valued features (e.g., stock prices in hundreds vs volumes in millions).  
- Helps gradient descent converge faster and more stably.  

---

### 4. Compare SimpleRNN and LSTM in terms of handling long-term dependencies.  
- **SimpleRNN**: Retains short-term dependencies but struggles with long sequences (vanishing gradient).  
- **LSTM**: Uses memory cells and gating mechanisms to **retain information over long time horizons**, making it better for stock prediction tasks.  

---

### 5. What regression metrics are appropriate for stock price prediction, and why?  
- **MAE (Mean Absolute Error)** – Easy to interpret as average dollar error.  
- **RMSE (Root Mean Squared Error)** – Penalizes larger errors more strongly, useful for financial predictions.  
- **MAPE (Mean Absolute Percentage Error)** – Useful to understand relative error (% off the true price).  

---

### 6. How can you assess if your model is overfitting?  
- Compare **training vs validation loss curves**: if validation loss increases while training loss decreases, overfitting is likely.  
- Use techniques like **dropout, early stopping, and regularization** to mitigate it.  

---

### 7. How might you extend the model to improve performance?  
- Add more **features** (e.g., volume, moving averages, external indicators).  
- Use a **deeper network** with stacked LSTMs/GRUs.  
- Try advanced architectures like **Bidirectional LSTMs or Transformers**.  
- Hyperparameter tuning (lookback window size, learning rate, batch size).  

---

### 8. Why is it important to shuffle (or not shuffle) sequential data during training?  
- **Do not shuffle** time-series data → order matters and must be preserved.  
- Shuffling would break temporal dependencies.  
- However, within **mini-batches**, careful sequential batching can stabilize training.  

---

### 9. How can you visualize model prediction vs actual values to interpret performance?  
- Plot **Predicted vs Actual price curves** over time.  
- Create a **scatter plot** of Predicted vs Actual values (perfect model lies on y=x line).  
- Visual inspection helps detect underestimation, lag, or trend mismatches.  

---

### 10. What real-world challenges arise when using RNNs for stock price prediction?  
- **Market volatility** and news events create unpredictable spikes.  
- **Overfitting** to historical data without generalization.  
- **Non-stationarity**: stock price distributions shift over time.  
- **Limited features**: price alone may not capture macroeconomic factors.  
- Risk of **data snooping bias** if future information leaks into training.  

---