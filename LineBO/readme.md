This repository contains the code used for the experiments of the ICML 2019 Paper by Johannes Kirschner et al.
"Adaptive and Safe Bayesian Optimization in High Dimensions via One-Dimensional Subspaces"

The paper can be found here: https://arxiv.org/abs/1902.03229

To reproduce the experiments,

1. Install a Python 3.6 environment
2. Install the package with "pip install -e ."
3. pip install git+https://github.com/automl/HPOlib2 
4. pip install git+https://github.com/befelix/SafeOpt.git


To run the experiments, replace "{problem_name}" in the instructions below by any of:

* Gaussian
* GaussianUn
* QP
* Rosenbrock

 and the "{experiment_name}" by any of: {problem_name}_{dimensionality}

Instructions to run experiments and create plots:

1. febo create {experiment_name} --config config/{problem_name}/{experiment_name}.yaml
2. febo run {experiment_name}
                (this will take a while, you can set the number of repetitions in the yaml file)
3. febo plot {experiment_name} --plots febo.plots.InferenceRegret
