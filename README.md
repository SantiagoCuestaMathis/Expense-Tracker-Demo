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
│  
├── Gmail Transaction Notifications  
├── Telegram Expense Entries  
│  
▼  

n8n Workflow Automation (Docker)  

▼  

Google Sheets Database  

▼  

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

## Project Structure

personal-finance-automation-demo/

dashboard/  
   index.html  

workflows/  
   expense-tracker.json  
   telegram-bot.json  

screenshots/  
   dashboard.png  
   workflow.png  

README.md  

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
Author

Santiago Cuesta
