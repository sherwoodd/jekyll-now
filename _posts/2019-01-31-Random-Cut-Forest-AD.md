---
layout: post
title: Random Cut Forest for Time Series Anomaly Detection
---
Amazon SageMaker provides an out-of-the-box algorithm for near-real time anomaly detection on streaming time series data

Resources: <https://docs.aws.amazon.com/sagemaker/latest/dg/randomcutforest.html>

Owner: David Sherwood

### Technical
----
**Data Sources:**
* Network Gear
* Web Proxy
* Endpoint
* DNS
* DHCP

**Data Manipulation/EDA:** While you can technically run Amazon RCF for anywhere, it is easiest for training to have it in an s3 bucket as a time series array

[Github](https://github.com/awslabs/amazon-sagemaker-examples/blob/master/introduction_to_amazon_algorithms/random_cut_forest/random_cut_forest.ipynb)

**Technical details:** Once trained, it is easy to make inferences to the model and return an "anomaly score" for each data point. The model can be extended to inferences on streaming data and deployed as an endpoint.

### Reltional
----
**Tactics:**

**Motivations:**
