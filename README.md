# Impact of Marijuana Policy on Injury Crashes


# A Comparative Analysis Across Three States.This project examines the impact of marijuana legislation on traffic injury crashes across Texas, Oklahoma, and Colorado. By analyzing # crash data from these states, this study seeks to provide insights into how marijuana policies influence road safety, using machine learning techniques to model injury outcomes.

# Table of Contents

Introduction
Problem Statement
Data Collection
Data Description
Data Cleaning and Preprocessing
Model Development
Results
Conclusion
Acknowledgements

# Introduction
The legalization of marijuana has brought attention to its impact on traffic safety. Studies show a significant rise in marijuana-related crashes, yet findings on the broader legislative impacts remain inconsistent. This project aims to analyze how marijuana policies and other explanatory factors, such as road type, weather, and light conditions, affect traffic injury crashes.

# Problem Statement
Existing research often focuses on a single region, ignoring the diverse legislative and environmental factors across states. This project seeks to address this gap by comparing the effects of marijuana legislation and other factors on traffic injury crashes across three states.

# Data Collection
Data was sourced from the Departments of Transportation for Texas, Oklahoma, and Colorado for the years 2019–2021. Links to data sources:

Texas Department of Transportation
Oklahoma Department of Public Safety
Colorado Department of Transportation

# Data Description
The combined dataset contains 65,049 rows and 54 columns, including attributes such as:

GISJOIN: Geographic details of the county
Lighting Conditions: e.g., daylight, dark_lighted
Weather Conditions: e.g., clear, cloudy, fog
Road Types: e.g., city street, interstate
Intoxication Type: e.g., alcohol, drug, marijuana
Injury Counts: Total number of injuries per incident

# Data Cleaning and Preprocessing
Missing values (e.g., in the Texas dataset's age variable) were handled by dropping rows with over 5% missing data.
Data was aggregated spatially at the block level using ArcGIS Pro and shapefiles from NHGIS.
# Model Development
A Random Forest Regressor was used to model injury outcomes:

Dependent Variable (y): Log-transformed injury counts (Log_Yes_inj)
Independent Variables: Road type, weather conditions, intoxication type, etc.
Performance:
R² Score: 0.82
MSE: 0.5
Feature Importance: Variables like weather (Clear), road type (City Street), and state policies (State_cat) were significant predictors.

# Results
The Random Forest model explains 82% of the variance in the dataset, indicating strong predictive performance. The analysis reveals that marijuana policies, along with environmental and road factors, significantly impact injury crash outcomes.

# Conclusion
While the current model provides promising results, further exploration with advanced techniques such as Structural Equation Modeling (SEM) is ongoing. Future work will aim to refine insights and enhance model robustness.

# Acknowledgements
This project was developed as part of a Research Assistant Project (Course Code: 6306) under the guidance of Dr. Jianling Li at the University of Texas at Arlington. Contributors:

Karan Yadav
Anirudh Kumar Menga
