# AcmeFlow – Automated Lead Capture & Qualification

## Project Overview
AcmeFlow is a fictional B2B SaaS company. This project automates its inbound demo-request lead management process using n8n.

When a prospect submits a demo request, the workflow validates the submitted information, calculates a lead score, determines qualification status, and routes the lead for Sales follow-up or Marketing nurture.

<img width="959" height="412" alt="acmeflow-lead-capture-workflow" src="https://github.com/user-attachments/assets/5e79c37b-acde-418c-bece-dac528e5d6f0" />


## Technology Stack
- **Frontend:** HTML, CSS, JavaScript
- **Automation:** n8n
- **Data Handling:** JSON, CSV
- **Version Control:** Git and GitHub

## Workflow Architecture

1. **Lead Capture:** Receives prospect submissions through an n8n webhook.
2. **Lead Validation:** Checks mandatory fields, email format, and optional company website.
3. **Lead Scoring:** Assigns points based on company size, job seniority, industry, product interest, and email format.
4. **Lead Qualification:** Classifies leads as Qualified or Not Qualified using a score threshold of 60.
5. **Lead Routing:**
   - Qualified leads → Sales Follow-up
   - Not Qualified leads → Marketing Nurture
6. **CSV Output:** Converts not-qualified lead data into CSV output for review.

## Lead Scoring Criteria

| Criteria | Score |
|---|---:|
| Company size: 201–500 | +20 |
| Company size: 501–1000 | +25 |
| Company size: 1000+ | +30 |
| Senior decision-maker | +25 |
| SaaS / Technology industry | +15 |
| Marketing / Sales Automation interest | +15 |
| Valid email format | +15 |

**Qualification threshold:** 60 points.

## Project Structure

```text
Project-01-Lead-Capture/
├── frontend/
│   └── index.html
├── workflows/
│   └── acmeflow-lead-capture.json
├── screenshots/
└── README.md
```

## Setup Instructions

1. Run n8n locally.
2. Import `workflows/acmeflow-lead-capture.json` into n8n.
3. Open the workflow and activate or test it using the webhook's test URL.
4. Open `frontend/index.html` using a local development server such as VS Code Live Server.
5. Submit a demo request and inspect the workflow execution.

## Project Objective
Demonstrate practical GTM Engineering concepts through lead capture, data validation, rule-based lead scoring, qualification, and automated lead routing.

*Note: AcmeFlow is a fictional company created for this portfolio project.*
