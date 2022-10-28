# KL-RF
## 1. Description
KL-RF is a method to predict the associations between disease and gene by fusing the information of heterogeneous datasets. This method first learns the latent feature representation from disease-gene similarity networks via graph representation learning methods, then utilizes a Beyesian approach to obtain the posterior distribution of the feature matrix, and subsequently fuses the posterior distribution based on KL divergence and predicts the associations by random forest (KL-RF) finally.

## 2. Input data
The four 'npy' files are the raw features extracted for genes and diseases in the PPI-based and GO-based models.

"InBioList.txt" contains all the genes being analyzed in the study. "GeneList_v1.1.txt" contains all the disease-associated genes.

"Classified_disease_id.txt" contains the classified OMIM IDs of the 1154 diseases analyzed in the study. For those diseases without official IDs, a temporary ID is assigned for each of them at the end of the file.

"5foldIdx_shuffle_RN" contains the indices of the disease-gene pairs used in the 5-fold cross-validation. In the de novo prediction, the training and testing indices are concatenated to generate known data which are used to train the multimodel DBN.

## 3. Implementation

KL-RF is implemented in Python3 and depends on cvxpy, numpy, sklearn, scipy, POT, and matplotlib for plotting. It is tested on both Windows and Linux operating system. They are freely available for non-commercial use.<br>

## 4. Running
run_simulation_with_plots.py demonstrates how to use KL-fusion on simulated data.

KL-RF.ipynb demonstrates how to use random forest to predict disease-gene associations after KL-fusion.

## 5. Contact
If any questions, please do not hesitate to contact me at:
<br>
Hongdong Li `hongdong@csu.edu.cn`

