---
layout: post
title: User/Asset Behavior Profiling
---
In contrast to User/Asset Behavior Clustering, this analytic attempts to track the patterns of a particular user relative to their own past behavior (rather than looking for anomalies across users). We use event log data (endpoint) to contruct typical process patterns based on the time of day for a certain user, and track similarity day-to-day or week-to-week.

Resources: <https://pdfs.semanticscholar.org/1a76/f0539a9badf317b0b35ea92f734c62467138.pdf?_ga=2.81780627.529039304.1547837895-752466249.1547837895>

Owner: David Sherwood

### Technical
----
**Data Sources:**
* Network Gear
* Endpoint

**Data Manipulation/EDA:** Starting with system call data (sendmail) and network data (tcpdump), we can use data mining algorithms to find common patterns. Two algorithms were used including the association rules algorithm and the frequent episodes algorithm. These algorithms can be used to compute the intra- and inter- audit record patterns, which are essential in describing program or user behavior.

[Github](...)

**Technical details:** To measure the similarity between a new pattern and the historical profile patterns, we introduced a similarity score, which is defined as m/n, where m is the number of new patterns that match historical normal profile patterns, and n is the number of all new patterns for detection. The higher the similarity score, the more possible the user performs normal behaviors in cyber systems

### Reltional
----
**Tactics:**

**Motivations:**
