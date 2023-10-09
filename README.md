# Predicting the Future Success of Nonprofit Funding


## Table of Contents

- [Overview of the Analysis](#overview-of-the-analysis)
- [Getting Started](#getting-started)
- [Data Preprocessing](#data-preprocessing)
- [Compiling, Training, and Evaluating the Model](#compiling-training-and-evaluating-the-model)
- [Software, Languages, and Libraries](#software-languages-and-libraries)
- [Results](#final-visualizations)
- [Acknowledgements](#acknowledgements)


## Overview of the Analysis
The purpose of this analysis is to provide a tool to a fictitious nonprofit foundation that can help it select applicants for funding with the best chance of success in their ventures by utilizing knowledge of machine learning and neural networks. Data provided for this analysis was a link to a CSV file containing more than 34,000 organizations that have received funding from the fictitious nonprofit.

After reading in the CSV data and creating the "application_df" dataframe, it was determined to use the "IS_SUCCESSFUL" column as the basis of the model training. After setting up the "Starter_Code" file per class instructions, the data was set up into feature and target arrays, then the model was scaled, defined and trained. This resulted in a Model Accuracy of 73.4%. 

The goal then was, using up to 3 different methods/attempts, to optimize the model to achieve higher than 75% accuracy.


## Getting Started
This project was created using Python in Jupyter Notebook. All that is needed is something to open and run the Jupyter Notebook files in the repository. The first created file is "Starter_Code.ipynb" which was used to create the initial neural network model. Code was then used from that file and the first optimization attempt was done using "Starter_Code - Optimize Attempt 1 - Keras Tuner.ipynb". Finally, "Starter_Code - Optimize Attempt 2 - NAME and Nodes.ipynb" was created. 

## Data Preprocessing
  * The variable (y) that is used for the target of the model is the column "IS_SUCCESSFUL".
  * The variables (X) used as the features of the model are the following columns:
    * "APPLICATION_TYPE"
    * "AFFILIATION"
    * "CLASSIFICATION"
    * "USE_CASE"
    * "ORGANIZATION"
    * "STATUS"
    * "INCOME_AMT"
    * "SPECIAL_CONSIDERATIONS"
    * "ASK_AMT"
  * I probably could have removed the "STATUS", "SPECIAL_CONSIDERATIONS", "ORGANIZATION", "USE-CASE" and/or "AFFILIATION" variables as there are few different options in those columns.
  
## Compiling, Training, and Evaluating the Model
  * I had 8 neurons/nodes in my first hidden layer, 5 neurons/nodes in my second hidden layer and then 1 neuron/node in the output layer. I used these because it seems like that is a standard beginning point when creating an initial model.
  * I was able to achieve the target model performance with an accuracy score of 76.4%.
  * 75% Attempt 1: Keras Tuner - In class, Keras Tuner was taught as a method to have the data evaluated and then be shown an optimal attempt at what might be the best model hyperparameters to use. I figured why not use it for this assignment! Unfortunately, Keras Tuner only received a Val Accuracy of 73.2%
  * 75% Attempt 2: "NAME" Column - I added the "NAME" column back into the data, and I also increased the first hidden layer neuron count to 80 and the second hidden layer neuron count to 50. Compiling and training with these changes resulted in an Accuracy score of 76.4%  

## Software, Languages, and Libraries
Full Listing:
* Jupyter Notebook
* Python
* Scikit-Learn
* TensorFlow


## Results
The initial model yielded a model accuracy of 73.4%. Success in achieving a higher than 75% accuracy took a few attempts. The first attempt was allowing Keras Tuner to try and offer the best model, which still did not get the accuracy over 75%. The second attempt, which included adding back data which had been removed and increasing the neurons in the layers, did achieve the goal of the model accuracy being over 75%. I would recommend being aware that certain data, if removed, could hurt your model. In this instance, seemingly the names of some of the organizations could weigh into the machine learning getting more useful data. Increasing the network by increasing he nodes also allows the deep learning more opportunities to compare the data for accuracy.

## Acknowledgements
This project was derived from my Data Analytics and Visualization Bootcamp from the University of Minnesota, Module 21, March 2023 cohort.


