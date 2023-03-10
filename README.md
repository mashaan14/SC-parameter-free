# SC-parameter-free

## 	A parameter-free graph reduction for spectral clustering and SpectralNet
This is an implementation for the following paper:
```
@article{ALSHAMMARI2022100192,
	title = {A parameter-free graph reduction for spectral clustering and SpectralNet},
	journal = {Array},
	volume = {15},
	year = {2022},
	doi = {https://doi.org/10.1016/j.array.2022.100192},
	author = {Mashaan Alshammari and John Stavrakakis and Masahiro Takatsuka}
}
```

## How to use:

Run BATCH_Points.m which will execute the following:
1.	PRE_Points.m to load toy data, csv files are the groundtruth labels.
2.	the variable k is the number of clusters, the algorithm will cluster data to k clusters
	- RUN_Points_VQ.m to perform approximate spectral clustering with parameter $\m$ for:
		- kmeans approximation	+ local sigma edges
		- kmeans approximation	+ CONN edges
		- SOM approximation		+ CONN edges
		- kmeans approximation	+ CONNHybrid edges
		- SOM approximation		+ CONNHybrid edges
	- RUN_Points_Fast_Old.m to perform spectral clustering with the refined k-nearest nieghbor with parameter $\mu_0$
	- RUN_Points_Fast.m to perform spectral clustering with the proposed method
3.	POST_Points.m to compute the accuracy and adjusted Rand index of clustering

---
Provided by Mashaan Alshammari<br/>
mashaan14 at gmail dot com<br/>
mashaan dot awad at outlook dot com<br/>
April 04, 2020.