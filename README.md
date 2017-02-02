# SVM-GMM
My implementation of SVM and GMM using python and numpy

## Problem 1
**Support Vector Machines**. In this problem, I implement SVM that supports the kernel trick.

1. Download the training data: https://www.csie.ntu.edu.tw/~cjlin/libsvmtools/datasets/binary/a1a. I prepare 5 training and validating pairs for 5-fold cross validation: I randomly partition this training data into 5 (almost) equal sized subsets. A single subset is retained as the validation and the remaining 4 are used for training, at a time. I also keep these training and validation pairs for other problems below.
2. Next I train your SVM and tune the hyper-parameter C (I try to find the best possible C) using 5 fold cross-validation. I draw the plot on the average of prediction errors on the five training sets vs. C. I also draw the plot on the average of prediction errors on the five validation sets vs.C.
3. Test set is also available from LIBSVM: https://www.csie.ntu.edu.tw/~cjlin/libsvmtools/datasets/binary/a1a.t. Since this dataset contains more than 30,000 points, I just use the first 1,000 data points for simplicity. For the best performing C, I then report the test error.

## Problem 2
**Kernel Trick**. Using the same 5 training validation pairs in #1, I train my SVM with the Gaussian kernel. Then I find the best performing hyper-parameters (C and σ) for the Gaussian kernel, plot averaged prediction error on training/validation sets vs. hyper parameters (in plots you can vary only one hyper parameter at a time fixing the other), and report the test error, as before.

## Problem 3

1. I first build a function to generate i.i.d samples of Gaussian mixture models.
2. Then I implement the EM algorithm for Gaussian mixture models.
3. I generate data points in 2 dimensional space, with two mixture components I choose a parameter set for this Gaussian mixture model: mixture weight for two components as well as the parameter of Gaussian distribution, (μ, σ 2 ), for each component. Then I use my EM algorithm to estimate these parameters. For each step of EM, I make plots on new cluster centroids (or means of Gaussian components) and hard membership assignments according the posterior distributions.
4. Finally, I repeat the previous step with various settings.
