 **AI-Powered Job Recommendation Automation System (using n8n)** 
**
## **📖 Project Overview**

This project automates the process of **fetching job postings, scoring them, generating personalized cover letters, and notifying users** with top job recommendations via email.
It integrates **n8n**, **Google Gemini API**, **Google Sheets**, and **Email services** into one seamless workflow.

---

## **📌 Features**

* 🔎 **Job Fetching** – Automatically retrieves job listings from external sources (e.g., LinkedIn, RSS feeds).
* 📊 **Job Scoring** – Uses AI to evaluate job relevance and assign a score.
* 📝 **Cover Letter Generation** – Generates a personalized cover letter for each job using Google Gemini.
* 📑 **Profile Extraction** – Extracts candidate details from uploaded resumes.
* 📈 **Google Sheets Integration** – Stores job recommendations (Title, Link, Location, Score, Job Description, Benefits, Cover Letter).
* 📧 **Email Notifications** – Sends top job recommendations (sorted by score) via email.
* 🔄 **Workflow Automation** – Entire pipeline powered by **n8n**.

---

## **📂 Repository Structure**

```
job-recommendation-automation/
│── n8n_workflow/
│   └── n8n_job_auto.json       # Exported n8n workflow
│
│── assets/
│   ├── google_sheet_sample.png # Sample Google Sheet output
│   ├── email_sample.png        # Example of email notification
│   ├── workflow_diagram.png    # Workflow diagram
│
│── README.md                   # Documentation
```

---

## **🚀 Setup & Installation**

### **1. Clone the Repository**

```bash
git clone https://github.com/Tejeswarreddy2000/job-recommendation-automation.git
cd job-recommendation-automation
```

### **2. Import Workflow**

* Import `n8n_workflow/n8n_job_auto.json` into your **n8n** instance.

### **3. Configure Credentials**

* **Google Sheets API**
* **Gmail / SMTP**
* **Gemini API Key** (stored in `.env` or n8n Credentials Manager)

---

## **▶️ How to Run**

1. Run **n8n** and load the workflow.
2. Add job sources (**RSS, APIs, or custom fetchers**).
3. The workflow will:

   ```
   Fetch jobs → Score jobs → Generate cover letters → Store in Google Sheets → Email Top 5 results
   ```

---

## **📸 Screenshots**

* **Google Sheets Output**
  *(Insert `google_sheet_sample.png`)*

* **Email with Top 5 Recommendations**
  *(Insert `email_sample.png`)*

---

## **⚡ Challenges & Solutions**

* **API Rate Limits** → Batched jobs (groups of 5), reduced request frequency, switched to higher RPM models.
* **Parsing Nested JSON** → Custom JavaScript functions to flatten Gemini output.
* **Email Formatting** → Designed raw text & HTML templates for structured readability.
* **Scoring Consistency** → Normalized scoring logic for fair ranking.
* **Cover Letter Quality** → Tailored generation per job role and candidate resume.

---

## **📚 Learnings**

* Hands-on experience with **n8n workflow automation**.
* Integrated **AI (Gemini)** for practical job search applications.
* Learned **workflow orchestration** with APIs, Sheets, and Email.
* Improved **prompt engineering** for structured outputs.
* Applied **data parsing, cleaning, and batching strategies** in automation pipelines.

