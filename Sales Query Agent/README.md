# 📊 Sales Query Agent (n8n + Telegram + Google Sheets)

This project is a practical automation built using **n8n**, designed to help a business owner retrieve **sales insights using natural language** through **Telegram**.  
It reads data from a Google Sheet and calculates the **total sales and total number of orders** between any date range provided by the user.

---

## 💡 Why I Built This

In a real business, owners often spend time manually checking spreadsheets to understand sales performance.  
With this agent, the user can simply send a message like:

> “What are the sales between 2025-10-31 and 2025-11-30?”

The agent extracts the dates, reads the sheet, calculates totals, and replies automatically through Telegram.

---

## 🚀 Workflow Summary

Here’s the flow of the agent:

1. **Telegram Trigger** – Accepts user message.  
2. **AI Agent (Chat Model)** – Understands the requested date range.  
3. **Code Node** – Converts the AI output string into flat JSON.  
4. **Google Sheets Tool** – Retrieves sales data from a configured sheet.  
5. **Code Node (Filter by Date)** – Keeps only rows between the start and end dates.  
6. **Calculator Tool** – Calculates total sales and number of orders.  
7. **Telegram Send Message** – Sends the final result back to the user.

---

## 🧪 Example Usage

### 🧵 User Input (Telegram)

```text
What are the sales between 2025-10-31 and 2025-11-30?
```

## 🔧 Credentials Required
```
| Service       | Credential Type in n8n | Purpose                                  |
| ------------- | ---------------------- | ---------------------------------------- |
| Telegram      | Telegram API Token     | Chat interface (user input/output)       |
| Azure OpenAI  | Chat Model (AI Agent)  | Date parsing and understanding           |
| Google Sheets | OAuth2 API             | Fetching sales data from the spreadsheet |

```

## 🔮 Possible Future Improvements

* Profit breakdown
* Product-wise or category-wise analysis
* Top-selling product summary
* Weekly / monthly sales summary sent by email
* Dashboard or API integration


## 🙋‍♂️ About Me

I enjoy working on real-world automation projects and exploring how AI can assist in everyday business operations.
This project helped me practise date handling, integrations with external tools, and building an end-to-end automation that a business owner can actually use.
I am motivated to enhance it further and build more intelligent agents in the future.
