# DetectionofAlzheimers
# EEG-Based Alzheimer's Disease Classification
This repository contains a Python script that performs EEG-based Alzheimer's disease classification using machine learning algorithms.

# Overview
The script consists of three main tasks:

Get Live EEG Data: Connect to an EEG stream using PyLSL, set up a buffer to store the last 90 seconds of EEG data, and compute the band powers (Delta, Theta, Alpha, Beta) for each epoch of 1 second with an overlap of 0.8 seconds.
Train Classification Model: Load EEG data from a folder, preprocess it using wavelet decomposition and wavelet coherence, extract features using Welch's method, and train a Random Forest Classifier on the extracted features.
Final Prediction: Use the trained model to make a prediction on the live EEG data collected in Task 1, compute the mean band powers for the live data, and pass them through the trained model to predict whether the patient has Alzheimer's disease or not.

# Requirements
Python 3.x
PyLSL (Lab Streaming Layer)
NumPy
Matplotlib
SciPy
Scikit-learn
PyWavelets
Joblib


# The script assumes that the EEG data is stored in a folder with the following structure:
EEG_data/
Healthy/
Eyes_open/
patient1.txt
patient2.txt
...
Eyes_closed/
patient1.txt
patient2.txt
...
AD/
Eyes_open/
patient1.txt
patient2.txt
...
Eyes_closed/
patient1.txt
patient2.txt
...
Each patient's EEG data is stored in a separate file, with the file name indicating the patient's ID.

# License
This repository is licensed under the MIT License. See LICENSE for details.

# Contributing
Contributions are welcome! If you'd like to contribute to this repository, please fork the repository, make your changes, and submit a pull request.

If you have any questions or issues, please contact Eshan Ghose (me) at eshanghose06@gmail.com
