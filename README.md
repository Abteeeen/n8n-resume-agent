<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&height=230&section=header&text=AI%20Resume%20Agent&fontSize=72&animation=fadeIn&fontAlignY=35&desc=Parse%20•%20Evaluate%20•%20Score%20•%20Decide&descAlignY=55&descAlign=50" />
</div>

<div align="center">

![n8n](https://img.shields.io/badge/n8n-FF6584?style=for-the-badge&logo=n8n&logoColor=white)
![Notion](https://img.shields.io/badge/Notion-000000?style=for-the-badge&logo=notion&logoColor=white)
![Google Gemini](https://img.shields.io/badge/Google%20Gemini-8E75B2?style=for-the-badge&logo=google&logoColor=white)
![OpenRouter](https://img.shields.io/badge/OpenRouter-111827?style=for-the-badge&logo=openai&logoColor=white)
![LLM Agents](https://img.shields.io/badge/LLM%20Agents-4B5563?style=for-the-badge)

</div>

---

# 🧠 AI Resume Agent

An **enterprise-grade n8n automation** that transforms raw resumes into **structured, explainable hiring insights**.  
This agent replaces manual resume screening with **AI-powered parsing, scoring, and role recommendations**, fully integrated with **Notion**.

Built for **ATS pipelines**, **HR automation**, and **high-volume hiring workflows**.

---

## 🎯 What Agent Solves

Hiring teams struggle with:
- Manual resume screening is being done 
- Inconsistent evaluations
- Biased or unclear decisions
- Scaling candidate analysis

This Resume Agent automates the entire process — **objectively, repeatably, and transparently**.
---

## 🚀 Key Capabilities

* **📄 Resume Parsing:** Automatically downloads and extracts text from PDF resumes.
* **🧩 Structured Extraction:** Converts unstructured resume text into clean, machine-readable JSON.
* **🧠 Dual-Agent Intelligence:**
  * **Parsing Agent** → structures resume data
  * **Decision Agent** → evaluates and scores candidates
* **📊 Explainable Scoring:**
  * Work Experience Score
  * Skills Score
  * Project Score
  * Total Score
* **💡 Human-Readable Insights:**
  * Candidate strengths & weaknesses.
  * Primary & secondary role recommendations
  * Learnability rating
* **🚫 Automated Rejection Logic:** Rule-based rejection (e.g., location mismatch).
* **🗂️ Notion-Native Storage:** Results written back into Notion for easy review and tracking.

---

## 🧠 Multi-Agent LLM Strategy

This workflow uses **specialized AI agents**, each optimized for its task:

| Agent | Responsibility |
|------|---------------|
| Parsing Agent | Resume → Structured JSON |
| Decision Agent | Evaluation, scoring, recommendations |
| Rule Engine | Conditional routing & rejection logic |

This separation improves:
- Accuracy
- Explainability
- Maintainability
- Cost effect

---

## 🏗️ System Architecture  

```mermaid
graph TD
    A["⏱️ Schedule Trigger"] --> B["📥 Fetch Candidates from Notion"]
    B --> C{"Pending Candidates?"}
    C -- No --> X["🛑 Stop Workflow"]
    C -- Yes --> D["📄 Download Resume PDF"]
    D --> E["📑 Extract Text from PDF"]
    E --> F["🧠 Parsing Agent (LLM)"]
    F --> G["🧠 Decision Agent (LLM)"]
    G --> H{"📍 Rule Checks"}
    H -- Reject --> I["❌ Update Status: Rejected"]
    H -- Accept --> J["📊 Store Scores & Insights"]
    J --> K["✅ Update Status: AI Parsed Done"]











































































































