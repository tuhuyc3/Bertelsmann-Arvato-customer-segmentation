# Bertelsmann/Arvato Project - Data Science Nanodegree

## Project Definition

In this project, we worked with a dataset containing demographic information of customers from a mail-order sales company in Germany. The goal was to analyze the data and apply machine learning techniques to predict customer responses (whether or not a person becomes a customer after a marketing campaign). 

### Key Objectives:
1. **Data Exploration and Preprocessing**: Clean the dataset by handling missing values and addressing different feature types.
2. **Customer Segmentation**: Perform unsupervised learning to segment customers and compare them to the general population.
3. **Predictive Modeling**: Use machine learning algorithms to build a model that predicts customer responses based on demographic features.

## Analysis

### 1. Data Exploration and Preprocessing
- **Missing Data Handling**: The dataset contained a significant number of missing values, which required imputation or removal strategies to avoid biases in model training.
- **Feature Engineering**: Several features were of different types (e.g., categorical, numerical), and careful transformations were necessary to make the data suitable for modeling.
  
### 2. Customer Segmentation
Using unsupervised learning, we clustered both customers and the general population into 13 groups. The results showed:
- **Overrepresented Clusters**: Clusters 1, 2, 5, and 7 contained a higher proportion of customers.
- **Underrepresented Clusters**: Clusters 0, 3, 4, and 10 were more representative of the general population.

These insights provide actionable information for targeting future customers based on their demographic characteristics.

### 3. Predictive Modeling
For predicting customer responses, we tested several machine learning models. The **Gradient Boosting Classifier** emerged as the best-performing model based on its ability to capture complex patterns in the data. However, upon evaluating the model on the test set, we faced the issue where:
- All predicted probabilities were ≤ 0.12.
- The model predicted `false` (0) for all instances.

This indicates that the model may be underfitting or suffering from issues such as class imbalance or miscalibration.

## Conclusion

The Bertelsmann/Arvato project was an engaging and insightful final exercise in the Data Science Nanodegree program. We were able to:
1. Effectively segment customers from the general population.
2. Build a robust predictive model with Gradient Boosting.

However, the model's performance on the test set highlights areas for improvement, such as:
- **Handling Class Imbalance**: The model’s bias towards predicting the negative class suggests the need for techniques like resampling or adjusting class weights.
- **Model Tuning**: Fine-tuning hyperparameters and adjusting model complexity may help improve its predictive power.
- **Threshold Adjustment**: Lowering the classification threshold could capture more positive responses.
- **Calibration**: Applying calibration methods (like Platt scaling) could help refine predicted probabilities.

With these improvements, the model could become more effective at forecasting customer responses, enabling better-targeted marketing campaigns.

---

### Acknowledgments

Kudos to **Udacity** and **Bertelsmann/Arvato** for providing this fun and challenging project! Tipping my hat also to **Elena Ivanova (lenuel)** and **DeepVen**, who inspired parts of the solutions.

For a detailed walk-through of this project, check out my blog post: [Udacity Capstone Project: Customer Segmentation for Arvato Financial Services](https://medium.com/@ha.huy.97/udacity-capstone-project-customer-segmentation-for-arvato-financial-services-b2c281d99fc5)
