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

Script Execution:
The script will connect to the specified IMAP server and fetch emails containing resumes.
It will parse the resumes, extract candidate information, and rank them using GPT-3.
Based on the ranking, the script will send personalized emails to candidates.
A summary of processed resumes will be saved to resume_data.json.
Configuration
Email Credentials: Update the EMAIL and PASSWORD variables in the script or .env file.
IMAP Server: Modify the IMAP_SERVER and IMAP_PORT variables if using a different email provider.
Search Keywords: Adjust the SEARCH_KEYWORDS list to match the subject lines of emails containing resumes.
Skills List: Update the SKILLS list to include relevant skills for your use case.
GPT-3 Model: Change the model parameter in the rank_resumes_with_gpt3 function if using a different GPT-3 model.
Dependencies
This script requires the following Python libraries:

imaplib: For connecting to the IMAP server.
email: For parsing email messages.
PyPDF2: For extracting text from PDF files.
python-docx: For extracting text from Word documents.
spacy: For natural language processing (NER).
nltk: For stopwords removal.
openai: For interacting with the GPT-3 API.
joblib: For loading the trained model and vectorizer.
smtplib: For sending emails.
Example Output
--------------------------------------------------
Candidate 1
Email: candidate1@example.com
Resume Category (Predicted Skills): Data Science
Ranking Text: This resume is well-structured and highlights relevant experience. Overall Ranking: 8
Ranking: 8
Email sent successfully to candidate1@example.com
--------------------------------------------------
Candidate 2
Email: candidate2@example.com
Resume Category (Predicted Skills): Software Engineering
Ranking Text: The resume lacks detail in key areas. Overall Ranking: 5
Ranking: 5
Email sent successfully to candidate2@example.com


Summary Data
The script saves a summary of processed resumes to resume_data.json:

{
    "Total resumes processed": 10,
    "Resumes progressed": 8,
    "High-ranked resumes": 5,
    "Low-ranked resumes": 3
}
