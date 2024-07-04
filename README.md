# Early prediction of cart abandonment
This group project aims to perform early prediction of whether a user will abandon their cart in the current shopping session after adding at least one product to the cart. This is a binary classification problem, where each session is classified as either abandoned (negative class) or completed (positive class). The project involves several tasks, including preprocessing the data, implementing a baseline Naïve Bayes classifier, developing an experimental model, creating an oracle model, and conducting error analysis.

## Main Goal
To predict cart abandonment based on user behavior during the shopping session, focusing on clicks and actions taken by the user.

## Dataset
The dataset was provided by the organizers of the challenge. It includes user sessions with details of actions performed during each session, such as adding products to the cart, viewing product details, and making purchases.

## Evaluation Metric
The primary evaluation metric for this project is the F1 score. Predictions are evaluated at 5, 10, and 15 clicks after the first add-to-cart event in a session.

## Methods
Given the nature of the assignment, several methods were selected and tried to enhance the prediction accuracy. The project includes a baseline Naïve Bayes classifier, an experimental Random Forest model, and an oracle model for upper bound performance estimation. Extensive error analysis was also conducted to improve and understand model performance.

## Files Details
- **training_data.csv**: Dataset provided for the training and validation sets containing several features that are preprocessed before model training.
- **test_sessions_5.json, test_sessions_10.json, test_sessions_15.json**: Datasets for testing the models, containing session data truncated to 5, 10, and 15 events post add-to-cart, respectively.
- **predictions_group9_baseline_at5.json, predictions_group9_baseline_at10.json, predictions_group9_baseline_at15.json**: Predictions made by the baseline Naïve Bayes model for the test sets at 5, 10, and 15 events.
- **predictions_group9_expModel_rf_at5.json, predictions_group9_expModel_rf_at10.json, predictions_group9_expModel_rf_at15.json**: Predictions made by the experimental Random Forest model for the test sets at 5, 10, and 15 events.
- **predictions_group9_oracle_at5.json, predictions_group9_oracle_at10.json, predictions_group9_oracle_at15.json**: Predictions made by the oracle model for the test sets at 5, 10, and 15 events.
- **Detailed_code.ipynb**: Jupyter notebook with extended work to further enhance the model's accuracy and incorporate explanations for better understanding. Last version we did as a group with fellow collegues Albert de Vries, Britt Geisler, and Enoh Isong.

- **best_model.h5**: Save the model that performs best on a validation set, so it can be used later for inference or further training without needing to retrain from scratch.
   
## Project Structure
1. **Setup**: Instructions for setting up the environment and installing necessary packages.
2. **Data Preprocessing**: Steps for sessionizing the data, filtering sessions, adding class labels, trimming sessions, and symbolizing actions.
3. **Baseline Model**: Implementation of a Naïve Bayes classifier to predict cart abandonment based on 4-grams of symbolized clicks.
4. **Experimental Model**: Development of a Random Forest classifier with engineered features to improve prediction accuracy.
5. **Oracle Model**: Creation of an oracle model to estimate the upper bound of performance.
6. **Error Analysis**: Conducting error analysis to understand the performance of the models and explore different techniques to handle class imbalance and improve predictions.
7. **Results**: Presentation of the accuracy, F1 score, and other relevant metrics for the baseline, experimental, and oracle models across different test sets.
