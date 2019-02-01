---
layout: post
title: Port Scanning Detection (Threshold Random Walk)
---
Attackers will attempt to gain information about a target and look for vulnerabilities prior to an attack through port scanning. Typically scans fall into three categories: vertical scan, horizontal scan, and coordinated scan. This analytic applies ML to network data in search of malicious port scanning behavior

Resources: <http://www.icir.org/vern/papers/portscan-oak04.pdf>

Owner: David Sherwood

### Technical
----
**Data Sources:**
* Network Gear

**Data Manipulation/EDA:** It is critical to have data on which connections were successful and which were rejected/failed

[Github](...)

**Technical details:** The resources provide a detailed description of the math, but effectively this method is based on the observation that benign remote sources have more precise knowledge about the targeted hosts and services than scanners, such that their successful connection rate is higher than the scan rate. Hence, different probability thresholds are selected for true positives and false positives.

### Reltional
----
**Tactics:**
* Discovery

**Motivations:**
* Sabotage
* Vandalism
* Theft
