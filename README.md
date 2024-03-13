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

After completing the installation, navigate through the `NeuralNetworkPredictions2.ipynb` notebook. This notebook will guide you through the process of loading the data, training the model, and making predictions on new datasets.

### Loading Input Monoculture Files and Blanks

- You have the flexibility to choose the columns to keep for training from the cytometry files.
- File names and paths can be adjusted at the bottom of the cell.
  For example:
  ```python
  bacteroides_data, bacteroides_files, bacteroides_samples = load_and_sample_data("C:/Users/herme/Desktop/Live_Dead_Data/BT", 'bacteroides', files_to_process=None)
  
This command loads the bacteroides data files from the specified path. You can also choose the number of files to process by changing files_to_process=None (default is to take all files from the folder).

The files that are loaded are concatenated into one dataframe, with the label originating from the imports. If they were bacteroides, they will have the bacteroides name in the label column.
Adjusting sample_size in the load_and_sample_data function changes how many sample rows will be taken from each FSC file:
For example:
       def load_and_sample_data(folder_path, species, sample_size=12000, files_to_process=None):

### Distribution Plots
Change your name and files as needed. For example:
            
                     datasets = { 'Bacteroides': bacteroides_data, 'Blautia': blautia_data, 'Blanks': blanks_data }

Depending on the names chosen initially, you can change them here.

### Preparing for Training the Model
-The data are standardized and then transformed with arcsinh/150.
-The labels from before are encoded into integers to be used for classification.
-The neural network script utilizes a feedforward model from the Keras library, with two hidden layers and an output layer with a softmax activation function to classify the data into bacteroides, blautia, and blanks.

### Importing the Coculture Cytometry File
Next, import the coculture cytometry file at the chosen path and predict. You can give the path to your coculture here:

      coculture_filepath = 'C:/Users/herme/Desktop/Live_Dead_Data/BHBT/05-t60_d100_wc_bhbtD-F5.fcs'  # Path to FSC file










