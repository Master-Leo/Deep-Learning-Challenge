# Deep-Learning-Challenge

# Report on Neural Network Model

Diving deep into learning whether charity funding projects predict success utilizing nueral networks

# Overview

I was responsible for creating a model that will predict nonprofit funding success for applicants in their ventures. I was provided a dataset to create a binary classifier that can predict the outcomes of their funding applicants by Alphabet Soup. The usage of a csv contatining a total of 34,0000 organizations metadata were extracted and transformed to an ideal dataframe. Within that dataset it captured a variety of columns that were aided into testing and training the neural netowrk model, such as: 
- EIN and NAME—Identification columns
- APPLICATION_TYPE—Alphabet Soup application type
- AFFILIATION—Affiliated sector of industry
- CLASSIFICATION—Government organization classification
- USE_CASE—Use case for funding
- ORGANIZATION—Organization type
- STATUS—Active status
- INCOME_AMT—Income classification
- SPECIAL_CONSIDERATIONS—Special considerations for application
- ASK_AMT—Funding amount requested
- IS_SUCCESSFUL—Was the money used effectively

#Results

1. Data Processing:
- Dataframe was loaded and dropped 'EIN' & 'NAME' columns for non-feature and target values
<img width="630" alt="Screenshot 2022-12-20 at 5 02 37 PM" src="https://user-images.githubusercontent.com/108318921/208796108-659f471e-6de5-41e0-b9b3-923425af719a.png">

