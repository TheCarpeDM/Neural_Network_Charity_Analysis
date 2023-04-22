# Neural_Network_Charity_Analysis
 
## Overview

Our goal was to help Beks create a neural network machine learning model that would help Alphabet Soup easily determine which applications they should approve for funding and which applications they should reject based on previous successes (and failures).

## Results
Using bulleted lists and images to support your answers, address the following questions.

### Data Preprocessing
Our target was to determine whether the features indicate that a project is likely to succeed.

The features were:
- Application Type: what kind of application it was
- Affiliation: Affiliated sector of industry
- Classification: Government organization classification
- Use-case: How the funding would be used
- Organization type: what kind of organization it was
- Income amount: Income classification
- Special Considerations: Special consideration for application
- Ask Amount: Funding amount requested

Variables which were ultimately removed from the data were:
- EIN: Identification number
- Name: organization name
- Status: Active status

### Compiling, Training, and Evaluating the Model

Ultimately, we used 3 hidden layers and an output layer. There were 42 input dimensions, but since so many were binary, we started with a layer of 5 neurons and a layer of 3 neurons, both using relu activations, and then had a sigmoid output layer with 1 neuron. 
We were not able to achieve 75% accuracy with our initial model, so we made some changes.
+ For our first optimization, we removed "Status" from the variables, since active or inactive status should not affect success of the funding. 
+ For our second optimization, we changed the second hidden layer to tanh activation, and increased the neurons in each hidden layer by 10. 
+ For the third optimization, we added an additional hidden layer with 7 neurons using relu activation.

Unfortunately, we were still unable to get much higher than 73% accuracy. 

## Summary

If I had understood more clearly what each column meant, I would probably have been able to better decide which features were unnecessary or unhelpful to the machine learning process, and less features would probably have made a big difference in the accuracy of the model.
