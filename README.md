<!-- Animated Header -->
<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:00C9FF,100:92FE9D&height=220&section=header&text=Salary%20Prediction%20Using%20SLR&fontSize=42&fontColor=ffffff&animation=fadeIn&fontAlignY=38&desc=Simple%20Linear%20Regression%20Machine%20Learning%20Project&descAlignY=58&descSize=18" />
</p>

<!-- Typing Animation -->
<p align="center">
  <img src="https://readme-typing-svg.herokuapp.com?font=Poppins&size=24&duration=3000&pause=800&color=00C9FF&center=true&vCenter=true&width=800&lines=Predicting+Salary+Based+on+Years+of+Experience;Built+with+Python+%7C+Pandas+%7C+Scikit-Learn;Simple+Linear+Regression+Model;Data+Visualization+%2B+Model+Evaluation" />
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.x-blue?style=for-the-badge&logo=python" />
  <img src="https://img.shields.io/badge/Pandas-Data%20Analysis-purple?style=for-the-badge&logo=pandas" />
  <img src="https://img.shields.io/badge/Scikit--Learn-ML-orange?style=for-the-badge&logo=scikit-learn" />
  <img src="https://img.shields.io/badge/Matplotlib-Visualization-green?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Model-Simple%20Linear%20Regression-red?style=for-the-badge" />
</p>

---

# 📌 Salary Prediction Using Simple Linear Regression

This project predicts an employee's **salary** based on their **years of experience** using a **Simple Linear Regression** model.  
The project demonstrates the complete beginner-friendly machine learning workflow: loading data, visualizing relationships, training a regression model, making predictions, and evaluating model performance.

---

## 🎯 Project Objective

The main objective of this project is to build a machine learning model that can estimate salary using only one independent variable:

> **Years of Experience → Salary**

This is a classic regression problem where the goal is to understand the linear relationship between professional experience and salary.

---

## 🚀 Demo Preview

<p align="center">
  <img src="https://media.giphy.com/media/KAq5w47R9rmTuvWOWa/giphy.gif" width="420" alt="Python Machine Learning Animation">
</p>

---

## 🧠 Machine Learning Concept Used

This project uses **Simple Linear Regression**, which fits a straight line between the input feature and target variable.

The equation used by the model is:

```text
Salary = m × YearsExperience + c
```

Where:

| Symbol | Meaning |
|---|---|
| `m` | Coefficient / slope |
| `c` | Intercept |
| `YearsExperience` | Input feature |
| `Salary` | Predicted output |

From the notebook, the trained model learned:

```text
Coefficient: 9449.96
Intercept: 24848.20
```

So the final regression equation is approximately:

```text
Salary = 9449.96 × YearsExperience + 24848.20
```

---

## 📂 Dataset Information

The dataset contains salary information based on years of experience.

| Column Name | Description |
|---|---|
| `YearsExperience` | Number of years of work experience |
| `Salary` | Salary amount |
| `Unnamed: 0` | Index column from the dataset |

Dataset shape:

```text
Rows: 30
Columns: 3
```

There are no missing values in the dataset.

---

## 🛠️ Technologies Used

| Tool / Library | Purpose |
|---|---|
| Python | Programming language |
| Pandas | Data loading and analysis |
| NumPy | Numerical operations |
| Matplotlib | Data visualization |
| Scikit-Learn | Machine learning model building and evaluation |
| Jupyter Notebook / Google Colab | Development environment |

---

## 📊 Data Visualization

The project first visualizes the relationship between **Years of Experience** and **Salary** using a scatter plot.

```python
plt.figure(figsize=(15,4))
plt.scatter(x, y, s=150, color='green')
plt.grid()
plt.xlabel('YearsExperience ----->')
plt.ylabel('Salary ---->')
plt.title('YearsExperience vs Salary')
plt.show()
```

The scatter plot clearly shows a positive linear relationship:

> As years of experience increase, salary also tends to increase.

---

## 🤖 Model Building

The model was built using `LinearRegression` from Scikit-Learn.

```python
from sklearn.linear_model import LinearRegression

model = LinearRegression()
model.fit(x, y)
```

The independent variable was:

```python
x = data[['YearsExperience']]
```

The target variable was:

```python
y = data['Salary']
```

---

## 🔮 Sample Prediction

The model can predict salary for a given number of years of experience.

Example:

```python
model.predict([[5]])
```

Output:

