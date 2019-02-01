---
layout: post
title: Port Scanning Detection (SPICE)
---
Attackers will attempt to gain information about a target and look for vulnerabilities prior to an attack through port scanning. Traditional IDS use the occurrence of connections on resource IPs within time windows to look for port scanning, and hence miss stealthier slow-randomized attacks. This analytic seeks to assign an anomaly score to estimate the total information of a scan footprint based on the conditional probability distribution of normal traffic packets.

Resources: <http://hoagland.org/papers/Practical%20automated%20detection%20of%20stealthy%20portscans.pdf>

Owner: David Sherwood

### Technical
----
**Data Sources:**
* Network Gear

**Data Manipulation/EDA:** ...

[Github](...)

**Technical details:** …

### Reltional
----
**Tactics:**
* Discovery

**Motivations:**
* Sabotage
* Vandalism
* Theft
