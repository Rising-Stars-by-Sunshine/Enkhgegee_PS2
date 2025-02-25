# Enkhgegee_PS2


## 1. Overview:
This repository contains a collection of scripts and notebooks designed to perform three key tasks:
1. **Explanation**: Implementing NLP methods (such as sentiment analysis and topic modeling) to explore and interpret textual data.
2. **Prediction**: Applying supervised machine learning models (e.g., Linear Regression) to predict career outcomes based on various factors.
3. **Causal Inference**: Implementing **Regression Discontinuity Design (RD)** analysis to estimate the treatment effect of internships on starting salary, including robustness checks.

The code utilizes a dataset, `education_career_success.csv`, containing various variables related to student demographics, academic performance, internships, and career outcomes.

## 2. Files Included:

- **`education_career_success.csv`**: This is the dataset used for analysis. It contains the following columns:
    - `Student_ID`: Unique identifier for each student.
    - `Age`, `Gender`, `High_School_GPA`, `SAT_Score`, `University_Ranking`, etc.: Features representing the student's background and performance.
    - `Starting_Salary`: The dependent variable representing the salary at the start of the student's career.
    - `Career_Satisfaction`: Text-based column for sentiment analysis.
    - `Field_of_Study`: Text-based column for topic modeling.
    
- **`sentiment_analysis.py`**: This script performs sentiment analysis using the VADER Sentiment Analyzer on the `Career_Satisfaction` column.

- **`topic_modeling.py`**: This script applies Latent Dirichlet Allocation (LDA) topic modeling on the `Field_of_Study` column.

- **`predict_salary.py`**: This script trains a supervised machine learning model (Linear Regression) to predict `Starting_Salary` based on various independent variables.

- **`rd_analysis.py`**: This script performs Regression Discontinuity Design (RD) analysis to estimate the effect of internship completion on starting salary.

## 3. Prerequisites:
Ensure the following libraries are installed to run the code. These are the recommended versions:
- **Python 3.9+**
- **pandas** (v1.2.0+)
- **numpy** (v1.18.5+)
- **matplotlib** (v3.3.4+)
- **seaborn** (v0.11.1+)
- **scikit-learn** (v0.24.2+)
- **nltk** (v3.6.3+)
- **statsmodels** (v0.12.2+)

To install all the dependencies, create a virtual environment and run:

```bash
pip install -r requirements.txt
```

Where `requirements.txt` should contain the following:

```plaintext
pandas==1.2.0
numpy==1.18.5
matplotlib==3.3.4
seaborn==0.11.1
scikit-learn==0.24.2
nltk==3.6.3
statsmodels==0.12.2
```

## 4. Usage Instructions:
### Loading the dataset:
To load the dataset, place the `education_career_success.csv` file in the same directory as the script or notebook. Then, simply run the following command in your notebook or script:

```python
data = pd.read_csv('education_career_success.csv')
```

### Running NLP or Social Network Analysis:
- **Sentiment Analysis**: Run the `sentiment_analysis.py` script to analyze sentiment in the `Career_Satisfaction` column.
  ```bash
  python sentiment_analysis.py
  ```
- **Topic Modeling**: Run the `topic_modeling.py` script to discover topics in the `Field_of_Study` column.
  ```bash
  python topic_modeling.py
  ```

### Training and Evaluating Predictive Models:
- **Predict Starting Salary**: Run the `predict_salary.py` script to train a Linear Regression model and evaluate its performance on predicting `Starting_Salary`.
  ```bash
  python predict_salary.py
  ```

### Running Causal Inference Analysis:
- **Regression Discontinuity Design (RD)**: Run the `rd_analysis.py` script to estimate the treatment effect of internships on `Starting_Salary` using RD design.
  ```bash
  python rd_analysis.py
  ```

## 5. Expected Outputs:
- **Sentiment Analysis**: A distribution of sentiment scores for the `Career_Satisfaction` text column, visualized using a histogram.
- **Topic Modeling**: A list of topics identified in the `Field_of_Study` column, with the top 10 words for each topic.
- **Predictive Model**: Performance metrics (MAE, MSE, and R-squared) for the Linear Regression model predicting `Starting_Salary`.
- **Causal Inference (RD)**: A scatter plot visualizing the RD design and a regression model summary indicating the treatment effect of internships on starting salary.
