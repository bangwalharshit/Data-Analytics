# Data-Analytics
Lead Score Model
Importing Libraries
This code is importing several Python modules from the scikit-learn and pandas libraries.
import pandas as pd imports the pandas library and assigns it the alias pd, which is a convention in Python.
import numpy as np imports the numpy library and assigns it the alias np.
from sklearn.model_selection import train_test_split imports the train_test_split function from the model_selection module of the scikit-learn library. This function is used to split data into training and testing sets.
from sklearn.preprocessing import LabelEncoder imports the LabelEncoder class from the preprocessing module of the scikit-learn library. This class is used to convert categorical data into numerical data.
from sklearn.metrics import accuracy_score, precision_score, recall_score, f1_score imports several evaluation metrics from the metrics module of the scikit-learn library. These metrics are used to evaluate the performance of machine learning models.
from sklearn.ensemble import RandomForestRegressor imports the RandomForestRegressor class from the ensemble module of the scikit-learn library. This class is used to create a machine learning model that can predict continuous values.
Overall, this code imports necessary libraries and modules to train and evaluate a regression model using a Random Forest algorithm on the given dataset.
Pandas: Pandas is a popular open-source data analysis and manipulation library. It provides data structures for efficiently storing and manipulating large datasets, and has built-in functions for data cleaning, merging, reshaping, slicing and indexing data. It is widely used in data science and machine learning for data preprocessing, data wrangling and data visualization tasks.
NumPy: NumPy is a fundamental package for scientific computing in Python. It provides a powerful N-dimensional array object, sophisticated functions for manipulating these arrays, and tools for integrating C/C++ and Fortran code. NumPy is used for scientific computing, numerical analysis, and data science tasks like linear algebra, Fourier transform, random number generation, and numerical optimization.
Scikit-Learn: Scikit-Learn is a Python library for machine learning built on top of NumPy and SciPy. It provides efficient tools for data analysis, data preprocessing, feature selection, and model selection. It also includes a wide range of machine learning algorithms such as regression, classification, clustering, and dimensionality reduction. Scikit-Learn is widely used in industry and academia for building machine learning models and pipelines.
Matplotlib: Matplotlib is a plotting library for Python. It provides a wide variety of 2D and 3D plots, including line plots, scatter plots, bar plots, histograms, and heatmaps. Matplotlib is a popular tool for visualizing data and presenting results in research and data analysis.
Seaborn: Seaborn is a Python data visualization library based on Matplotlib. It provides a high-level interface for creating informative and attractive statistical graphics, such as heatmaps, time series plots, and categorical plots. Seaborn is commonly used for exploratory data analysis and data visualization in data science.
TensorFlow: TensorFlow is an open-source software library for dataflow and differentiable programming across a range of tasks. It is used for building and training deep learning models, including neural networks, convolutional neural networks (CNNs), and recurrent neural networks (RNNs). TensorFlow is widely used in industry and academia for developing machine learning models in various fields, such as image recognition, natural language processing, and speech recognition.

This code loads a dataset, drops some unnecessary columns and filters the data by keeping only those rows where the status column has a value of either 'WON' or 'LOST'.
data = pd.read_csv("Data_Science_Internship - Dump.csv") loads the dataset from a CSV file named "Data_Science_Internship - Dump.csv" into a pandas dataframe named data.
data.describe() provides a summary of statistical information of the dataset, such as the mean, standard deviation, minimum, maximum, and quartiles for each numeric column.
data.info() provides information about the dataset, such as the number of rows, the number of columns, the data type of each column, and the amount of memory used by the dataset.
data = data[(data['status'] == 'WON') | (data['status'] == 'LOST')] filters the dataset by keeping only those rows where the value in the status column is either 'WON' or 'LOST'. Rows where status has any other value will be dropped.
data = data.drop(['lead_id', 'status', 'lost_reason'], axis=1) drops the unnecessary columns lead_id, status, and lost_reason from the dataset using the drop() function with axis=1 parameter. This will remove those columns from the dataset and return the updated dataframe.
Overall, this code is performing some initial data preprocessing steps to clean and filter the dataset to make it ready for further analysis and modeling.
