---
layout: post
title: Beaconing Detection
---
It is common for malware to check in with the command and control server once it has infected a host. This activity is typically done in period time intervals and is referred to as "beaconing".  This analytic attempts to find these regular pings within common network traffic to provide an early warning sign of infection.

Resources: <http://www.austintaylor.io/detect/beaconing/intrusion/detection/system/command/control/flare/elastic/stack/2017/06/10/detect-beaconing-with-flare-elasticsearch-and-intrusion-detection-systems/>

Owner: Zander Lanfried
Data Sources:
* DNS
* DHCP
* Network Gear
