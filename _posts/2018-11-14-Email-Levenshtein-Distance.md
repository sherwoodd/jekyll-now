---
layout: post
title: Levenshtein for spoofing emails/urls
---
Some phishing attemps may use domains and emails similar in name to the company they are targeting. (ex. sending an email as rozanski_horaceo@beh.com saying to enter an updated client list and log-in credentials at www.booz-ellen-hamiltin.com/I_LOVE_PHISHING ). Normal Regular expressions wouldn't pick up on this obvious trick, but comparing sender email addresses and url domains with a list of known Executives/internal domains using a Levenshtein distance would show this.

Resources: <Splunk as a levenshtein distance implementation, python also has some modules to do this as well. Not too difficult to write yourself either.>

Owner: Benjamin Hahn
Data Sources:
* Internal
