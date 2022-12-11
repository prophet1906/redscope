---
title: Maltego CE
layout: default
---

# Maltego CE
It is an open source intelligence(OSINT) and graphical link analysis tool for gathering and connecting information for investigative tasks.

Detailed information [here](https://www.maltego.com/maltego-community/).

Maltego transforms data node in graph and populates more nodes in graph. There are more than 100 transforms in maltego.

{: .info }
Consider paid version for professional red team and bug bounty. Community version shows limited results.

# Techniques covered
- Technical Information Gathering
    - T1253 Conduct passice scanning
    - T1250 Determine domain and IP address space
- People Information Gathering
    - T1269 Identify People of Interest

# Basic Usage
Set domain name as root node, then run transforms as shown below.

globomantics.com
    - List of subdomains
        - List if IPs for each subdomain
    - List of key technical people
        - E-mail addresses
            - E-mails in previous data breaches

You need to register for Maltego Community Edition.

## Steps
1. Create a new graph by pressing + button on top left corner.
2. Create a new node by dragging and dropping domain from left entity palette.
3. Right click on domain node to see transforms menu.
4. Click on `To DNS Name - NS(name server)`, this should create child nodes with name server information.
5. You can also delete nodes from graph.
6. We are trying to collect technical information from nasa.gov domain.
7. Maltego community edition is limited to max of 12 results per transform.
8. Use transform `To DNS Name (interesting) [SecurityTrails]`.
9. Go with least common subdomains as target, common domains are usually patched frequently.
10. You can now apply transform `To IP Address [DNS]` on any dns node. This will generate IP node.
11. You can find location of IP, by applying transform `To Location [city, country]`.
12. You can stack more transforms on different nodes at every layer.
13. Save the graph and You can reuse it in future.

Note: You can install plugins from maltego homepage to get more transforms.

# Maltego Versions
|         Community Edition        |        Classic/XL        |               Enterprise              |
|:--------------------------------:|:------------------------:|:-------------------------------------:|
| Limited Transforms               | All OSINT transforms     | On-Premise Deployments                |
| Maximum 12 results per transform | Access to commercial hub | Integration with own data             |
| Not for commercial use           | Commercial Use           | No rates or limits for own transforms |