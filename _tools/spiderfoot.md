---
title: SpiderFoot
layout: default
---

# SpiderFoot
SpiderFoot automates OSINT for threat intelligence and mapping your attack surface.

Detailed information [here](https://github.com/smicallef/spiderfoot).

# Techniques covered
- TA0043 Reconnaissance
    - T1595 Active Scanning
    - T1592 Gather Victim Host Information
    - T1589 Gather Victim Identity Information
    - T1590 Gather Victim Network Information
    - T1591 Gather Victim Org Information
    - T1597 Search Closed Sources
    - T1596 Search Open Technical Databases
    - T1593 Search Open Websites/Domains
    - T1594 Search Victim Owned Websites

# Basic Usage
```
# run following command to start spiderfoot
spiderfoot -l 0.0.0.0:8080

# open browser and explore localhost:8080
# Most things should be obvious and easy to understand
```