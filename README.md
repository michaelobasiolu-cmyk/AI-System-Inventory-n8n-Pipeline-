# Enterprise AI Governance & Intake Pipeline 🤖🛡️

An automated, asynchronous workflow designed to eliminate "Shadow AI" by providing employees with a frictionless intake form, while giving Legal and Finance teams real-time, AI-evaluated compliance visibility.

Built using **n8n, OpenAI (gpt-4o), and Notion.**

## 🏗️ Architecture Overview

<img width="1536" height="552" alt="image" src="https://github.com/user-attachments/assets/0e79d57e-4897-4d7f-97e4-d0b5c9a531d1" />


This pipeline bridges the gap between raw employee requests and structured database management:
1. **Intake Trigger:** Captures requested AI tool, Use Case, and Data Types via a user-facing web form.
2. **System of Record Logging:** Instantly generates a unique database ID in Notion to ensure no requests are lost.
3. **AI Compliance Bouncer (LLM Chain):** Utilizes an OpenAI system prompt constrained with `Temperature: 0` and a Structured Output Parser. It evaluates the request against EU AI Act Risk Tiers and US/EU Liability frameworks, outputting strictly formatted JSON.
4. **Database Injection:** Automatically routes the LLM's compliance verdict back to the precise Notion record.

## 📊 The Resulting Database
<img width="1597" height="290" alt="image" src="https://github.com/user-attachments/assets/ac0d46cf-e4e2-4310-8c7e-81d1a51484c7" />
<img width="1432" height="330" alt="image" src="https://github.com/user-attachments/assets/0c5fe3dd-81c9-490e-9ca4-568d8a104113" />



## 💡 Business Value
* **Risk Mitigation:** Prevents employees from bypassing IT procurement by offering an instant, automated approval process.
* **Audit Readiness:** Maintains a continuously updated, permanent AI System Inventory.
* **Financial Strategy:** Exposes potential strict liability and copyright infringement exposure before a vendor contract is signed.

## 🚀 How to Use This Workflow
1. Download the `AI_Intake_Pipeline.json` file from this repository.
2. In your n8n workspace, go to the top right menu and select **Import from File**.
3. Re-authenticate your own Notion and OpenAI credentials.
4. Map the final Notion node to your own workspace database.
