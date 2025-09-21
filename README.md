# 🗣️ Natural Language to SQL Query Agent (n8n + AI + Postgres)

🚀 Ask database-related questions in **plain English** and get direct answers from a **PostgreSQL database** — no SQL required.  

Built using **n8n automation**, **Google Gemini LLM**, and **Postgres**.

🎥 **[Project Demo (Google Drive Link)]([https://drive.google.com/your-demo-link-here](https://drive.google.com/file/d/1mxVSjow8oQKQJ6dWUUH2JzsDZzsFIcPS/view?usp=sharing))**

---

## ✨ Use Case

Business users can ask natural questions like:

- “Show me sales from Mumbai last month”
- “What is the total revenue from India in 2020?”

The agent will automatically:

1. **Understand the question**  
2. **Convert it into SQL**  
3. **Execute the query on Postgres**  
4. **Return the result in conversational format**  

---

## 🛠️ Solution Design

**Workflow Steps:**

1. **Trigger** → User sends a chat message → Workflow starts  
2. **AI Agent** → Interprets natural language → Generates SQL query  
3. **Database Connector** → Executes SQL query on Postgres  
4. **Response** → Returns results back in conversational format  

---

## ⚙️ Architecture

- **Workflow 1:** `nat-lang-to-sql-query-agent.json`  
  - Handles chat input  
  - Uses Gemini for SQL generation  
  - Invokes SQL execution  

- **Workflow 2:** `sql_query_executor.json`  
  - Executes SQL queries  
  - Returns results back to the agent  

---

## 🔧 Tech Stack

- **[n8n](https://n8n.io/)** – Orchestration & workflow automation  
- **Google Gemini Chat Model** – Natural language → SQL conversion  
- **Postgres** – Database backend  
- **AI Agent Node** – SQL planning & reasoning  
- **Memory Node** – Retains chat context across turns  

---

## 🚀 How to Run

1. **Clone Repo**
   ```bash
   git clone https://github.com/yourusername/nat-lang-to-sql-agent.git
   cd natural-language-sql-agent


2. **Import Workflows**
   - Open **n8n** (cloud or local setup)
   - Import both JSON workflows from the `/workflows/` folder
  
3. **Connect Postgres DB**
   - Update Postgres credentials inside the workflow
  
4. **Start Chatting!**
   **Example:**
   **Input:**  
   - Show me sales for India in 2020
   **Output:**
   - The total sales quantity for India in 2020 was 8,595,336.
  

---

## ✅ Features
- Convert **Natural Language → SQL**  
- Handles **follow-up questions** if query is unclear  
- Explains gracefully when **no data is available**  
- **Context-aware** (remembers past chat history)  
- Works with **any Postgres database**  

     
