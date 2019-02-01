---
layout: post
title: Feature Selection for Intrusion Detection Systems
---
It is tedious to test the match between an input element and a rule (signature) by sequentially comparing every element. To improve this, we can cluster rules according to selected criteria. For instance we can put rules with the same constraints in the same group. Kruegel and Toth (2003) introduced a decision tree to detect the most discriminating features for a rule set and allowed it to perform a parallel evaluation of every feature.

Resources: <Page 76 of Data Mining and Machine learning (actual article: http://citeseerx.ist.psu.edu/viewdoc/download;jsessionid=9ACE76666A2BAE20681C5051B0B5DCB3?doi=10.1.1.10.9927&rep=rep1&type=pdf )>

Owner: David Sherwood

### Technical
----
**Data Sources:**

**Data Manipulation/EDA:** ...

[Github](...)

**Technical details:** In the decision tree, the root node corresponded to the set consisting of all rules. The children nodes were the direct subsets that were partitioned from the rule set according to the first feature. Nodes were portioned further until each node had only one rule. Each node was labeled with the feature used for the corresponding partitioning. Each arrow leading from a node to a child was associated with the value of the feature specified in the child node. Each leaf node contained one rule or the rules that could not be distinguished by features.

### Reltional
----
**Tactics:**

**Motivations:**
