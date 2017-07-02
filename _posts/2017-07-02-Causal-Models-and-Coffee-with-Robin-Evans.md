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

We discussed the use of the vanishing tetrad test in constructing latent variable models.  "Tetrad" refers to the difference between the product of a pair of covariances and the product of another pair among four random variables.

* Bollen, Kenneth A., and Kwok-fai Ting. "A tetrad test for causal indicators." Psychological methods 5.1 (2000): 3. [pdf](http://hbanaszak.mjr.uw.edu.pl/TempTxt/BollenTing_2000_A%20tetrad%20test%20for%20causal%20indicators.pdf)

We also talked about Robin's own work on in causal graphical models with latent variables.

* Richardson, Thomas S., Robin J. Evans, James M. Robins, and Ilya Shpitser. "[Nested Markov properties for acyclic directed mixed graphs.](https://arxiv.org/abs/1701.06686)" arXiv preprint arXiv:1701.06686 (2017).