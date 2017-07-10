---
title: Causal Models and Coffee with Robin Evans
layout: post
---

Yesterday, I enjoyed the company of [Robin Evans](http://www.stats.ox.ac.uk/~evans/), Oxford Statistician and causal inference expert.  A few friends from the [Bay Area Probabilistic Programming](https://www.meetup.com/Bay-Area-Probabilistic-Programming/events/241194856/) meetup were in attendence.  

We discussed how the Bay Area machine learning community thinks about causal inference and causal models.  

The goal of causal machine learning as evaluating and improving counterfactual predictions.  A counterfactual prediction means predicting the data we would observe if we were to _intervene in_ (i.e. change) the conditions that generated the training data. In other words, it predicts "what would happen if we were to do something different?", like serving a new kind of ad or changing a gene.  Using regular non-causal models like deep learning to predict counterfactuals is just extrapolation, which is often unreliable.  Causal models model the mechanism that generates the data, and thus can represent changes interventions make to that mechanism.  A key task in causal machine learning is addressing the nuances of randomization strategy.

Some references

* [Causality in machine learning - The Unofficial Google Data Science Blog](http://www.unofficialgoogledatascience.com/2017/01/causality-in-machine-learning.html)
* [A/B Testing and Beyond: Improving the Netflix Streaming Experience with Experimentation and Data Science](https://medium.com/netflix-techblog/a-b-testing-and-beyond-improving-the-netflix-streaming-experience-with-experimentation-and-data-5b0ae9295bdf)
* Vicarious's post about [General Game Playing with Schema Networks](https://www.vicarious.com/general-game-playing-with-schema-networks.html).  _The recent adaptation of deep neural network-based methods to reinforcement learning and planning domains has yielded remarkable progress on individual tasks. Nonetheless, progress on task-to-task transfer remains limited. In pursuit of efficient and robust generalization, we introduce the Schema Network, an objectoriented
generative physics simulator capable of disentangling multiple causes of events and reasoning backward through causes to achieve goals._
* Zhang, Junzhe, and Elias Bareinboim. Markov decision processes with unobserved confounders: A causal approach. Technical Report R-23, Purdue AI Lab, 2016. [pdf](https://www.cs.purdue.edu/homes/eb/mdp-causal.pdf)

We discussed the role of causal models in addressing algorithmic bias and discriminiation.

* [Pro Publica - Machine Bias](https://www.propublica.org/article/machine-bias-risk-assessments-in-criminal-sentencing)
* [Moritz Hardt - How Machine Learning is Unfair](https://medium.com/@mrtz/how-big-data-is-unfair-9aa544d739de)
* [U. Washington - Who's a CEO? Google image results can shift gender biases](https://www.eurekalert.org/pub_releases/2015-04/uow-wac040915.php)
* Nabi, Razieh, and Ilya Shpitser. "[Fair Inference On Outcomes.](https://arxiv.org/abs/1705.10378)"" arXiv preprint arXiv:1705.10378 (2017).

From the latter article: _As statistical and machine learning models become an increasingly ubiquitous part of our lives, policymakers, regulators, and advocates have expressed fears about the harmful impact of deployment of such models that encode harmful and discriminatory biases of their creators._

Dat Nguyen asked Robin for his general recommendation on how to handle a causal problem where there’s potentially hidden latent variables, is high dimensional, and experimentation is possible but costly and/or time consuming (i.e. can't just do ad hoc A/B testing). 

Robin suggests using the PC algorithm or graphical lasso to try to get a sparse representation of the system (or at least to find the strongest apparent effects).  He also suggested applying methods that try to obtain the direction of causal effects by making assumptions about additivity, sugh as Jonas Peters' work on causal discovery, or the LINGAM method.

Having found some good candidates for important effects, the next step would be to try to run an experiment with interventions that would distinguish between models of interest.  Finding the whole causal model would be very hard, but answering a narrower question is plausible.  This experiment should make it much clearer what directions some effects are in, and how strong they are.  Now you can update and repeat.

Theoretically, a small number of experiments is sufficient to identify the whole causal model, though this tends to assume that interventions are very clean in a way that often isn't very realistic (see [this (pdf)](http://people.hss.caltech.edu/~fde/papers/HEH2013jmlr.pdf)).

* Hoyer, P.O., Janzing, D., Mooij, J.M., Peters, J. and Schölkopf, B.Hoyer, Patrik O., et al. "[Nonlinear causal discovery with additive noise models.](http://papers.nips.cc/paper/3548-nonlinear-causal-discovery-with-additive-noise-models)" Advances in Neural Information Processing Systems. 2009.

* Shimizu, Shohei, et al. "[A linear non-Gaussian acyclic model for causal discovery (LINGAM).](http://www.jmlr.org/papers/v7/shimizu06a.html)" Journal of Machine Learning Research 7.Oct (2006): 2003-2030.

We discussed the use of the vanishing tetrad test in constructing latent variable models.  "Tetrad" refers to the difference between the product of a pair of covariances and the product of another pair among four random variables.

* Bollen, Kenneth A., and Kwok-fai Ting. "A tetrad test for causal indicators." Psychological methods 5.1 (2000): 3. [pdf](http://hbanaszak.mjr.uw.edu.pl/TempTxt/BollenTing_2000_A%20tetrad%20test%20for%20causal%20indicators.pdf)

We also talked about Robin's own work on in causal graphical models with latent variables.

* Richardson, Thomas S., Robin J. Evans, James M. Robins, and Ilya Shpitser. "[Nested Markov properties for acyclic directed mixed graphs.](https://arxiv.org/abs/1701.06686)" arXiv preprint arXiv:1701.06686 (2017).