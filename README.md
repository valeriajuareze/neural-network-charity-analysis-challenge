# Neural Network Charity Analysis

## Project Overview 

From Alphabet Soup’s business team, Beks received a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years. Within this dataset are a number of columns that capture metadata about each organization, such as the following:

- **EIN and NAME**—Identification columns

- **APPLICATION_TYPE**—Alphabet Soup application type

- **AFFILIATION**—Affiliated sector of industry

- **CLASSIFICATION**—Government organization classification

- **USE_CASE**—Use case for funding

- **ORGANIZATION**—Organization type

- **STATUS**—Active status

- **INCOME_AMT**—Income classification

- **SPECIAL_CONSIDERATIONS**—Special consideration for application

- **ASK_AMT**—Funding amount requested

- **IS_SUCCESSFUL**—Was the money used effectively

And with my knowledge adcquired of machine learning and neural networks, I’ll use the features in the provided dataset to help Beks create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup.

## Results 

### Data Preprocessing

**1. What variable(s) are considered the target(s) for your model?**

The variable that I considered the target was IS_SUCCESSFUL

![image](https://user-images.githubusercontent.com/108365182/201737937-d20758ae-18ed-4f10-b819-53ad94176678.png)

**2. What variable(s) are considered to be the features for your model?**

All the remaining variables in the database were considered as features

![image](https://user-images.githubusercontent.com/108365182/201738528-4a37575b-dfb8-4d4b-aba3-fb0539525a8c.png)

**3. What variable(s) are neither targets nor features, and should be removed from the input data?**

The unuseful variables that I removed were "EIN" and "NAME" 

![image](https://user-images.githubusercontent.com/108365182/201738983-9d7711b4-f2d2-447c-8f80-0b9c2e21e87a.png)

### Compiling, Training, and Evaluating the Model

**1. How many neurons, layers, and activation functions did you select for your neural network model, and why?**

I selected only two layers with 80 and 30 neurons respectively because it´s enough to have a high perfoemance, also I selected the "relu" activitation in both because it´s the best non-linear activiation function to use. Finally I used the sigmoid function in the oputput layer because it is used for binary classification method where we only have two classes.

![image](https://user-images.githubusercontent.com/108365182/201739508-70620d23-d81b-485c-80c4-4231a3533cf9.png)

**2. Were you able to achieve the target model performance?**

No, I couldn´t achive the target model perfomance with an accuracy over 75%

![image](https://user-images.githubusercontent.com/108365182/201742688-8fbe0b70-7c95-48d9-abbb-84ecfe41d2de.png)

**3. What steps did you take to try and increase model performance?**

Trying to increase the model performance I removed the "SPECIAL_CONSIDERATIONS" and "USE_CASE" features and added a third hidden layer and changed the activitation function of the second and third layer to "tanh", changing the nunmber of nodes to 80 too.  

![image](https://user-images.githubusercontent.com/108365182/201742576-e8c70c52-45d2-4a06-833d-6b3a55a08c56.png)

## Summary

In brief, the first neural network model performed an accuracy of almost 66%, with a loss of 2.01, while the second model performed a lower accuracy of 46% and a lower loss of 0.733. That´s why I recommend to try a different model to increase the performance, such as Random Forest Classifier, which combines a lot of decision trees to predict a classified value. 
