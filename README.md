# Kuria Company Tanzanian Well Analysis 
# Business Understanding
## Overview

The Ministry of Water under the Republic of Tanzania has been collecting data on the functionality of water pumps across the country. The dataset includes various features such as the location, type, and condition of the pumps, as well as environmental and socio-economic factors that may influence their functionality. The goal is to analyze this data to predict the operational status of water pumps and identify key factors affecting their performance which will aid in future constructions of wells.

## Objectives
The company has the following objectives in this project:

1. Identify factors influencing the functionality of wells.

2. Provide a strategy for building new wells to the Ministry of Water or donors.

3. Detect patterns that lead to unfunctionality of wells.

4. Recommend a repair strategy for non‑functional wells.

##  Data Understanding and Analysis

## Source of data
The datasets were compiled from Kaggle, being already split into a training set and a testing set. 

## Data Description
 The training set had the following features describing wells;location, installer, funder, source, waterpoint type, etc.
 The target for this project is the status_group.

 The test set consisted only of the features only.

# Key Features
THe features which were utilized to accomplish the objectives were;amount_tsh (total static head, water quantity indicator),gps_height (altitude of well),installer, funder (responsible parties),source, source_type, waterpoint_type (design and water source),payment_type (community payment model),public_meeting, permit (community governance indicators)

# Conclusion
Out of the models used in the project the Random Forest achieved the best macro F1 score and balanced recall across classes.


# Recommendations

1. New wells should be constructed in low-risk areas with reliable installers to reduce the need for frequent repairs.

2. Highly functional water sources should be utilized and constructed more.

3. Introduce manaegable fees to the community that will source income for well repairs.

4. Constant management and monitoring of the water sources so as to track reliability and factors affecting it.
