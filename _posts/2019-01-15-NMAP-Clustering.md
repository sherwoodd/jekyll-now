---
layout: post
title: NMAP Clustering
---
Kmeans clustering technique using results from the NMAP port scanning tool in order to identify groups of similar IP addresses across a large number of ports, e.g. when auditing the security of a network

Resources: <…>

Owner: Zander Lanfried

### Technical
----
**Data Sources:**
* Nmap

**Data Manipulation/EDA:** XML must be parsed into numerical features to prepare for K-means clustering. The github provides a script to do this (parsing.py) or you can write your own

[Github](https://github.com/CylanceSPEAR/NMAP-Cluster)

**Technical details:** K-means is used to find groups of IP addresses from a matrix of features where every row is a unique IP. The Github repo provides scripts to tune hyperparameters like the number of clusters through brute force error calculations (elbow method). Clustering IPs could be a preliminary step in anomaly detection.

### Reltional
----
**Tactics:**

**Motivations:**
