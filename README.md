# Deep Learning for Healthcare Final Project: Reproducing Applying Convolutional Neural Networks to Predict the ICD-9 Codes of Medical Records

We researched the paper "Applying Convolutional Neural Networks to Predict the ICD-9 Codes of Medical Records" and reproduced the results from this paper.

Original Paper Citation: 
Hsu J-L, Hsu T-J, Hsieh C-H, Singaravelan A. Applying Convolutional Neural Networks to Predict the ICD-9 Codes of Medical Records. Sensors. 2020; 20(24):7116. https://doi.org/10.3390/s20247116

Link to codebase: https://github.com/zliendo/AI_MedicalNotes/blob/master/pipeline/icd9_lstm_cnn_workbook.ipynb

Dependencies: 
- pandasql
- numpy
- pandas
- keras
- sklearn
- tensorflow

Dataset: MIMIC III 
https://mimic.mit.edu/

Instructions for downloading dataset: https://eicu-crd.mit.edu/gettingstarted/access/

  - This is the Medical Information Mart for Intensive Care Dataset. You can obtain it by getting approval on the Physionet website. This is dataset is publically available and contains deidentified health-related data. You will also need to complete the Collaborative Institutional Training Initiative (CITI) Program's "Data or Specimens Only Research" course. Once you complete this training program and apply you can become a credentialed Physionet user.

Data Cleaning and Pre-Processing:
- used pandasql and regular expressions for the initial cleaning of the code and consolidation to a dataframe with the proper formatting of ICD-9 codes. We then pre-processed the data by vectorizing the document
- 10 fold cross-validation

Models:
- LSTM Model
- CNN Model
  - convolution layer
  - embedding layer: we created our own pretrained glove embedding
  - max pooling layer
  - flatten
  - dropout layer
  - 15 epochs
  - 32 batch size
  - 0.001 learning rate
  - Adam Optimizer

Evaluation:
- accuracy
- recall
- precision
- f1 score

Table of Results for CNN Model:

<img width="412" alt="Screen Shot 2022-05-07 at 9 24 51 PM" src="https://user-images.githubusercontent.com/24924126/167281679-721ee3ce-2e13-4c8f-8d4b-1b71cb0c2e8f.png">

<img width="400" alt="Screen Shot 2022-05-07 at 9 25 06 PM" src="https://user-images.githubusercontent.com/24924126/167281681-a800f866-d042-4707-8c7a-eab9972fe2c8.png">

