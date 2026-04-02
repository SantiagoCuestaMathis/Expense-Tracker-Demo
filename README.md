# Personal Finance Automation System — Demo

A local-first automation system that consolidates financial transactions from multiple sources into a single operational dashboard.

Built using workflow automation and API integrations, this project demonstrates practical implementation of event-driven data pipelines, structured financial data processing, and lightweight deployment using accessible infrastructure.

This repository contains a demonstration version of the system using anonymized workflows, generic templates, and visual demo assets.

---

## Executive Summary

Managing expenses across multiple financial accounts often results in fragmented visibility into spending and cash flow. Transactions are distributed across emails, payment platforms, and messaging systems, creating operational friction and increasing the risk of manual errors.

This system addresses that problem by automating transaction ingestion, standardizing data processing, and presenting consolidated financial insights through a responsive dashboard.

The project demonstrates the ability to design and implement production-style automation workflows using low-cost tools while maintaining responsible handling of sensitive information.

---

## Problem Statement

Individuals managing multiple financial accounts face three recurring operational challenges:

- Fragmented financial data across platforms
- Manual reconciliation of transactions
- Limited real-time visibility into spending

These issues create inefficiencies in financial tracking and increase the likelihood of incomplete or inaccurate records.

---

## Solution

This system implements an automated workflow architecture that:

- Captures transaction notifications from email and messaging platforms
- Standardizes and stores transaction data in a structured format
- Aggregates financial metrics automatically
- Presents actionable insights through a mobile-friendly dashboard

The design prioritizes reliability, simplicity, and responsible handling of sensitive data.

---

## System Architecture

Input sources feed into workflow automation, which processes and stores structured transaction data for dashboard visualization.

- Gmail transaction notifications
- Telegram expense entries
- n8n workflow automation
- Google Sheets data layer
- Web dashboard interface

---

## Core Capabilities

### Automation

- Automated expense ingestion from email notifications
- Manual expense logging via Telegram bot
- Structured transaction normalization
- Event-driven workflow execution

### Analytics and Reporting

- Monthly income and expense tracking
- Savings and balance monitoring
- Category-level spending analysis
- Budget tracking and variance visibility

### User Experience

- Mobile-responsive interface
- Search and filtering capabilities
- Summary dashboard views
- Multi-tab navigation for overview, budgets, and transactions

---

## Technology Stack

### Automation Layer

- n8n
- Docker
- ngrok

### Integration Layer

- Gmail API
- Telegram Bot API
- Google Sheets API
- Anthropic API

### Front End

- HTML
- CSS
- JavaScript

### Hosting

- Netlify for demo deployment when needed

---

## Deployment Model

The system is designed using a local-first architecture.

Key characteristics:

- Automation workflows run locally
- Data remains under user control
- Credentials are user-provided and not stored in this repository
- Infrastructure can be demonstrated without maintaining a permanent live deployment

This approach provides a practical balance between accessibility, reproducibility, and responsible data governance.

---

## Responsible Data Handling

Financial information is inherently sensitive. This project was intentionally structured to minimize unnecessary exposure of personal financial data.

Design principles applied:

- Local execution of automation workflows
- Controlled external integrations
- Separation between private usage and public demonstration assets
- No private credentials included in the repository
- Public-facing assets use anonymized or generic demo representations

All data and workflow exports included here are intended solely for demonstration purposes.

---

## Demo Assets

This repository is designed to be reviewed through its code, workflow exports, README, and visual demo assets.

Recommended review path:

1. Read this README for architecture and implementation context
2. Review the workflow files in the `workflows/` folder
3. Open the dashboard HTML template
4. View screenshots or screen recordings associated with the project

A live deployment may not always be active. The project is intended to demonstrate implementation quality, workflow design, and reproducibility rather than serve as a permanent public production system.

---

## How to Reproduce Locally

This repository includes generic templates and exported workflows. To run the system locally, a user must connect their own credentials.

### Requirements

- Docker
- n8n
- Google account
- Telegram account and bot setup if using the Telegram workflow
- Anthropic API key if using AI extraction nodes

### Local Setup Overview

1. Start n8n locally
2. Import the workflow files from the `workflows/` folder
3. Create and attach your own credentials for Gmail, Telegram, Google Sheets, and Anthropic where applicable
4. Configure the dashboard template for your own environment if needed
5. Activate the workflows locally

This repository does not include any private credentials, access tokens, or production data connections.

---

## Project Structure

    Expense-Tracker-Demo/
    ├── workflows/
    │   ├── expense-tracker-demo.json
    │   └── telegram-expense-bot-demo.json
    ├── .env.example
    ├── .gitignore
    ├── LICENSE
    ├── README.md
    └── my-finance-demo.html

If screenshots or recordings are added later, they can be organized in optional folders such as:

    screenshots/
    media/

---

## Workflow Logic

1. A financial transaction event is received through email or Telegram
2. The workflow detects and parses the input
3. Transaction data is extracted and normalized
4. Structured data is appended to the storage layer
5. Aggregated financial views are refreshed
6. The dashboard reflects the updated financial state

This demonstrates a practical implementation of event-driven automation using lightweight infrastructure.

---

## Demonstrated Skills

### Automation Engineering

- Workflow design and orchestration
- Event-driven processing
- API integration
- Multi-step automation logic

### Data Engineering

- Structured data normalization
- Automated aggregation logic
- Lightweight storage architecture

### System Design

- Modular architecture
- Local-first deployment strategy
- Separation between private and public environments
- Responsible handling of sensitive data

### Front-End Delivery

- Dashboard interface design
- Responsive layout implementation
- Data presentation and filtering logic

---

## Future Enhancements

Potential future improvements include:

- Automated budget alerts
- Recurring expense detection
- Predictive spending analysis
- Multi-currency support
- Exportable reports
- More advanced portfolio and investment tracking

---

## License

MIT License

---

## Author

Santiago Cuesta
