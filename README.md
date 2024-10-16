# deep-learning-challenge-


Results

1. Data Preprocessing

Target Variable:
  -IS_SUCCESSFUL column

- Feature Variable(s):
  - Key features used to predict the target include:
    - Application Type
    - Classification
    - Other numerical and categorical features from the dataset.

- Variables Removed:
  - We initially removed the EIN and Name columns as they do not contribute to the prediction process and serve as unique identifiers.

- Binning and Filtering:
  - To ensure the data was manageable and focused, we filtered:
    - Rows in the `Application Type` column that had fewer than 500 occurrences.
    - Rows in the `Classification` column that had fewer than 1,500 occurrences.



2. Compiling, Training, and Evaluating the Model

Initial Model

- Neurons, Layers, and Activation Functions:
  - We designed a neural network with two hidden layers:
    - Hidden Layer 1: 80 neurons, with 3,520 parameters.
    - Hidden Layer 2: 30 neurons, with 2,430 parameters.
  - Output Layer: The output layer was shaped with 1 neuron and 31 parameters, using a sigmoid activation function for binary classification.
  - The activation function for the hidden layers was ReLU, which is common in deep learning models for classification tasks.

- Model Performance:
  - After training the model, the performance metrics were as follows:
    - Accuracy: 72.98%
    - Loss: 0.5653




Optimized Model

- Changes Made:
  - For the optimized model, we reintroduced the Name column, which was initially dropped.
  - We also increased the data thresholds for the Application Type and Classification columns, including only rows where:
    - Application Type had more than 1,500 occurrences.
    - Classification had more than 1,500 occurrences.

- Neurons, Layers, and Activation Functions:
  - We used the same basic structure for the neural network but observed differences in the model parameters:
    - Hidden Layer 1: 80 neurons, with 1,568,480 parameters (an increase from the initial model).
    - Hidden Layer 2: 30 neurons, with 2,430 parameters (same as before).
  - Output Layer: Shaped with 1 neuron and 31 parameters, as in the initial model.

- Model Performance:
  - After training the optimized model, the performance improved:
    - Accuracy: 74.43%
    - Loss: 0.7935


Summary

In this analysis, we compared two different versions of the neural network model to solve a classification problem. The initial model performed with an accuracy of 72.98% and a loss of 0.5653. After optimizing the model by reintroducing the Name column and increasing the threshold for both Application Type and Classification, the model performance improved to an accuracy of 74.43%. However, the loss increased to 0.7935, suggesting that while the accuracy improved, the model may still have room for refinement.


Recommendation:

A potential next step to further improve performance could be to fine-tune the model through hyper-parameter tuning or using regularization techniques such as dropout to prevent overfitting.

Additionally, trying different models like Random Forest or Gradient Boosting Machine could provide better results. These models are robust to feature scaling and often perform well in classification tasks involving mixed data types.


This format should be easy to copy into a text file or document. Let me know if you need further adjustments!