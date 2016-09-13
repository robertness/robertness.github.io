---
title: Simulation of a Protein Signaling Perceptron
layout: post
---



A principle mechanism in signaling transduction is the multi-layer kinase cascade.  Uri Alon* presents a toy model of this mechanism based on a multi-layer perceptrion.  This structure, illustrated below is characteristic of the network motifs (bi-fan and diamond) that are typical of signaling cascades found in nature. 



![plot of chunk perceptronGraphPlot](/assets/figure/perceptronGraphPlot.png) 

I [implemented an ODE-based simulation](https://gist.github.com/osazuwa223/d554d77f237bc1e4eae5) of this system in R, making use of the [deSolve](http://cran.r-project.org/web/packages/deSolve/index.html) package to solve the ODEs and [igraph](http://igraph.org/r/) package as a data structure.  

<!--break-->

My goal was not just to simulate the trajectories of the nodes in the system, but to simulate a typical proteomics dataset by repeatly simulating trajectories, and in each case taking a single point from steady state and using it as a single observation in a dataset.  In other words, I wanted to simulate multiple single timepoint "snapshots" of the dynamic system.  In taking 1000s of such observations, one can simulate single cell dataset.  In taking the averages for a given node, one can simulate a sample in a bulk proteomics dataset.

There are two inputs to the cascade, "R1" and "R2", and on output "T".  The simulation of a signaling cascade is conducted by viewing each node as a protein that is either activated or inactivated.  The value for each node is the proportion of activated protein over the total amount of the protein.  Data is simulated by using random (uniform 0, 1) inputs for R1 and R2 (when the inputs are at low levels, the pathway will be inactivated).  The levels of R1 and R2 do not degrade (are constant).  Each subsequent layer is modeled using ODEs with first order kinetics $$\frac{dY^*}{dt} = k_{1} Y X_1^* + k_{2} Y X_{2}^* - \alpha_1 Y^*_1\\$$, where the rate of change in amount of activated protein $$Y^*$$ is determined by the amount of unactivated $$Y$$ and the amount of activated proteins in the previous layer $$X1^*$$ and $$X2^*$$ and rate parameters $$k_1$$ and $$k_2$$ (analogous to a double phosphorylation), as well as rate $$\alpha$$ of deactivation (analogous to the presence of phosphotase).  An example time course of a system with 2 middles layer looks like this:

![plot of chunk testParams](/assets/figure/testParams.png) 

Targeted interventions are included in the simulation.  These are used to test methods designed to learn the causal relationships between the nodes.  This is simulated by fixing the activation rate for a given node to be 0.  This forces proportion of the protein in active state to degrade to 0 in steady state, assuming the rate of deactivation is non-zero.  This is analogous to use of an inhibitor that blocks the phosphorylation of a given protein.

### References

*Alon, Uri. [An introduction to systems biology: design principles of biological circuits](http://books.google.com/books/about/An_Introduction_to_Systems_Biology.html?id=MWXdQgAACAAJ). CRC press, 2006.
