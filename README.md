# Machine Learning Regression Using Grid Search

## 📌 Project Overview

This project implements and compares multiple supervised Machine Learning regression algorithms to predict medical insurance expenses based on customer information.

The project uses GridSearchCV for hyperparameter tuning, evaluates model performance using the R² score, and saves the trained model for future predictions. It also explores deploying the insurance expense prediction model using Streamlit.

## 🎯 Project Objective

To predict medical insurance expenses using features such as age, BMI, number of children, sex, smoking status, and geographical region.

## 🤖 Algorithms Implemented

- Multiple Linear Regression
- Decision Tree Regression
- Random Forest Regression
- Support Vector Regression (SVR)

## 📂 Dataset Features

The project uses the `insurance.csv` dataset.

**Input Features:**
- Age
- BMI (Body Mass Index)
- Children
- Sex
- Smoker
- Region

**Target Variable:**
- `expenses` — Medical insurance expenses

## 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- Pickle
- Streamlit

## ⚙️ Project Workflow

1. Load the insurance dataset using Pandas.
2. Preprocess categorical features using one-hot encoding.
3. Separate independent and dependent variables.
4. Split the data into training and testing sets.
5. Apply GridSearchCV for hyperparameter tuning.
6. Train regression models using the selected parameters.
7. Predict insurance expenses for test data.
8. Evaluate models using the R² score.
9. Save the trained model using Pickle.
10. Develop an interactive insurance expense prediction application using Streamlit.

## 📊 Model Performance

The following R² scores were recorded in the project:

| Regression Algorithm | R² Score |
|---|---:|
| Multiple Linear Regression | 0.8226 |
| Decision Tree Regression | 0.8911 |
| Random Forest Regression | 0.9213 |
| Support Vector Regression (SVR) | 0.8875 |

**Best recorded result:** Random Forest Regression, with an R² score of approximately **0.9213**.

An R² score measures how well a regression model explains the variation in the target variable. A higher score generally indicates a better fit on the evaluated dataset.

*Note: These are the recorded project results. For a fair comparison, evaluate every model using the same test dataset and evaluation procedure.*

## 🔍 Hyperparameter Tuning

GridSearchCV is used to test different model settings and select the best combination based on cross-validation.

For Multiple Linear Regression, the parameter grid includes:

- `fit_intercept`: `True` or `False`
- `positive`: `True` or `False`

The model is evaluated using the R² scoring metric during cross-validation.

## 💾 Model Deployment

The trained regression model is saved using Pickle.

Example:

```python
import pickle

filename = "Insurance_expense.sav"
pickle.dump(regressor, open(filename, "wb"))
```

The saved model can later be loaded to predict insurance expenses for new customer inputs.

**Security note:** Only load Pickle files from trusted sources.

## 🌐 Streamlit Application

The project also includes a Streamlit application for interactive insurance expense prediction.

Users can enter customer details, such as age, BMI, number of children, sex, smoking status, and region, to obtain a predicted insurance expense.

To install the required packages:

```bash
pip install pandas numpy matplotlib scikit-learn streamlit
```

To launch the application, run:

```bash
streamlit run app.py
```

Ensure that `app.py`, the saved model file (`Insurance_expense.sav`), and any required project files are available in the appropriate directory.

## 📈 Key Learnings

- Understanding supervised Machine Learning regression.
- Comparing multiple regression algorithms.
- Encoding categorical variables.
- Applying GridSearchCV for hyperparameter tuning.
- Evaluating regression models using R² scores.
- Saving and loading trained models with Pickle.
- Building an interactive prediction application using Streamlit.

## 🔮 Future Improvements

- Evaluate models using MAE, MSE, and RMSE.
- Perform cross-validation for more reliable performance estimates.
- Improve model selection through additional hyperparameter tuning.
- Add visualizations comparing actual and predicted insurance expenses.
- Deploy the Streamlit application online.

## 👩‍💻 Author

**Sowmiya S**

- LinkedIn:(https://www.linkedin.com/in/sowmiya-s-70546b275/)


## ⭐ Acknowledgement

This project was developed as a practical exercise in regression modelling, hyperparameter tuning, model evaluation, and deployment using Python and Scikit-learn.
