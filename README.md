# 📊 Data  Analysis Project

This repository contains a modular and version-controlled data analysis workflow focused on analyzing claim risks and premium profitability patterns for an insurance portfolio. It includes Jupyter notebooks for exploratory data analysis (EDA), reusable Python scripts, and unit testing setup to ensure reproducibility and maintainability.

---

## 🧭 Project Overview

The goal of this project is to understand key risk drivers (geographic, demographic, and vehicle-related) behind claim patterns and to provide insights for improved risk modeling and premium pricing strategies.

The project is organized using best practices including:
- 📓 Modular notebooks for step-by-step EDA
- 🧩 Reusable Python functions for data preprocessing and analysis
- 🧪 Unit testing
- 📦 DVC (Data Version Control) setup
- 🔄 CI/CD integration with GitHub Actions

---

## 📁 Project Structure

- ├── .vscode/
- │ └── settings.json # VSCode project settings
- ├── .github/
- │ └── workflows/
- │ └── unittests.yml # GitHub Actions for CI
- ├── .gitignore # Ignored files and folders
- ├── requirements.txt # Python dependencies
- ├── README.md # Project overview (this file)
- ├── src/
- │ └── init.py # Source directory for potential modules
- ├── notebooks/
- │ ├── EDA.ipynb # Jupyter notebook for EDA
- │ └── README.md # Notebook-specific readme
- ├── tests/
- │ └── init.py # Unit test framework placeholder
- └── scripts/
- ├── init.py
- └── EDA_functions.py # Reusable EDA functions


---

## 🔍 Key Components

### `notebooks/`
Contains interactive Jupyter notebooks for data exploration.  
- **EDA.ipynb**: Step-by-step implementation for:
  - Data import and exploration
  - Handling missing values
  - Removing duplicates
  - Outlier detection using IQR method
  - Using reusable functions from `scripts/`

### `scripts/`
Houses Python scripts with modular functions:
- **EDA_functions.py**:
  - `clean_data(df)`: Handles missing values and duplicate removal
  - `detect_outliers(df, column)`: Detects and removes outliers using IQR
  - Additional EDA utilities

### `tests/`
Provides a framework to implement unit tests for validating functions in `scripts/`.

### `.github/workflows/`
Contains GitHub Actions CI pipeline (`unittests.yml`) to run tests automatically on push or PR.

---

### 2. Running the Jupyter Notebook
- Navigate to the `notebooks/` directory.
- Open `EDA.ipynb` in Jupyter Notebook or JupyterLab.
- Run the notebook cells sequentially to perform data cleaning, exploratory data analysis, and visualization.

### 3. Using Modular Functions
The reusable functions in `scripts/EDA_functions.py` can be imported and used in your notebooks or Python scripts to keep your code clean and maintainable:


---

## Exploratory Data Analysis (EDA) Focus

- **Data Understanding & Quality Assessment:**  
  - Review data types, check for missing values, and assess data quality.  
  - Calculate descriptive statistics for key numerical variables such as `TotalPremium` and `TotalClaims`.

- **Univariate Analysis:**  
  - Plot histograms for numerical variables and bar charts for categorical variables like `Province`, `VehicleType`, and `Gender`.  
  - Detect outliers using box plots, focusing on `TotalClaims` and `CustomValueEstimate`.

- **Bivariate/Multivariate Analysis:**  
  - Calculate overall and segmented Loss Ratios (`TotalClaims / TotalPremium`).  
  - Explore relationships between monthly changes in `TotalPremium` and `TotalClaims` by `ZipCode` using scatter plots and correlation matrices.  
  - Analyze temporal trends in claim frequency and severity over the 18-month period.  
  - Identify vehicle makes/models with the highest and lowest claim amounts.

- **Visualization:**  
  - Produce at least three creative and insightful plots that capture key findings from the EDA.

---

## Git & CI/CD Practices

- Repository is version-controlled with Git and hosted on GitHub.  
- Branch `task-1` is used for the day 1 analysis work.  
- Frequent commits (minimum three per day) with descriptive messages are maintained.  
- GitHub Actions workflow automates testing and validation on each push to `main` and `task-1` branches.

---

## References & Learning Resources

- [Pandas Documentation](https://pandas.pydata.org/docs/) – Data manipulation and analysis.  
- [Matplotlib & Seaborn](https://seaborn.pydata.org/) – Visualization libraries for statistical graphics.  
- [GitHub Actions Documentation](https://docs.github.com/en/actions) – Automating workflows for CI/CD.  
- [Exploratory Data Analysis Techniques](https://www.datacamp.com/tutorial/exploratory-data-analysis-python) – Guide to EDA best practices.

---

## Contact & Contribution

Feel free to open issues or submit pull requests for improvements or additional analyses. Collaboration and knowledge sharing are encouraged!

---

*This README was generated to support the Week 1 task of the Insurance Risk Analytics project, focusing on Git/GitHub setup, CI/CD, and foundational exploratory data analysis.*
