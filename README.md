# PREDICTING MAJOR DEPRESSIVE DISORDER WITH EEG DATA: THE ROLE OF FRONTAL ALPHA ASYMMETRY AND DEEP LEARNING MODELS - A GENDER-SPECIFIC ANALYSIS USING THE TD-BRAIN DATASET

## Overview
This repository contains the code and data used in the thesis project titled **"Predicting Major Depressive Disorder with EEG Data: The Role of Frontal Alpha Asymmetry and Deep Learning Models - A Gender-Specific Analysis Using the TD-BRAIN Dataset."** The study evaluates the effectiveness of Frontal Alpha Asymmetry (FAA) and complete EEG data in classifying Major Depressive Disorder (MDD) using traditional and advanced machine learning models.

## Context and Importance of the Study
Major Depressive Disorder (MDD) is a leading cause of disability worldwide, affecting millions of individuals and imposing significant societal and economic burdens. The early detection of MDD is crucial for customizing timely and effective treatment strategies. This study leverages the TD-BRAIN dataset, which provides comprehensive EEG data, to explore the potential of FAA as a biomarker and the comparative performance of traditional and deep learning models in diagnosing MDD.

## Societal and Scientific Relevance
Accurate prediction of MDD is essential for effective treatment and management. This research aims to deliver significant societal benefits by enabling better anticipation of MDD onset, which can guide timely interventions. Scientifically, this thesis advances the field of psychiatric diagnostics by integrating traditional statistical methods with innovative machine learning techniques. This study enhances our understanding of MDD dynamics and lays the foundation for handling complex biomedical datasets.

## Methodology
This study employs a 5-fold cross-validation strategy to ensure robust model evaluation and explores gender-specific variations by analyzing male and female subgroups separately. The research utilizes several machine learning models:
- Support Vector Machine (SVM) with FAA features
- SVM with complete EEG data
- LSTM with complete EEG data
- CNN-LSTM with complete EEG data

## Research Questions
The central research question addressed in this thesis is: **How effectively can FAA and complete EEG data classify MDD when analyzed using traditional and deep learning models, and how do these classification methods vary in effectiveness based on gender?**

To address this question, the main research question has been divided into three subquestions. Each subquestion targets a specific aspect of the overall inquiry, allowing for a detailed exploration of the variables involved.

1. **RQ1.1:** *Is FAA a reliable biomarker for distinguishing between participants with MDD and healthy participants?*
2. **RQ1.2:** *To what extent can deep learning models outperform traditional ML models in classifying participants with MDD and healthy participants as a control group?*
3. **RQ1.3:** *Is there a difference in the classification of MDD patients between genders using EEG data?*

## Datasets
The research utilizes the TD-BRAIN dataset, which includes comprehensive EEG recordings. The dataset consists of:
- EEG data from 94 participants (62 male and 32 female)
- Each participant contributed 120 seconds of EEG data, segmented into 12 epochs of 10 seconds each

## Results
The findings indicate that while FAA can serve as a biomarker, its standalone effectiveness is limited compared to using complete EEG data. The LSTM model achieved the highest validation accuracy at 66.4% and a test accuracy of 63.2%, demonstrating superior performance over the SVM model. Gender-specific analysis revealed that female participants generally achieved higher classification accuracy with the SVM model, while the performance of deep learning models varied across genders.

## Conclusion
These results highlight the potential of integrating comprehensive EEG data with advanced ML techniques to improve MDD diagnosis, emphasizing the need for personalized diagnostic approaches. The study's insights contribute to a nuanced understanding of MDD and set the stage for future innovations in psychiatric diagnostics and personalized medicine.

## Future Research
This study confronts several limitations, such as reliance on subjective clinical diagnoses and computational resource constraints. Future research should focus on developing more objective diagnostic criteria and expanding the sample size and diversity. Extending training durations and increasing the number of epochs could also enhance model performance.

## Repository Structure
- `1_Participants.ipynb`: Data preparation and participant information
- `2_Featureextraction_FAA.ipynb`: Extraction of FAA features
- `3_SVM_with_FAA.ipynb`: SVM model with FAA features
- `4_EEG_DATA_EC.ipynb`: Preprocessing of EEG data (eyes closed)
- `4_EEG_DATA_EO.ipynb`: Preprocessing of EEG data (eyes open)
- `5_EEG_DATA_SVM_GENERAL.ipynb`: SVM model with complete EEG data
- `5_EEG_DATA_SVM_FEMALE.ipynb`: SVM model for female participants
- `5_EEG_DATA_SVM_MALE.ipynb`: SVM model for male participants
- `6_EEG_DATA_LSTM_GENERAL.ipynb`: LSTM model with complete EEG data
- `6_EEG_DATA_LSTM_FEMALE.ipynb`: LSTM model for female participants
- `6_EEG_DATA_LSTM_MALE.ipynb`: LSTM model for male participants
- `7_EEG_DATA_CNN_LSTM_GENERAL.ipynb`: CNN-LSTM model with complete EEG data
- `7_EEG_DATA_CNN_LSTM_FEMALE.ipynb`: CNN-LSTM model for female participants
- `7_EEG_DATA_CNN_LSTM_MALE.ipynb`: CNN-LSTM model for male participants
- `McNemartest.ipynb`: Statistical analysis using McNemar's test

## Acknowledgments
I would like to thank my supervisor Dr. Rostami Kandroodi for guiding me throughout this process. I am also grateful to Martijn Arts for testing my models on the test set which ranked seconds based on sensitivity, Tuur Smolders for explaining the function of all channels and helping with the calculation of frontal alpha asymmetry, and Ilaria Gavetti for assisting in understanding the data.
