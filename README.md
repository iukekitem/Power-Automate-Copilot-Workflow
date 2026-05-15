# 📧 AI-Powered Email Question Analyzer (Power Automate + Copilot)

## 🚀 Overview
This project demonstrates an automated workflow built using **Microsoft Power Automate and M365 Copilot** to enhance productivity and knowledge management.

The workflow monitors incoming emails, automatically detects questions, researches answers using Copilot, and delivers structured insights via Outlook and Microsoft Teams.

This solution is designed to reduce manual effort, improve response quality, and create a personal knowledge assistant for professional use.

---

## ⚙️ Workflow Architecture

### 1. Trigger – New Email Detection
- **Service:** Office 365 Outlook  
- **Action:** When a new email arrives in the Inbox  
- Automatically initiates the workflow upon receiving new emails.

---

### 2. AI Processing – Question Detection & Research
- **Service:** M365 Copilot  

**What it does:**
- Analyzes the email content
- Detects questions directed to the user
- Performs research using available knowledge sources
- Generates structured outputs including:
  - List of detected questions
  - Detailed answers for each question
  - References and links (when applicable)
  - Diagrams (if relevant)
  - Summary of each answer

**Additional metadata captured:**
- Sender name and email  
- Original email content  
- User timezone context

---

### 3. Output Delivery – Email (HTML Format)
- **Service:** Office 365 Outlook  

**Behavior:**
- Sends a structured **HTML email to self**
- Includes:
  - All detected questions
  - Detailed answers with references
  - Original email content
- Designed for readability and professional formatting

⚠️ Note:  
This workflow does **NOT reply to the original sender** to maintain independence and avoid unintended communication.

---

### 4. Notification – Microsoft Teams Summary
- **Service:** Microsoft Teams  

**What it sends:**
- A summary message via "Chat with Flow bot"
- Includes:
  - Sender information
  - List of detected questions
  - Brief summary of each answer

---

## 🧠 Key Features

- ✅ Automated question detection from emails  
- ✅ AI-powered research and response generation  
- ✅ Structured knowledge output (email + Teams)  
- ✅ Professional formatting (HTML email responses)  
- ✅ Maintains compliance boundaries (no auto-reply to sender)  
- ✅ Centralized personal knowledge tracking  

---

## 🏗️ Use Cases

- Compliance engineering (regulatory questions analysis)  
- Technical support workflows  
- Knowledge management and documentation  
- Email triage and prioritization  
- Personal AI assistant for research tasks  

---

## 🧩 Tech Stack

- Microsoft Power Automate  
- Microsoft 365 Copilot  
- Office 365 Outlook  
- Microsoft Teams  

---

## 📊 Workflow Summary

```text
New Email → AI Analysis (Copilot)
          → Detect Questions
          → Research & Generate Answers
          → Send HTML Email to Self
          → Send Teams Summary
