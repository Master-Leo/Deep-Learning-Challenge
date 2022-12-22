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
- The variable that is the target for our model is the "IS_SUCCESSFUL" column
- Variables that include the features for our model is all columns except IS_SUCCESSFUl while dropping 'EIN' & 'NAME' columns for non-feature and target values
<img width="630" alt="Screenshot 2022-12-20 at 5 02 37 PM" src="https://user-images.githubusercontent.com/108318921/208796108-659f471e-6de5-41e0-b9b3-923425af719a.png">
<img width="586" alt="Screenshot 2022-12-21 at 9 31 37 PM" src="https://user-images.githubusercontent.com/108318921/209064004-ca940f6e-9710-454c-96cf-3a3d96d35c29.png">

2. Compiling, Training & Evaluating the Model
My first model consisted of the following neuron, layers and activation function parameters:

  - The first hidden node layer consisted of 8 units and the second total value of the x_trained_scaled shape for input_dim, and 'relu' as the the activation function. It brought the total Param # to 156,904
  - The second hidden node layer consisted of 4 units with activation of the 'sigmoid' function with a Param # total of 36
  - The output node layer was set to 1 due to being a binary classifier model of whether it was yes or no for an applicant. I then set the output activation to 'sigmoid' function'

<img width="1115" alt="Screenshot 2022-12-20 at 5 37 26 PM" src="https://user-images.githubusercontent.com/108318921/208800020-81031f7f-9c70-4cc8-b52c-a58130a12f4c.png">

  - After compiling the model with 'adam' optimizer and trained the model with 100 epochs, it evaulated the model to have a best of 0.759 accuracy and .59 Loss

<img width="1125" alt="Screenshot 2022-12-20 at 5 37 42 PM" src="https://user-images.githubusercontent.com/108318921/208800059-1ccc83b5-2511-439c-8603-49aa06f64169.png">

3. Optimize the Model
  - First step into optimizing the model to get the best possible accurate model was implementing a method function that creates Keras sequential model through keras-tuner that loops through a range of input node layers and activation for the hyperparamters 

<img width="946" alt="Screenshot 2022-12-21 at 9 23 12 PM" src="https://user-images.githubusercontent.com/108318921/209063013-3486e561-b43c-4ad7-8995-bd37719c0dd6.png">

  - Next was importing the keras-tuner library and setting a hyperband that will repeat 20 epochs trial for each activation parameter and run the kerastuner search
 
 <img width="1076" alt="Screenshot 2022-12-21 at 9 25 34 PM" src="https://user-images.githubusercontent.com/108318921/209063283-5dc30911-57ec-4869-8b38-1b5d69790f99.png">

  - This process took about an hour to automatically retrieve the best accurate model out of every hyperparameter. Ultimately, selecting sigmoid as the best activatio nand 4 layers and a units ranging from 1-9 for 20 epochs.

<img width="1073" alt="Screenshot 2022-12-21 at 9 27 42 PM" src="https://user-images.githubusercontent.com/108318921/209063544-4ae1c5b7-67d7-4e99-bc53-5728c12d2286.png">

  - The final optimized model selected an accuracy score of .798 and .668 loss 
 
<img width="696" alt="Screenshot 2022-12-21 at 9 30 26 PM" src="https://user-images.githubusercontent.com/108318921/209063863-b8d3b3b6-84f9-44a8-a687-ae0580fbf53c.png">

 
 # Summary: 
