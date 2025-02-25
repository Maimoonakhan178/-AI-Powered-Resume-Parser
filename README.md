# -AI-Powered-Resume-Parser
# Resume Ranking and Email Automation

This Python script automates the process of fetching resumes from an email inbox, ranking them using GPT-3, and sending personalized emails to candidates based on their ranking. The script is designed to handle PDF and Word documents, extract candidate information, and categorize resumes based on skills.

## Features

- **Email Fetching**: Connects to an IMAP server to fetch emails containing resumes.
- **Resume Parsing**: Extracts text from PDF and Word documents.
- **Candidate Information Extraction**: Extracts candidate names, emails, and phone numbers from resumes.
- **Resume Ranking**: Uses GPT-3 to rank resumes on a scale of 1 to 10.
- **Email Automation**: Sends personalized emails to candidates based on their resume ranking.
- **Data Logging**: Saves summary data of processed resumes to a JSON file.

## Prerequisites

Before running the script, ensure you have the following:

- Python 3.x installed.
- An OpenAI API key for GPT-3.
- Email credentials (IMAP and SMTP) for fetching and sending emails.

