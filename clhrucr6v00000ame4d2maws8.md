---
title: "Neural Network"
datePublished: Wed May 17 2023 15:11:56 GMT+0000 (Coordinated Universal Time)
cuid: clhrucr6v00000ame4d2maws8
slug: neural-network
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1684336217946/e1e9a20b-a9e5-420a-8e24-f83b858ed038.png
tags: machine-learning, neural-networks

---

## Linearity vs non-Linearity

### Linearity

In machine learning, linearity refers to a relationship between two variables where a change in one variable is proportional to the change in the other variable. For example, the relationship between height and weight is linear. As people get taller, they typically weigh more.

In neural networks, a linear relationship is one where the output of a neuron is a linear combination of its inputs. This means that the output of a linear neuron is simply the sum of its inputs, multiplied by their weights.

### Non-Linearity

Non-linearity refers to a relationship between two variables where a change in one variable is not proportional to the change in the other variable. For example, the relationship between the price of a product and the number of units sold is non-linear. As the price of a product increases, the number of units sold typically decreases. However, the decrease is not proportional to the increase in price.

In neural networks, a non-linear relationship is one where the output of a neuron is not a linear combination of its inputs. This means that the output of a non-linear neuron is a more complex function of its inputs.

## Activation Functions

In artificial neural networks, activation functions are used to introduce non-linearity into the model. This allows the network to learn more complex relationships between the input and output data.

Many different activation functions can be used in neural networks. Some of the most common activation functions include:

* Sigmoid function
    
* Tanh function
    
* ReLU function
    
* Leaky ReLU function
    
* Exponential linear unit (ELU) function
    

The choice of activation function depends on the specific problem that the neural network is being trained to solve. For example, sigmoid and tanh functions are often used in classification problems, while ReLU functions are often used in regression problems.

### Sigmoid Function

