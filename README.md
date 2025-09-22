# 🤖 LendiBot – Smart Loan Assistant

LendiBot is a chatbot prototype designed to **help customers understand their loan eligibility, limits, and repayment options** in a clear and customer-friendly way.  
The project simulates how a chatbot can integrate with **CRM interfaces, USSD menus, and customer wallet APIs** to provide customized responses while protecting sensitive data.

---

## Features
- **Interactive Chat UI (WhatsApp-style):**
  - Customers or agents can chat with LendiBot.
  - Dynamic menus (Why is my limit 0? How to increase limit? Repayment options, etc.).
  - Customized responses based on wallet data (simulated).

- **USSD Simulation:**
  - White-theme mockup of a USSD menu.
  - Pop-up styled like an SMS notification.
  - Supports menu navigation and returning to main menu.

- **CRM Simulation:**
  - Helpdesk/Zendesk-style interface.
  - Customer list, tickets view, and integration with LendiBot.
  - LendiBot assists agents by fetching insights from customer tickets.

- **Step-by-Step Simulation:**
  - Shows how a request travels from **Frontend → Middleware → API Gateway → Wallet DB**.
  - Spinner animations demonstrate the process until a final customer-friendly response is returned.

---

##  Tech Stack
- **Frontend:** HTML, CSS, JavaScript
- **Simulation:** Custom logic (no backend required)
- **Hosting:** GitHub Pages

---

##  Project Structure

---

##  Architecture Overview
LendiBot interacts with:
1. **Frontend (UI)** – CRM, USSD, App
2. **Middleware** – Chatbot logic (menu + query mapping)
3. **API Gateway** – Filters & enforces safe parameters
4. **Wallet DB** – Customer data (limit, balances, repayment history)

🔒 Only **whitelisted parameters** (loan_limit, balance, repayment_history, etc.) are fetched.  
Sensitive info (like KYC docs, internal flags) is **never shared** with the bot.

---

## Example Use Case
**Customer asks:** *“Why is my limit 0?”*  
1. LendiBot maps the query → needs wallet activity data.  
2. API Gateway fetches safe parameters from DB.  
3. Rejection rules are checked:
   - Avg received < 20,000  
   - Inactivity > 14 days  
   - Wallet age < 3 months  
4. LendiBot responds in **simple language**:
   > “Your limit is 0 because your wallet is new. Keep it active and repay on time to grow your limit.”

---

##  Deployment
To deploy on **GitHub Pages**:
1. Push your repo to GitHub.
2. Go to **Settings → Pages**.
3. Set branch: `main` → `/root`.
4. Access your project at:  
   `https://<username>.github.io/LendiBot-mockupUI/`

---

##  Future Enhancements
- API integration with real scoring models.
- NLP-based chatbot for natural questions.
- Secure agent-customer audit logs.
- Multilingual support (English, Kiswahili).

---

##  Contributors
- **Alfonce Mulumba** – Project Lead & Innovator
- **LendiBot** – Your friendly loan assistant 🤝  
