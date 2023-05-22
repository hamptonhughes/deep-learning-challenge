# deep-learning-challenge

## Overview of the Analysis

For this project, we are using historical funding data from non-profit Alphabet Soup to try to predict whether a venture will be successful.  We have data on over 34,000 ventures--including use case, organization type, income amount, and how much money they are asking for.  The target variable that we will be using to test the model against is whether or not the venture was successful. <br><br>

We built a neural network in order to try to make predictions a venture's success.  We took the following steps in order to pre-process the data:<br>
    *Separating the features and the target variables <br>
    *Splitting the data into testing and training data<br>
    *Removed EIN and NAME columns, which are neither targets nor features <br>
    *Scaling the data using StandardScaler<br>
    *Encode categorical variables using getdummies<br>
    *Place the rarer instances "APPLICATION TYPE" and "CLASSIFICATION" variabes into an "other" bin<br><br>
    ![alt text](images/binning.png)
    
## Model Build and Optimiation

For the model build, I initially used one hidden layer with 5 neurons and a relu activation function.  For the output layer, I used a sigmoid function.  This model yielded a roughly 72.5% accuracy for the training data.  

I tried various tactics to optmimize the model, including adding more neurons, more hidden layers, different activations functions and changing the bins of the two variables we used earlier.  Ultimately, I was not able to increase the accuracy by a substantial amount.  I ended up using 2 hidden layers with 20 and 10 neurons, each.  I used a tanh activation function for the hidden layers and a sigmoid function for the output layer.  I also changed the bins on the Classification and Application type variables in order to include more rare instances.  <br><br>
    ![alt text](images/model_build.png)
    
## Results

After numerous tries at different configurations, I was able to only slightly optimize the model and get an accuracy score around 73.6% for the training data.  Ultimately, there is still a lot of room for improvement in this model and I would not recommend the model for assessing whether or not a new venture will be successful.  

It is possible that a supervised learning model such as a logistic regression, decision tree, or random forest could do a better job at predicting venture success.  With more time, I would try some of these different models and also keep trying to drop various columns to see if the model is overfitting on too much data.  

  