![](https://media.geeksforgeeks.org/wp-content/uploads/20221013120722/1.png align="center")

The sigmoid function is a non-linear function that has a sigmoid shape. It is often used in classification problems, where the output of the neuron is a probability.

The sigmoid function is defined as:

`σ(x) = 1 / (1 + exp(-x))`

The sigmoid function has a range of \[0, 1\]. This means that the output of the sigmoid function can be interpreted as a probability. For example, if the output of the sigmoid function is 0.7, then the neuron is predicting that the input data belongs to the positive class with a probability of 70%.

### Tanh Function

![](https://media.geeksforgeeks.org/wp-content/uploads/20190408115639/tanh3.png align="center")

The tanh function is like the sigmoid function, but it has a range of \[-1, 1\]. This makes it more suitable for regression problems, where the output of the neuron is a continuous value.

The tanh function is defined as:

`tanh(x) = (exp(x) - exp(-x)) / (exp(x) + exp(-x))`

### ReLU Function

![](https://cdncontribute.geeksforgeeks.org/wp-content/uploads/Screenshot-from-2018-01-04-22-45-49-e1515086199933.png align="center")

The ReLU function is a non-linear function that is becoming increasingly popular in neural networks. It is very efficient to compute, and it can learn complex relationships between variables.

The ReLU function is defined as:

`ReLU(x) = max(0, x)`

The ReLU function has a few advantages over other activation functions. First, it is very efficient to compute. Second, it can learn complex relationships between variables. Third, it is less prone to overfitting than other activation functions.

**In simple words, RELU learns *much faster* than the sigmoid and Tanh functions.**

### Other Activation Functions

There are many other activation functions that can be used in neural networks. Some of the other popular activation functions include:

* Leaky ReLU function
    
* Exponential linear unit (ELU) function
    

The Leaky ReLU function is a variation of the ReLU function that allows for a small positive gradient for negative inputs. This helps to prevent the ReLU function from becoming "dead" when the inputs are negative.

The ELU function is a non-linear function that has a similar shape to the sigmoid function, but it has a wider range. This makes it more suitable for regression problems where the output data can be negative.

## Weights and Bias

Weights and bias are the learnable parameters of a neural network. They are used to transform the input data into a representation that can be used to make predictions.

![Weights and Bias in a Neural Network | Towards Data Science](https://miro.medium.com/v2/resize:fit:1400/1*upfpVueoUuKPkyX3PR3KBg.png align="center")

### Weights

Weights are the real numbers that are associated with each input feature. They control how much influence each feature has on the output of the neuron.

The weights of a neural network are initialized randomly. They are then adjusted during the training process using backpropagation. The goal of backpropagation is to find a set of weights that minimize the error between the network's predictions and the desired output.

The weights of a neural network can have a significant impact on the performance of the network. If the weights are not chosen carefully, the network may not be able to learn to make accurate predictions.

### Bias

Bias is a real number that is added to the weighted sum of the inputs. It controls the overall output of the neuron.

The bias of a neural network is initialized randomly. It is then adjusted during the training process using backpropagation. The goal of backpropagation is to find a set of weights and bias that minimize the error between the network's predictions and the desired output.

The bias of a neural network can have a significant impact on the performance of the network. If the bias is not chosen carefully, the network may not be able to learn to make accurate predictions.

## Loss Function

A loss function is a function that measures the error between the predicted output of a model and the actual output. The loss function is used to train the model to minimize the error.

### Mean Squared Error

Mean squared error (MSE) is a loss function that is commonly used for regression problems. MSE measures the average squared difference between the predicted output and the actual output.

The formula for MSE is:

`MSE = (1/n) * Σ(yᵢ - ŷᵢ)^2`

where:

* n is the number of samples
    
* yᵢ is the actual output for the i-th sample
    
* ŷᵢ is the predicted output for the i-th sample
    

MSE is a simple and intuitive loss function that is easy to understand and interpret. It is also a relatively efficient loss function to compute. However, MSE can be sensitive to outliers, and it may not be the best choice for all regression problems.

### Mean Absolute Error (MAE)

Mean absolute error (MAE) is a loss function that is commonly used for regression problems. MAE measures the average absolute difference between the predicted output and the actual output.

The formula for MAE is:

`MAE = (1/n) * Σ|yᵢ - ŷᵢ|`

where:

* n is the number of samples
    
* yᵢ is the actual output for the i-th sample
    
* ŷᵢ is the predicted output for the i-th sample
    

MAE is less sensitive to outliers than MSE, but it is also less powerful. MAE is also a relatively efficient loss function to compute.

## Gradient Descent

Gradient descent is an iterative optimization algorithm used in machine learning to find the minimum of a function. The function to be minimized is typically the loss function of a machine learning model.

![Gradient Descent in Machine Learning](https://static.javatpoint.com/tutorial/machine-learning/images/gradient-descent-in-machine-learning1.png align="center")

Gradient descent works by taking repeated steps in the direction of the negative gradient of the function. The gradient of a function is a vector that points in the direction of the steepest ascent of the function. By taking steps in the direction of the negative gradient, gradient descent can find the minimum of the function.

### Gradient Descent Algorithm

The gradient descent algorithm is as follows:

1. Start with an initial guess for the parameters of the model.
    
2. Calculate the gradient of the loss function with respect to the parameters.
    
3. Update the parameters by moving in the direction of the negative gradient.
    
4. Repeat steps 2 and 3 until the loss function converges to a minimum.
    

### Stochastic Gradient Descent

Stochastic gradient descent is a variant of gradient descent that uses a single data point at a time to calculate the gradient. This can be useful for large datasets, as it can reduce the computational cost of gradient descent.

The stochastic gradient descent algorithm is as follows:

1. Start with an initial guess for the parameters of the model.
    
2. Select a single data point from the dataset.
    
3. Calculate the gradient of the loss function with respect to the parameters using the selected data point.
    
4. Update the parameters by moving in the direction of the negative gradient.
    
5. Repeat steps 2 to 4 until the loss function converges to a minimum.
    

### Mini-Batch Gradient Descent

Mini-batch gradient descent is a variant of gradient descent that uses a small batch of data points to calculate the gradient. This can be useful for large datasets, as it can reduce the variance of the gradient estimate.

The mini-batch gradient descent algorithm is as follows:

1. Start with an initial guess for the parameters of the model.
    
2. Select a mini-batch of data points from the dataset.
    
3. Calculate the gradient of the loss function with respect to the parameters using the mini-batch.
    
4. Update the parameters by moving in the direction of the negative gradient.
    
5. Repeat steps 2 to 4 until the loss function converges to a minimum.
    

## Backpropagation Algorithm

Backpropagation is an algorithm for training artificial neural networks. It is a gradient-based optimization algorithm that uses the chain rule to calculate the derivative of the error function with respect to the weights of the network. This derivative is then used to update the weights of the network in the direction of the negative gradient, which minimizes the error function.

The backpropagation algorithm works as follows:

1. The network is presented with an input.
    
2. The network outputs a prediction.
    
3. The error between the prediction and the desired output is calculated.
    
4. The derivative of the error function with respect to the weights of the network is calculated using the chain rule.
    
5. The weights of the network are updated in the direction of the negative gradient.
    
6. Steps 1-5 are repeated until the error function converges to a minimum.
    

The backpropagation algorithm is a powerful tool for training artificial neural networks. It is relatively simple to implement and can be used to train networks with a wide variety of architectures. However, the backpropagation algorithm can be computationally expensive, especially for large networks.

![exploding and vanishing gradients back propagation](https://editor.analyticsvidhya.com/uploads/12203Schematic-diagram-of-backpropagation-training-algorithm-and-typical-neuron-model_W640.jpg align="center")

## Weight Initialization

Weight initialization is the process of assigning initial values to the weights of a neural network. The weights of a neural network are the parameters that the network learns during training. The initial values of the weights can have a significant impact on the speed and accuracy of training.

## Training

Training is the process of teaching a machine learning model to perform a task. The model is given a set of training data, which includes examples of the input and output for the task. The model then uses the training data to learn the relationship between the input and output.

### Training Process

The training process for a machine learning model typically involves the following steps:

1. **Data preparation:** The training data is prepared by cleaning it, removing any errors or outliers, and splitting it into a training set and a test set.
    
2. **Model selection:** A machine learning model is chosen for the task. The model is typically chosen based on the type of data and the complexity of the task.
    
3. **Model training:** The model is trained on the training set. The model learns the relationship between the input and output by adjusting its parameters.
    
4. **Model evaluation:** The model is evaluated on the test set. The model's performance is measured by its accuracy, precision, and recall.
    
5. **Model tuning:** The model may be tuned to improve its performance. This may involve adjusting the model's parameters or choosing a different model.
    

### Overfitting

Overfitting is a problem that can occur when a machine-learning model is trained on too much data. The model learns the training data too well and becomes too sensitive to minor changes in the data. This can lead to the model performing poorly on new data that it has not seen before.

### Underfitting

Underfitting is a problem that can occur when a machine-learning model is not trained on enough data. The model does not learn the relationship between the input and output well enough and is unable to perform the task.

To avoid overfitting and underfitting:

* **Use a validation set:** The validation set is a set of data that is held out from the training set. The model is not trained on the validation set. The model is evaluated on the validation set to see how well it performs on new data.
    
* **Use regularization:** Regularization is a technique that can help to prevent overfitting. Regularization adds a penalty to the model's loss function that discourages the model from learning the training data too well.
    
* **Use a smaller model:** A smaller model has fewer parameters and is less likely to overfit the training data.
    
* **Collect more data:** Collecting more data can help to prevent underfitting. The model will have more data to learn from and will be able to perform the task better.
    

## Testing

Testing is the process of evaluating a machine learning model's performance on new data that it has not seen before. The goal of testing is to ensure that the model can generalize to new data and perform the task as expected.

### Testing Process

The testing process typically involves the following steps:

1. **Split the data:** The data is split into a training set and a test set. The training set is used to train the model, and the test set is used to evaluate the model's performance.
    
2. **Train the model:** The model is trained on the training set.
    
3. **Evaluate the model:** The model is evaluated on the test set. The model's performance is measured by its accuracy, precision, and recall.
    
4. **Interpret the results:** The results of the testing process are interpreted to determine how well the model performs. The results may be used to improve the model or to make decisions about how to use the model.
    

![Train and Test datasets in Machine Learning](https://static.javatpoint.com/tutorial/machine-learning/images/train-and-test-datasets-in-machine-learning.png align="center")

## Unstable Gradient Problem

The unstable gradient problem is a problem that can occur when the gradient of a loss function is very large or very small. This can make it difficult for the neural network to learn, as the updates to the weights can be too large or too small.

### Vanishing Gradient Problem

The vanishing gradient problem is a problem that can occur when the weights of a neural network are initialized to very small values. This can make it difficult for the neural network to learn long-range dependencies, as the gradients of the loss function with respect to the weights can become very small.

### Exploding Gradient Problem

The exploding gradient problem is a problem that can occur when the weights of a neural network are initialized to very large values. This can make it difficult for the neural network to learn, as the gradients of the loss function with respect to the weights can become very large.

## Autoencoders

Autoencoders are a type of neural network that is used to learn efficient representations of data.

Autoencoders are composed of two parts:

* Encoder
    
* Decoder
    

The encoder takes the input data and compresses it into a latent representation.

The decoder then takes the latent representation and reconstructs the original input data.

### Autoencoder Architecture

The architecture of an autoencoder is typically composed of three layers:

* Input layer
    
* Hidden layer
    
* Output layer
    

The input layer takes the input data and passes it to the hidden layer.

The hidden layer compresses the input data into a latent representation.

The latent representation is then passed to the output layer, which reconstructs the original input data.

![](https://media.geeksforgeeks.org/wp-content/uploads/20190619140203/450.png align="center")

### Applications of Autoencoders

Autoencoders can be used for a variety of tasks, including:

* **Dimensionality reduction:** Autoencoders can be used to reduce the dimensionality of data while preserving the most important information. This can be useful for tasks such as image compression and feature extraction.
    
* **Denoising:** Autoencoders can be used to remove noise from data. This can be useful for tasks such as image denoising and speech denoising.
    
* **Feature learning:** Autoencoders can be used to learn features from data. This can be useful for tasks such as classification and clustering.
    
* **Generative modelling:** Autoencoders can be used to generate new data that is similar to the training data. This can be useful for tasks such as image generation and text generation.
    

## Batch Normalization

Batch normalization is a technique that is used to improve the training of neural networks. Batch normalization normalizes the activations of a neural network layer before they are passed to the next layer. This helps to stabilize the training process and can improve the accuracy of the model.

### Batch Normalization Algorithm

The batch normalization algorithm works as follows:

1. The activations of a neural network layer are normalized. This is done by subtracting the mean of the activations and dividing them by the standard deviation of the activations.
    
2. The normalized activations are then passed to the next layer.
    

Batch normalization can be used with any type of neural network layer. However, it is most used with layers that have nonlinear activation functions, such as ReLU and sigmoid.

Batch normalization has been shown to improve the training of neural networks on a variety of tasks. It can help to stabilize the training process, improve the accuracy of the model, and reduce the time it takes to train the model.

## Dropout

Dropout is a regularization technique that is used to prevent neural networks from overfitting. Dropout works by randomly dropping out (i.e., setting to zero) a certain percentage of neurons during training. This forces the neural network to learn to rely on other neurons to make predictions, which can help to prevent the network from becoming too reliant on any one set of neurons.

The dropout algorithm works as follows:

1. A random percentage of neurons are dropped out.
    
2. The neural network is then trained on the remaining neurons.
    
3. Steps 1 and 2 are repeated for a number of epochs.
    

The dropout rate is a hyperparameter that can be tuned to improve the performance of the neural network. A higher dropout rate will force the neural network to rely on more neurons, which can help to prevent overfitting. However, a higher dropout rate can also reduce the accuracy of the neural network.

Dropout has been shown to be an effective regularization technique for neural networks. It can help to prevent overfitting and improve the accuracy of the neural network on a variety of tasks.

## L1 and L2 Regularization

L1 and L2 regularization are two types of regularization techniques that are used to prevent neural networks from overfitting. Regularization works by adding a penalty to the loss function that is proportional to the size of the weights. This forces the neural network to learn weights that are smaller, which can help to prevent the network from becoming too reliant on any one set of weights.

### L1 Regularization

L1 regularization is also known as lasso regularization. It adds a penalty to the loss function that is proportional to the absolute value of the weights. This can help to reduce the number of weights in the neural network, as some weights may become zero during training. This can make the model easier to interpret and can also improve the accuracy of the model on sparse data sets.

### L2 Regularization

L2 regularization is also known as ridge regularization. It adds a penalty to the loss function that is proportional to the square of the weights. This can help to improve the stability of the neural network and can also improve the accuracy of the model on noisy data sets.

## Momentum

Momentum is a technique that is used to improve the training of neural networks. Momentum works by adding a term to the weight update that is proportional to the previous weight update. This helps to accelerate the training process and can help to prevent the neural network from getting stuck in local minima.

**How Momentum Works**

Momentum works by maintaining a running average of the weight updates. This running average is called the momentum term. The momentum term is then added to the weight update. The momentum term helps to accelerate the training process by giving the weight update a "kick" in the direction that the neural network is already moving.

![machine learning - What is momentum in neural network? - Data Science Stack  Exchange](https://i.stack.imgur.com/epW89.jpg align="center")

**Momentum Algorithm**

The momentum algorithm works as follows:

1. Initialize the momentum term to 0.
    
2. Calculate the gradient of the loss function with respect to the weights.
    
3. Update the momentum term using the following equation:
    
    `v = βv + ηg`
    
    where:
    
    * β is the momentum hyperparameter
        
    * η is the learning rate
        
    * g is the gradient of the loss function with respect to the weights
        
4. Update the weights using the following equation:
    
    `w = w − v`
    
    where:
    
    * w is the weights
        
    * v is the momentum term
        

## Tuning Hyperparameters

Hyperparameters are parameters that control the learning process of a machine learning model. They are typically not learned from the data, but instead set by the user. The best hyperparameters for a given model and data set will vary, and so it is important to tune them to get the best results.

There are several ways to tune hyperparameters. One common approach is to use a grid search, where a range of values for each hyperparameter is explored and the best combination is found. Another approach is to use a Bayesian optimization algorithm, which can automatically search for the best hyperparameters.

The hyperparameter tuning process can be broken down into the following steps:

1. **Define the hyperparameters to tune.** The first step is to identify the hyperparameters that can be tuned. These will vary depending on the machine learning model being used.
    
2. **Choose a hyperparameter tuning method.** There are several hyperparameter tuning methods available. The best method to use will depend on the specific problem being solved.
    
3. **Set the hyperparameter search space.** The hyperparameter search space is the range of values that will be explored for each hyperparameter. It is important to set the search space to a wide enough range to find the best hyperparameters, but not so wide that the search becomes too computationally expensive.
    
4. **Run the hyperparameter tuning experiment.** The next step is to run the hyperparameter tuning experiment. This involves training the machine learning model with different combinations of hyperparameters and evaluating the results.
    
5. **Evaluate the results.** The final step is to evaluate the results of the hyperparameter tuning experiment. This involves selecting the combination of hyperparameters that produces the best results.
    

There are a number of different hyperparameter tuning methods available. The best method to use will depend on the specific problem being solved. Some common hyperparameter tuning methods include:

* **Grid search:** Grid search is a brute-force method that tries all possible combinations of hyperparameter values. This can be computationally expensive, but it is guaranteed to find the best combination of hyperparameters.
    
* **Random Search:** Random search is a more efficient method than grid search. It randomly samples hyperparameter values from a pre-defined distribution. This can be less accurate than grid search, but it is much faster.
    
* **Bayesian optimization:** Bayesian optimization is a more sophisticated method than grid search or random search. It uses Bayesian statistics to estimate the best combination of hyperparameters. This can be more accurate than grid search or random search, but it is also more computationally expensive.