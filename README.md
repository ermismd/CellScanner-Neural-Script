# Neural Network Predictions for Flow Cytometry
## Overview

This project aims to train a neural network using flow cytometry data to predict coculture compositions. The model is designed to analyze monoculture flow cytometry files, as well as blanks, to identify species present in coculture files. Additionally, the model employs gating strategies to classify cells into categories such as live, dead, and debris.

### Installation Instructions 

This project is designed to run in a Jupyter Notebook.

#### Windows Users (Using Anaconda)
Install Anaconda: Download and install Anaconda from Anaconda's official website. 
1. Open Anaconda Navigator application and launch JupyterLab

2. Open the Notebook <<NeuralNetworkPredictions2.ipynb>>
   
3. The notebook includes commented-out commands to install the necessary Python packages via pip. 
    - Simply uncomment them and run the corresponding cell in the notebook. 

#### Linux users
1. Ensure that Python 3 is installed
2.Create a Virtual Environment (Optional):
    -Open a terminal. Navigate to the project directory. Create a virtual environment by running:
     
         python3 -m venv myenv
         source myenv/bin/activate

3.With the virtual environment activated, install JupyterLab using pip:

             pip install jupyterlab

4.Start JupyterLab:

             jupyter lab

5.Install Dependencies:

 In JupyterLab you can install the necessary libraries directly within the notebook by uncommenting 
 and running the pip installation commands like before.


