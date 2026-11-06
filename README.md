# Advertising Sales Prediction - Multiple Linear Regression

Predicts product sales from advertising spend on TV, radio and newspaper using multiple linear regression, then uses the model to estimate sales for a planned budget.

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat-square&logo=scikitlearn&logoColor=white)
![pandas](https://img.shields.io/badge/pandas-150458?style=flat-square&logo=pandas&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=flat-square&logo=jupyter&logoColor=white)

## Dataset

`Advertising.csv` - 200 markets with ad spend on **TV**, **Radio** and **Newspaper** and the resulting **Sales**.

## Approach

1. Statistical summary of all variables
2. 80/20 train-test split
3. Fit a `LinearRegression` model on all three channels
4. Evaluate with MAE, MSE, RMSE and R²
5. Classify each prediction as high (Sales >= 15) or low performance and check accuracy and F1
6. Predict sales for a new budget and plot actual vs predicted sales

## Results

| Metric | Value |
|---|---|
| R² | 0.906 |
| MAE | 1.27 |
| RMSE | 1.70 |
| Accuracy (Sales >= 15 threshold) | 97.5% |
| F1 score | 0.973 |

**Coefficients** (sales change per unit of spend): TV 0.054, Radio 0.101, Newspaper 0.004.
Radio has the strongest effect per unit spent, while newspaper spend adds almost nothing.

**Scenario:** a budget of TV 150, Radio 20, Newspaper 30 predicts sales of about **15.0**.

## Files

| File | Description |
|---|---|
| `multilinear_regression.ipynb` | Full notebook with outputs |
| `Advertising.csv` | Dataset |

## Run

```bash
pip install pandas numpy scikit-learn matplotlib jupyter
jupyter notebook multilinear_regression.ipynb
```

## Author

**Paramkusam Saketha Sreevatsa** - [GitHub](https://github.com/Klusaketh) · [LinkedIn](https://www.linkedin.com/in/paramkusamsakethasreevatsa)
