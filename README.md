# Phylogenetic Inference with MCMC

This project consists of simulating phylogenetic trees, and then reconstructing them by means of inference. In particular, synthetic trees are generated with the Jukes-Cantor (JC) model. Inference is then performed on the leaf sequences with the Markov Chain Monte Carlo approach. Here, the JC model is used to define the likelihood of the leaves with respect to a particular tree topology. 

In order to explore both the tree topology space and the internal degrees of freedom (edge lengths), a combination of "external" and internal Monte Carlo (MC) steps are used. The external steps explore the tree space by means of nearest neighbor interchange (NNI) and subtree prune and regraft (SPR) moves. On the other hand, the internal steps explore possible edge lengths by means of a multiplicative symmetric proposal for each edge.

Both for the data simulation and inference, the edge lengths are drawn from an exponential prior. The scale parameter of this prior determines the correlation between parent and child sequences. Therefore, a suitable value was derived theoretically to ensure that the synthetic sequences had enough correlation so that the comparison between the inferred and true trees was meaningful.

The project was developed in Python, and all of the code and execution results can be found in the "development.ipynb" Jupyter notebook. 