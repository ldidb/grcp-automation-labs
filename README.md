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

## About
Built as part of a personal learning journey into GRC Engineering and Privacy 
Engineering, combining 15 years of GRC and privacy expertise with automation 
and modern tooling.
