# lightcurve_classification
Exploring unsupervised lightcurve classification on ZTF and subsequently LSST observations.

## Unresolved Questions:
- What are "designer features"? From Mahabal et. al. 2017, "The designer features are better for specific classes, but carry with them a bias that does not necessarily translate to the classification of a wider set."
- What is the difference between "classification error" and "purity" (and "efficiency")?
- What do the latent features of an autoencoder look like? What does machine learning do on stochastic processes?
- 1D convolutional autoencoders? Pytorch?

## Resolved Questions:
- The dmdt image classification method (Mahabal et. al. 2017) seems suspiciously instrumentally-motivated rather than physically-motivated. We are suspicious that this method would not translate well to new surveys once trained on a particular survey.
- Within a neural network, "neurons" are just series of functions used to describe the observed data (e.g. activation function). There's no magic. See https://github.com/AstroHackWeek/AstroHackWeek2018/blob/master/day3_machine_learning/deep-learning/deep-learning-101.pdf.
- Tree-based classifiers are highly scalable because they are based in simplistic decision / inequalities. There are no high-order functions to consider.
- Physically-motivated features will always out-perform data-motivated features. When no physically-motivated features introduced, algorithm essentially has to rediscover physical laws. It's exciting to explore neural networks that respect physical laws. See: Joshua Bloom + Ellie Schwab at UC Berkely.


## References:
- Giles & Walkowicz 2018: The authors explore unsupervised classification of Kepler objects using the Density-Based Spatial 
Clustering of Applications with Noise (DBSCAN) algorithm. They considered Tabby's Star as a proof-of-concept case from which they could determine the effectiveness of their classifier.
- Mahabal et. al. 2017: The authors approach the question of object classification by first translating astronomical light curves into "dmdt" images and subsequently performing imaging classification on these two-dimensional representations via a convolutional neural network (CNN).
- Richards et. al. 2011: [Insert here]

