---
layout: post
title: Supervised Learning for Intrusion Detection Systems
---
Traditional IDS take in either network data or process data and generate signatures with are binary codes that represent patterns of behavior. They then attempt to match these signatures with a list of known bad signatures and take an action to stop it. This analytic attemps to improve the signature based detection by performing supervised learning to look for and alert on signatures that are "similar to known bad"

Resources: <Page 68 to 73 of Data Mining and Machine Learning>

Owner: David Sherwood

### Technical
----
**Data Sources:**
* Network Gear
* Endpoint

**Data Manipulation/EDA:** In network based IDS, a signature can be a specific pattern of the packets such as packet content signature and/or header content signatures that can indicate unauthorized actions such as improper FTP initiation. The features extracted include the protocol ID, source port, destination port, source address, destination address, ICMP type, ICMP code, raw data length, and raw data.

[Github](...)

**Technical details:** Researchers have used SVM, Artifical Neural Nets (ANN), Decision Trees, and Genetic Programming (GP) to classify network evetns as normal and intrusive. Details on the implementations can be found in the attached resource and the associated articles. In most cases the NSL-KDD dataset was used for network data, and the 1998 DARPA dataset was used for process data. One particularly good exmaple can be found here: https://teams.microsoft.com/_#/pdf/viewer/teams/https%3A~2F~2Fboozallen.sharepoint.com~2Fsites~2FAdvancedAnalytics~2FShared%20Documents~2FGeneral~2FAA%20Investment%20Review%20Folder~2FAnalytics%20Portfolio~2FMulti-PerspectiveMachineLearningAClassifierEnsemblemethodforintrusiondetection.pdf?threadId=19%3A38cbba7ef58c4c83883092c35ba00197%40thread.skype&baseUrl=https%3A~2F~2Fboozallen.sharepoint.com~2Fsites~2FAdvancedAnalytics&fileId=4D637079-55C9-47E3-8A2F-864F1F11026D&ctx=files&viewerAction=view

### Reltional
----
**Tactics:**
* Initial Access
* Discovery
* Command & Control
* Execution

**Motivations:**
* Sabotage
* Vandalism
* Theft
