# 4p

# Business Problem

The business problem is a radiologist who wants to double-check their work with a model that classifies x-rays as Pneumonia or normal.

# Data Understanding

The data consists of 5,856 chest x-ray images. Each image is labelled as either normal or pneumonia.  27% of the images are labelled normal and 73% pneumonia.  

# Modeling

- Building initial model, a neural network with 1 hidden layer, with 64 neurons.


- Builing second model by adding an additional layer with 32 neurons and same tanh activation function.  

- Building third model by increasing the learning rate of the optimizer from default .001 to .05 in order to try to reduce overfitting.  

- Appears to be over-learning, minimum loss is overshot.  Model2 has best performance.



Accuracy on test set is 88%.

105 false negatives 70 false positives out of 1464 predictions.

![corrmatrx](./Images/cnfm.png)

# Results/Conclusions

The 2nd model performed best based on the validation sets, higher accuracy than the baseline model and the faster learning model.  The chosen model's accuracy on the holdout test set was 88%.  This can be compared to guessing based on the sample balance, which would yield 73% accuracy.  Thus this model can be used as a check by the radiologist, for instance on x-rays that they are less certain about.  