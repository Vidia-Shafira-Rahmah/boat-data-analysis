# Boat Data Analysis Project

## Project Overview
An end-to-end data analysis project that transforms boat listing data from its initial, varied format through extensive data cleaning, in-depth Exploratory Data Analysis (EDA), and various visualizations, culminating in the development and evaluation of a Machine Learning model for predicting boat listing views.

## Data Source
This dataset was obtained from Kaggle: "Boat Sales"
(https://www.kaggle.com/datasets/karthikbhandary2/boat-sales).

## Methodology
This project follows a standard data science workflow:
1.  **Data Acquisition & Initial Exploration:** The original dataset was obtained from Kaggle. The initial data analysis and preprocessing were first performed in Excel, resulting in the `boat_data analysis.xlsx` file, which then serves as the foundation for further steps.
2.  **Data Cleaning & Preprocessing:**
    * Handling missing values (dropping duplicates, dealing with NaNs).
    * Cleaning and transforming numerical features (e.g., Price_USD, Length, Width, Year Built).
    * Extensive cleaning and standardization of categorical features (e.g., Location, Boat Type, Manufacturer, Material), including text encoding fixes and country mapping.
3.  **Exploratory Data Analysis (EDA):**
    * Analyzing price distribution and comparing it for top-viewed boats.
    * Identifying top categories for Boat Type, Manufacturer, Material, and Location.
    * Analyzing the correlation between Price and Number of Views.
    * Creating various insightful visualizations (box plots, bar plots, scatter plots).
4.  **Machine Learning Modeling:**
    * Preparing features (X) and target (y).
    * Splitting data into training and testing sets.
    * Implementing a robust preprocessing pipeline (StandardScaler for numerical, OneHotEncoder for categorical) using ColumnTransformer.
    * Training and evaluating two regression models: Linear Regression and Random Forest.
    * Analyzing model performance using MAE and R-squared, and examining residuals.

## Key Findings
* Boat prices tend to have a **right-skewed distribution**, indicating the prevalence of lower-priced vessels and the suitability of logarithmic scaling for analysis.
* Exploration of top categories reveals that certain **Boat Types, Manufacturers, and Countries** dominate both the overall listings and the top-viewed boat lists, highlighting market preferences and regional supply.
* A **positive correlation exists between `Price_USD` and `Number of views last 7 days`**. This suggests that, to some extent, more expensive boats might attract greater attention, or specific buyer segments actively seek boats within particular price ranges.
* **Location (Country)** has a significant impact on boat views, as evidenced by its prominence in top-viewed categories.
* The **Random Forest Regression model significantly outperforms Linear Regression** in predicting views, exhibiting a lower Mean Absolute Error (MAE) and a higher R-squared value, showcasing its ability to capture complex relationships in the data.

## Technologies Used
* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* Google Colab

## How to Run
1.  Clone this repository: `git clone https://github.com/Vidia-Shafira-Rahmah/boat-data-analysis.git`
2.  Open the `Boat_data_Analysis.ipynb` file in Google Colab (click the "Open in Colab" badge on GitHub) or any Jupyter Notebook environment.
3.  Run all cells to reproduce the analysis and model.

## License
This project is licensed under the MIT License - see the LICENSE file for details.
