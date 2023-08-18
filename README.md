# Défi Textmine 2024
## CRIT Team

Corresponding author: Nicolas Gutehrlé, nicolas.gutehrle@univ-fcomte.fr

### Description

This repository contains the data and files for exploring the dataset provided for the Textmine 2024 task (https://textmine.sciencesconf.org/resource/page/id/8). 

Our proposal relies on linear-chain Conditional Random Field (CRF) classifier and simple features extracted for each token such as their shape, their case, as well as linguistic features such as POS tags and dependency roles. We have trained several classifiers on different sets of features. Moreover, we have performed exhaustive grid search in order to find the optimal hyperparameters combinations.

### Structure
This repository is built as follows:
* data: contains the data provided for the TextMine task, ie the train, test and sample files in CSV format
* main: contains two Jupyter Notebooks:
    * exploration: simple exploration of the datasets
    * models: codes to train the CRF classifier and generate the submission files. This files contains the code to train the classifier with different parameters (hyperparameters, features)
* models: contains the trained models. Each folder contains the trained model in joblib format, the training parameters in json format and the corresponding submission file in the CSV format.
* README.md : this file
* requirements.txt: the dependency to install in order to run this project

### Note

This repo contains another branch named "old". This branch contains previous experiments on this task which proved less fruitful than this one.