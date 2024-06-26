### Repository Name:
HeartDiseasePredictionModels

### Project Description:

This repository contains implementations of logistic regression models for predicting heart disease based on a dataset originally consisting of 77 features, later reduced to 14 after published experiments. The models were developed as part of the Ai for Medicine course, focusing on two approaches: gradient descent with sigmoid activation and regularized logistic regression using sklearn.

### Dataset:

The dataset comprises records from the Cleveland, Hungary, Switzerland, and Long Beach V databases, featuring numeric attributes such as age, gender, cholesterol levels, and various clinical parameters related to heart health. Each entry is labeled as 1 (presence of heart disease) or 0 (absence of heart disease).

### Features (numeric):

- age
- sex
- chest pain type (4 values)
- resting blood pressure
- serum cholesterol in mg/dl
- fasting blood sugar > 120 mg/dl
- resting electrocardiographic results (values 0, 1, 2)
- maximum heart rate achieved
- exercise induced angina
- oldpeak (ST depression induced by exercise relative to rest)
- slope of the peak exercise ST segment
- number of major vessels (0-3) colored by fluoroscopy
- thal: 0 = normal, 1 = fixed defect, 2 = reversible defect

### Methodology:

Due to the dataset size (1026 entries), 80% was allocated for training and 20% for testing. Logistic regression was chosen based on its performance in similar studies. Two models were developed:

**Model A:** Implemented using gradient descent with sigmoid activation. Initial attempts encountered overflow issues due to large data values, necessitating normalization.

**Model B:** Utilized regularized logistic regression with sklearn's LogisticRegression module. Data preprocessing included standardization using StandardScaler from sklearn.

### Implementation Details:

- **Data Handling:** Data parsing and manipulation were facilitated using numpy for numerical operations and pandas for structured data representation.
- **Model Training:** Models were trained using a split dataset (80% training, 20% testing) and evaluated based on accuracy metrics.
- **Tools:** Python libraries such as numpy, pandas, and sklearn were instrumental in data handling, preprocessing, and model training.

### References:
- Kaushalya, A. (2021). [Research Paper Title]. Retrieved from [Link to the research paper].

### Conclusion:

This project demonstrates the application of logistic regression models in predicting heart disease risk factors using clinical data. Both implementations provide insights into the effectiveness of different logistic regression techniques for medical diagnostics.

