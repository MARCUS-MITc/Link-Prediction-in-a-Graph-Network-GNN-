# CP 318: Data Science for Smart City Applications
Project 1 Report

Team Jupiter  :  

Suraj Kumar, GVS Mothish , Naveen Reddi

This code contains 2 parts 

## Part 1 - Preprocessing, Sampling and Feature Generation.
### 1) ./sampling_and_feature_generation/sampling.ipynb
Takes the input data file and convert it into edges (From - To). 
And samples the edges from the full graph.

Input : 

individual_links.txt (obtained by melting the original train.csv given in project)

Output: 

edges_pos_random_100k.csv / edges_neg_random_100k.csv for random sampling

edges_pos_strategic_100k.csv / edges_neg_strategic_100k.csv for strategic sampling

### 2) ./sampling_and_feature_generation/preprocessing.ipynb
This file generates the features and gives the file with data containing feature params for training.

Input : 

edges_pos_random_100k.csv / edges_neg_random_100k.csv for random sampling

edges_pos_strategic_100k.csv / edges_neg_strategic_100k.csv for strategic sampling

test.csv

Output : 

train_100k_random.csv / test_100k_random.csv for random sampling

train_100k_str.csv / test_100k_str.csv for strategic sampling


## Part 2 - Training the model and Saving the trained Predictions.



### 1) logistic_regression.ipynb
### 2) Adaboost.ipynb 

Input : 

train_100k_random.csv / test_100k_random.csv for random sampling

train_100k_str.csv / test_100k_str.csv for strategic sampling

Output :

submission.csv

### 3) Big graph (./GNN) adopted from [4]



Input : 

individual_links.txt (obtained by melting the original train.csv given in project)

Output :

submission.csv

## References

1.  Fire, Michael, Lena Tenenboim-Chekina, Rami Puzis, Ofrit Lesser, Lior Rokach, and Yuval Elovici. "Computationally efficient link prediction in a variety of social networks." ACM Transactions on Intelligent Systems and Technology (TIST) 5, no. 1 (2014): 1-25.
2.    Cukierski, William, Benjamin Hamner, and Bo Yang. "Graph-based features for supervised link prediction." In The 2011 International joint conference on neural networks, pp. 1237-1244. IEEE, 2011.
3.    https://vgnshiyer.medium.com/link-prediction-in-a-social-network-df230c3d85e6.
4.    https://github.com/Bachfischer/COMP90051-StatML-Assignment-1/tree/master.
