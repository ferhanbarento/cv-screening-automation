# AI-Powered CV Screening Automation

An end-to-end automation that screens job application resumes automatically using UiPath, Claude AI, and Google Sheets.

## The Problem

HR managers and hiring teams receive dozens of resumes by email and spend hours manually reading, scoring, and logging candidate information into spreadsheets. This process is slow, inconsistent, and error-prone.

## The Solution

This automation watches a Gmail inbox for incoming resumes, reads each PDF with AI, extracts and scores the candidate, logs the result to Google Sheets, and alerts the hiring manager when a candidate needs manual review — all without any human intervention.

## Workflow Diagram

Email arrives with PDF → UiPath detects it → PDF text extracted → Claude AI reads and scores → Google Sheets row added → Low score triggers HR alert email

## How It Works

1. **Input:** A candidate emails their resume (PDF) to a dedicated Gmail inbox
2. **AI Processing:** Claude AI (Anthropic) reads the resume and extracts structured data
3. **Output:** A new row is added to Google Sheets with all candidate details
4. **Quality Control:** Candidates scoring below 5/10 trigger an automatic alert email to the hiring manager

## AI Prompt

Claude AI is given a custom prompt that instructs it to return a structured JSON object containing:
- Candidate name, email, and phone
- Years of experience
- Top 3 skills
- Fit score (1–10)
- One-sentence reason for the score
- Flag for review (true/false)

## Tools Used

| Tool | Purpose |
|------|---------|
| UiPath Studio Web | Automation platform and workflow orchestration |
| UiPath Orchestrator | Monitoring, logging, and audit trail |
| Gmail (Google Workspace) | Email trigger and notification sender |
| Claude AI (Anthropic API) | Resume reading, extraction, and scoring |
| Google Sheets | Structured candidate database |

## Project Requirements Met

| Requirement | Implementation |
|-------------|---------------|
| Takes in data | Resume PDF received via Gmail |
| Processes with AI | Claude AI extracts and scores the resume |
| Outputs structured results | Google Sheets row added automatically |
| Quality control | Fit score check + HR alert email + Try Catch error handling |

## Google Sheets Output Structure

| Column | Data |
|--------|------|
| Timestamp | Date and time processed |
| Candidate Name | Extracted by AI |
| Email | Extracted by AI |
| Phone | Extracted by AI |
| Years Experience | Extracted by AI |
| Top Skills | Extracted by AI |
| Fit Score | AI score 1-10 |
| Score Reason | AI explanation |
| Flag for Review | TRUE/FALSE |
| Status | Pending / Reviewed |

## Business Value

- Eliminates hours of manual resume reading per hiring round
- Creates a consistent, bias-reduced screening process
- Provides a full audit trail of every candidate processed
- Only surfaces candidates needing human judgment to the hiring manager

## Screenshots

*Add screenshots of your workflow, Google Sheets output, and email notifications here*

## Author

Ferhan Barento
