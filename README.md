# Classification Challenge

## Dataset
The dataset contains email data labeled as either spam (1) or not spam (0). Each email is represented by various features, such as word frequency and character patterns, enabling the models to distinguish spam from legitimate messages.

- **Source**: [UCI Machine Learning Repository](https://static.bc-edx.com/ai/ail-v-1-0/m13/challenge/spam-data.csv)
- **Features**: Includes word frequencies, character frequencies, and capital letter statistics.
- **Target**: Binary labels (`1 = Spam`, `0 = Not Spam`).

## Project Goals
The objective is to develop and evaluate two supervised machine learning models—Logistic Regression and Random Forest Classifier—to determine which model performs better at detecting spam emails.

## Methodology
1. **Data Preparation**:
   - Split the data into training and testing sets (80/20 split).
   - Used the `StandardScaler` to scale feature data for improved model performance.
   
2. **Models Implemented**:
   - **Logistic Regression**:  
     A linear classification model assigning probabilities to each class and classifying based on a threshold (typically 0.5). 
   - **Random Forest Classifier**:  
     An ensemble method that builds multiple decision trees and aggregates their predictions to handle complex patterns effectively.

3. **Evaluation**:
   - Accuracy was used to compare model performance on testing data.

## Results
| Model                | Training Accuracy | Testing Accuracy |
|-----------------------|-------------------|------------------|
| Logistic Regression  | 92.98%           | 92.70%           |
| Random Forest        | 99.97%           | 95.55%           |

- **Logistic Regression**: Showed consistent performance between training and testing data, indicating good generalization but slightly lower accuracy.
- **Random Forest**: Outperformed Logistic Regression in terms of accuracy but exhibited a larger gap between training and testing accuracy, suggesting slight overfitting.

## Conclusion
The **Random Forest Classifier** performed better overall, aligning with initial expectations. Its ability to handle complex patterns makes it an excellent choice for this dataset, though further tuning could reduce overfitting.

## Usage
Run the `spam_detector.ipynb` notebook to:
- Train the models.
- Evaluate their performance.
- Compare the results.
