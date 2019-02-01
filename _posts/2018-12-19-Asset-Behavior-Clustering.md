---
layout: post
title: Asset Behavior Clustering (Aggregate)
---
The goal of this analytic is to find hosts that exhibit atypical behavior compared to their peers. This involves performing clustering analysis on a large number of features representing behavior of a particular machine including the frequency of parent and child processes running, the types of accounts accessing the machine, the average file size, file extension, drive, etc.

Resources: <…>

Owner: David Sherwood

### Technical
----
**Data Sources:**
* Endpoint

**Data Manipulation/EDA:** Extract features from a set time window (currently using 15 minutes). Prepare your feature matrix so that each row is a different host and each column is a feature (usually frequencies or counts).

[Github](https://github.boozallencsn.com/commercial-analytics/Lighthouse-POC-analytics/blob/master/Asset-Behavior-POC.ipynb)

**Technical details:** Once you gather the feature matrix, normalize your columns so that each feature has a equal weight (TF-IDF proved to be the best method of normalizing due to the high sparseness and the large variance in "term-frequency"). Then, perform dimensionality reduction using PCA, and finally clustering using k-means. An ideal number of clusters can be determined with the "elbow point" method. By observing the hosts with the largest euclidean distance to their cluster-center, we can obtain both global and local outliers. You can either look at the top N outliers or the top X percentile.

### Reltional
----
**Tactics:**
* Initial Access
* Discovery
* Exfiltration

**Motivations:**
* Sabotage
* Vandalism
* Theft
