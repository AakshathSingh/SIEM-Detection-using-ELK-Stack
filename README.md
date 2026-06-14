# SIEM Detection using ELK Stack

## Description

This project demonstrates the implementation of a **Security Information and Event Management (SIEM)** solution using the **ELK Stack (Elasticsearch, Logstash, Kibana)** to detect and analyze real-world cyberattack scenarios. Custom correlation rules were developed to identify malicious activities such as **credential stuffing**, **PowerShell exploitation**, and **DNS tunneling**.

---

## Objectives

* Deploy the **ELK Stack** using Docker
* Ingest and analyze logs through Logstash pipelines
* Simulate real-world cyberattack scenarios
* Develop and test custom SIEM detection rules
* Validate attack detection through Kibana dashboards

---

## Tools & Technologies

* **Elasticsearch** – Data indexing and search
* **Logstash** – Log ingestion and processing
* **Kibana** – Data visualization and analysis
* **Docker & Docker Compose** – Containerized deployment
* **PowerShell** – Attack simulation
* **nslookup** – DNS tunneling simulation

---

## Architecture

1. Logs are generated from simulated attack scenarios
2. Logstash processes and forwards logs to Elasticsearch
3. Elasticsearch indexes and stores logs
4. Kibana visualizes events and detection alerts

---

## Setup

### 1. Deploy ELK Stack

Run the ELK Stack using Docker Compose:

```bash
docker-compose up -d
```

### 2. Configure Log Ingestion

* Configure Logstash pipelines
* Send logs to Elasticsearch
* Verify indexing in Kibana

### 3. Access Kibana

Open Kibana in the browser and analyze ingested logs.

---

## Attack Simulations & Detection

### 1. Credential Stuffing Attack

**Scenario:** Multiple failed login attempts using different usernames from the same IP address.

**Detection Logic:**

* Same source IP
* Multiple failed login attempts
* Different usernames within a short time window

**Outcome:** Attack successfully detected using log correlation.

---

### 2. PowerShell Exploitation

**Scenario:** Malicious PowerShell commands executed using encoded payloads.

**Detection Logic:**

* Detection of encoded commands
* Identification of the `-enc` flag

**Outcome:** Suspicious PowerShell activity flagged successfully.

---

### 3. DNS Tunneling

**Scenario:** Data exfiltration through unusual DNS queries.

**Detection Logic:**

* Long or random subdomain names
* Repeated DNS requests
* Unusual query patterns

**Outcome:** Potential DNS tunneling behavior detected.

---

## Detection Logic

Correlation rules were created based on:

* **Source IP Analysis**
* **Time Window Correlation**
* **Query Pattern Detection**
* **Command Signature Matching**

---

## Screenshots

### ELK Stack Dashboard

![Dashboard](screenshots/dashboard.png)

### Credential Stuffing Detection

![Credential Stuffing](screenshots/credential-stuffing.png)

### PowerShell Exploitation Detection

![PowerShell Detection](screenshots/powershell-detection.png)

### DNS Tunneling Detection

![DNS Tunneling](screenshots/dns-tunneling.png)

---

## Learning Outcomes

Through this project, I gained hands-on experience in:

* SIEM architecture and implementation
* Log ingestion pipelines
* Detection engineering and correlation rules
* Cyberattack simulation
* Security event analysis using Kibana

---

## Future Improvements

* Add more attack simulations
* Integrate threat intelligence feeds
* Automate alerting mechanisms
* Improve detection accuracy with advanced correlation rules
