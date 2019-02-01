---
layout: post
title: Data Stacking on Executables
---
This analytic demonstrates how we can provide deep insights into a single varaible--in this case process counts. By creating a live-histogram of process counts and tracking counts over time, we can provide visibility into "low and slow" tactics by revealing uncommon processes or worms that are spreading throughout the network.

Resources: <…>

Owner: David Sherwood

### Technical
----
**Data Sources:**
* Endpoint

**Data Manipulation/EDA:** Aggregate by process name (often you are given a full path to the process, so some regex is required), then roll over a set time window--in this case I do 15 minutes batches. The result is a time series for each Windows process (.exe) in your environment which represent how many machines it is running on at a given time.

[Github](https://github.boozallencsn.com/commercial-analytics/Lighthouse-POC-analytics/blob/master/Data-Stacking-POC.ipynb)

**Technical details:** Correlate each process against the mean of the remaining processes and you will find movements that are separate from the global daily cycle. Another method would be to use STL decomposition or a Recurrent Neural Net to forecast counts over time. SageMaker provides one out of the box (DeepAR) which works well for this

### Reltional
----
**Tactics:**
* Lateral Movement
* Persistence
* Execution

**Motivations:**
* Sabotage
* Vandalism
* Theft
