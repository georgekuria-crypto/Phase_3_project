# Phase_3_project
# Business Understanding
## Overview

The Ministry of Water under the Republic of Tanzania has been collecting data on the functionality of water pumps across the country. The dataset includes various features such as the location, type, and condition of the pumps, as well as environmental and socio-economic factors that may influence their functionality. The goal is to analyze this data to predict the operational status of water pumps and identify key factors affecting their performance.

## Objectives
Identify factors influencing the functionality of wells.

Provide a strategy for building new wells to the Ministry of Water or donors.

Detect patterns that lead to unfunctionality of wells.

Recommend a repair strategy for non‑functional wells.

## Data
Training set: Features describing wells (location, installer, funder, source, waterpoint type, etc.) and labels (status_group).

Test set: Features only, used for generating predictions.

Rows: ~59,000 wells.

Columns: ~40 features (numeric + categorical).

# Key Features
amount_tsh (total static head, water quantity indicator)

gps_height (altitude of well)

installer, funder (responsible parties)

source, source_type, waterpoint_type (design and water source)

payment_type (community payment model)

public_meeting, permit (community governance indicators)

# Methodology

1. Data Preparation
Dropped identifiers and redundant columns to prevent leakage.

Handled missing values (None for categorical, median for numeric).

Converted categorical features to strings for consistent encoding.

Removed highly correlated numeric features (threshold > 0.85).

Stratified train/test split to preserve class balance.

2. Preprocessing Pipelines
Numeric: imputation + scaling.

Categorical: imputation + one‑hot encoding.

Combined using ColumnTransformer for reproducibility.

3. Models
Baseline Logistic Regression: interpretable benchmark.

Tuned Logistic Regression: optimized regularization (C).

Decision Tree: interpretable rules, non‑linear splits.

Random Forest: ensemble for robustness and feature importance.

4. Evaluation
Metrics: macro F1, per‑class precision/recall, confusion matrix.

Emphasis on recall for “needs repair” and “non‑functional” classes.

5. Feature Importance
Permutation importance to identify top drivers of well functionality.

Risk tables for categorical features (e.g., source type, payment type).

# Results
Random Forest achieved the best macro F1 and balanced recall across classes.

Key drivers of well functionality include:

Source type (groundwater vs. surface water).

Waterpoint type (communal standpipe vs. borehole).

Installer/funder quality.

GPS height and water quantity indicators.

# Recommendations
For New Wells
Prioritize low‑risk regions and reliable installers.

Adopt design standards linked to higher functionality (e.g., boreholes, protected sources).

Require community payment models that sustain maintenance.

For Detecting Failures
Monitor wells with surface water sources and seasonal quantity patterns.

Flag wells installed by vendors with poor historical performance.

For Repairs
Triage repairs using model probabilities.

Focus on components most linked to failure (e.g., pump/extraction type).

Deploy repair teams regionally to hotspots.

# Visuals
Class distribution bar chart.

Correlation heatmap.

Confusion matrix heatmap.

Feature importance bar chart.

# 
Next Steps
Incorporate geospatial analysis for regional risk mapping.

Deploy predictive model for real‑time monitoring.

Continuous retraining with updated well data.

Ethical communication of model limitations to stakeholders.

<img width="853" height="699" alt="Distribution of wells" src="https://github.com/user-attachments/assets/2cca617e-e94f-43d4-9c46-7eeda8d099aa" />

<img width="908" height="680" alt="Correlation heatmap" src="https://github.com/user-attachments/assets/28974055-678d-43ac-91be-194f9ed2f9b0" />

<img width="548" height="453" alt="Confusion matrix" src="https://github.com/user-attachments/assets/a046fa91-8028-4891-97cf-022524acf6ca" />

<img width="589" height="453" alt="y_classes" src="https://github.com/user-attachments/assets/286ba0f4-0015-4e84-a354-d6ae94307c71" />

<img width="567" height="433" alt="Model comparisons" src="https://github.com/user-attachments/assets/45da0df8-5368-4ffe-b50a-5ea16b5d2e73" />


