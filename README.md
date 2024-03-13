# Neural Network Predictions for Flow Cytometry

## Overview

This project aims to train a neural network using flow cytometry data to predict the composition of cocultures. By analyzing monoculture flow cytometry files, along with blanks, the model identifies the species present in coculture files. The model utilizes gating strategies to classify cells into categories such as live, dead, and debris.

## Prerequisites

- Python 3.7.0 or higher
- pandas
- numpy
- fcsparser
- scikit-learn
- tensorflow
- keras
- matplotlib
- seaborn
- plotly

## Installation Instructions

This project is designed to run in a Jupyter Notebook environment.

### For Windows Users (Using Anaconda)

1. **Install Anaconda**: Download and install Anaconda from [Anaconda's official website](https://www.anaconda.com/products/distribution).
2. **Launch JupyterLab**:
   - Open the Anaconda Navigator application.
   - Launch JupyterLab.
3. **Open the Notebook**:
   - Open the notebook named `NeuralNetworkPredictions2.ipynb`.
4. **Install Dependencies**:
   - The notebook includes commented-out commands for installing the necessary Python packages via pip. Simply uncomment them and run the corresponding cells in the notebook.

### For Linux Users

1. **Ensure Python 3 is Installed**: Verify that Python 3.7.0 or higher is installed on your system.
2. **Create a Virtual Environment (Optional)**:
   - Open a terminal and navigate to the project directory.
   - Create a virtual environment by running:
     ```
     python3 -m venv myenv
     source myenv/bin/activate
     ```
3. **Install JupyterLab**:
   - With the virtual environment activated, install JupyterLab using pip:
     ```
     pip install jupyterlab
     ```
4. **Start JupyterLab**:
   - Launch JupyterLab by running:
     ```
     jupyter lab
     ```
5. **Install Dependencies**:
   - In JupyterLab, you can install the necessary libraries directly within the notebook by uncommenting and running the pip installation commands as shown in the notebook.

## Getting Started

After completing the installation, navigate through the `NeuralNetworkPredictions2.ipynb` notebook. It will guide you through loading the data, training the model, and making predictions on new data sets.

Enjoy exploring and predicting with your flow cytometry data!
