# King County House Sales Dataset Analysis

## Project Overview
This project focuses on analyzing the King County House Sales dataset to provide insights into the real estate market in King County, Washington. Leveraging data science and machine learning techniques, specifically linear regression, the aim is to predict house prices based on various property characteristics and determine how renovations might affect property values. This analysis will assist real estate agencies and homeowners in making informed decisions regarding property sales and renovations.

## Team Members
- Aggrey Timbwa
- Alex Irungu
- Annah Mukethe
- Brian Ouko
- Petra Kibugu

**Group:** GROUP 16  
**Pace:** Part Time  
**Scheduled Review:** Phase 2  
**Instructor:** Samuel Karu

## Objectives
1. **Develop a Predictive Model:** Build a linear regression model to predict property prices using historical data and property characteristics.
2. **Understand Key Features:** Identify the key features that significantly impact property prices.
3. **Improve Decision Making:** Provide a reliable tool for estimating property prices to enhance decision-making for stakeholders.
4. **Evaluate Model Performance:** Use appropriate metrics to assess the accuracy and performance of the model.

## Dataset Description
The dataset, `kc_house_data.csv`, is a comprehensive collection of house sales in King County, Washington, spanning from May 2014 to May 2015. It consists of 21,597 entries, each representing a unique house sale, and includes 21 features that describe various aspects of the houses sold. These features encompass basic information such as the number of bedrooms (`bedrooms`) and bathrooms (`bathrooms`), as well as more detailed data like the square footage of the living space (`sqft_living`), lot size (`sqft_lot`), and the year the house was built (`yr_built`). Additionally, the dataset includes geographical data such as latitude (`lat`) and longitude (`long`), and economic indicators like the price at which each house was sold (`price`). A separate file, `column_names.md`, provides a detailed description of each column, ensuring clarity and ease of understanding for users analyzing the dataset.

## Project Structure

The project is organized into several key directories and files for ease of navigation and understanding:

- **`data/`**: This directory contains the dataset files.
  - `kc_house_data.csv`: The main dataset file with house sales data.
  - `column_names.md`: Descriptions of the dataset columns.
- **`notebooks/`**: Jupyter Notebooks for analysis and modeling.
  - `index.ipynb`: The primary notebook containing the data analysis, visualization, and modeling steps.
- **`src/`**: Source code for custom functions and utilities used within the notebooks.
  - `data_preprocessing.py`: Functions for data cleaning and preparation.
  - `feature_engineering.py`: Functions for creating new features from the existing data.
  - `model_evaluation.py`: Utilities for evaluating model performance.
- **`requirements.txt`**: A list of Python packages required to run the project.
- **`LICENSE`**: The MIT License file.
- **`README.md`**: The project overview, setup instructions, and additional information.

## Methodology
The project follows a structured data science process:
- **Data Collection and Inspection:** Gather and inspect the provided dataset.
- **Data Cleaning and Preparation:** Handle missing values, outliers, and incorrect data types.
- **Exploratory Data Analysis (EDA):** Analyze the data to find patterns, relationships, and insights.
- **Modeling:** Build predictive models to estimate house prices based on selected features.
- **Model Evaluation:** Assess the models' performance using appropriate metrics.
- **Interpretation:** Draw conclusions from the model results and provide recommendations.

## Detailed Modeling Section

The modeling phase of this project involves several key steps, from feature selection to model evaluation, aimed at building a robust linear regression model to predict house prices. Here's a detailed breakdown:

### 1. Feature Selection

- Initial features were selected based on their expected impact on house prices, as identified during the exploratory data analysis (EDA) phase.
- Correlation analysis was performed to identify highly correlated features that might cause multicollinearity.
- A combination of domain knowledge and statistical tests (e.g., ANOVA for categorical variables) helped refine the feature set.

### 2. Data Preprocessing

- Categorical variables were encoded using one-hot encoding to convert them into a format that could be provided to the model.
- Continuous variables were scaled to have a mean of 0 and a standard deviation of 1, ensuring that no variable would dominate the model due to its scale.

### 3. Model Building

- A linear regression model was chosen as the starting point due to its simplicity, interpretability, and the linear relationship observed between many predictors and the target variable during EDA.
- The model was implemented using the `LinearRegression` class from `scikit-learn`.

### 4. Model Training

- The dataset was split into training and testing sets, with 80% of the data used for training and 20% for testing, to evaluate the model's performance on unseen data.
- The model was trained using the training set, fitting it to predict the house prices based on the selected features.

### 5. Model Evaluation

- The model's performance was evaluated using several metrics, including Root Mean Squared Error (RMSE), Mean Absolute Error (MAE), and R-squared (R²) values, to assess its accuracy and explanatory power.
- A comparison was made between the training and testing set performances to check for overfitting.

### 6. Model Interpretation

- The coefficients of the model were analyzed to understand the impact of each feature on the house price, providing insights into the real estate market in King County.

### 7. Next Steps

- Based on the initial model's performance, further steps could include exploring more complex models, such as polynomial regression or ensemble methods, and conducting feature engineering to uncover more nuanced relationships within the data.

This detailed approach to modeling ensures a thorough understanding of the factors influencing house prices in King County, providing a solid foundation for making informed real estate decisions.

## Tools and Libraries Used
The project utilizes a range of tools and libraries for data analysis and machine learning. Here are the key technologies used:

- **Data Analysis and Manipulation:** 
  - ![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white)
  - ![NumPy](https://img.shields.io/badge/numpy-%23013243.svg?style=for-the-badge&logo=numpy&logoColor=white)
- **Visualization:** 
  - ![Matplotlib](https://img.shields.io/badge/Matplotlib-%23323330.svg?style=for-the-badge&logo=matplotlib&logoColor=white)
- **Machine Learning:** 
  - ![Scikit-learn](https://img.shields.io/badge/scikit_learn-%23F7931E.svg?style=for-the-badge&logo=scikit-learn&logoColor=white)

## How to Run the Project

Before you begin, ensure you have Python 3.8 or later installed on your machine. Follow these steps to set up and run the project:

1. **Clone the Repository:**
   - Open your terminal and run:
     ```
     git clone https://github.com/your-repository-url.git
     cd your-repository-directory
     ```

2. **Install Dependencies:**
   - Ensure `pip` is up to date:
     ```
     python -m pip install --upgrade pip
     ```
   - Install project dependencies:
     ```
     pip install -r requirements.txt
     ```

3. **Launch Jupyter Notebook:**
   - Run the following command to open the project in Jupyter Notebook:
     ```
     jupyter notebook index.ipynb
     ```
   - Run the cells sequentially to reproduce the analysis and results.

## Data Understanding

The initial phase of the project involves importing necessary libraries such as pandas, numpy, matplotlib, seaborn, and various sklearn modules for preprocessing, model selection, and evaluation. The dataset is then loaded for inspection, revealing it contains 21,597 rows and 21 columns, encompassing a wide range of property characteristics.

## Conclusion and Recommendations

This project aims to provide a comprehensive analysis of the King County House Sales dataset to aid real estate agencies and homeowners in making informed decisions regarding property sales and renovations. Through meticulous data preparation, exploratory analysis, and model development, we have uncovered the factors that significantly influence house prices in King County, Washington.

### Recommendations
- **Further Analysis:** Consider conducting a deeper temporal and geospatial analysis to understand market trends over time and the impact of location more precisely.
- **Model Enhancement:** Explore more advanced machine learning models and feature engineering techniques to improve prediction accuracy.
- **Stakeholder Engagement:** Engage with real estate professionals and homeowners to validate findings and gather feedback for future improvements.

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
