# Enhancing the Diagnosis of Major Depressive Disorder: A Comparative Study of Machine Learning Models Utilizing EEG Data and the Impact of Gender-Specific Variations

## Overview
This repository contains the code and data used in the thesis project titled **"Enhancing the Diagnosis of Major Depressive Disorder: A Comparative Study of Machine Learning Models Utilizing EEG Data and the Impact of Gender-Specific Variations."** The study evaluates the effectiveness of Frontal Alpha Asymmetry (FAA) and complete EEG data in classifying Major Depressive Disorder (MDD) using traditional and advanced machine learning models.

## Context and Importance of the Study
Major Depressive Disorder (MDD) is a leading cause of disability worldwide, affecting millions of individuals and imposing significant societal and economic burdens. The early detection of MDD is crucial for customizing timely and effective treatment strategies. This study leverages the TD-BRAIN dataset, which provides comprehensive EEG data, to explore the potential of FAA as a biomarker and the comparative performance of traditional and deep learning models in diagnosing MDD.

## Methodology
This study employs a 5-fold cross-validation strategy to ensure robust model evaluation and explores gender-specific variations by analyzing male and female subgroups separately. The research utilizes several machine learning models:
- SVM with FAA features
- SVM with complete EEG data
- LSTM with complete EEG data
- CNN-LSTM with complete EEG data

## Research Questions
The central research question addressed in this thesis is: **To what extent can Frontal Alpha Asymmetry (FAA) and complete EEG data classify Major Depressive Disorder (MDD) when analyzed using traditional and deep learning models, and do these classification methods require gender-specific adaptations to ensure accuracy and reliability?**

To address this question, the main research question has been divided into three subquestions. Each subquestion targets a specific aspect of the overall inquiry, allowing for a detailed exploration of the variables involved.

1. **RQ1.1:** *How does the reliability of FAA as a biomarker compare to complete EEG data in distinguishing between participants with MDD and healthy participants?*
2. **RQ1.2:** *To what extent can deep learning models outperform traditional ML models in classifying participants with MDD and healthy participants as a control group?*
3. **RQ1.3:** *How do the classification accuracies of MDD differ between male and female participants using EEG data across different models?*

## Datasets
The research utilizes the TD-BRAIN dataset, which includes comprehensive EEG recordings. The dataset consists of:
- EEG data from 94 participants (62 male and 32 female)
- Each participant contributed 120 seconds of EEG data, segmented into 12 epochs of 10 seconds each

## Results
This study shows that SVM models using complete EEG data outperform those based on FAA. Furthermore, deep learning models, especially CNN-LSTM, surpass traditional models like SVM and LSTM in classifying MDD from EEG data and even outperformed some models from the literature. However, gender-specific analysis reveals no statistically significant differences in performance across models, suggesting that the current models are robust enough to handle gender-specific variations in EEG data. Overall, complete EEG data and deep learning models offer superior accuracy and robustness in MDD classification.

## Future Research
This study confronts several limitations, such as reliance on subjective clinical diagnoses and computational resource constraints. Future research should focus on developing more objective diagnostic criteria and expanding the sample size and diversity. Extending training durations and increasing the number of epochs could also enhance model performance.

## Repository Structure
- 1_Participants.ipynb: Data preparation and participant information
- 2_Featureextraction_FAA.ipynb: Extraction of FAA features
- 3_SVM_with_FAA.ipynb: SVM model with FAA features
- 4_Feature_Extraction_SVM_EEG_DATA.ipynb: Preprocessing of EEG data
- 5_SVM_EEG_Female.ipynb: SVM model for female participants
- 5_SVM_EEG_General.ipynb: SVM model with complete EEG data
- 5_SVM_EEG_Male.ipynb: SVM model for male participants
- PreparingData_DLModels_EC.ipynb: Preprocessing of EEG data (eyes closed)
- PreparingData_DLModels_EO.ipynb: Preprocessing of EEG data (eyes open)
- 6_LSTM_FEMALE.ipynb: LSTM model for female participants
- 6_LSTM_General.ipynb: LSTM model with complete EEG data
- 6_LSTM_MALE.ipynb: LSTM model for male participants
- 7_CNNLSTM_FEMALE.ipynb: CNN-LSTM model for female participants
- 7_CNNLSTM_General.ipynb: CNN-LSTM model with complete EEG data
- 7_CNNLSTM_MALE.ipynb: CNN-LSTM model for male participants

## Acknowledgments
I would like to thank my supervisor Dr. Rostami Kandroodi for guiding me throughout this process. I am also grateful to Martijn Arts for testing my models on the test set which ranked seconds based on sensitivity, Tuur Smolders for explaining the function of all channels and helping with the calculation of frontal alpha asymmetry, and Ilaria Gavetti for assisting in understanding the data.
