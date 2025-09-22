# Machine-Learning-for-Store-Demand-Forecasting-using-Time-Series-and-Neural-Networks

📋 Introduction:
Demand forecasting is critical for efficient retail operations and supply chain management. Accurate predictions help prevent stockouts and overstocking, ensuring the right product quantities are available at the right time and location. This project leverages advanced neural networks and time-series forecasting techniques to improve sales prediction accuracy across retail stores.

🎯 Project Goal:
Develop a robust forecasting model using state-of-the-art machine learning and time-series analysis techniques to predict future sales across multiple retail outlets. The insights from this model aim to optimize inventory management, streamline resources, and maximize profitability.

📊 Dataset Description:

Source: Store Item Demand Forecasting Challenge dataset (Kaggle)

Attributes:

Date: Sales record date
Store ID: Store identifier
Item ID: Item identifier
Sales: Units sold
Data Span: Jan 1, 2013 – Dec 31, 2017, across 10 stores and 50 items

🛠️ Data Preprocessing:

Checked and removed duplicates
Standardized date format
Verified absence of null values
Noted weak correlations with sales but retained all features
Chronologically split data into 75% train / 25% test

🚀 Methodology:

Model Selection:
Time-Series Models: LSTM, BiLSTM, ARIMA, LSTM+CNN Hybrid, BiLSTM+CNN Hybrid
Baseline Regression Models: Random Forest Regressor, XGBoost Regressor, ANN, CNN

Data Transformation:

Label encoding for Store ID and Item ID
Converted DATE to discrete ordinal values

Tools & Technologies:
Python, Pandas, Numpy, Scikit-learn, Keras, TensorFlow, Matplotlib

📈 Modeling and Evaluation:

Hybrid Model Architecture:

LSTM+CNN: CNN extracts spatial features, LSTM captures temporal patterns, followed by dense layers to refine features and combine outputs for prediction.
BiLSTM+CNN: Similar to LSTM+CNN but LSTM layers use bidirectional wrapping for enhanced temporal context.
Models trained with batch size = 256 and manually fine-tuned hyperparameters.

Evaluation Metrics:

Mean Squared Error (MSE): Quantifies the average squared difference between predicted and actual sales values.
