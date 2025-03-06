# **Steel Industry Sales Forecasting: An Ensemble Learning Approach**

## Overview
This repository implements an ensemble-based regression pipeline to forecast quarterly sales for a B2B steel manufacturer. The system integrates domain-specific financial metrics and macroeconomic indicators to generate robust, data-driven predictions.

## Data Description
- **train.csv**: Training data containing financial ratios, revenue and market share projections, bond/stock ratings, and regional/industry classifications.
- **test.csv**: Evaluation dataset.
- **sample_submission.csv**: Template for prediction submissions.
- **EconomicIndicators.csv**: Monthly economic indices (Consumer Sentiment, Interest Rate, PMI, Money Supply, National & Regional Economic Activity Indexes).

## Preprocessing
- **Numerical Pipeline**: Applies mean imputation and standard scaling.
- **Categorical Pipeline**: Executes one-hot encoding with error-tolerant handling of unseen categories.
- **Integration**: Combined via a `ColumnTransformer` to ensure consistent feature engineering across the pipeline.

## Modeling
Multiple regression algorithms are benchmarked, including:
- **Linear Models**: Linear Regression, Lasso, Ridge.
- **Ensemble Methods**: Gradient Boosting, AdaBoost, Random Forest, Extra Trees, Voting Regressor.
- **Advanced Techniques**: XGBoost, SVR, Kernel Ridge, MLP Regressor, among others.
  
A meta-model using a Voting Regressor aggregates top-performing models to enhance prediction stability and accuracy.

## Hyperparameter Optimization
The model tuning employs a Randomized Search Cross-Validation framework with a K-Fold strategy to optimize hyperparameters, particularly focusing on minimizing Mean Absolute Error (MAE).

## Evaluation Metrics
Model performance is quantified using:
- Mean Absolute Error (MAE)
- Mean Squared Error (MSE)
- Root Mean Squared Error (RMSE)
- R² Score
- Explained Variance Score

## Execution
The pipeline is executed end-to-end via a modular script, ensuring reproducibility and scalability for both research and production-level experimentation.

## Dependencies
- Python 3.x
- scikit-learn
- XGBoost
- NumPy
- Pandas
- Tabulate

## Conclusion
This project presents a comprehensive framework for sales forecasting, leveraging advanced ensemble techniques and rigorous hyperparameter tuning to address complex predictive modeling challenges in a dynamic economic landscape.

## Contributing

Contributions are welcome! Feel free to submit issues or pull requests.


## License

This project is licensed under the [MIT License](LICENSE).

Thank you for using this software ! Feel free to reach out with any questions or feedback.

<em style="color: #ff66b2; font-weight: bold;">✨ --- Designed & made by Shib Kumar Saraf ✨</em>
