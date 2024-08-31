# Breast Cancer Diagnosis Using Machine Learning

## Live Demo
You can view and interact with the deployed Streamlit application [here](https://breast-cancer-predictor-app-ml.streamlit.app/).

## 1. Introduction to Breast Cancer
Breast cancer is one of the most prevalent forms of cancer, affecting millions of women worldwide. It originates in the cells of the breast, typically in the ducts or lobules, and can spread to other parts of the body if not diagnosed and treated early. According to the World Health Organization (WHO), breast cancer accounts for approximately 15% of all cancer-related deaths among women, making it a significant public health concern (World Health Organization, 2021).

Early detection through screening and advancements in medical imaging techniques have improved the prognosis for many patients. Fine Needle Aspiration (FNA) is one of the minimally invasive methods used to extract samples from suspicious breast tissue, which are then analyzed to determine the presence of malignancy. The ability to accurately classify these samples as benign or malignant is crucial for effective treatment planning (Elmore et al., 2015).

Machine learning models have increasingly been employed to assist in this classification task, leveraging features extracted from cell nucleus images to improve diagnostic accuracy and speed. These models not only provide a reliable second opinion for pathologists but also reduce diagnostic errors, especially in areas with limited access to specialized healthcare professionals (Litjens et al., 2017)

## 2. Objective
The goal of this project is to create a machine learning model designed to determine the nature of breast tissue samples, whether they are benign or malignant, based on features derived from cell nucleus images obtained via fine needle aspiration (FNA). By automating this classification, the model aims to enhance diagnostic efficiency and accuracy, offering a dependable secondary assessment to assist healthcare professionals.

## 3. Dataset
The dataset utilized is the "Breast Cancer Wisconsin (Diagnostic)" dataset, sourced from the UCI Machine Learning Repository. It comprises 569 samples, each with 30 features derived from cell nucleus images, alongside the diagnosis (benign or malignant).

### Columns:
- **ID number**: Unique sample identifier
- **Diagnosis**: Classification of the sample (M = malignant, B = benign)
- **Features**: Each cell nucleus is characterized by ten real-valued metrics, which are computed in three variations: mean, standard error, and the "worst" value (average of the three highest values). These metrics include:
  - Radius (mean distance from center to perimeter points)
  - Texture (standard deviation of gray-scale values)
  - Perimeter
  - Area
  - Smoothness (local variation in radius lengths)
  - Compactness (perimeter² / area - 1.0)
  - Concavity (severity of concave portions of the contour)
  - Concave points (number of concave portions of the contour)
  - Symmetry
  - Fractal dimension (coastline approximation - 1)

## 4. Methodology

### 4.1 Import Libraries
Started by importing essential libraries for data manipulation, visualization, machine learning, model evaluation, and others as required for the analysis.

### 4.2 Exploratory Data Analysis (EDA)
- **4.2.1 Uni-Variate Analysis**: Analyzed individual features to understand their distributions and identify any anomalies or patterns.
- **4.2.2 Bi-Variate Analysis**: Examined relationships between pairs of features to uncover correlations and interactions.
- **4.2.3 Multi-Variate Analysis**: Assessed the interactions among multiple features to understand their combined effects on the target variable.

### 4.3 Data Cleaning
Addressed missing values and outliers to ensure data quality and integrity.

### 4.4 Feature Engineering
- **4.4.1 Log Transformation**: Applied to features with high skewness and large values, to compress value ranges and normalize distributions.
- **4.4.2 Square Root Transformation**: Used for features with moderate skewness, to reduce skewness while maintaining the original data structure.

### 4.5 Target Column Separation and Data Scaling
Separated the target variable from the features and standardized the data to ensure uniform scaling across all features.

### 4.6 Multicollinearity Assessment
Utilized Variance Inflation Factor (VIF) to identify and address multicollinearity among features.

### 4.7 Feature Selection with PCA
Applied Principal Component Analysis (PCA) to reduce dimensionality and enhance model performance by focusing on the most significant components.

### 4.8 Model Selection
Evaluated various classification algorithms including Logistic Regression, Decision Tree Classifier, K-Nearest Neighbors (KNN), Random Forest, XGBoost, and Gradient Boosting.

### 4.9 Hyperparameter Tuning
Optimized model performance by tuning hyperparameters using techniques such as GridSearchCV.

### 4.10 Evaluation of the Model
Assessed model performance using metrics like accuracy, precision, recall, and F1-score to select the best-performing model.

### 4.11 Implementation of the Model
Finalized the top-performing model for deployment in a diagnostic support system. The trained model will be saved for future use and integrated into a Streamlit application.

## 5. Expected Benefits
- **5.1 Enhanced Accuracy**: The automated system aims to minimize diagnostic errors and improve the precision of breast tissue classification, leading to more reliable results.
- **5.2 Increased Efficiency**: By streamlining the diagnostic process, the system accelerates the evaluation of samples, enabling healthcare professionals to dedicate more time to complex cases and patient care.
- **5.3 Greater Accessibility**: The tool offers a valuable resource for regions with limited access to specialized breast cancer expertise, facilitating earlier detection and treatment in underserved areas.

## 6. Conclusion
The machine learning model developed for breast cancer diagnosis shows great promise in improving diagnostic accuracy and efficiency. By thoroughly exploring and preprocessing data, and evaluating multiple algorithms, the optimized Logistic Regression model effectively distinguishes between benign and malignant tissue samples. This model can reduce diagnostic errors and expedite decision making in clinical settings. Integrating it into platforms like Streamlit makes it a valuable tool for diverse healthcare environments. Continued refinement and use of larger datasets could further enhance its accuracy and applicability in breast cancer detection.

---

### Streamlit Implementation
The final model has been integrated into a **Streamlit** web application, providing an interactive user interface for medical professionals to input data and obtain classification results. Additionally, **CSS** was used within the Streamlit app to enhance the user interface for better visualization and a more professional, user-friendly design.
