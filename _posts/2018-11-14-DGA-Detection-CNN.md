---
layout: post
title: CNN for DGAs (Domain Generating Algorithms)
---
Most URL paths follow some degree of randomness and patterns. DGA's usually have more randomness as the urls are created in bulk using some algorithm. These patterns may be impossible to detect by humans or even Regex, but Neural Networks have been shown to have high accuracy at tasks like this. Using CNNs on URLs and trained using PhishTank and Proxy labelled Phishing URLs could provide some 'score' for phishing attempts which get through the firewall.

Resources: <TFLearn was used to create a basic 4 layer CNN on first 300 characters in URL. The SIG also has developed a similar capability using the same methodology.>

Owner: Benjamin Hahn

### Technical
----
**Data Sources:**
* Web Proxy
* Public Dataset

**Data Manipulation/EDA:** Sending URLS with encoded characters must be consistent. Some number of characters must be used for CNN (300 was chosen, more than that had diminishing returns). Other features such as separating domain from url, http vs https, etc... can be used to increase accuracy. 

[Github](...)

**Technical details:** (see consideration implementation considerations + outputs)

### Reltional
----
**Tactics:**
* Initial Access
* Pre-ATT&CK

**Motivations:**
* All
