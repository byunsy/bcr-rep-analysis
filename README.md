# bcr-rep-analysis

## Description
Bcr-rep-analysis is a repository for all the code utilized in analyzing BCR Reperotires in COVID-19 patients. The google colab file provides a step-by-step guide for the user to follow and analyze BCR sequences and repertoires. 

## Abstract
Analyzing B cell receptor (BCR) repertoires is immensely useful in evaluating one’s immunological status. Conventionally, repertoire analysis methods have focused on comprehensive assessments of clonal compositions, including V(D)J segment usage, nucleotide insertions/deletions, and amino acid distributions. Here, we introduce a novel computational approach that applies deep-learning-based protein embedding techniques to analyze BCR repertoires. By selecting the most frequently occurring BCR sequences in a given repertoire and computing the sum of the vector representations of these sequences, we represent an entire repertoire as a 100-dimensional vector and eventually as a single data point in vector space. We demonstrate that this new approach enables us to not only accurately cluster BCR repertoires of coronavirus disease 2019 (COVID-19) patients and healthy subjects but also efficiently track minute changes in immune status over time as patients undergo treatment. Furthermore, using the distributed representations, we successfully trained an XGBoost classification model that achieved a mean accuracy rate of over 87% given a repertoire of CDR3 sequences.

Correspondence: iykim@snu.ac.kr

## Installation
This code requires installation of Elasticsearch (version 7.14.1 or above). 
```
pip install elasticsearch==7.14.1
```
All BCR sequences used in this study were downloaded from [Observed Antibody Space](http://opig.stats.ox.ac.uk/webapps/oas/) and stored in a private elasticsearch database for efficient storage and maintainence. Unfortunately, this code will not provide authentication code to access the database. 

Google colab provides all other necessary libraries and packages. The version-specific packages we've used are as follows:
```
pandas: 1.1.5
numpy: 1.19.5
matplotlib: 3.2.2
seaborn: 0.11.1
scikit-learn: 0.22.2.post1
xgboost: 0.90
```
