---
title: OWASP Amass
layout: default
---

# OWASP Amass

Detailed information [here](https://github.com/OWASP/Amass).
Amass also integrates with Maltego.

# Techniques covered
- TA0043 Reconnaissance
    - T1596 Search Open Technical Databases
        - .001 DNS/Passive DNS
        - .002 WHOIS
        - .003 Digital Certificates

# Basic Usage
**ASN** - autonomous system number.

Globomantics is a fictional company used in trainings.
I am using globomantics website setup by pluralsight for their security training courses. Feel free to use other domains.

```shell
# Use non-recursive if there are too many subdomains
amass enum -v -d globomantics.com -src -ip [-norecursive] -dir globomantics
# Bruteforce domain names available at /usr/share/amass/wordlists
amass enum -v -d globomantics.com -src -ip -brute -dir globomantics
# ASN scan freezes system sometimes
amass intel -asn 16509
# whois lookup
amass intel -whois -d globomantics.com -dir globomantics
# list enumeration attempts
amass db -dir globomantics -list
# show details of enumeration attempt
amass db -dir globomantics -enum 1 -show
# visualize graph using d3
amass viz -dir globomantics -d3
```

{: .warning }
ASN scan may reveal domains which are running on shared infrastructure but are not part of the target.
Limit the scope to target when you don't have explicit permission to explore other domains.