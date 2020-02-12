# Session based Recommender using RNN

## Introduction

Session-based Recommenders aim to predict the user's immediate next actions based on implicit feedback from them via interactions like clicks. 

Here, we train GRU4Rec, a GRU-based RNN model for modeling behavior sequence and to make predictions for the next item to recommend based on the likelihood for each item. 

This model is tested against the following 2 datasets
1. RecSys Challenge 2015 - 6 months of clickstream data from an e-commerce site
2. Retail Rocket - Implicit data on user evens from an e-commerce site 

Item KNN is used as a baseline to compare metrics.

- Original paper: [Session-based Recommendations with Recurrent Neural Networks(ICLR 2016)](https://arxiv.org/pdf/1511.06939.pdf)
- Extension over the Original paper: [Recurrent Neural Networks with Top-k Gains for Session-based
Recommendations(CIKM 2018)](https://arxiv.org/abs/1706.03847)
- https://github.com/hidasib/GRU4Rec (code from authors of the papers)
- https://github.com/rn5l/session-rec (evaluation framework)

## Instructions

Install dependencies from requirements file.
conda install --yes --file requirements_conda.txt

Unzip raw data from the dataset to the corresponding folder ex. data/retailrocket/raw

Edit config file in conf/preprocess

Run the preprocessing script with config file as input
python run_preprocesing.py conf/preprocess/<<path to yml file>>

Train and test the model like below
python run_config.py conf/<<yml file with model config>>

### Dataset

RecSys Challenge 2015 Dataset can be retreived from [HERE](https://2015.recsyschallenge.com/)<br/>
Retail Rocket Dataset https://www.kaggle.com/retailrocket/ecommerce-dataset
