---
title: Nikto
layout: default
---

# Nikto
It is a free and open source web server and web application assessment tool. The primary function of nikto is to identify security weaknesses such as default files, misconfigurations, or published security vulnerabilities.

Detailed information [here](https://github.com/sullo/nikto).

Nikto can integrate well with other tools like:
- Metasploit
- Nmap
- Nessus
- OpenVAS

# Techniques covered
- Technical Weakness Identification
    - T1293 Analyze application security posture
    - T1288 Analyze architecture and configuration posture

{: .warning }
Do not use against target you do not own, or have explicit permission from.
Nikto sends **1000's** of requests to target and then indexes the responses to identify problems.

# Basic Usage
You can download of copy of sample vulnerable app from [here](https://www.vulnerablewebapps.org/). Run this vulnerable app inside sandbox to test stuff out.

```shell
# These scans can take some time
# Press space to check status
nikto -host https://www.vulnerablewebapps.org/
# a txt file with targets can also be used
echo "<host1>" > niktotargets.txt
echo "<host2>" >> niktotargets.txt
nikto -host niktotargets.txt
# list plugins
nikto -list-plugins
# Example for passive robots file scan
nikto -Plugins "robots(nocheck)" -host <host>
# Example for active robots file scan
nikto -Plugins robots -host <host>
# save positive findings to current directory
nikto -host <host> -Save .
# replay saved request
replay.pl <saved-txt-file>
```

## Using nikto with proxy while authenticated
1. Open BurpSuite
2. Open BurpSuite project
3. Go to proxy tab, turn intercept off
4. Check proxy listener address in options tab
5. Run nikto scan through proxy
```shell
nikto -host <host> -useproxy <burp-proxy-address> -nossl
```
6. All requests will get proxied through burp suite
7. If you are using same config everytime, update /etc/nikto.conf
8. You can also set cookies to use with nikto
9. The output can also be saved using `-Format htm -output report.html`
10. Template for saving reports can be edited from `/var/lib/nikto/templates/*.tmpl`

{: .warning }
**Note:** You are not permitted to remove copyright statement from these templates.