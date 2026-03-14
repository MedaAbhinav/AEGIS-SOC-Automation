# AEGIS – AI Driven SOC Automation

AEGIS is a Security Operations Center (SOC) automation project that integrates
Wazuh SIEM with automation workflows to detect, analyze, and respond to security alerts.

The platform simulates a real SOC pipeline by combining security monitoring,
automation workflows, AI-assisted alert analysis, threat intelligence enrichment,
and real-time incident notifications.

---

## Architecture

![Architecture Diagram](architecture/architecture.png)

Wazuh SIEM → Webhook → n8n Automation → AI Analysis → VirusTotal → Telegram Alerts

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

![Wazuh Dashboard](screenshots/wazuh-dashboard.png)

---

### Automation Workflow

![n8n Workflow](screenshots/n8n-workflow.png)

---

### SOC Alert Notification

![Telegram Alert](screenshots/telegram-soc-alert.png)

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