```text
Predicted Salary for 5 years of experience: 72098.02
```

---

## 📈 Actual vs Predicted Visualization

The project compares actual salary values with predicted salary values.

```python
plt.figure(figsize=(12,4))
plt.scatter(x, y, s=160, color='green', label='Actual Data Points')
plt.scatter(x, y_pred, s=160, color='red', marker='x', label='Model Prediction')
plt.plot(x, y_pred, color='red', linestyle='--', label='Model Line')
plt.xlabel('YearsExperience ----->')
plt.ylabel('Salary ---->')
plt.title('YearsExperience vs Salary')
plt.grid()
plt.legend()
plt.show()
```

This visualization helps show how well the regression line fits the actual data points.

---

## 📏 Model Evaluation

The model was evaluated using the following regression metrics:

| Metric | Value |
|---|---:|
| Mean Absolute Error | `4644.20` |
| Mean Squared Error | `31270951.72` |
| Root Mean Squared Error | `5592.04` |
| R² Score | `0.9569` |

---

## ✅ Model Performance Summary

The model achieved an **R² Score of 0.9569**, which means the model explains around **95.69% of the variation in salary** using years of experience.

This indicates that the model performs very well for this simple dataset.

---

## 📌 Key Findings

- Salary has a strong positive relationship with years of experience.
- Simple Linear Regression is suitable for this dataset because the relationship is mostly linear.
- The model can predict salaries with reasonably low error.
- The high R² score shows strong model performance.
- Years of experience is a strong predictor of salary in this dataset.

---

## 📁 Project Structure

```text
Salary-Prediction-Using-SLR/
│
├── Salary_Preduction_using_SLR.ipynb
├── Salary_dataset.csv
├── README.md
└── images/
    ├── scatter_plot.png
    └── regression_line.png
```

> Note: You can create an `images` folder and save your notebook plots there to display them directly in the README.

---

## ⚙️ How to Run This Project

### 1. Clone the Repository

```bash
git clone https://github.com/your-github-username/Salary-Prediction-Using-SLR.git
```

### 2. Navigate to the Project Folder

```bash
cd Salary-Prediction-Using-SLR
```

### 3. Install Required Libraries

```bash
pip install pandas numpy matplotlib scikit-learn
```

### 4. Open the Notebook

```bash
jupyter notebook
```

Then open:

```text
Salary_Preduction_using_SLR.ipynb
```

You can also run this project in **Google Colab**.

---

## 🧾 Complete Workflow

```text
1. Import required libraries
2. Load salary dataset
3. Explore dataset information
4. Select input and target variables
5. Visualize data using scatter plot
6. Train Simple Linear Regression model
7. Predict salaries
8. Add predictions to dataframe
9. Calculate errors
10. Evaluate model using MAE, MSE, RMSE, and R² Score
11. Visualize actual vs predicted values
```

---

## 📚 What I Learned

Through this project, I practiced:

- Loading and exploring datasets using Pandas
- Creating scatter plots using Matplotlib
- Understanding independent and dependent variables
- Building a Simple Linear Regression model
- Making salary predictions
- Evaluating regression models using error metrics
- Understanding the meaning of coefficient, intercept, and R² score

---

## 🔥 Future Improvements

- Add train-test split for better generalization testing
- Build a Streamlit web app for live salary prediction
- Add multiple features such as education level, job role, location, and skill set
- Compare Linear Regression with other regression models
- Save the trained model using Pickle or Joblib
- Deploy the project on Streamlit Cloud or Hugging Face Spaces

---

## 🖥️ Example Output

```text
Input: 5 years of experience
Output: Predicted Salary = 72098.02
```

---

## 📌 Important Note

This project is created for learning and demonstration purposes.  
The predictions are based on a small dataset and should not be used for real-world salary decisions without using a larger and more detailed dataset.

---

## 🙋‍♀️ Author

**Rucha Deshmukh**

<p>
  <a href="https://github.com/your-github-username">
    <img src="https://img.shields.io/badge/GitHub-Profile-black?style=for-the-badge&logo=github" />
  </a>
  <a href="https://www.linkedin.com/in/your-linkedin-profile">
    <img src="https://img.shields.io/badge/LinkedIn-Connect-blue?style=for-the-badge&logo=linkedin" />
  </a>
</p>

---

## ⭐ Support

If you found this project helpful, please consider giving it a star on GitHub.

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:92FE9D,100:00C9FF&height=120&section=footer" />
</p>
