# Neural_Network_Charity_Analysis
![image](https://thomsonlab-webpage-files.s3.amazonaws.com/media/original_images/Banner-AI-2.jpg)


## Background 

Alphabet Soup Foundation is a non-for-profit philanthropic foundation that invests in, and donates to, organizations which protect the environment, promote people's wellbeing and unify the world. The purpose of this challenge is to help the Foundation predict where to make investments using  machine learning and neural networks tehcniques. 

Using a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years, we will create a binary classifier using nerual network design that is capable of predicting whether applicants will be successful if funded by Alphabet Soup. We will analyze the impact of each donation and vet potential recepients to ensure the foundation's money is being used effectively and in an impactful manner. 

The various steps involved in this exercise include:

* Preprocessing Data for a Neural Network Model
* Compile, Train, and Evaluate the Model
* Optimize the Model

## Results: 

### Data Preprocessing

**What variable(s) are considered the target(s) for your model?**

The target for the model is the "Is-Successful" column, reflecting if the funds were used effectively by the business. This is what Alphabet Soup is trying to predict using the model - whether potential recepients will be successful if funded. 

**What variable(s) are considered to be the features for your model?**

The features of this model are the NAME, APPLICATION, TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, INCOME_AMT,SPECIAL_CONSIDERATIONS, STATUS, and ASK_AMT.

**What variable(s) are neither targets nor features, and should be removed from the input data?**

EIN (Employer identificaiton) and NAME were dropped because the numbers could confuse the system into thinking its significant. For the optimization exercise, I also dropped SPECIAL_CONSIDERATIONS because there is only a small percentage of cases that had any special consideration.

### Compiling, Training, and Evaluating the Model

**How many neurons, layers, and activation functions did you select for your neural network model, and why?**
For the initial model (deliverable 2), we used 2 hidden layers with 80 and 30 neurons respectively.
The output layer is made of a unique neuron as it is a binary classification.
To speed up the training process, we used the activation function ReLU for the hidden layers. As our output is a binary classification, Sigmoid is used on the output layer.
For the compilation, the optimizer is adam and the loss function is binary_crossentropy.
**These steps gave us an accuracy of 72.6%**

**Were you able to achieve the target model performance?**

Yes

**What steps did you take to try and increase model performance?**

It required converting the NAME column into data points, which has the biggest impact on improving efficiency. And, it also required adding a third layer and using the "sigmoid" activation function for the 2nd and 3rd layer.

## Summary: 

Overall, by increasing the accuracy above 75% we are able to correctly classify each of the points in the test data 75% of the time. And, an applicant has a 80% chance of being successful if they have the following:
- The NAME of the applicant appears more than 5 times (they have applied more than 5 times)
- The type of APPLICATION is one of the following; T3, T4, T5, T6, T7, T8, T10, and T19
- The application has the following CLASSIFICATION; C1000, C2000, C3000, C1200, and C2100.

A good model to recommend is the Random Forest model because Random Forest are good for classification problems. Using this model produces a 78% accuracy. 
