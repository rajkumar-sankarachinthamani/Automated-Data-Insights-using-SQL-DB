--This project is an end-to-end natural language to insights system that lets users ask questions in plain English and get analytical insights back, without writing a single line of SQL. The app turns CSV data into a SQL database, then uses LLM tooling to generate and execute SQL queries and present the results in an intuitive chat interface.
​

What this project does
Natural language → insights (no SQL needed)
Users type questions such as “What are the top 5 products by revenue in 2024?” and the system automatically translates them into SQL, runs the queries, and returns answers plus summaries in natural language.

CSV → SQL data pipeline with LangChain toolkit
The project builds a pipeline that:

Ingests one or more CSV files.

Loads them into a relational database (e.g., SQLite/MySQL/PostgreSQL) using a configurable connection string.

Uses LangChain’s SQL tooling (e.g., SQLDatabase, SQL agents/toolkits) to connect to the database and let an LLM reason over the schema and data.
​

Chat-based analytics app (Streamlit + LangChain)
A Streamlit UI provides a chat-like experience where:

The user sends natural language questions.

LangChain orchestrates the LLM, SQL generation, execution, and result interpretation.

The app returns both the generated SQL and human-readable insights, making data exploration accessible to non-technical users.
​

#Tech stack
Frontend: Streamlit for an interactive chat-style analytics interface.

Orchestration: LangChain for LLM prompting, SQL toolkit/agents, and tool integration.

Data & Storage: CSV files loaded into a SQL database (e.g., SQLite for local dev, or MySQL/Postgres in production).

LLM Provider: OpenAI / other LLM backends (configurable via environment variables).
