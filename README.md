# scaling-laws-paper
Code for "Neural Scaling Laws Rooted in the Data Distribution", [Brill (2024)](https://arxiv.org/abs/2412.07942)

## percolation.ipynb
This file contains the code used for all experiments, including generating percolation simulations and fitting regression models to the data. It was run as a Google Colab notebook. For the hyperparameters used in the paper, this requires either a high-RAM (Colab Pro) or GPU runtime to avoid running out of RAM. After the notebook finishes, all output files are downloaded to the user's machine. The notebook usually takes about 10-15 minutes to run depending on the size of the largest cluster generated assuming the parameterized DOF scan is skipped, or otherwise roughly double that. To repoduce the experiments in the paper, the notebook should be run multiple times following the sequence:

1) seed = 0, do_cluster_plots = True, do_scan = True: generate most plots
2) seed = 1, 2, ... 49, do_cluster_plots = False, do_scan = False: download results for each seed
3) \(upload all results\) seed = 0, do_cluster_plots = False, do_scan = False: generate scaling plots

Performing the cluster plots visualizations and parameterized DOF scan only in the first run saves significant time.

## plots.ipynb
This file contains the code to generate all other (e.g. theoretical) plots. It should run in about 30 seconds.
