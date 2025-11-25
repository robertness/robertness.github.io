---
layout: page
title: Causal AI Book
permalink: /causal-ai-book/
---

# Causal AI Book

![Causal AI Book Cover](/assets/images/causal-ai-book-cover.jpg)

*Causal AI* is Robert Osazuwa Ness' [book on causality](https://www.manning.com/books/causal-ai).  

This page contains links to tutorials, notebooks, references, and errata.

---

## Chapter 1: Introduction

### Book recommendations

This book takes an opinionated approach to causality that focuses on graphs, probabilistic machine learning, Bayesian decision-making, and using deep learning tools such as PyTorch.

For books with alternative perspectives that focus on econometrics, social science, and practical data science themes, check out:

- [Causal Inference: The Mixtape](https://mixtape.scunning.com/)

- [Causal Inference and Discovery in Python](https://www.packtpub.com/product/causal-inference-and-discovery-in-python/9781804612989)

- [Causal Inference in Statistics: A Primer](https://www.amazon.com/Causal-Inference-Statistics-Judea-Pearl/dp/1119186846/ref=sr_1_1?adgrpid=1332608660533906&hvadid=83288112523943&hvbmt=be&hvdev=c&hvlocphy=95641&hvnetw=o&hvqmt=e&hvtargid=kwd-83288395424312%3Aloc-190&hydadcr=3240_10731484&keywords=causal+inference+in+statistics+a+primer&qid=1693072626&sr=8-1)

### Key references in the chapter

- D'Amour, A., Heller, K., Moldovan, D., Adlam, B., Alipanahi, B., Beutel, A., Chen, C., Deaton, J., Eisenstein, J., Hoffman, M.D. and Hormozdiari, F., 2020. **Underspecification presents challenges for credibility in modern machine learning.** *arXiv preprint arXiv:2011.03395*.

---

## Chapter 2: Primer on probability modeling

Our course on [probabilistic machine learning](https://www.altdeep.ai/p/probml) covers in detail the elements of Bayesian and probabilistic inference covered in this chapter.

- [Chapter 2 notebooks](https://github.com/altdeep/causalML/tree/master/book/chapter%202)

### Book recommendations

- Murphy, K.P., 2022. [Probabilistic Machine Learning: An Introduction](https://probml.github.io/pml-book/book1.html). MIT Press.

- Hsu, H.P., 1997. [Schaum's Outline of Theory and Problems of Probability, Random Variables, and Random Processes](https://www.amazon.com/Schaums-Probability-Variables-Processes-Outlines-dp-1260453812/dp/1260453812/ref=dp_ob_title_bk). McGraw-Hill.

---

## Chapter 3: Building a causal graphical model

- [Chapter 3 notebooks](https://github.com/altdeep/causalML/tree/master/book/chapter%203)

- See additional code and causal modeling ideas in the [projects directory](https://github.com/altdeep/causalML/tree/master/projects).

### Causal abstraction

- Beckers, S. and Halpern, J.Y., 2019, July. **Abstracting causal models.** In *Proceedings of the AAAI Conference on Artificial Intelligence* (Vol. 33, No. 01, pp. 2678–2685).

- Beckers, S., Eberhardt, F. and Halpern, J.Y., 2020, August. **Approximate causal abstractions.** In *Uncertainty in Artificial Intelligence* (pp. 606–615). PMLR.

- Rischel, E.F. and Weichwald, S., 2021, December. **Compositional abstraction error and a category of causal models.** In *Uncertainty in Artificial Intelligence* (pp. 1013–1023). PMLR.

### Independence of mechanism

- Schölkopf, B., Janzing, D., Peters, J., Sgouritsa, E., Zhang, K. and Mooij, J., 2012. **On causal and anticausal learning.** *arXiv preprint arXiv:1206.6471*.

- Rojas-Carulla, M., Schölkopf, B., Turner, R. and Peters, J., 2018. **Invariant models for causal transfer learning.** *Journal of Machine Learning Research*, 19(36), pp.1–34.

- Besserve, M., Shajarisales, N., Schölkopf, B. and Janzing, D., 2018, March. **Group invariance principles for causal generative models.** In *International Conference on Artificial Intelligence and Statistics* (pp. 557–565). PMLR.

- Parascandolo, G., Kilbertus, N., Rojas-Carulla, M. and Schölkopf, B., 2018, July. **Learning independent causal mechanisms.** In *International Conference on Machine Learning* (pp. 4036–4044). PMLR.

### Causal data fusion and transfer learning

- Bareinboim, E. and Pearl, J., 2016. **Causal inference and the data-fusion problem.** *Proceedings of the National Academy of Sciences*, 113(27), pp.7345–7352.

- Rojas-Carulla, M., Schölkopf, B., Turner, R. and Peters, J., 2018. **Invariant models for causal transfer learning.** *Journal of Machine Learning Research*, 19(36), pp.1–34.

- Magliacane, S., van Ommen, T., Claassen, T., Bongers, S., Versteeg, P. and Mooij, J.M., 2017. **Causal transfer learning.** *arXiv preprint arXiv:1707.06422*.

### Causally invariant prediction

- Arjovsky, M., Bottou, L., Gulrajani, I. and Lopez-Paz, D., 2019. **Invariant risk minimization.** *arXiv preprint arXiv:1907.02893*.

- Heinze-Deml, C., Peters, J. and Meinshausen, N., 2018. **Invariant causal prediction for nonlinear models.** *Journal of Causal Inference*, 6(2), p.20170016.

- Rosenfeld, E., Ravikumar, P. and Risteski, A., 2020. **The risks of invariant risk minimization.** *arXiv preprint arXiv:2010.05761*.

- Lu, C., Wu, Y., Hernández-Lobato, J.M. and Schölkopf, B., 2021. **Nonlinear invariant risk minimization: A causal approach.** *arXiv preprint arXiv:2102.12353*.

---

## Chapter 4: Testing your causal graph

- [Chapter 4 notebooks](https://github.com/altdeep/causalML/tree/master/book/chapter%204)

### Tools for d-separation

- *NetworkX*'s [`d_separation` algorithm](https://networkx.org/documentation/stable/reference/algorithms/d_separation.html).

- *pgmpy*'s [`get_independencies` method](https://github.com/pgmpy/pgmpy/blob/467ada830ca3b9fff0acf8ce49e86e4de00e050e/pgmpy/base/DAG.py#L394) enumerates all d-separations in a DAG.

- [Dagitty.net](http://dagitty.net/) provides both an online application for building DAGs and evaluating d-separation. It also provides an R package.

- The [`dsep`](https://www.bnlearn.com/documentation/man/dsep.html) function in the *bnlearn* R package evaluates simple d-separation statements as true or false.

- [Causalfusion](https://causalfusion.net/) is an online app like Dagitty but with a valuable set of additional features. You need to apply for access.

### Background on statistical hypothesis testing

- See chapter 8 of [Schaum's Outline of Probability, Random Variables, and Random Processes](https://www.amazon.com/Schaums-Probability-Variables-Processes-Outlines-dp-1260453812/dp/1260453812/ref=dp_ob_title_bk) for a good introduction to statistical hypothesis testing.

- Wikipedia has good descriptions of the [Chi-squared test](https://en.wikipedia.org/wiki/Chi-squared_test), [G-test](https://en.wikipedia.org/wiki/G-test), and [likelihood-ratio test](https://en.wikipedia.org/wiki/Likelihood-ratio_test) for conditional independence.

- Conditional independence tests [implemented in pgmpy](https://pgmpy.org/_modules/pgmpy/estimators/CITests.html) and [SciPy](https://docs.scipy.org/doc/scipy/reference/generated/scipy.stats.power_divergence.html).

- The PyWhy suite has a library for advanced statistical independence tests called [pywhy-stats](https://github.com/py-why/pywhy-stats).

### Tools for causal discovery

- The PyWhy suite contains the popular [causal-learn](https://github.com/py-why/causal-learn) library for causal discovery.

- PyWhy also contains an experimental library called [dodiscover](https://github.com/py-why/dodiscover), which focuses on being a user-friendly interface for discovery.

- The [bnlearn package](https://www.bnlearn.com/) is an R package, and it has a corresponding [Python library](https://pypi.org/project/bnlearn/).

### False discovery rate and causal discovery

- Wikipedia page on the [multiple comparisons problem](https://en.wikipedia.org/wiki/Multiple_comparisons_problem) that occurs when doing repeated hypothesis testing. Standard statistical remedies are to do a [family-wise error rate correction](https://en.wikipedia.org/wiki/Family-wise_error_rate) or calculate a [false discovery rate](https://en.wikipedia.org/wiki/False_discovery_rate).

- Pena, J.M., 2008, March. **Learning Gaussian graphical models of gene networks with false discovery rate control.** In *European Conference on Evolutionary Computation, Machine Learning and Data Mining in Bioinformatics* (pp. 165–176). Springer.

- The bnlearn package implements the interleaved incremental association algorithm with FDR in the [`iamb.fdr`](https://www.bnlearn.com/documentation/man/constraint.html) function.

- Gasse, M., Aussem, A. and Elghazel, H., 2014. **A hybrid algorithm for Bayesian network structure learning with application to multi-label learning.** *Expert Systems with Applications*, 41(15), pp.6755–6772.

### Go deeper on functional constraints (Verma constraints)

- Tian, J. and Pearl, J., 2012. **On the testable implications of causal models with hidden variables.** *arXiv preprint arXiv:1301.0608*.

- Bhattacharya, R. and Nabi, R., 2022, August. **On testability of the front-door model via Verma constraints.** In *Uncertainty in Artificial Intelligence* (pp. 202–212). PMLR.

### More on causal faithfulness

- Zhang, J. and Spirtes, P., 2016. **The three faces of faithfulness.** *Synthese*, 193, pp.1011–1027.

- Ramsey, J., Zhang, J. and Spirtes, P.L., 2012. **Adjacency-faithfulness and conservative causal inference.** *arXiv preprint arXiv:1206.6843*.

### Selected readings on causal discovery

- Spirtes, P., 2001, January. **An anytime algorithm for causal inference.** In *International Workshop on Artificial Intelligence and Statistics* (pp. 278–285). PMLR.

- Spirtes, P., Glymour, C. and Scheines, R., 2001. *Causation, Prediction, and Search.* MIT Press. (Introduces the PC algorithm, though one might enjoy [this intro](https://www.youtube.com/watch?v=o2A61bJ0UCw&ab_channel=BradyNeal-CausalInference) by Brady Neal.)

- Chickering, D.M., 2002. **Optimal structure identification with greedy search.** *Journal of Machine Learning Research*, 3(Nov), pp.507–554.

- Friedman, N. and Koller, D., 2003. **Being Bayesian about network structure. A Bayesian approach to structure discovery in Bayesian networks.** *Machine Learning*, 50, pp.95–125.

- Heckerman, D., Meek, C. and Cooper, G., 2006. **A Bayesian approach to causal discovery.** In *Innovations in Machine Learning: Theory and Applications*, pp.1–28.

- Meek, C., 2013. **Causal inference and causal explanation with background knowledge.** *arXiv preprint arXiv:1302.4972*.

- Cooper, G.F. and Yoo, C., 2013. **Causal discovery from a mixture of experimental and observational data.** *arXiv preprint arXiv:1301.6686*.

- Ogarrio, J.M., Spirtes, P. and Ramsey, J., 2016, August. **A hybrid causal search algorithm for latent variable models.** In *Conference on Probabilistic Graphical Models* (pp. 368–379). PMLR.

- Ness, R.O., Sachs, K. and Vitek, O., 2016. **From correlation to causality: statistical approaches to learning regulatory relationships in large-scale biomolecular investigations.** *Journal of Proteome Research*, 15(3), pp.683–690.

- Glymour, C., Zhang, K. and Spirtes, P., 2019. **Review of causal discovery methods based on graphical models.** *Frontiers in Genetics*, 10, p.524.

- Zheng, Y., Huang, B., Chen, W., Ramsey, J., Gong, M., Cai, R., Shimizu, S., Spirtes, P. and Zhang, K., 2024. **Causal-learn: Causal discovery in Python.** *Journal of Machine Learning Research*, 25(60), pp.1–8.

---

## Chapter 5: Building causal graphs with deep probabilistic machine learning

- [Chapter 5 notebooks](https://github.com/altdeep/causalML/tree/master/book/chapter%205)

- [Typeface MNIST data (Kaggle)](https://bit.ly/3QbdSFv)

### An explanation of the case study on independence of mechanism in semi-supervised learning

One way to understand this example is to use the combined perspectives of Bayesian reasoning and d-separation. In both the causal learning and anti-causal case, during training, we're learning some set of parameters for a model of \( P(X, Y) \). Let's decouple this set into \(\theta_y\) for the parameter set that parameterizes the causal Markov kernel for \(Y\) and \(\theta_x\) for the parameter set that parameterizes the causal Markov kernel for \(X\). Further, let's take the Bayesian approach of treating \(\theta_x\) and \(\theta_y\) as random variables, and give them their own nodes in the DAG, as shown in the following figure.

![DAG illustrating causal vs anti-causal learning. The DAG on the left depicts causal learning, with the feature causing the label. The DAG on the right depicts anti-causal learning, with the label causing the feature. Theta-x and theta-y are parameter oracles made explicit as nodes. Assume only X is observed. X is d-separated from theta-y in the causal learning case but not in the anti-causal case.](https://uploads.teachablecdn.com/attachments/7hS6zIXdSt2Kt2Gs1yKX_Learning+copy.png)

We'll interpret these "Greek" nodes as oracles that set the parameters of the causal Markov kernels of \(X\) and \(Y\), and our job during unsupervised training is to infer these unknown parameters from \(X\) alone. We can see that in the causal learning case, \(X\) and \(\theta_y\) are d-separated and thus \(X\) is not informative of \(\theta_y\). But in the anti-causal learning case, \(X\) and \(\theta_y\) are d-connected, thus \(X\) is informative of \(\theta_y\).

For more information, see:

- Schölkopf, B., Janzing, D., Peters, J., Sgouritsa, E., Zhang, K. and Mooij, J., 2012. [On causal and anticausal learning](https://icml.cc/2012/papers/625.pdf). *arXiv preprint arXiv:1206.6471*.

### Vision as Inverse Graphics

- [Intro to Vision as Inverse Graphics](https://ps.is.mpg.de/research_fields/inverse-graphics) from Max Planck Institute for Intelligent Systems.

- Romaszko, L., Williams, C.K., Moreno, P. and Kohli, P., 2017. **Vision-as-inverse-graphics: Obtaining a rich 3D explanation of a scene from a single image.** In *Proceedings of the IEEE International Conference on Computer Vision Workshops* (pp. 851–859).

### Causal representation learning and disentanglement

- [Intro to Causal Representation Learning](https://ei.is.mpg.de/research_projects/causal-representation-learning) from Max Planck Institute for Intelligent Systems.

- Kumar, A., Sattigeri, P. and Balakrishnan, A., 2017. **Variational inference of disentangled latent concepts from unlabeled observations.** *arXiv preprint arXiv:1711.00848*.

- Locatello, F., Bauer, S., Lucic, M., Raetsch, G., Gelly, S., Schölkopf, B. and Bachem, O., 2019, May. **Challenging common assumptions in the unsupervised learning of disentangled representations.** In *International Conference on Machine Learning* (pp. 4114–4124). PMLR.

- Yang, M., Liu, F., Chen, Z., Shen, X., Hao, J. and Wang, J., 2020. **CausalVAE: Structured causal disentanglement in variational autoencoder.** *arXiv preprint arXiv:2004.08697*.

- Wang, Y. and Jordan, M.I., 2021. **Desiderata for representation learning: A causal perspective.** *arXiv preprint arXiv:2109.03795*.

- Ahuja, K., Hartford, J. and Bengio, Y., 2021. **Properties from mechanisms: an equivariance perspective on identifiable representation learning.** *arXiv preprint arXiv:2110.15796*.

- Reddy, A.G. and Balasubramanian, V.N., 2022, June. **On causally disentangled representations.** In *Proceedings of the AAAI Conference on Artificial Intelligence* (Vol. 36, No. 7, pp. 8089–8097).

### Miscellaneous

- Ali Rahimi's quote comparing machine learning to alchemy can be found at the [11:59 mark in this video](https://youtu.be/ORHFOnaEzPc?t=719) of his NIPS 2017 Test-of-Time Award presentation.

---

## Chapter 6: Structural Causal Models

- [Chapter 6 notebooks](https://github.com/altdeep/causalML/tree/master/book/chapter%206)

- Javaloy, A., Sánchez-Martín, P., & Valera, I., 2023. *Causal normalizing flows: from theory to practice.* In: A. Oh, T. Naumann, A. Globerson, K. Saenko, M. Hardt, & S. Levine, eds. *Neural Information Processing Systems.* Curran Associates, Inc., pp. 58833–58864. doi: [10.48550/arXiv.2306.05415](https://proceedings.neurips.cc/paper_files/paper/2023/hash/b8402301e7f06bdc97a31bfaa653dc32-Abstract-Conference.html).

---

## Chapter 7: Interventions and Causal Effects

- [Chapter 7 notebooks](https://github.com/altdeep/causalML/tree/master/book/chapter%207)

---

## Chapter 8: Counterfactuals and Parallel Worlds

- Verma, S., Dickerson, J. and Hines, K., 2020. **Counterfactual explanations for machine learning: A review.** *arXiv preprint arXiv:2010.10596*.

- Pearl, J., 2010. **Brief report: On the consistency rule in causal inference: "axiom, definition, assumption, or theorem?".** *Epidemiology*, pp.872–875.

### Probabilities of Causation

- Beckers, S., 2021. **Causal sufficiency and actual causation.** *Journal of Philosophical Logic*, 50(6), pp.1341–1374.

- Knobe, J. and Shapiro, S., 2021. **Proximate cause explained.** *The University of Chicago Law Review*, 88(1), pp.165–236.

- Pearl, J., 2022. **Probabilities of causation: three counterfactual interpretations and their identification.** In *Probabilistic and Causal Inference: The Works of Judea Pearl* (pp. 317–372).

### Uplift Modeling

- Li, A. and Pearl, J., 2019, August. **Unit selection based on counterfactual logic.** In *Proceedings of the Twenty-Eighth International Joint Conference on Artificial Intelligence*.

- Gutierrez, P. and Gérardy, J.Y., 2017, July. **Causal inference and uplift modelling: A review of the literature.** In *International Conference on Predictive Applications and APIs* (pp. 1–13). PMLR.

---

## Chapter 9: The Counterfactual Inference Algorithm

- [Chapter 9 notebooks](https://github.com/altdeep/causalML/tree/master/book/chapter%209)

- [ChiRho library](https://github.com/BasisResearch/chirho) for causal inference with probabilistic models (extension of Pyro).

### Intractable likelihood methods in probabilistic inference

- Papamakarios, G., et al. **Normalizing flows for probabilistic modeling and inference.** *Journal of Machine Learning Research*, 22.1 (2021): 2617–2680.

- Matsubara, T., et al. **Robust generalised Bayesian inference for intractable likelihoods.** *Journal of the Royal Statistical Society Series B: Statistical Methodology*, 84.3 (2022): 997–1022.

- Ritchie, D., Horsfall, P. and Goodman, N.D., 2016. **Deep amortized inference for probabilistic programs.** *arXiv preprint arXiv:1610.05735*.

- Murphy, K.P., 2023. *Probabilistic Machine Learning: Advanced Topics.* MIT Press.

---

## Chapter 10: Causal Hierarchy and Identification

- [Chapter 10 notebook](https://github.com/altdeep/causalML/blob/master/book/chapter%2010/Chapter_10_Identification_notebook.ipynb)

### Do-calculus, Pearl's causal hierarchy and identification algorithms

- The [Y0 repository for causal inference and identification](https://github.com/Chrisejorge/Causal-Inference).

- Bareinboim, E., Correa, J.D., Ibeling, D. and Icard, T., 2022. **On Pearl's hierarchy and the foundations of causal inference.** In *Probabilistic and Causal Inference: The Works of Judea Pearl* (pp. 507–556).

- Shpitser, I. and Pearl, J., 2006, July. **Identification of joint interventional distributions in recursive semi-Markovian causal models.** In *Proceedings of the National Conference on Artificial Intelligence* (Vol. 21, No. 2, p. 1219).

- Shpitser, I. and Pearl, J., 2008. **Complete identification methods for the causal hierarchy.** *Journal of Machine Learning Research*, 9, pp.1941–1979.

- Huang, Y. and Valtorta, M., 2006. **Pearl's calculus of intervention is complete.** *arXiv preprint arXiv:1206.6831*.

### Potential outcomes, single world intervention graphs, and related concepts

- Malinsky, D., Shpitser, I. and Richardson, T., 2019, April. **A potential outcomes calculus for identifying conditional path-specific effects.** In *The 22nd International Conference on Artificial Intelligence and Statistics* (pp. 3080–3088). PMLR.

- Shpitser, I., Richardson, T.S. and Robins, J.M., 2022. **Multivariate counterfactual systems and causal graphical models.** In *Probabilistic and Causal Inference: The Works of Judea Pearl* (pp. 813–852).

- Robins, J.M. and Richardson, T.S., 2010. **Alternative graphical causal models and the identification of direct effects.** In *Causality and Psychopathology: Finding the Determinants of Disorders and Their Cures*, 84, pp.103–158.

- Richardson, T.S. and Robins, J.M., 2013, July. **Single world intervention graphs: a primer.** In *Second UAI Workshop on Causal Structure Learning*, Bellevue, Washington.

- Robins, J.M., vanderWeele, T.J. and Richardson, T.S., 2007. **Contribution to discussion of "Causal Effects in the Presence of Non-compliance: a Latent Variable Interpretation" by A. Forcina.** *Metron*, LXIV (3), pp. 288–298.

- Geneletti, S. and Dawid, A.P., 2007. **Defining and identifying the effect of treatment on the treated.** Technical Report No. 3, Imperial College London, Department of Epidemiology and Public Health.

### Identification of effect of treatment on the treated

- Shpitser, I. and Tchetgen, E.T., 2016. **Causal inference with a graphical hierarchy of interventions.** *Annals of Statistics*, 44(6), p.2433.

### Partial identification bounds

- Mueller, S. and Pearl, J., 2022. **Personalized decision making — A conceptual introduction.** *arXiv preprint arXiv:2208.09558*.

- Li, A. and Pearl, J., 2022. **Probabilities of causation with nonbinary treatment and effect.** *arXiv preprint arXiv:2208.09568*.

- Li, A. and Pearl, J., 2022, June. **Unit selection with causal diagram.** In *Proceedings of the AAAI Conference on Artificial Intelligence* (Vol. 36, No. 5, pp. 5765–5772).

---

## Chapter 11: Building a Causal Effect Estimation Workflow

- [Notebooks](https://github.com/altdeep/causalML/tree/master/book/chapter%2011)

---

## Chapter 12: Primer on Causality in Decisions, Bandits, and Reinforcement Learning

- [Notebooks](https://github.com/altdeep/causalML/tree/master/book/chapter%2011)

### Causal decision theory, Newcomb's paradox, and introspection/deliberation

- [Causal decision theory](https://en.wikipedia.org/wiki/Causal_decision_theory) — Wikipedia.

- [Newcomb's paradox](https://en.wikipedia.org/wiki/Newcomb%27s_paradox) — Wikipedia.

- [Agent causation](https://en.wikipedia.org/wiki/Agent_causation) — Wikipedia.

- Stern, R., 2018. **Diagnosing Newcomb's problem with causal graphs.** In *Newcomb's Problem*, pp.201–220.

- Skyrms, B., 1982. **Causal decision theory.** *The Journal of Philosophy*, 79(11), pp.695–711.

- Lewis, D., 1981. **Causal decision theory.** *Australasian Journal of Philosophy*, 59(1), pp.5–30.

- Joyce, J.M., 2002. **Levi on causal decision theory and the possibility of predicting one's own actions.** *Philosophical Studies*, 110, pp.69–102.

- Clarke, R., 1993. **Toward a credible agent-causal account of free will.** *Noûs*, 27(2), pp.191–203.

### Causal bandits and reinforcement learning, counterfactual risk minimization

- Bareinboim, E., Forney, A. and Pearl, J., 2015. **Bandits with unobserved confounders: A causal approach.** *Advances in Neural Information Processing Systems*, 28.

- Buesing, L., Weber, T., Zwols, Y., Racaniere, S., Guez, A., Lespiau, J.B. and Heess, N., 2018. **Woulda, coulda, shoulda: Counterfactually-guided policy search.** *arXiv preprint arXiv:1811.06272*.

- Swaminathan, A. and Joachims, T., 2015, June. **Counterfactual risk minimization: Learning from logged bandit feedback.** In *International Conference on Machine Learning* (pp. 814–823). PMLR.

- Scott, S.L., 2010. **A modern Bayesian look at the multi-armed bandit.** *Applied Stochastic Models in Business and Industry*, 26(6), pp.639–658. (This paper doesn't use causal reasoning, but its Bayesian framing of the bandit problem can extend to counterfactual reasoning by admitting counterfactual notation.)

### Causality in games, counterfactual regret minimization in multiagent games

- Zinkevich, M., Johanson, M., Bowling, M. and Piccione, C., 2007. **Regret minimization in games with incomplete information.** *Advances in Neural Information Processing Systems*, 20.

- Brown, N., Lerer, A., Gross, S. and Sandholm, T., 2019, May. **Deep counterfactual regret minimization.** In *International Conference on Machine Learning* (pp. 793–802). PMLR.

- Hammond, L., Fox, J., Everitt, T., Carey, R., Abate, A. and Wooldridge, M., 2023. **Reasoning about causality in games.** *Artificial Intelligence*, 320, p.103919.

- Soto, M.G., Sucar, L.E. and Escalante, H.J., 2020. **Causal games and causal Nash equilibrium.** *Research in Computing Science*, 149, pp.123–133.

---

## Chapter 13: Causality and Large Language Models

- [Chapter 13 notebooks](https://github.com/altdeep/causalML/tree/master/book/chapter%2013)

### Key references in the chapter

- Kıcıman, E., Ness, R., Sharma, A. and Tan, C., 2023. **Causal reasoning and large language models: Opening a new frontier for causality.** *arXiv preprint arXiv:2305.00050*.

