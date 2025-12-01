# 📬 Daily Sales Summary Agent (n8n + Google Sheets + Email)

This project is a practical automation built using **n8n**, designed to automatically send a **daily sales summary email** to the business owner at **6:00 PM**.  
It reads data from a Google Sheet, filters today’s sales, calculates totals, and sends a formatted summary email.  
If no sales are found for the day, the agent sends a **warning alert email** instead.

---

## 💡 Why I Built This

In many businesses, owners manually check their sales spreadsheet at the end of each day to understand performance.  
This agent eliminates that manual work by delivering a **daily automated sales summary**, ensuring consistency and saving time.

With this automation, the owner receives a daily email like:

> “Here is your sales summary for 2025-12-01.”

This improves clarity, efficiency, and daily reporting.

---

## 🚀 Workflow Summary

Here’s the flow of the agent:

1. **Cron Trigger (6 PM Daily)** – Automatically runs every evening at 18:00.  
2. **Google Sheets Node** – Reads all sales rows from the sheet.  
3. **Code Node (Filter + Calculate)** – Filters for today’s date and calculates:
   - Total sales  
   - Total number of orders  
   - Currency  
4. **IF Node** – Checks whether any sales exist for today.  
5. **Email Node – Summary Email** – Sends a formatted sales report if sales exist.  
6. **Email Node – Alert Email** – Sends a warning if no sales were found.

---

## 🧪 Example Daily Email Output

### 📧 Sales Found

```
Subject: 📈 Daily Sales Summary – 2025-12-01

Hi,

Here is the sales summary for 2025-12-01:

Total Orders: 5
Total Sales: $1,240.00
Regards,
Daily Sales Summary Agent
```
### 📧 Sales Found

```
Subject: ⚠️ Alert – No Sales Recorded on 2025-12-01

Hi,

There were no sales recorded today.
Please verify if this is expected or if there was any issue with data entry or system updates.

Regards,
Daily Sales Summary Agent
```


## 📷 Workflow Screenshot

<img width="1326" height="417" alt="image" src="https://github.com/user-attachments/assets/475d27e2-d6a1-48a2-9540-43d850118b5d" />

## 🔮 Possible Future Improvements

* Weekly sales summary
* Profit calculation
* Product-wise breakdown
* Telegram notifications
* Monthly executive report
* Dashboard integration
