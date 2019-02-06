# lightcurve_classification
Exploring unsupervised lightcurve classification on ZTF and subsequently LSST observations.

## References:
- Giles & Walkowicz 2018: The authors explore unsupervised classification of Kepler objects using the Density-Based Spatial 
Clustering of Applications with Noise (DBSCAN) algorithm. They considered Tabby's Star as a proof-of-concept case from which they could determine the effectiveness of their classifier.
- Mahabal et. al. 2017: The authors approach the question of object classification by first translating astronomical light curves into "dmdt" images and subsequently performing imaging classification on these two-dimensional representations via a convolutional neural network (CNN).

## Questions:
- Daniela noted that she's not entirely set on the dmdt image classification method. I would like to hear more about why not.
- I want to gain a greater understanding of what happens compuationally within a neural network. (E.g. What *are* the "neurons" exactly? What does having different layers do to a neural network?)
- What are "designer features"? From Mahabal et. al. 2017, "The designer features are better for specific classes, but carry with them a bias that does not necessarily translate to the classification of a wider set."
