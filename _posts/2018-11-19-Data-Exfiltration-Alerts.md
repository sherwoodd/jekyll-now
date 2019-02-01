---
layout: post
title: Data Exfiltration Alerts
---
Email alerts of top potential data exfiltration events/entities each day. Dashboard detailing each event, and providing context about the characteristics that triggered alert specifically. Leverages combinations of thresholds/rules/outlier detection across multiple data sources (linked by individual user or entity) to create dynamic and holistic measures of anomalous behavior. Information was previously collected by standard security solutions, but not useful until abnormal activity was tracked across multiple tools.

Resources: <…>

Owner: Jillian Puskas

### Technical
----
**Data Sources:**
* Web Proxy
* VPN
* O365
* Windows Event Logs
* Printing

**Data Manipulation/EDA:** Some ETL needed to manipulate network gear log. Derived feature extraction to calculate how many bytes/time each session corresponded to. Filtering only the information that was relevant to potential exfil incidents (e.g. not all emails sent, but only ones with attachments included).

[Github](...)

**Technical details:** Provide contextual information about all of the tools and technologies touched by the anomalous user. Give context enrichment to the users behavior and potential indicators of exfiltration action.

### Reltional
----
**Tactics:**
* Collection
* Exfiltration
* Credential Access

**Motivations:**
* Theft
* Fraud
