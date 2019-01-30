---
layout: post
title: DGA Detection (CNN)
---

Most URL paths follow some degree of randomness and patterns. DGA's usually have more randomness as the urls are created in bulk using some algorithm. These patterns may be impossible to detect by humans or even Regex, but Neural Networks have been shown to have high accuracy at tasks like this. Using CNNs on URLs and trained using PhishTank and Proxy labelled Phishing URLs could provide some 'score' for phishing attempts which get through the firewall.

Owner: [Ben Hahn](https://github.boozallencsn.com/hahn-benjamin)

Resources: TFLearn was used to create a basic 4 layer CNN on first 300 characters in URL. The SIG also has developed a similar capability using the same methodology.

Data Sources: 
* Web Proxy (Bluecoat)
* Public Dataset (Phishtank)
