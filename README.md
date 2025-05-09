---

# 📊 CNN-BiLSTM Learning Rate Evaluation for TSMC Stock Price Forecasting

In this section, we analyze the performance of a hybrid **CNN-BiLSTM** model trained on **TSMC stock price data** using different learning rates. The goal is to identify which learning rate provides the best forecasting accuracy based on key regression metrics.

---

## 🔍 Model Evaluation Summary

| Learning Rate | RMSE        | MAE         | R² Score     |
| ------------- | ----------- | ----------- | ------------ |
| **0.00001**   | 4.416       | 2.216       | 0.9886       |
| **0.00010**   | ✅ **2.843** | ✅ **1.812** | ✅ **0.9953** |
| **0.00100**   | 2.936       | 2.329       | 0.9950       |
| **0.01000**   | 5.478       | 5.009       | 0.9824       |

> **Note:** Lower values of RMSE and MAE indicate better prediction accuracy, while R² closer to 1 indicates a better model fit.

---

## 📈 Key Insights

* 🔹 **Learning rate = 0.0001** clearly outperforms others, offering the **lowest RMSE and MAE** and the **highest R² score**, making it the optimal choice for this task.
* 🔸 Learning rates that are too small (e.g., 0.00001) or too large (e.g., 0.01) tend to either **converge slowly** or **overshoot the minima**, leading to reduced performance.
* ⚠️ At a learning rate of **0.01**, the model performance drops significantly, suggesting unstable learning and potential overfitting.

---

## 📊 Visual Results

### 🔁 Training & Validation Loss

For each learning rate, the loss curves were plotted to observe model convergence. The best-performing learning rate showed stable and steadily decreasing loss.

### 📉 Actual vs Forecast Plots

The forecasted stock prices closely tracked the actual values when using the optimal learning rate (0.0001), indicating strong generalization on unseen data.

---

## 🧠 Conclusion

This evaluation highlights the **critical role of tuning the learning rate** when training deep learning models like CNN-BiLSTM. With the right learning rate (0.0001), the model demonstrates **high accuracy, stability**, and **forecasting potential** for real-world financial time series tasks.

---
