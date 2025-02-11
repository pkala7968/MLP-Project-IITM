# MLP-Project-IITM
Machine Learning project for IIT Madras (kaggle competition)

## Overview
This project aims to predict the probability of a system getting infected by various families of malware based on system properties. The dataset consists of telemetry data collected from antivirus software, including system configurations, security settings, and malware detection reports.

## Dataset Description
Each row in the dataset represents a machine, uniquely identified by a MachineID. The target variable indicates whether malware was detected on the machine (target). The dataset consists of the following files:
- train.csv: Training dataset with labeled samples.
- test.csv: Unlabeled dataset for predictions.
- sample_submission.csv: Example submission format.


### Features
The dataset contains a variety of features related to system properties and security settings. Some key features include:

- **System Identifiers**: `MachineID`, `CountryID`, `CityID`
- **Antivirus Information**: `ProductName`, `EngineVersion`, `AppVersion`, `SignatureVersion`, `NumAntivirusProductsInstalled`
- **Operating System Details**: `OSVersion`, `OSBuildNumber`, `OSProductSuite`, `OSArchitecture`
- **Security Settings**: `IsBetaUser`, `RealTimeProtectionState`, `IsSystemProtected`, `FirewallEnabled`, `IsSecureBootEnabled`
- **Hardware Specifications**: `Processor`, `ProcessorCoreCount`, `TotalPhysicalRAMMB`, `PrimaryDiskCapacityMB`
- **User and Region Details**: `LocaleEnglishNameID`, `RegionIdentifier`, `OSUILocaleID`
- **Malware-related Timestamps**: `DateAS` (malware signature dates), `DateOS` (last OS update)

## Project Workflow
1. **Data Preprocessing**:
   - Handle missing values
   - Convert categorical features into numerical representations
   - Normalize or standardize numerical data where necessary

2. **Exploratory Data Analysis (EDA)**:
   - Summary statistics
   - Distribution visualizations
   - Correlation analysis

3. **Feature Engineering**:
   - Extract meaningful insights from date-related features
   - Create derived features based on system configurations
   - Reduce dimensionality using feature selection techniques

4. **Model Training & Evaluation**:
   - Train various machine learning models (Logistic Regression, Random Forest, XGBoost, etc.)
   - Optimize hyperparameters using cross-validation
   - Evaluate model performance using accuracy, F1-score, and AUC-ROC

5. **Prediction & Submission**:
   - Generate predictions on `test.csv`
   - Format results as per `sample_submission.csv`
   - Submit predictions for evaluation
