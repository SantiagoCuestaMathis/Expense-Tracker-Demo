# Personal Finance Automation System — Demo

A local-first automation system that consolidates financial transactions from multiple sources into a single operational dashboard.

Built using workflow automation and API integrations, this system demonstrates practical implementation of event-driven data pipelines, responsible handling of sensitive information, and lightweight deployment using free-tier infrastructure.

This repository contains a demonstration version of the system using anonymized sample data.

---

## Executive Summary

Managing expenses across multiple financial accounts often results in fragmented visibility into spending and cash flow. Transactions are distributed across emails, payment platforms, and messaging systems, creating operational friction and increasing the risk of manual errors.

This system addresses that problem by automating transaction ingestion, standardizing data processing, and presenting consolidated financial insights through a responsive web dashboard.

The project demonstrates the ability to design and implement production-style automation workflows using accessible tools while maintaining responsible data handling practices.

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
- Standardizes and stores transaction data in a structured database
- Aggregates financial metrics automatically
- Presents actionable insights through a mobile-friendly dashboard

The design prioritizes reliability, simplicity, and responsible handling of sensitive data.

---

## System Architecture

User Inputs  
├── Gmail Transaction Notifications  
└── Telegram Expense Entries  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;│  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;▼  
n8n Workflow Automation (Docker)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;│  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;▼  
Google Sheets Database  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;│  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;▼  
Web Dashboard (Netlify)

---

## Core Capabilities

### Automation

- Automated expense ingestion from email notifications
- Manual expense logging via Telegram bot
- Structured data normalization
- Event-driven workflow execution

### Analytics and Reporting

- Monthly income and expense tracking
- Savings and balance monitoring
- Category-level spending analysis
- Budget tracking and variance visibility

### User Experience

- Mobile-responsive interface
- Real-time dashboard updates
- Search and filtering capabilities
- Light and dark mode support

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

### Presentation Layer

- HTML
- CSS
- JavaScript

### Deployment

- Netlify

---

## Deployment Model

The system is designed using a local-first architecture.

Key characteristics:

- Automation workflows run locally
- Data remains under user control
- Infrastructure operates without paid cloud services
- System availability depends on local runtime

This deployment model demonstrates a practical balance between accessibility and responsible data governance.

---

## Responsible Data Handling

Financial information is inherently sensitive. This system was intentionally designed to minimize unnecessary exposure of personal financial data.

Design principles applied:

- Local execution of automation workflows
- Controlled external integrations
- Minimal data persistence outside the user environment
- Separation between production data and demonstration environments

All data included in this repository is anonymized and used solely for demonstration purposes.

---

## Demonstration Scope

The dashboard displays:

- Monthly income
- Monthly expenses
- Savings performance
- Remaining balance
- Category spending distribution
- Transaction history
- Budget tracking indicators

The demonstration environment uses simulated data and does not connect to live financial systems.

---

## How to Run This Demo

This repository includes a public demonstration version of the system. You can either view the deployed dashboard directly or reproduce the automation workflow locally using your own credentials.

### Option 1 — View the Live Demo

Open the live dashboard:

`https://expense-tracker-demo-data.netlify.app`

No installation is required.

This option is intended for quickly reviewing the interface, reporting logic, and overall system design using anonymized data.

### Option 2 — Run the Workflow Locally

This option reproduces the event-driven automation pipeline locally.

#### Prerequisites

- Docker installed
- n8n available locally
- A Google account for Google Sheets integration
- A Telegram account and bot token if you want to test the Telegram workflow
- A Gmail account if you want to test the email workflow
- An Anthropic API key if you want to use the AI extraction nodes

#### Step 1 — Start n8n

Run the following command:

    docker run -it --rm \
    -p 5678:5678 \
    -v ~/.n8n:/home/node/.n8n \
    n8nio/n8n

Then open:

`http://localhost:5678`

#### Step 2 — Import the Workflows

Inside n8n:

1. Click **Import**
2. Select the workflow files in the `workflows/` folder

Included workflow files:

- `expense-tracker-demo.json`
- `telegram-expense-bot-demo.json`

#### Step 3 — Configure Credentials

Create and assign your own credentials for the services you want to test:

- Gmail
- Telegram
- Google Sheets
- Anthropic

Important:

This repository does **not** include credentials. To run the workflows locally, each user must connect their own accounts and services.

#### Step 4 — Activate the Workflows

After credentials are configured, activate the relevant workflows inside n8n.

The system will then begin processing incoming events according to the selected workflow.

#### Step 5 — View the Dashboard

You can view the dashboard in either of two ways:

- Open the deployed version at `https://expense-tracker-demo-data.netlify.app`
- Open the local dashboard HTML file if you are running it locally

Depending on your setup, you may use the included HTML dashboard file directly or deploy your own copy to Netlify.

---

## Architecture Overview

The system follows a simple event-driven pipeline:

User Event  
├── Gmail Notification  
└── Telegram Message  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;│  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;▼  
n8n Workflow Automation  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;│  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;▼  
Data Processing  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;│  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;▼  
Google Sheets Database  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;│  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;▼  
Web Dashboard

---

## Layered Architecture

### Input Layer

- Gmail Notification
- Telegram Message

### Processing Layer

- n8n Workflow Engine
- Event Detection
- Data Extraction
- Data Normalization
- Validation

### Storage Layer

- Google Sheets Database

### Presentation Layer

- Web Dashboard
- Netlify Deployment

---

## Project Structure

    personal-finance-automation-demo/
    ├── dashboard/
    │   └── index.html
    ├── workflows/
    │   ├── expense-tracker-demo.json
    │   └── telegram-expense-bot-demo.json
    ├── screenshots/
    │   ├── dashboard.png
    │   └── workflow.png
    ├── .env.example
    ├── .gitignore
    ├── LICENSE
    └── README.md

---

## Workflow Logic

1. A financial transaction notification is received
2. The automation workflow detects the event
3. Transaction data is extracted and standardized
4. Data is appended to the centralized database
5. Aggregated metrics are recalculated
6. The dashboard updates to reflect current financial status

This workflow demonstrates a practical implementation of event-driven automation using low-cost infrastructure.

---

## Demonstrated Skills

### Automation Engineering

- Workflow design and orchestration
- Event-driven processing
- API integration

### Data Engineering

- Structured data normalization
- Automated aggregation logic
- Lightweight database management

### System Design

- Modular architecture
- Local-first deployment strategy
- Responsible data handling

### Software Delivery

- Front-end dashboard development
- Deployment configuration
- Operational reliability

---

## System Design Characteristics

- Event-driven architecture
- Local-first execution model
- Stateless workflow processing
- Lightweight storage layer
- Serverless dashboard hosting
- Free-tier infrastructure compatibility

---

## Future Enhancements

Planned improvements include:

- Automated budget alerts
- Recurring expense detection
- Predictive spending analysis
- Multi-currency support
- Automated reporting exports
- Notification-based financial insights

---

## License

MIT License

---

## Author

Santiago Cuesta
