---
layout: post
title: Network Traffic Anomaly Detection (One-class SVM/KNN/Cluster-based)
---
This paper presents a detailed, three-algorithm approach to anomaly detection to find intrusions in unlabeled data. This algorithm should detect malicious behaviors including stealthy reconnaissance attempts, backdoor service on a well-known standard port, natural failures in the network, new buffer overflow attacks, HTTP traffic on a nonstandard port, intentionally stealthy attacks, variants of existing attacks in new environments, and so on.

Resources: <http://www.andrewoarnold.com/uad-dmsa02.pdf>

Owner: David Sherwood

### Technical
----
**Data Sources:**
* Network Gear
* Firewall

**Data Manipulation/EDA:** The sample data had already gone feature extraction to gather 41 features -- see KDD cup 99 for details (or the newer NSL-KDD)

[Github](0)

**Technical details:** After extracting features describing a network connection, the researches used cluster-based estimation, K-nearest neighbor, and one class svm to detect points which lie in sparse regions of the feature space.

### Reltional
----
**Tactics:**
* Initial Access
* Discovery
* Lateral Movement

**Motivations:**
* Sabotage
* Vandalism
* Theft
