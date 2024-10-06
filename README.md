This code builds and trains an Artificial Neural Network (ANN) for customer churn prediction using the Churn Modelling dataset. Here's a breakdown:

Data Preprocessing:

The dataset is loaded using Pandas (data = pd.read_csv()), and the features (X) and target variable (Y) are extracted.
Categorical variables like gender and country are transformed. Label Encoding is used for gender, and OneHotEncoding for the geography column to convert categorical values into numerical.
The data is split into training and test sets using train_test_split.
Feature scaling is applied using StandardScaler to normalize the data before feeding it to the ANN.
Building the ANN:

A Sequential model is defined using TensorFlow’s Keras API.
The first Dense layer has 6 units with ReLU activation, followed by an output layer with 1 unit and a Sigmoid activation function (since it's a binary classification problem).
The model is compiled using the Adam optimizer, binary cross-entropy loss function, and accuracy as the performance metric.
Training the Model:

The model is trained using ann.fit() for 100 epochs with a batch size of 32, where the accuracy progressively improves with each epoch.
Making Predictions:

A test prediction is made using ann.predict(), and the result is compared to 0.5 to decide if a customer will churn or not.
Activation Functions:

Three activation functions (Sigmoid, Tanh, and ReLU) are implemented separately and plotted:
Sigmoid: Compresses values between 0 and 1.
Tanh: Outputs values between -1 and 1.
ReLU: Outputs 0 for negative inputs and the input itself for positive values.
This code demonstrates both the ANN model-building process and the role of activation functions in transforming neural network outputs.
