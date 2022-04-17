# DLH_Final_Project

We researched the paper "Applying Convolutional Neural Networks to Predict the ICD-9 Codes of Medical Records" and replicated the results from this paper.

Dataset: MIMIC III 

Data Cleaning and Pre-Processing:
- used pandas for the initial cleaning of the code and consolidation to a dataframe with the proper formatting of ICD-9 codes. We then pre-processed the data by vectorizing the document
- 10 fold cross-validation

Models:
- baseline model to predict top 4 ICD-9 Codes
- LSTM Model
- CNN Model
  - convolution layer
  - embedding layer
  - max pooling layer
  - flatten
  - dropout layer
  - 20 epochs
  - Adam Optimizer

Evaluation:
- accuracy
- recall
- precision
- f1 score

