# NLP for Clinical Text

NLP for Clinical Text to support ICD coding automation, comparing the prediction performance of the following 3 models: CAML (Convolutional Attention for Multi-Label classification), LSTM (Long Short-Term Memory) and GRU (Gated Recurrent Unit).

The reference paper: [Explainable Prediction of Medical Codes from Clinical Text](https://arxiv.org/abs/1802.05695).

The reference code: [caml-mimic](https://github.com/jamesmullenbach/caml-mimic).

## Dependencies
* Python 3.7.7
* Python Built-in Modules (Collections, CSV, OS, Random, String, Sys, Warnings Math)
* numpy 1.18.2
* pandas 1.2.2
* gensim 3.8.3
* torch 1.7.1+cpu
* sklearn 0.24.1
* matplotlib 3.2.1
* jupyter-notebook 6.2.0

## Project File Structure

```
masamip2_NLPforClinicalTextCode
|   main.ipynb
|   README.md
└───mimic-iii-1.4/
|   |   caml.model (recommended)
|   |   codes_top.csv (recommended)
|   |   DIAGNOSES_ICD.csv (required)
|   |   gru.model (recommended)
|   |   lstm.model (recommended)
|   |   NOTEEVENTS.csv (required)
|   |   PROCEDURES_ICD.csv (required)
|   |   random_indices.csv (optional)
|   |   vocab.csv (optional)
|   |   w2v.embed (optional)
|   |   w2v.model (optional)

```

Open main.ipynb in Jupyter Notebook, go to 'Cell' tab and choose 'Run All'. It take about 15 minutes in the environment: Windows 10 Pro, CPU: 3.20 GHz, RAM: 32.0 GB

## Required Dataset
The MIMIC-III Clinical Database can be obtained from [PhysioNet](https://physionet.org/content/mimiciii/1.4/).
* DIAGNOSES_ICD.csv
* NOTEEVENTS.csv
* PROCEDURES_ICD.csv

## Recommended Files
### 1) Prelearned Models
The following models are already learned. To train the models, it will take a half day in the environment used for this project.
* caml.model
* gru.model
* lstm.model

### 2) Other Files
The following file is only for reducing the running time.
* codes_top.csv

## Optional Files
The following files will be needed with the 3 pre-trained models to reproduce the same results as this project.
* random_indices.csv
* vocab.csv
* w2v.embed
* w2v.model
