# OverheadMNIST - A Semi-Supervised Learning Project

This repository contains the code for a semi-supervised learning project using the OverheadMNIST dataset. The dataset is obtained from Kaggle, and can be accessed [here](https://www.kaggle.com/datasets/datamunge/overheadmnist).

## Project Overview

1. Data Preprocessing: The images are read and converted into NumPy arrays. They are then normalized and augmented by rotating and reflecting to obtain more detailed information.
2. Exploratory Data Analysis (EDA) on the classes.
3. Semi-supervised learning: A combination of unsupervised and supervised learning techniques are used to train models and make predictions.

## Semi-Supervised Learning

The semi-supervised learning approach involves the following steps:

1. Dimensionality reduction using Principal Component Analysis (PCA) to obtain the most significant attributes.
2. Clustering using the K-means algorithm. The optimal number of clusters (k) is determined using the elbow method.
3. Manually labeling the clusters.
4. Training supervised models (Logistic Regression, MLP, and SVM) on the labeled data.
5. Using Grid Search Cross Validation to find the best hyperparameters for each model.
6. Selecting the best performing model (SVM in this case) for further improvement.
7. Propagating labels to a certain percentile of nearby datapoints.
8. Training the final SVM model with the propagated labels.

## Results

The final SVM model achieved an accuracy of *29%* and a precision of *42%* on this dataset.

## How to Use

1. Clone the repository.
2. Install the required packages listed in the `requirements.txt` file.
3. Download the dataset from [Kaggle](https://www.kaggle.com/datasets/datamunge/overheadmnist) and place it in the `data/` directory.
4. Run the Jupyter Notebook to preprocess the data, perform EDA, and train the semi-supervised models.

## Contributing

Feel free to contribute by submitting pull requests or raising issues for improvements, bug fixes, or new features.

## License

This project is licensed under the GPL v3.0 License.
