---
title: "The rise of probabilistic programming and causal inference"
layout: post
categories: [graphical models, causal inference, probabilistic programming]
---

People new to data science often ask me about the fast path to becoming a deep learning expert.  I encourage them that the strategic career-move is not to focus on what is hot now, but what will hot in the future.  My bet on the next big thing is causal inference.  The impetus behind this trend is the growing popularity of probabilistic programming.

In the typical case, an engineer has to think about which of the countless choices for machine learning algorithms he should choose to solve his problem.  This requires him spend a great deal of time learning the technical details of different algorithms, and inevitably the selection is biased towards algorithms and software he already understands or is skilled at using.  Moreover, like the Procrustean bed, the problem often has to be artificially reformulated to suit the requirements of the algorithm.

In contrast, probabilistic programming encourages a model-based approach to machine learning.  *Model-based machine learning* entails the creation of models tailored to each new application.   This model is then used to create a model-specific algorithm to solve the specific machine learning problem.  As people from domain-specific fields enter into machine learning (cognitive psychologists, molecular biologists, linguists), this will be the most attractive approach because it allows them to spend their time thinking deeply about how to map their problem domain to an explicit model, as opposed to trying to learn the technical and implementation details of the many ML algorithms out there in the wild.

Across probabilistic programming platforms, a common way of specifying a model is with a [directed acyclic network](https://en.wikipedia.org/wiki/Directed_acyclic_graph) or DAG.  The structure of the DAG captures assumptions about the plausible class of probability distributions that could be relevant to the application.  The intuition behind this is to interpret the DAG as the mechanism that generates the data by sampling at the root nodes, then sampling downstream from the conditional distribution of each node given the samples drawn from its parents in the DAG.

DAGs are a key element of causal modeling and inference.  Indeed, causal reasoning is typically exactly what we doing when we work with DAGs, though we often don’t realize it.  Domain-experts aren’t inclined to think of their domain merely in terms of joint probabilities or statistical correlations;

> The ubiquity of DAG models in statistical and AI applications stems (often unwittingly) primarily from their causal interpretation — that is, as a system of processes, one per family, that could account for the generation of the observed data.  It is this causal interpretation that explains why DAG models are rarely used in any variable ordering other than those which respect the direction of time and causation. ~ Judea Pearl, *Causality*. Cambridge University Press, 2009.

The hallmarks of causal inference are counterfactual reasoning and reasoning about interventions.  As probabilistic programming gains ground in machine learning, it will likely open up these paths of analysis to a audience broader than statisticians and researchers in causal inference.