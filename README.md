# SIEM-Detection-using-ELK-Stack

# Description
This project focuses on building and testing custom SIEM correlation rules using the ELK Stack to detect real-world cyberattacks such as credential stuffing, DNS tunneling, and PowerShell exploitation.

# Objectives
- Deploy ELK Stack using Docker  
- Ingest and analyze logs  
- Simulate attack scenarios  
- Develop detection rules  
- Validate attack detection  

# Tools & Technologies
- Elasticsearch  
- Logstash  
- Kibana  
- Docker & Docker Compose  
- PowerShell  
- nslookup  

# Setup
- ELK Stack deployed via Docker  
- Logs ingested using Logstash pipelines  
- Data visualized in Kibana  

# Attack Simulations & Detection

# 1. Credential Stuffing
- Multiple failed logins from same IP  
- Different usernames used  
- Detected using log correlation  

# 2. PowerShell Exploitation
- Encoded command execution detected  
- Usage of `-enc` flag identified  

# 3. DNS Tunneling
- Long/random subdomain queries detected  
- Repeated DNS requests flagged  

#  Detection Logic
- Correlation based on:
  - Source IP  
  - Time window  
  - Query patterns  
  - Command signatures  

#  Learning Outcomes
- SIEM architecture  
- Log ingestion pipelines  
- Detection engineering  
- Attack simulation  
- Kibana analysis  
