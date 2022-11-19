---
title: Introduction
layout: default
nav_order: 1
---

# NIST Cybersecurity Framework
![NIST Cybersecurity Framework](/assets/images/nist-framework.png)

# Pen-testing
- Tests all applications and services
- Test against all things looking for any exploit
- Provide a report but don't generally interact

# Red Team Operation
- Emulates known adversary group behavior
- Replicate techniques over full attack lifecycle
- Provide actionable results for detection

# Kill Chain
- Recon
- Exploit
- Escalate
- Lateral Movement
- Evade
- Action

# Kill chain phases relevant for different Roles
- **Pen-tester** - Recon + Exploit
- **Next Gen Pen-tester** - Recon + Exploit + Escalate + Lateral Movement(optionally)
- **Red Team** - Recon + Exploit + Escalate + Lateral Movement + Evade + Action

# MITRE ATT&CK
It is a globally accessible knowledge base of adversary tactics and techniques based
on real-world observations.

**Tactics** are what attackers are trying to achieve.
**Techniques** are how they accomplish those steps or goals.

**MITRE ATT&CK** defines following matrices:
- **Enterprise**
    - PRE
    - Windows
    - macOS
    - Linux
    - Cloud
    - Network
    - Containers
- **Mobile**
    - Android
    - iOS
- **Industrial Control Systems(ICS)**

Every matrice contains Tactics which contain a list of Techniques.
A technique may further include sub-techniques, depending on complexity.

[MITRE ATT&CK Navigator](https://mitre-attack.github.io/attack-navigator/) is a web-based tool for annotating and exploring [ATT&CK matrices](https://attack.mitre.org/).