This repository contains the code used for the experiments of the paper by Ilnura Usmanova, Yarden As, Maryam Kamgarpour, and Andreas Krause.
"Log Barriers for Safe Black-box Optimization with Application to Safe Reinforcement Learning"

The paper can be found here: https://arxiv.org/pdf/2207.10415.pdf

- All results of the experiments we made on our machine are saved in /runs folder. 
- The corresponding plots lie in /plots folder. 
- The code responsible for the LB_SGD, for plotting the plots, and for running the SafeOpt lies in /lib folder.

To reproduce the experiments,

1. Open the file /evals/experiments.ipynb (all the experiments are already there). 
2. Install a Python 3 environment and missing packages if needed using command: 
    pip install {library name} 
    (one can do that directly in Jupyter Notebook in a separate cell)
3. Run the cells corresponding to the LB_SGD experiments (they will rewrite the results in /runs folder)
4. Same for the SafeOpt experiments if you want (running them takes longer time)
5. Run the cells corresponding to plotting the experiments (this will use the information saved in /runs folder, and save the plot in /plots folder)

To reproduce the LineBO experiments, use the instruction we left in the corresponding readme.md file inside the /LineBO folder. We slightly modified the original code https://github.com/kirschnj/LineBO from the Johanness Kirschner's Github repository (we added the corresponding constraint functions to their benchmarks, and added the corresponding config files)