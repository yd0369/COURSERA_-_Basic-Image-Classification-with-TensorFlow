COURSERA_-_Basic-Image-Classification-with-TensorFlow
# COURSERA - Basic Image Classification with TensorFlow

---

## Project-Based Course Overview
- Welcome to TensorFlow Beginner: Basic Image Classification. This is a project-based course which should take approximately 2 hours to finish. Before diving into the project, please take a look at the course objectives and structure:

### Course Objectives
- In this course, we are going to focus on three learning objectives:

  1. Learn to create, train and evaluate neural network models with TensorFlow and Keras.
  2. Understand the basics of neural networks.
  3. Learn to solve classification problems with the help of neural networks.

- By the end of this course, you will be able to create a neural network model which will be able to classify images of hand written digits with a high degree of accuracy.

### Course Structure
- This course is divided into 4 parts:

  1. Course Overview: This introductory reading material.

  2. Basic Image Classification Project: This is the hands on project that we will work on in Rhyme.

  3. Ungraded Quiz: Check your understanding of the concepts learned in the hands on project with this ungraded quiz.

  4. Graded Quiz: This is the final assignment that you need to pass in order to finish the course successfully.

### Project Structure
- The hands on project on Basic Image Classification is divided into following tasks:

#### Task 1: Introduction
- Introduction to the basic image classification problem.
- What is TensorFlow?
- Introduction to the Rhyme interface.

#### Task 2: The Dataset
- Importing the MNIST dataset.
- A quick look at the structure of the dataset.
- A quick look at the MNIST image examples.

#### Task 3: One Hot Encoding
- What is one hot encoding?
- How to encode the labels from the dataset.

#### Task 4: Neural Networks
- Graphical representation of linear equations.
- What are neural networks?
- What are activation functions?

#### Task 5: Pre-processing the Examples
- Unrolling the input features.
- Data normalization with mean and standard deviation.

#### Task 6: Creating the Model
- Creating a sequential model with Keras.
- Model architecture - hidden layers and hidden units.
- Softmax and ReLU activation functions.
- Compiling the model by specifying an optimizer and a loss function.

#### Task 7: Training the Model
- Training the model to fit to training data.
- Evaluating the model on the test data.

#### Task 8: Predictions
- Predictions on the test set.
- Visualizing the predictions.

---
---


# My Steps :

### Session 1

- Copy all template given in the workspace.

- Create Python Virtual Environment
```bash
python3 -m venv COURSERA_PROJECT_VENV
```

- Activate Virtual Environment
```bash
source COURSERA_PROJECT_VENV/bin/activate
```

- Installing JupyterLab and Jupyter Notebook
```bash
pip3 install jupyter-lab notebook
```

- Installing Tensorflow
```bash
pip3 install tensorflow
```

- Commented Line as it was using deprecated function of logging
```python
# tf.compat.v1.logging.set_verbosity(tf.logging.ERROR)
```

---

### Session 2

#### 1. Import MNIST

- Added to shell to import the mnist dataset
```python
from tensorflow.keras.datasets import mnist
(x_train, y_train), (x_test, y_test) = mnist.load_data()
```
  Log : 
  ```text
  Downloading data from https://storage.googleapis.com/tensorflow/tf-keras-datasets/mnist.npz
  11490434/11490434 [==============================] - 2s 0us/step
  ```

- Will try to check the size of the train and test dataset.
```python
print("x_train size :", len(x_train))
print("y_train size :", len(y_train))
print("x_test  size :", len(x_test))
print("y_test  size :", len(y_test))
```
  Log : 
  ```text
  x_train size : 60000
  y_train size : 60000
  x_test  size : 10000
  y_test  size : 10000
  ```
  - Coming to conclusion there are 60000 Training Images and 10000 for Testing and Model Evaluation Purposes

