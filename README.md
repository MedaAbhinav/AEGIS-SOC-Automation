# AEGIS – AI Driven SOC Automation

AEGIS is a Security Operations Center (SOC) automation project that integrates
Wazuh SIEM with automation workflows to detect, analyze, and respond to security alerts.

The platform simulates a real SOC pipeline by combining security monitoring,
automation workflows, AI-assisted alert analysis, threat intelligence enrichment,
and real-time incident notifications.

---

## Project Overview

AEGIS is an AI-assisted SOC automation system designed to simulate a modern Security Operations Center pipeline.  
It integrates Wazuh SIEM, automation workflows, threat intelligence enrichment, and real-time incident notification.

The platform demonstrates how security alerts can be automatically detected, analyzed, enriched, and delivered to security analysts without manual intervention.

---

## Architecture

![AEGIS SOC Architecture](architecture.jpeg)

### Architecture Flow

1. Attacker machine simulates malicious activity using Kali Linux or Windows attack tools.
2. The Windows 10 victim machine runs Sysmon and the Wazuh agent to collect detailed security logs.
3. Wazuh Manager (Ubuntu) acts as the SIEM detection engine and generates security alerts.
4. A custom webhook script forwards alerts from Wazuh to the automation pipeline.
5. n8n automation engine processes the alert and sends it for AI analysis.
6. AI analysis using Ollama TinyLlama evaluates the alert and determines threat context.
7. A decision engine determines whether threat intelligence enrichment is required.
8. If required, the system queries the VirusTotal API for reputation analysis.
9. The final SOC alert is sent automatically through a Telegram bot.

---

## Key Features

- Real-time security monitoring using Wazuh SIEM
- Automated alert processing with n8n workflows
- AI-assisted threat analysis using Ollama (TinyLlama)
- Threat intelligence enrichment using VirusTotal API
- Automated SOC alert notifications through Telegram bot

---

## Lab Environment

- Attacker Machine: Kali Linux
- Victim Machine: Windows 10 (Sysmon + Wazuh Agent)
- SIEM Server: Ubuntu (Wazuh Manager)
- Automation Engine: n8n
- AI Model: Ollama TinyLlama

---

## Technologies Used

- Wazuh SIEM
- Sysmon
- n8n Automation
- VirusTotal API
- Telegram Bot

---

## Workflow

1. Wazuh detects suspicious activity on monitored systems.
2. Alerts are forwarded through a webhook to an n8n automation workflow.
3. AI analyzes the alert and determines severity and threat context.
4. VirusTotal enrichment checks threat intelligence for malicious indicators.
5. A structured SOC alert is automatically delivered through a Telegram bot.

---

## Screenshots

### Wazuh Detection

![Wazuh Dashboard](wazuh-dashboard.png)

---

### Automation Workflow

![n8n Workflow](n8n-workflow.png)

---

### SOC Alert Notification

![Telegram Alert](telegram-alert.png)

---

## Project Objective

The goal of this project is to demonstrate how Security Operations Centers can
automate alert analysis and threat intelligence enrichment to reduce manual
investigation effort and improve incident response time.

---

## Future Improvements

- Add automated threat blocking
- Integrate additional threat intelligence sources
- Expand detection rules and monitoring coverage
