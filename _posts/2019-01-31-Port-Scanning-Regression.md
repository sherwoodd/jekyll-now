---
layout: post
title: Port Scanning Detection (Logistic Regression)
---
Attackers will attempt to gain information about a target and look for vulnerabilities prior to an attack through port scanning. Several scan detection techniques do not scale to very large networks where packet-level information may not be available. This analytic uses a Baysian logistic regression to detect port scanning using only unidirectional flow data.

Resources: <https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=1691061>

Owner: David Sherwood

### Technical
----
**Data Sources:**
* Network Gear

**Data Manipulation/EDA:** Researchers started with 21 features, and determined the six most meaningful. The six features included (1) the percentage of traces that appear to have a payload, (2) the percentage of flows with fewer than three packets, (3) the ratio of flag combinations with an ACK flag set to all flows, (4) the average number of source ports per destination IP address, (5) the ratio of the number of unique destination IP addresses to the number of traces, and (6) the ratio of traces with a backscatter-related flag combination such as SYN-ACK to all traces.

[Github](...)

**Technical details:** Use these six features as input in logistic regression model to calculate the probability of an event containing a scan. A Bayesian approach to logistic regression modeling was used instead of a traditional one. The Bayesian approach seeks to assign priors to each of the co-efficients based on expert opinion of the contribution each variable makes. (See resources for detailed implementation)

### Reltional
----
**Tactics:**
* Discovery

**Motivations:**
* Sabotage
* Vandalism
* Theft
