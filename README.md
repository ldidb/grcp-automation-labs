# GRC & Privacy Automation Labs

A collection of automation workflows built with n8n, demonstrating real-world 
privacy engineering and GRC automation use cases.

## Workflows

### 1. DSAR Automation Workflow
Simulates an enterprise DSAR intake pipeline triggered by a webhook 
(e.g. from DataGrail), routing requests by type and automating logging and notifications.

**Features:**
- Webhook trigger simulating DataGrail integration
- Switch node routing for all 6 GDPR data subject rights
- Automatic logging to Google Sheets DSAR tracker
- Automated confirmation email to requestor
- 23-day deadline reminder with automatic Google Sheets status update
- Fallback alert for unrecognized request types ensuring no request is ever lost

**GDPR Rights Covered:**
- Right to Deletion (Article 17)
- Right of Access (Article 15)
- Right to Correction (Article 16)
- Right to Portability (Article 20)
- Right to Restriction (Article 18)
- Right to Object (Article 21)

## Tech Stack
- n8n (self-hosted via Docker)
- Google Sheets API
- Gmail API
- Webhooks




### 2. DPIA Intake & Automated Risk Scoring
Automates the privacy review process for new product features, automatically 
scoring risk and routing based on severity.

**Features:**
* n8n Form trigger simulating a Jira/product intake integration
* Python-based risk scoring algorithm weighing GDPR risk factors
* Switch node routing for High, Medium, and Low risk outcomes
* Automatic logging to Google Sheets DPIA Risk Register
* Urgent email alerts for High risk features requiring full DPIA
* Standard PIA notifications for Medium risk features
* Parallel execution of logging and notifications

**Risk Scoring Logic:**
* Special category data (Health, Biometric, Financial, Children's) = +20 pts each
* Location data = +15 pts
* Personal data collection = +10 pts
* Third party data sharing = +20 pts
* High Risk = 40+ pts (DPIA Required)
* Medium Risk = 20-39 pts (PIA Required)
* Low Risk = under 20 pts (No review needed)

## About
Built as part of a personal learning journey into GRC Engineering and Privacy 
Engineering, combining 15 years of GRC and privacy expertise with automation 
and modern tooling.
