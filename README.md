# Parallel_KNN
This repository contains implementations of the K-Nearest Neighbors (KNN) algorithm in both non-parallel and parallel versions. The parallel version leverages the joblib library to speed up the prediction phase. The project uses a synthetic dataset generated using sklearn.datasets.make_classification


**Reproducing Results:**   
the used dataset is a synthetic one so we only need to run the code


**Parallelization Strategy:**   
The parallel version of the KNN algorithm focuses on speeding up the prediction phase. Here’s how it works:    

	1- The test dataset is split into chunks.    

	2- Each chunk is processed independently using multiple CPU cores.    

	3- The joblib.Parallel function is used to distribute the workload across the available cores.   
	
	4- The results from each chunk are combined to produce the final predictions.

**Why Parallelize the Prediction Phase?**   

The prediction phase involves computing distances between each test sample and all training samples, which is computationally expensive.

Parallelizing this phase significantly reduces the prediction time, especially for large datasets.
