
#  Neural Network with TensorFlow

This project is part of the **Program Neural Networks with TensorFlow** pathway by Google for Developers.

The goal of this project is to create your first machine learning model that learns the mathematical relationship between two sets of numbers using TensorFlow.

---

#  Project Overview

The dataset used in this project follows the pattern:

* **X:** `-1, 0, 1, 2, 3, 4`
* **Y:** `-2, 1, 4, 7, 10, 13`

The relationship between the values is:

[
Y = 3X + 1
]

The neural network is trained to learn this pattern using TensorFlow.

---

#  Model Explanation

The model is a simple neural network built using:

* **1 Dense Layer**
* **1 Neuron**
* **Input Shape:** 1 value

```python
model = tf.keras.Sequential([
    keras.layers.Dense(units=1, input_shape=[1])
])
```

The model is compiled using:

* **Loss Function:** `mean_squared_error`
* **Optimizer:** `sgd` *(Stochastic Gradient Descent)*

```python
model.compile(
    optimizer='sgd',
    loss='mean_squared_error'
)
```

---

#  Training

The model is trained on 6 data points using:

```python
model.fit(xs, ys, epochs=500)
```

During training, the model:

* Guesses the relationship between X and Y
* Calculates the loss
* Improves predictions using gradient descent
* Eventually learns a function close to:

[
Y = 3X + 1
]

---

#  Prediction

Once trained, the model can predict the value of **Y** for any new value of **X**.

Example:

```python
input_data = np.array([[10.0]])
model.predict(input_data)
```

### Expected Value

```python
31
```

### Model Output

The prediction will be close to `31`, but may not be exact.

### Reason

Neural networks learn probabilistic approximations, especially when trained on very small datasets.

---

#  Key Concepts Learned

This project helps in understanding:

* Creating a Sequential model
* Using Dense layers
* Loss functions
* Optimizers *(SGD)*
* Training models using `.fit()`
* Making predictions using `.predict()`

---

#  Technologies Used

* Python
* TensorFlow
* NumPy
* Keras

---


#  Learning Outcome

By completing this project, you will understand:

* Basics of Neural Networks
* Linear relationships in Machine Learning
* TensorFlow model creation
* Model training process
* Prediction using trained models

---

#  Conclusion

This project is a beginner-friendly introduction to Machine Learning using TensorFlow.
It demonstrates how neural networks can learn mathematical patterns from data and make predictions on unseen values.


