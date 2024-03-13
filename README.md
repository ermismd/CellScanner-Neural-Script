# Neural Network Predictions for Flow Cytometry
## Overview

This project aims to train a neural network using flow cytometry data to predict coculture compositions. The model is designed to analyze monoculture flow cytometry files, as well as blanks, to identify species present in coculture files. Additionally, the model employs gating strategies to classify cells into categories such as live, dead, and debris.

### Installation Instructions 

This project is designed to run in a Jupyter Notebook.

#### Windows Users (Using Anaconda)
Install Anaconda: Download and install Anaconda from Anaconda's official website. 
Open Anaconda Navigator application and launch JupyterLab, open the Notebook <<NeuralNetworkPredictions2.ipynb>>
The notebook includes commented-out commands to install the necessary Python packages via pip. To execute these commands,
simply uncomment them and run the corresponding cell in the notebook. 

#### Linux users
Ensure that Python 3 is installed on your system. Y
Create a Virtual Environment (Optional):
Open a terminal. Navigate to your project directory. Create a virtual environment by running:
>>python3 -m venv myenv
>>source myenv/bin/activate

With your virtual environment activated, install JupyterLab using pip:
>>pip install jupyterlab

Start JupyterLab:
>> jupyter lab

Install Dependencies:
In JupyterLab, open the notebook file. You can install the necessary libraries directly within the notebook by uncommenting 
and running the pip installation commands provided in the notebook cells.
