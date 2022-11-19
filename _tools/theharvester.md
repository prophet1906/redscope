---
title: theHarvester
layout: default
---

# theHarvester
E-mails, subdomains and names Harvester - Open Source Intelligence Gathering(OSINT)
Helps determine a company's external threat landscape on the internet.
Gathers emails, names, subdomains, IPs and URLs using multiple public data sources.
theHarvester complements other tools but doesn't replace any.

Detailed information [here](https://github.com/laramies/theHarvester).

# Techniques covered
Most external tools used by **theHarvester** require API keys, never got an opportunity to configure all keys and check which techniques from [TA0043 Reconnaissance](http://attack.mitre.org/tactics/TA0043/) are covered. I personally prefer [Spiderfoot](/tools/spiderfoot) over theHarvester.

# Basic Usage
The scans are non-intrusive as they depend on publicly availble information from different sites.

Many data sources block IP when you make too many calls to their APIs. Either restrict your search results with some cooldown between searches or use VPN to dodge IP blocks.
```shell
# check which sources are available with your version of harvester
theharvester -h
# passive recon
# limit to 500 searches
theharvester -d globomantics.com -l 500 -b anubis,baidu,bing,certspotter,crtsh,dnsdumpster,duckduckgo,hackertarget,omnisint,otx,qwant,rapiddns,sublist3r,threatcrowd,threatminer,urlscan,yahoo

# active recon - very noisy
# this will bruteforce dns names
theharvester -d globomantics.com -c

# dns lookup
theharvester -d globomantics.com -l 500 -b yahoo,bing -n

# all data source
theharvester -d nasa.gov -l 500 -b all
```