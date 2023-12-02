#McD_Nutrition_Planner

This code is a Streamlit web application designed to help users plan a nutritionally balanced meal at McDonald's. The application takes user input for various nutrition constraints, filters McDonald's menu items based on these constraints, and recommends a set of menu items that best match the user's preferences. The recommendations are then visualized through a table and a bar plot showing the nutrition information of the recommended items.

Let's break down the code:
Importing Libraries
streamlit, pandas, matplotlib, and seaborn libraries are imported to create a web application, handle data, and visualize the recommendations.
Loading McDonald's Menu Data
The code loads menu data from a CSV file named 'Menu.csv' using pd.read_csv('Menu.csv').
Column names are converted to lowercase for consistency using menu_data.columns = menu_data.columns.str.lower().
Streamlit Application Setup
The Streamlit application is initialized with a title and introductory text.
User Input for Nutrition Constraints
The user can set various nutrition constraints through sliders in the sidebar. These constraints include maximum/minimum values for total fat, saturated fat, sugar, carbohydrates, and protein.
Filtering Menu Items
The menu items are filtered based on user-defined constraints using boolean indexing.
Calculating Similarity Scores
Similarity scores are calculated to find items that are closest to the user's preferences. The scores are computed based on the squared differences between user input and menu item nutrition values.
Sorting and Displaying Recommendations
The menu items are sorted based on similarity scores, and the top recommendations are displayed in a table using st.table().
Visualizing Nutrition Information
A bar plot is created using matplotlib and seaborn to visualize the nutrition information of the recommended items.
The bar plot includes information about total fat, saturated fat, sugar, carbohydrates, and protein for the recommended items.
Displaying Total Calories
The total calories for the recommended items are calculated and displayed as a subheader.
Data Science/Analysis Concepts Used:
Data Loading: Loading menu data from an external CSV file using pandas.
Data Cleaning: Converting column names to lowercase for consistency.
Data Filtering: Filtering menu items based on user-defined nutrition constraints.
Similarity Calculation: Computing similarity scores to find items that closely match user preferences.
Data Visualization: Using matplotlib and seaborn for visualizing nutrition information through a bar plot.
Interactive Web Application: Creating an interactive web application using Streamlit for user input and displaying recommendations.

This code integrates various data science and data analysis concepts to provide a user-friendly tool for planning a balanced meal based on nutrition constraints.
