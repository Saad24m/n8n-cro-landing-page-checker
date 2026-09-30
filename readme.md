# CRO & Landing Page Checker AI Agent n8n Workflow

An advanced multi-agent n8n workflow that automates conversion rate optimization (CRO) audits by analyzing both the visual user experience and copywriting performance of any landing page, compiling everything into a structured Google Doc report, and emailing it automatically[cite: 5].

---

## 🚀 What This Workflow Does

1. **Form Trigger (`On form submission`):** Collects the target Landing Page URL from a user submission form[cite: 5].
2. **Web Scraping (`Get LP Screenshot (Fixed)`):** Uses Firecrawl to scrape the page's markdown content and capture a high-resolution visual screenshot[cite: 5].
3. **Dual AI Analysis (`AI Agent` & `Analyze image`):**
   - **Visual CRO Analyst:** Evaluates layout, visual hierarchy, CTA placement, trust badges, and mobile responsiveness[cite: 5].
   - **Copywriting Strategist:** Analyzes headlines, value propositions, objection handling, and copy clarity[cite: 5].
4. **Report Consolidation (`AI Agent1` & `Merge`):** Merges both specialist reports, eliminating duplication and ranking issues by business impact[cite: 5].
5. **Document Generation & Archiving:** Automatically creates a Google Doc report, converts and archives a PDF copy in Google Drive, and sends the final report link straight to your inbox via Gmail[cite: 5].

---

## 🛠️ Prerequisites & Credentials

To run this workflow successfully, you will need to set up and configure the following credentials/APIs in your n8n instance:

* **OpenAI API** (For the multi-agent LLM analysis nodes)[cite: 5]
* **Firecrawl API** (For scraping landing page markdown and screenshots)[cite: 5]
* **Google Drive OAuth2 API** (For creating documents, converting to PDF, and organizing files)[cite: 5]
* **Gmail OAuth2 API** (For sending the automated report email)[cite: 5]

---

## ⚙️ How to Use

1. Download the cleaned `cro-checker.json` file from this repository.
2. Import the JSON file into your **n8n** instance (`Workflows` -> `Import from File`).
3. Re-link your respective **OpenAI**, **Firecrawl**, **Google Drive**, and **Gmail** credentials[cite: 5].
4. Update the **Google Drive Folder ID** placeholder (`YOUR_FOLDER_ID`) in the Google Drive and HTTP request nodes to match your target drive folder[cite: 5].
5. Update the recipient email address in the **Gmail** nodes[cite: 5].
6. Activate the workflow and test it using the Form trigger URL[cite: 5]!
