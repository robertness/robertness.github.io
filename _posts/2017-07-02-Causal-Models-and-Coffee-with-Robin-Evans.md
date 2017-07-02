---
title: Causal Models and Coffee with Robin Evans
layout: post
---

Yesterday, I enjoyed the company of [Robin Evans](http://www.stats.ox.ac.uk/~evans/), Oxford Statistician and causal inference expert.  A few friends from the [Bay Area Probabilistic Programming](https://www.meetup.com/Bay-Area-Probabilistic-Programming/events/241194856/) meetup were in attendence.  

We discussed causal inference and modeling and its role in machine learning.

Some items that came up in the discussion.

The role of causal models in addressing algorithmic bias and discriminiation.
* [Pro Publica - Machine Bias](https://www.propublica.org/article/machine-bias-risk-assessments-in-criminal-sentencing)
* [Moritz Hardt - How Machine Learning is Unfair](https://medium.com/@mrtz/how-big-data-is-unfair-9aa544d739de)
* [U. Washington - Who's a CEO? Google image results can shift gender biases](https://www.eurekalert.org/pub_releases/2015-04/uow-wac040915.php)
* Nabi, Razieh, and Ilya Shpitser. "[Fair Inference On Outcomes.](https://arxiv.org/abs/1705.10378) arXiv preprint arXiv:1705.10378 (2017)".

From the latter article: _As statistical and machine learning models become an increasingly ubiquitous part of our lives, policymakers, regulators, and advocates have expressed fears about the harmful impact of deployment of such models that encode harmful and discriminatory biases of their creators._

We discussed the use of the vanishing tetrad test in constructing latent variable models.  "Tetrad" refers to the difference between the product of a pair of covariances and the product of another pair among four random variables.

* Bollen, Kenneth A., and Kwok-fai Ting. "A tetrad test for causal indicators." Psychological methods 5.1 (2000): 3.

We also talked about Robin's own work on in causal graphical models with latent variables.

* Richardson, Thomas S., Robin J. Evans, James M. Robins, and Ilya Shpitser. "Nested Markov properties for acyclic directed mixed graphs." arXiv preprint arXiv:1701.06686 (2017).