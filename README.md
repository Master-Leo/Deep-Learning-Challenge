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

# Results

1. Data Processing:
- THe variable that is the target for our model is the "IS_SUCCESSFUL" column
- Variables that include the features for our model is all columns except IS_SUCCESSFUl while dropping 'EIN' & 'NAME' columns for non-feature and target values
<img width="630" alt="Screenshot 2022-12-20 at 5 02 37 PM" src="https://user-images.githubusercontent.com/108318921/208796108-659f471e-6de5-41e0-b9b3-923425af719a.png">
<img width="628" alt="Screenshot 2022-12-20 at 5 21 28 PM" src="https://user-images.githubusercontent.com/108318921/208798193-3e7a0e37-370c-4f21-b663-af853d3bbafb.png">

2. Compiling, Training & Evaluating the Model
My first model consisted of the following neuron, layers and activation function parameters:
  - The first hidden node layer consisted of 8 units and the second total value of the x_trained_scaled shape for input_dim, and 'relu' as the the activation function. It brought the toal Param # to 156,904
  - The second hidden node layer consisted of 4 units with activation of the 'sigmoid' function with a Param # total of 36
  - The output node layer was set to 1 due to being a binary classifier model of whether it was yes or no for an applicant. I then set the output activation to 'sigmoid' function'
<img width="1115" alt="Screenshot 2022-12-20 at 5 37 26 PM" src="https://user-images.githubusercontent.com/108318921/208800020-81031f7f-9c70-4cc8-b52c-a58130a12f4c.png">
  - After compiling the model with 'adam' optimizer and trained the model with 100 epochs, it evaulated the model to have a best of 0.72 accuracy and .58 Loss
<img width="1125" alt="Screenshot 2022-12-20 at 5 37 42 PM" src="https://user-images.githubusercontent.com/108318921/208800059-1ccc83b5-2511-439c-8603-49aa06f64169.png">



