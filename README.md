# Stock Price Prediction Using Machine Learning

This project aims to investigate whether machine learning models can accurately predict stock price movements based on historical market data. The dataset consists of stock data from 10 companies over the period from 2013 to 2023.

## Dataset

- Source: Kaggle (scraped from NASDAQ)
- Number of rows: 25,161
- Companies: Apple, Starbucks, Microsoft, Cisco Systems, Qualcomm, Meta, Amazon, Tesla, Advanced Micro Devices (AMD), and Netflix
- Columns: `Company`, `Date`, `Close/Last`, `Volume`, `Open`, `High`, `Low`

## Preprocessing

- Converted dates to datetime format
- Formatted price columns to remove dollar signs
- Removed NA values
- Dropped the `Company` column to avoid overfitting

## Machine Learning Models

Three models were used to predict stock prices:

1. **Linear Regression**
2. **Multi-layer Perceptron (MLP) Regressor**
3. **Random Forest Regressor**

### Model Training

- Dataset was split 70/30 for training and testing
- StandardScaler was used to normalize input data for MLP
- Hyperparameters were tuned for the MLP model, while the other models used default settings

## Evaluation

The models were evaluated using the R-squared (R²) score, where:

- **Linear Regression:** 0.99981
- **MLP Regressor:** 0.99979
- **Random Forest Regressor:** 0.99975

All models showed a strong positive correlation between predicted and actual values, indicating high accuracy.

## Key Takeaways

- Machine learning models, particularly those utilizing regression, can predict stock price movements with high accuracy when trained on historical data.
- The project demonstrates how well regression models can handle this type of data.

## Limitations

- Dataset is limited to 10 companies (mainly tech-focused), which may introduce industry bias.
- The time range (2013-2023) does not account for earlier financial events like the 2008 financial crisis.
- Only the R² metric was used for model evaluation, and hyperparameter tuning was limited.

## Future Work

- Expand the dataset to include more companies from different sectors and a broader historical range.
- Experiment with more evaluation metrics and alternative models.
