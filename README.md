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

# Visualizations


<img width="853" height="699" alt="Distribution of wells" src="https://github.com/user-attachments/assets/2cca617e-e94f-43d4-9c46-7eeda8d099aa" />

The graph shows the distribution of the different classes of wells according to location in Tanzania.



<img width="908" height="680" alt="Correlation heatmap" src="https://github.com/user-attachments/assets/28974055-678d-43ac-91be-194f9ed2f9b0" />

This shows a correlation heatmap between the features used in the models.



<img width="548" height="453" alt="Confusion matrix" src="https://github.com/user-attachments/assets/a046fa91-8028-4891-97cf-022524acf6ca" />

This is a confusion matrix from the Random forest model.



<img width="589" height="453" alt="y_classes" src="https://github.com/user-attachments/assets/286ba0f4-0015-4e84-a354-d6ae94307c71" />

This bar graph shows the distribution of the target classes(wells according to their functionality). 


<img width="567" height="433" alt="Model comparisons" src="https://github.com/user-attachments/assets/45da0df8-5368-4ffe-b50a-5ea16b5d2e73" />

This shows the model perfomances according to the F1 scores.

# Conclusion
Out of the models used in the project the Random Forest achieved the best macro F1 score and balanced recall across classes.


# Recommendations

1. New wells should be constructed in low-risk areas with reliable installers to reduce the need for frequent repairs.

2. Highly functional water sources should be utilized and constructed more.

3. Introduce manaegable fees to the community that will source income for well repairs.

4. Constant management and monitoring of the water sources so as to track reliability and factors affecting it.





