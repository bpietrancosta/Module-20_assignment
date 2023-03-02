# Module-20_assignment
## The purpose of this assignment is to define a Machine Learning module which will predict whether an application is successful based on a set of variables.
### Data pre-processing: The first part of the analysis is defining which variables we will concern ourselves with
 - Our target for this model is whether the application was successful. We've defined this variable as a column in our dataframe called "IS_SUCCESSFUL" see ![image](https://user-images.githubusercontent.com/114181709/222299070-ebcfcf10-910d-4a64-8e7a-60a0159f65be.png)
 
 - The key features of our model are the application: type, classification, income, ask amount, special considerations... 

 - We are only looking for applications with a defined classification and type. We've filtered those categorizations by the volume of applications that fall in each. When the volume was below a certain threshold they were binned into an "Other" category. For our purposes these could've been removed, however we had some admin difficulties which prevented us from doing so. Nonetheless, see the binning: ![image](https://user-images.githubusercontent.com/114181709/222299006-c476fc08-da9e-4239-beed-15416f30ac3e.png)

 
 ### Compiling, training and executing the model:
After some trial and error we found that we could only run the model with a single neuron - that remained constant. However, we played with the number of epochs, activation functions and hidden layers. 
Our optimal model performance reached 73% accuracy by adding 1 layer to the model and reducing the number of epochs to 3. We tried to change all the activation functions to "relu" but that decreased our model accuracy by 10 points. Therefore, we kept our input layer activation function as "relu" and kept the other 3 as sigmoid. This allowed us to reach our maximum accuracy for the model given the technical constraints. See our model code:![image](https://user-images.githubusercontent.com/114181709/222300466-f826fd67-eae9-42a1-91d7-935d51d96a04.png)


## Conclusion: 
More layers led to greater accuracy and having a large number of epochs can be wasteful when the mathematical limit of the model is reached after a relatively small number of epochs.
