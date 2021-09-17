# LSTM-Pair-Trading

## Introduction

Data: List of 1,600 U.S. ETFs of various Type.

Data: Pick Small Cap & Technology ETFs from the List.

Data: Retrieve Data from Yahoo Finance

Methodology:
    Prepare Data for Clustering: Run PCA on ETFs Return and Retrieve Principle Component Weights to cluster on.

    Clustering: Cluster the ETFs using DBSCAN & K-Means.

    Co-integration: Test for Co-integration between all possible pairs with in each Cluster.

    LSTM: Predict the spread of cointegrated pairs, and display all results of all Pairs.

Results: Pick Best Best Pair based on Results (Sharpe ratio, CAGR, Avg Return (WhiteReality Check))

## Execution
1. Run step1_findpairs.ipynb to get two csv files which are the ticker pairs outputted by cointegration after clustering (both DBSCAN and K-Means).

2. Run step2_LSTM.ipynb to get the results passing White’s reality check from both DBSCAN and K-Means ticker pairs for both “Technology” and “Small Capital” ETFs.

Seed app of the project: https://github.com/israeldi/Final-Project-EECS545