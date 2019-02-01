---
layout: post
title: Process Behavior Anomaly Detection
---
The goal of this analytic is to find processes that are behaving abnormally by studying the frequency and ordering of their system calls and sub processes.

Resources: <Page 97 of Data Mining and Machine Learning>

Owner: David Sherwood

### Technical
----
**Data Sources:**
* Endpoint

**Data Manipulation/EDA:** Similar to user/asset behavior clustering, we extract features for every executable including the frequency of system calls like "open", "read", "write", "kill", etc. We then use TF-IDF (where your terms are system calls and the document is the process) to normalize the data

[Github](0)

**Technical details:** A K-Nearest Neighbor Classifier is used to mark program behavior as normal or intrusive, using the 1998 Darpa IDS data as training. Processes were ranked according to their distance and a threshold was applied on the averaged K distances as a cutoff of anomaly detection. Various thresholds were tested using burte force ROC curves. See Liao and Vemuri, 2002 for full paper.

### Reltional
----
**Tactics:**
* Command & Control
* Persistence
* Execution

**Motivations:**
* Sabotage
* Vandalism
* Theft
