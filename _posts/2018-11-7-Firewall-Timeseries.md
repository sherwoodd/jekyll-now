---
layout: post
title: Firewall Time Series Anomaly Detection
---

Time series analysis attempts to track individual characteristics (e.g. Source IP and destination ports) over time to find unusual trends or activity at the perimeter of the network. This analytic technique attempts to find traces of port scanning or the initial signs of malware in a network. Time series forecasting and STL decomposition are used to find outliers within a signal that is cyclical or globally trending.

Owner: [David Sherwood](https://github.boozallencsn.com/sherwood-david)

Resources: 
* <https://machinelearningmastery.com/decompose-time-series-data-trend-seasonality> 
* <https://pdfs.semanticscholar.org/5a26/068dc9e216591f3afde777566c0469dcae0f.pdf>

Data Sources: 
* Firewall (checkpoint, juniper)

EDA: Extract counts of source IPs and destination ports over time - typically in 5 min intervals

[Github](https://github.boozallencsn.com/commercial-analytics/Lighthouse-POC-analytics/blob/master/Firewall-Timeseries-POC.ipynb)
