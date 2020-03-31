# IFN-Python
This repository contains a python implementation of the Iterative Feature Normalization algorithm proposed by [Busso et al](https://ieeexplore.ieee.org/document/5947652). The algorithm is trained and evaluated on the [RAVDESS](https://zenodo.org/record/1188976#.XoONI5IzYx9) speech dataset. The following are the considerations taken:

- The first 18 speakers are taken as the training dataset and the last 6 speakers are taken as the held-out test dataset
- The IFN algorithm requires a reference neutral dataset. In this case, the first neutral sample from every speaker is taken and these 24 speech samples are aggregated to form the reference neutral dataset.
- A Gaussian Mixture Model containing two mixture distributions is considered.
- F0 contours are extracted by using the autocorrelation method. For more details, you can refer to this [link](https://gist.github.com/endolith/255291)
- Each speech sample is represented by a set of 7 F0 contour statistics: [F0 mean, F0 standard deviation, F0 range, F0 quantile 1, F0 quantile 3, F0 IQR, F0 median]

This algorithm was implemented as an assignment for the Affective Computing course (Spring'20) at IIIT Delhi.
