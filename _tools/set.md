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

## Example: Spearphishing
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

## Example: Credential Harvesting
1. Website Attack Vectors
2. Credential Harvester Attack Method
3. Site Cloner
4. IP address for the POST back in Harvester/Tabnabbing: Listening server external IP
5. Enter the url to clone: <some-login-page>
6. Target enters username and password, fake website redirects to original site
7. We can see username and password in listener program

## Example: Creating Infectious Media
1. Infectious Media Generator
2. File-Format Exploits
3. Adobe PDF Embedded EXE Social Engineering
4. Use built-in BLANK PDF for attack
5. Windows Meterpreter Reverse_TCP(x64)
6. IP address or URL for the payload listener
7. Port for payload listener
8. You can start the listener
9. Copy payload and share with target

## Example: QR Code Attack
1. QRCode Generator Attack Vector
2. Enter the URL you want the QRCode to go to: <malicious-url>
3. Share QRCode with target

## Example: Google Analytics Attack
1. Third Party Modules
2. Google Analytics Attack by @ZonkSec
3. Choose mode (automatic/manual): manual
4. Enter TrackingID (tid)(UA-XXXXX): <tracking-id>
5. Enter target host (dh): <target-url>
6. Enter target page (dp): <target-page>
7. Enter target page title (dt): <target-page-title>)
8. Enter referal page to spoof (dr): <target-referal-page/fake-site>
9. Print Payload
10. Send Payload (on loop)
11. Seconds between payload send: 1
12. This will show our fake-site as top referrals in google analytics dashboard for target
13. The target will click to check what the site is about
14. This redirects to fake site that can spoof target data