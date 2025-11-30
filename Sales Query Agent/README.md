# 📊 Sales Query Agent (n8n + Telegram + Google Sheets)

This project is a practical automation built using **n8n**, designed to help a business owner retrieve **sales insights using natural language** through **Telegram**.  
It reads data from a Google Sheet and calculates the **total sales and total number of orders** between any date range provided by the user.

---

## 💡 Why I Built This

In a real business, owners often spend time manually checking spreadsheets to understand sales performance.  
With this agent, the user can simply send a message like:

> "What are the sales between 2025-10-31 and 2025-11-30?"

The agent extracts the dates, reads the sheet, calculates totals, and replies with the answer — automatically.

---

## 🚀 Workflow Summary

Here’s the flow of the agent:

1. **Telegram Trigger** – Accepts user message.
2. **AI Agent (Chat Model)** – Understands date range.
3. **Code Node** – Converts AI output into flat JSON.
4. **Google Sheets Tool** – Retrieves sales data.
5. **Code Node (Filter by Date)** – Keeps only rows between start & end dates.
6. **Calculator Tool** – Calculates total sales and number of orders.
7. **Telegram Send Message** – Sends result back to user.

---

## 🧪 Example Usage

**User Message (Telegram):**

What are the sales between 2025-10-31 and 2025-11-30?


**AI Response (JSON):**
```json
{
  "start_date": "2025-10-31",
  "end_date": "2025-11-30",
  "total_sales": 18500.50,
  "total_orders": 42,
  "currency": "USD",
  "status": "success"
}


Telegram Reply Sent to User:

Sales Report:
From: 2025-10-31
To: 2025-11-30

Total Orders: 42
Total Sales: $18,500.50
```
📁 Suggested Folder Structure
sales-query-agent/
│
├── workflow.json             ← n8n export file
├── sample_sales_sheet.xlsx   ← Example data sheet
├── README.md                 ← This document
└── screenshots/              ← Your screenshots here


🔧 Credentials Required

Before running the workflow, the following credentials must be added inside n8n:

Service	Credential Type in n8n	Purpose
Telegram	Telegram API Token	Chat interface (user input/output)
Azure OpenAI API	Chat Model (AI Agent)	Date extraction & understanding
Google Sheets	OAuth2 API	Fetching data from sales sheet

⚠️ No actual API keys are included in the JSON.
Only credential references are used — the real secrets stay securely stored inside n8n.

