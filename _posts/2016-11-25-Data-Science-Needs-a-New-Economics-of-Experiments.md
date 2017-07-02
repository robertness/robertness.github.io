---
title: Data Science Needs a New Economics of Experiments
layout: post
---

The economics of running an experiment has fundamentally changed.  People who tell people how to run experiments need to change too.

Much ado has been made about big data.  It is increasingly possible to run experiments that affect how big data is generated, especially in IT-centric domains.  It is even easier to generate medium-sized data (roughly meaning more than a sparse few and less than a million observations) across a wider variety of domains.  In either case, these types of experiments are much cheaper to run than they were historically.  

Statistical experimental design was developed in Ronald Fisher’s era, when the cost of acquiring data was quite high.  Before any experiment, one had to think long and hard about the following;
* What are the questions I want to ask of the data specifically?
* Which factors do I want to test exactly?
* What is the smallest amount of data I need to acquire that will allow me to answer my question?
* How do I specify combinations of factors in a way that will allow me to get more information out of one data point?
* Can I block contextual factors (e.g. by gender) to reduce variance?

In this classical approach, planning has to address all these questions in the very beginning, before seeing any data.  Then you run a cash and time intensive experiment.  Don’t screw anything up!

However, with modern data, it often possibly to run experiments relatively cheaply and get results relatively quickly.  The data can inform some of these questions, enabling better follow up experiments.  So the investigator can iterate quickly from experiment to analysis back to experiment.  What's missing are methods that tell you how to do that. 

So the costs have have shifted from data production to data opportunity costs.  The opportunity cost lies in exploratory analysis of the data that wastes time and other resources in the best case, and leads to biased conclusions in the worst case.

It is time for statistics as a profession to step up and address the changing economics of experiments.  The methods are there (e.g. bandit optimization, Bayesian sequential experimental design).  This is a communications problem.