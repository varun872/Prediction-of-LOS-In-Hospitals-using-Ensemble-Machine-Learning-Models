# Predicting Length of Stay in Hospitals using Ensemble Machine Learning Models
## Introduction
Length of Stay (LOS) in hospitals refers to the duration a patient spends in a healthcare facility from admission to discharge. Accurately predicting the length of stay is crucial for efficient resource allocation, bed management, and overall improvement of healthcare services. By employing machine learning models, particularly ensemble methods, we can enhance the accuracy of LOS predictions and contribute to better patient care.

## LOS and its Significance
Understanding and predicting LOS is essential for several reasons:
1. Resource Optimization: Accurate predictions help hospitals allocate resources effectively, ensuring that enough beds, staff, and other resources are available to meet patient needs.
2. Cost Management: Predicting LOS aids in cost management by reducing unnecessary expenses and streamlining resource utilization.
3. Quality of Care: Efficient bed management contributes to better patient care, allowing healthcare providers to focus on delivering high-quality services.

## Regression vs. Classification
In the context of predicting LOS, both regression and classification approaches can be considered. Regression predicts a continuous variable (e.g., the exact number of days a patient will stay), while classification assigns instances to discrete categories (e.g., short stay, medium stay, extended stay).
In the case of LOS prediction, classification is often more practical and interpretable. It allows healthcare providers to categorize patients into meaningful groups, facilitating targeted interventions and resource allocation based on the predicted length of stay categories.

## About the dataset
<b>New York Hospital Inpatient Discharge 2015 Dataset</b>. This dataset is easily accessible to the public at <a href="https://health.data.ny.gov/Health/Hospital-Inpatient-Discharges-SPARCS-De-Identified/82xm-y6g8/about_data">Link to dataset</a>. It has around 2.3 million records and contains 34 unique features. 

## Ensemble Machine Learning Models Used
Ensemble models combine the predictions of multiple base models to improve overall performance. Here, we explore five popular ensemble models for LOS prediction:
1. Logistic Regression
2. Random Forest
3. Gradient Boosting
4. Catboost
5. XGBoost

## Conclusions
In our effort to predict Length of Stay (LOS), we explored both regression and classification models. Among the regression models, XGBoost emerged as the top performer, achieving the lowest Mean Absolute Error (MAE) at 2.783. Notably, we found no significant correlations among the columns, prompting an investigation into classification models.
For the classification task, we strategically divided the dataset into three distinct bin classes, taking into account the average LOS of approximately 6 days. The classes were defined as (0-6), (6-120+), and (0-6, 6-30, 30-120+). In this context, CatBoost outperformed other models, demonstrating an overall accuracy of 83%. Even after employing cross-validation, the accuracy remained consistently high. Interestingly, attempts to address dataset imbalance through under-sampling resulted in a 5% reduction in the overall accuracy of all models.
