# SC-parameter-free

[![DOI](http://img.shields.io/badge/doi-10.1016/j.array.2022.100192-36648B.svg)](https://doi.org/10.1016/j.array.2022.100192)

## 	A parameter-free graph reduction for spectral clustering and SpectralNet
This is an implementation for the following paper:
```bibtex
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

BATCH_Points.m executes the following commands:
1.	PRE_Points.m loads toy data, csv files are the groundtruth labels.
2.	the variable $k$ is the number of clusters, the algorithm will cluster data to $k$ clusters
	- RUN_Points_VQ.m to perform approximate spectral clustering with parameter $m$ for:
		- kmeans approximation	+ local sigma edges
		- kmeans approximation	+ CONN edges
		- SOM approximation		+ CONN edges
		- kmeans approximation	+ CONNHybrid edges
		- SOM approximation		+ CONNHybrid edges
	- RUN_Points_Fast_Old.m to perform spectral clustering with the refined $k$-nearest nieghbor with parameter $\mu_0$
	- RUN_Points_Fast.m to perform spectral clustering with the proposed method
3.	POST_Points.m to compute the accuracy and adjusted Rand index of clustering
