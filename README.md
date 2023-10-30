# Fed-MStacking
The Code of Fed-MStacking: Heterogeneous Federated Learning with Stacking Misaligned Labels for Abnormal Heart Sound  Detection

## Abstract
Stuttering is a complicated language disorder. The most common  form of stuttering is developmental stuttering, which begins  in childhood. Early monitoring and intervention are essential  for the treatment of children with stuttering. Automatic  speech recognition technology has shown its great potential  for non-fluent disorder identification, whereas the previous  work has not considered the privacy of users  data. To  this end, we propose federated intelligent terminals for automatic  monitoring of stuttering speech in different contexts.  Experimental results demonstrate that the proposed federated  intelligent terminals model can analyse symptoms of stammering  speech by taking the personal privacy protection into  account. Furthermore, the study has explored that the Shapley  value approach in the federated learning setting has comparable  performance to data-centralised learning.

#### Index Terms— Stuttering Monitoring, Federated Learning, Computer Audition, Healthcare

## Data
Preparation and Analysis of the Signals for [PhysioNet/CinC Challenge Dataset:](https://physionet.org/content/challenge-2016/1.0.0/)

Since the study involves heterogeneous local models, as shown in Fig 1, we processed raw heart sound recordings based on two modalities. 

<div align="center">
<img src="/results/data.jpg" width="400" height="400">
</div>
<div align="center">Fig.1 Illustration of pre-processing for heart sound recordings.</div>

Common acoustic signal features are extracted through the openSMILE toolkit and are used for ML models.
   
``openSmile_raw": one-dimensional signal features from the raw recordings.

``openSmile_balanced": one-dimensional signal features from the balanced recordings.

Another modality involves image representation, where we adopted the continuous wavelet transform (CWT) for sound-image transformation used in DL models.
   
``image_CWT_raw": two-dimensional image features from the raw recordings.

``image_CWT_balanced": two-dimensional image features from the balanced recordings.

## Base Model

The Federated Learner: Binary=(RF, ANN, CNN)

gms: Gassian Mixture Models (List of GMMs)

The data to be decided (Acc, Se, Sp, UAR, UF1)

clfs: The binary classifiers;(List of Classifiers)

p_nodes: The proportion of the nodes; (List)


## Files

``Centralised_ensemble_learn.ipynb": We set up a set of baseline models based on data-centralised learning.

``Fed_ensemble_learn.ipynb": We present two medical institutions with three clients respectively, and perform homogeneous and heterogeneous stacked FL based on the local model under balanced data. 

## Remarks

In the code above, the scalar function is trained by full test data. We point out that this scalar is nothing but means and variances. One can equivalently train a scalar given the mean and variance of each node and their proportions in real processes.

## Contact

Please contact the authors of this work if you have any questions or comments.
