# MNIST Digit Classification

A handwritten digit classification project using the MNIST dataset and
comparing a simple Perceptron-style model, an Artificial Neural Network
(ANN), and a Convolutional Neural Network (CNN).

## Project Overview

This project loads the MNIST training and test datasets from CSV files,
preprocesses the image data, trains three models using TensorFlow/Keras,
evaluates them on the test dataset, and visualizes training and
validation performance.

## Dataset

-   `mnist_train.csv` --- training dataset
-   `mnist_test.csv` --- test dataset
-   Each image contains 28 × 28 = 784 pixel values.
-   The `label` column contains the digit class from 0 to 9.
-   The training dataset contains 60,000 samples and 785 columns.

> `mnist_train.csv` is stored using Git LFS because it is larger than
> GitHub's regular file-size limit.

## Workflow

1.  Load the training and test CSV files.
2.  Inspect the dataset and missing values.
3.  Separate labels from pixel values.
4.  Normalize pixel values from 0--255 to 0--1.
5.  Reshape the image data.
6.  Convert labels to one-hot encoded vectors.
7.  Train and evaluate a Perceptron-style model.
8.  Train and evaluate an ANN.
9.  Train and evaluate a CNN.
10. Compare model performance.
11. Plot training and validation accuracy and loss.

## Models and Results

  Model                      Test Accuracy
  ------------------------ ---------------
  Perceptron-style Model            90.84%
  ANN                               97.69%
  CNN                               98.99%

### Perceptron-style Model

-   Flatten
-   Dense output layer with 10 neurons
-   Softmax activation
-   SGD optimizer
-   Categorical cross-entropy loss
-   5 epochs

### ANN

-   Flatten
-   Dense: 128 neurons, ReLU
-   Dense: 64 neurons, ReLU
-   Dense output: 10 neurons, Softmax
-   Adam optimizer
-   Categorical cross-entropy loss
-   5 epochs

### CNN

-   Conv2D: 32 filters, 3×3 kernel, ReLU
-   MaxPooling2D: 2×2
-   Conv2D: 64 filters, 3×3 kernel, ReLU
-   MaxPooling2D: 2×2
-   Flatten
-   Dense: 128 neurons, ReLU
-   Dropout: 0.5
-   Dense output: 10 neurons, Softmax
-   Adam optimizer
-   Categorical cross-entropy loss
-   5 epochs

## Technologies Used

-   Python
-   NumPy
-   Pandas
-   Matplotlib
-   Seaborn
-   Scikit-learn
-   TensorFlow / Keras
-   Google Colab / Jupyter Notebook

## Project Structure

``` text
mnist-digit-classification/
├── CNN.ipynb
├── mnist_train.csv
├── mnist_test.csv
├── .gitattributes
└── README.md
```

## How to Run

1.  Clone the repository.
2.  Make sure Git LFS is installed.
3.  Pull the LFS dataset:

``` bash
git lfs pull
```

4.  Open `CNN.ipynb` in Jupyter Notebook, JupyterLab, or Google Colab.
5.  Run the notebook cells in order.

### Install Dependencies

``` bash
pip install numpy pandas matplotlib seaborn scikit-learn tensorflow
```

## Notes

-   The notebook uses CSV versions of the MNIST datasets.
-   Pixel values are normalized by dividing by `255.0`.
-   CNN input images are reshaped to `(28, 28, 1)` for grayscale image
    processing.
-   The current notebook trains each model for 5 epochs.

## Author

**Madhav Kr. Yadav**

GitHub: [@madhav28](https://github.com/madhav28)
