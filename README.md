# Loan Approval Prediction with Random Forest

## Problem Statement and Goal of Project
The goal of this project is to develop a machine learning model to predict loan approval status based on applicant information. The problem is to accurately classify whether a loan application will be approved (`Y`) or rejected (`N`) using features such as gender, marital status, income, loan amount, credit history, and property area. This predictive model can assist financial institutions in automating and improving the efficiency of their loan approval processes.

## Solution Approach
The solution employs a **Random Forest Classifier** to predict loan approval outcomes. The approach involves the following steps:
1. **Data Preprocessing**:
   - Encoding categorical variables (e.g., Gender, Married, Education) into numerical values using mapping.
   - Handling missing values by imputing them with the mode for categorical features and the mean for numerical features.
   - Replacing specific values (e.g., `3+` in Dependents) with numerical equivalents.
2. **Feature Selection**:
   - Features include Gender, Married, Dependents, Education, Self_Employed, ApplicantIncome, CoapplicantIncome, LoanAmount, Loan_Amount_Term, Credit_History, and Property_Area.
   - The `Loan_ID` column is excluded as it is not relevant for prediction.
3. **Model Training**:
   - A Random Forest Classifier is used due to its robustness with large datasets and ability to handle complex feature interactions.
   - Feature importance is analyzed to understand which variables most significantly impact loan approval predictions.
4. **Visualization**:
   - A horizontal bar plot is created to display the feature importance scores derived from the Random Forest model, highlighting the relative contribution of each feature.

## Technologies & Libraries
The project is implemented in Python within a Jupyter Notebook environment, utilizing the following libraries:
- **Pandas**: For data manipulation and analysis.
- **NumPy**: For numerical operations.
- **Matplotlib** and **Seaborn**: For data visualization, including the feature importance plot.
- **Scikit-learn**: For implementing the Random Forest Classifier and data preprocessing (e.g., LabelEncoder, though commented out in favor of manual mapping).
- **Jupyter Notebook**: For interactive development and visualization.

## Description about Dataset
The dataset, stored in `train.csv`, contains 614 entries with 13 columns describing loan applicants. Key features include:
- **Loan_ID**: Unique identifier for each loan application (not used in modeling).
- **Gender**: Male (1) or Female (0).
- **Married**: Yes (1) or No (0).
- **Dependents**: Number of dependents (0, 1, 2, 3+ mapped to 3).
- **Education**: Graduate (1) or Not Graduate (0).
- **Self_Employed**: Yes (1) or No (0).
- **ApplicantIncome**: Income of the primary applicant.
- **CoapplicantIncome**: Income of the co-applicant.
- **LoanAmount**: Loan amount requested (in thousands).
- **Loan_Amount_Term**: Term of the loan in months.
- **Credit_History**: Credit history status (1 for good, 0 for bad).
- **Property_Area**: Urban (2), Semiurban (1), or Rural (3).
- **Loan_Status**: Target variable (Y=1 for approved, N=0 for not approved).

The dataset contains missing values in columns such as Gender (13), Married (3), Dependents (15), Self_Employed (32), LoanAmount (22), Loan_Amount_Term (14), and Credit_History (50), which are handled during preprocessing.

## Installation & Execution Guide
To run this project locally, follow these steps:
1. **Clone the Repository**:
   ```bash
   git clone https://github.com/imehranasgari/loan-approval-prediction.git
   cd loan-approval-prediction
   ```
2. **Set Up a Virtual Environment** (recommended):
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```
3. **Install Dependencies**:
   Ensure you have Python 3.9 installed, then run:
   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn jupyter
   ```
4. **Run the Jupyter Notebook**:
   ```bash
   jupyter notebook "Random Forest (Classification).ipynb"
   ```
5. **Dataset Requirement**:
   - Place the `train.csv` file in the same directory as the notebook.
   - The dataset is not included in the repository but should match the structure described above.

## Key Results / Performance
- The project successfully preprocesses the dataset, handling missing values and encoding categorical variables.
- A Random Forest Classifier is trained, and feature importance is visualized, indicating which features (e.g., Credit_History, ApplicantIncome) most influence loan approval predictions.
- **Note**: The notebook does not include explicit performance metrics (e.g., accuracy, precision, recall) or a train-test split evaluation, as the focus is on data preprocessing and feature importance analysis. This demonstrates an exploratory approach to understanding the Random Forest algorithm and its application to classification tasks.

## Screenshots / Sample Outputs
The notebook generates a horizontal bar plot showing the feature importance scores from the Random Forest Classifier. Below is a description of the output:
- **Feature Importance Plot**:
  - Displays the relative importance of each feature (e.g., Credit_History, ApplicantIncome, LoanAmount) in predicting loan approval.
  - The plot uses a purple color scheme and is sorted in ascending order of importance.
  - **Note**: The actual plot image is embedded in the notebook but may not render correctly on GitHub. Please view the notebook via [nbviewer.org](https://nbviewer.org) for full visualization.

## Additional Learnings / Reflections
This project was an opportunity to explore the Random Forest Classifier for a real-world classification problem. Key learnings include:
- **Data Preprocessing**: Gained hands-on experience in handling missing values and encoding categorical variables, critical steps in preparing data for machine learning.
- **Feature Importance**: Learned how to interpret feature importance scores from Random Forest, providing insights into which factors drive loan approval decisions.
- **Visualization**: Developed skills in creating clear, professional visualizations using Matplotlib to communicate model insights effectively.
- **Exploratory Approach**: While the project focuses on preprocessing and feature analysis rather than final model evaluation, it showcases a strong understanding of the Random Forest algorithm and its application to large datasets with complex feature interactions.

This project reflects my ability to tackle practical machine learning problems, preprocess data effectively, and derive meaningful insights, which are valuable skills for roles in data science and AI development.

## 👤 Author
**Mehran Asgari**  
**Email**: [imehranasgari@gmail.com](mailto:imehranasgari@gmail.com)  
**GitHub**: [https://github.com/imehranasgari](https://github.com/imehranasgari)

## 📄 License
This project is licensed under the Apache 2.0 License – see the `LICENSE` file for details.

> 💡 *Some interactive outputs (e.g., plots, widgets) may not display correctly on GitHub. If so, please view this notebook via [nbviewer.org](https://nbviewer.org) for full rendering.*
```