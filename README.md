🕵️ Network Traffic Investigation using Wireshark
📘 Overview

This project documents a network investigation performed in a virtual environment. The task was to analyze suspicious outbound connections triggered after a user opened a phishing email attachment.

🧰 Tools Used

Wireshark – for packet capture and traffic analysis

VirusTotal – for verifying suspicious domains and files

Sandbox environment – for safe file extraction and inspection

🧩 Investigation Summary

A phishing email delivered a malicious attachment (documents.zip).

The infected endpoint initiated several outbound connections to suspicious domains:

attirenepal.com → 85.187.128.24

finejewels.com.au → 148.72.192.206

thietbiagt.com → 210.245.90.247

new.americold.com → 140.72.53.144

VirusTotal confirmed these URLs/IPs as malicious.

The malicious webserver used LiteSpeed / PHP 7.2.34.

SSL details (GoDaddy certificate) indicated potentially spoofed legitimate services.

🚨 Actions & Recommendations

Block all identified malicious IP addresses.

Escalate the XLS payload for malware analysis.

Review outbound traffic logs for further IOCs.

Implement email filtering and user awareness training.

📄 Outcome

The alert was confirmed as a true positive.
The analysis demonstrated the use of Wireshark for packet inspection, correlation with external threat intelligence, and SOC-style reporting.
