# CRIT submissions for Défi Textmine 2024

## Description

This repository contains the data and files for exploring the dataset provided for the Textmine 2024 task. It also contains the files for training the proposed pipeline. 

We propose a two-step pipeline, which consists in a candidate extraction step and a candidate classification step: 

The candidate extraction step is performed with a CRF classifier. To train this classifier, we have modified the training set to as to make it binary (either 'aucun' or 'NER'). Thus, this classifier predicts if a token is part of an NER of not.

The candidate classification step is performed with a machine-learning classifier. The classifier predicts if a token is either 'geogFeature', 'geogName' or 'name'. Here, we cast the task as a multi-label classification task. Thus, a token may be classified with a least 1 label. As for now, we have trained a KNN and XGBoost classifier.

## Structure
This repository is built as follows:
* data: contains the data provided for the Textmine Task
* embeddings: contains the French section of the ConceptNet word embeddings. These are stored in the format required to load them with the gensim library. You'll need to decompress the 'embeddings.zip' file first to acces the folder.
* exploration: contains four notebooks: exploration, crf, classifier and pipeline, with which we can train each model and build the final pipeline and make predictions
* models: contains the trained models
* submissions: contains the different generated submission for the task, in the required format