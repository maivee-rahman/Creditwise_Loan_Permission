# Loan Approval Data Analysis & Preprocessing

Welcome to my Loan Approval Data Analysis project! In this notebook, I explored a dataset containing loan applicant details to understand the data structure, clean it up, and find patterns regarding loan approvals.

##  Tools & Libraries Used
This project is built using my core data science stack:
* **Python** 
* **Pandas & NumPy** (For data manipulation and number crunching)
* **Matplotlib & Seaborn** (For bringing the data to life with visualizations)
* **Scikit-Learn** (For data preprocessing)

##  What's Inside?
Here is a quick breakdown of my workflow in this notebook:

1. **Data Loading & Inspection:** 
   I loaded the `loan_approval_data.csv` (which contains 1000 records and 20 features like Income, Credit Score, and Loan Term) and checked the basic statistics to see what I was working with.

2. **Data Cleaning & Handling Missing Values:** 
   Real-world data is rarely perfect. I found some missing values and handled them systematically:
   * Separated the columns into numerical and categorical data.
   * Used Scikit-Learn's `SimpleImputer` to fill missing numerical values with the **mean**.
   * Filled missing categorical values with the **most frequent** category.

3. **Exploratory Data Analysis (EDA):** 
   With clean data in hand, I started visualizing the key features to find insights. The EDA starts by exploring the core question of the dataset: *"Is the Loan Approved or Not?"*

##  How to Run
1. Make sure you have Jupyter Notebook or JupyterLab installed.
2. Ensure the `loan_approval_data.csv` file is in the same directory as the notebook.
3. Open the notebook and run the cells sequentially!

Feel free to explore the code and reach out if you have any questions or feedback.