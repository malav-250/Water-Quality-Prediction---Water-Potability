# Water Quality Assessment for Drinking Purpose Using Machine Learning Models

## Project Overview
This project applies various supervised machine learning techniques to assess water quality and predict whether water is potable (safe for drinking) based on several physicochemical parameters. The implementation uses classification algorithms to effectively categorize water samples as potable or non-potable without requiring expensive and time-consuming laboratory analysis.

## Dataset
The dataset used in this project was obtained from Kaggle and contains water quality parameters with a binary classification target (Potability: 1 for potable, 0 for non-potable). The dataset includes 9 input features:

- pH
- Hardness
- Solids (Total dissolved solids)
- Chloramines
- Sulfates
- Conductivity (Specific conductivity)
- Trihalomethanes
- Organic Carbon
- Turbidity

## Data Preprocessing
Several preprocessing steps were implemented to improve the quality of the dataset:

- **Handling Missing Values**: The dataset contained NULL values in Sulfate (23.84%), pH (14.98%), and Trihalomethanes (4.94%) columns. These were filled with mean values to ensure model accuracy.
- **Outlier Detection and Treatment**: Box-plot analysis was used to identify outliers. An upper/lower bound approach was implemented where values exceeding the bounds were replaced with the respective bound values.
- **Correlation Analysis**: Pearson correlation was used to examine relationships between features. The analysis showed that all features were independent, justifying the use of all parameters for prediction.
- **Feature Scaling**: Z-score normalization was applied using StandardScaler from sklearn to address the varying ranges of different parameters and improve model performance.

## Machine Learning Models
Five supervised machine learning algorithms were implemented and compared:

- **Logistic Regression**: A binary classification algorithm based on the logistic sigmoid function.
- **Decision Tree**: A tree-based classification algorithm using entropy (ID3 classifier).
- **Gaussian Naive Bayes**: A probabilistic classification model based on Bayes' theorem.
- **K-Nearest Neighbors (KNN)**: Classification based on the majority class of the k-nearest neighbors (n=7).
- **Support Vector Machine (SVM)**: Classification by defining an optimal hyperplane to distinguish between classes.

## Performance Metrics
The models were evaluated using the following metrics:
- Accuracy
- Precision
- Recall
- F1 Score

## Results
- SVM demonstrated the best performance among all models for drinking water potability prediction.
- Decision Tree had the lowest accuracy at approximately 61%.
- The models achieved reasonable accuracy using the given parameters, making the approach viable for real-time water quality determination.

## Implementation
The implementation was carried out using Python with the sklearn library for machine learning algorithms and data preprocessing.

### Key steps in the implementation:
1. Data loading and exploration
2. Handling missing values and outliers
3. Feature scaling
4. Training multiple classification models
5. Evaluating model performance
6. Comparing results across different algorithms

## Future Work
- Implementation of deep learning models like neural networks to potentially improve prediction accuracy
- Integration with IoT-based online monitoring systems for real-time water quality assessment
- Development of a comprehensive system that can collect data from sensors and immediately predict water potability

## Contributors
- Nilay Lilawala (20BCE141)
- Malav Gajera (20BCE146)
- Malav Shah (20BCE147)

## Institution
Institute of Technology, Nirma University, Ahmedabad, Gujarat, 382481
