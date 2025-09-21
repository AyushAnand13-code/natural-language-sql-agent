# 🗣️ Natural Language to SQL Query Agent (n8n + AI + Postgres)

🚀 Ask database-related questions in **plain English** and get direct answers from a **PostgreSQL database** — no SQL required.  

Built using **n8n automation**, **Google Gemini LLM**, and **Postgres**.

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
   cd nat-lang-to-sql-agent
