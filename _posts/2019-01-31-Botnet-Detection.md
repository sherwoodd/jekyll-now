---
layout: post
title: Botnet Panels Detection with Ensembled Decision Trees
---
Botnets are covert networks of connected devices with massive computational power that are most often leveraged for large-scale email spam operations or denial of service (DOS) attack campaigns. While the typical method of Botnet detection is manually intensive and require expert knowledge, decisions trees and supervised learning can aid in the detection of new botnets with similar characteristics of known bad panels.

Resources: <https://threatvector.cylance.com/en_us/home/teaching-machines-security-identifying-botnet-panels.html>

Owner: David Sherwood

### Technical
----
**Data Sources:**
* DNS
* DHCP

**Data Manipulation/EDA:** There is a script (create_prevectors.py) to process each URL by making a series of requests to getting the HTTP response code and the ssDeep (fuzzy hash) of the content. Then there is a script to generate numerical features for training and inference (extract_features_from_prevectors.py) 

[Github](https://github.com/CylanceSPEAR/IDPanel)

**Technical details:** Once the vector is built, we can pass that into all of our decision trees. Each decision tree will produce a prediction for its assigned label, and the votes for each label are collected and combined. The most dominant label (i.e.: the one with the most votes) is then considered the prediction.

### Reltional
----
**Tactics:**
* Command & Control

**Motivations:**
* All
