---
layout: post
title: Endpoint & Asset Management
---
Synthesize multiple scanning log sources to create automated list of active assets. Allows for data from multiple sources to be integrated into a singular resource. Consolidated data is used to create a visual dashboard/tool for analysts to track assets, explore new metrics of vulnerability, and benchmark security across entire enterprise.

Resources: <…>

Owner: Jillian Puskas

### Technical
----
**Data Sources:**
* DNS
* DHCP
* Endpoint
* Vulnerability Scanners
* Malware Scanner
* Databases

**Data Manipulation/EDA:** All converted to PySpark dictionary objects. Each data source is fit to a standard schema from individual, uniquely structured SQL tables. Manipulation involves extracting relevant data from tables and converting to constant schema to merge information about same assets/locations. As necessary, perform feature engineering/extraction from original tables.

[Github](...)

**Technical details:** Use new tables of information and aggregated views to provide new metrics like site grades, stronger integration into SOC and Incident Response capabilities.

### Reltional
----
**Tactics:**

**Motivations:**
