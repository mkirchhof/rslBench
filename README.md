# pRSL: Multi-label Benchmark Dataset Experiments

This repo contains the pRSL and other classifier's code run on the six multi-label benchmark datasets emotions, yeast, birds, medical, enron, and mediamill, each in one folder. In each folder, there is a /data folder, one folder for each classifier (BOOMER, MLWSE, NN) and some folders containing the pRSL hyperparameter tuning and final benchmarks reported in the paper. Additionally, there are some side experiments regarding calibration. Each pRSL folder is a self-contained experiment that includes (possibly outdated) code of rsl.R and norn.R, an experiment.R that runs the actual experiment (usually parallelized for cluster usage) and saves its results in *_res.RData files, and an analysis.R file that summarizes these results. 

So, to reproduce the experiments:
1. Select a dataset folder
2. Optional: Run the prepareData.R to download and k-fold the data from scratch
3. Run the hyperparameter tuning experiment.R in the corresponding folder
4. Select hyperparameters by running analysis.R
5. Run the final benchmark by running experiment.R in the corresponding folder
6. Summarize the results via analysis.R

The code for the other learners had to be partially omitted for copyright reasons. Feel free to message me if you need it.
Due to github size restrictions, the files for enron and mediamill are hosted on https://tu-dortmund.sciebo.de/s/elYhJXSlpSOt60J . If you run into problems in downloading, send me a message. 

# Further Resources:

- Main pRSL code repo (with up-to-date version of pRSL): https://github.com/mkirchhof/rsl
- Approximate inference experiments: https://github.com/mkirchhof/rslSim
- Benchmarks of pRSL on multi-label datasets: https://github.com/mkirchhof/rslBench
- Application of pRSL for transfer learning in human activity recognition: https://github.com/mkirchhof/rslAppl
- Paper: Kirchhof, M., Schmid, L., Reining, C., ten Hompel, M., Pauly, M.: pRSL: Interpretable Multi–label Stacking by Learning Probabilistic Rules. In: Proceedings of the 37th Conference on Uncertainty in Artificial Intelligence, PMLR, in press (2021).