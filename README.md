# Agentic Text-to-SQL LLM

An AI-powered Text-to-SQL application that enables users to interact with databases using natural language. Built with **LangChain**, **Llama 3 (Groq)**, **Streamlit**, and **SQLAlchemy**, the application automatically converts user questions into SQL queries and returns results in a conversational format.

---

## Project Overview

Writing SQL queries can be challenging for non-technical users and time-consuming even for experienced analysts. This project demonstrates how Large Language Models (LLMs) can bridge the gap between humans and structured databases.

Users can simply ask questions in plain English, and the AI agent:

1. Understands the request.
2. Examines the database schema.
3. Generates the appropriate SQL query.
4. Executes the query.
5. Returns results in natural language.

The system supports both **SQLite** and **MySQL** databases.

---

## Features

### Natural Language Database Querying

Ask questions such as:

```text
How many students are in the database?

Show me the top 5 students based on marks.

Which department has the highest average score?

List all students whose age is above 20.
```

No SQL knowledge is required.

---

### Agentic AI Workflow

The application leverages a LangChain SQL Agent that:

- Interprets user intent
- Explores database schema
- Generates SQL queries
- Executes queries safely
- Returns interpretable results

---

### Multiple Database Support

Supported databases:

- SQLite
- MySQL

Users can either:

- Query a local SQLite database
- Connect to their own MySQL database

---

### Conversational Interface

Built using Streamlit's chat interface with:

- Chat history retention
- Interactive responses
- Real-time SQL generation

---

### Llama 3 via Groq

Uses:

```text
Llama3-8B-8192
```

hosted through the Groq API for fast inference and low latency.

---

## System Architecture

```text
User Question
       │
       ▼
Streamlit UI
       │
       ▼
LangChain SQL Agent
       │
       ▼
Llama 3 (Groq)
       │
       ▼
Database Schema Inspection
       │
       ▼
SQL Query Generation
       │
       ▼
Query Execution
       │
       ▼
Natural Language Response
```

---

## Technology Stack

### Artificial Intelligence

- LangChain
- Llama 3
- Groq API

### Backend

- Python
- SQLAlchemy

### Databases

- SQLite
- MySQL

### Frontend

- Streamlit

### Agent Framework

- LangChain SQL Agent
- SQLDatabaseToolkit

---

## Repository Structure

```text
.
├── app.py
├── student.db
├── requirements.txt
├── README.md
├── .gitignore
└── .env.example
```

---

## Installation

### Clone Repository

```bash
git clone https://github.com/yourusername/agentic-text-to-sql-llm.git

cd agentic-text-to-sql-llm
```

---

### Create Virtual Environment

```bash
python -m venv venv
```

Linux/macOS

```bash
source venv/bin/activate
```

Windows

```bash
venv\Scripts\activate
```

---

### Install Dependencies

```bash
pip install -r requirements.txt
```

---

### Configure Groq API Key

Create a `.env` file:

```env
GROQ_API_KEY=your_api_key_here
```

---

### Run the Application

```bash
streamlit run app.py
```

---

## Usage

### SQLite Mode

Select:

```text
Use SQLite 3 Database - student.db
```

Example prompts:

```text
How many students are present?

Show all student names.

Who scored the highest marks?

What is the average score?
```

---

### MySQL Mode

Provide:

```text
Host
Username
Password
Database Name
```

Then ask questions naturally:

```text
Show the top-selling products.

How many customers registered this year?

What is the monthly revenue trend?
```

---

## Example

### User Query

```text
Which students scored above 80 marks?
```

### Agent Workflow

```text
Question
    ↓
Generate SQL
    ↓
Execute Query
    ↓
Retrieve Results
    ↓
Summarise Output
```

### Response

```text
There are 12 students who scored above 80 marks.
The highest score recorded is 96.
```

---

## Key Concepts Demonstrated

### Text-to-SQL

Translating natural language questions into executable SQL statements.

### Agentic AI

Using autonomous agents to reason about database schemas and generate valid queries.

### LLM-Powered Analytics

Leveraging Large Language Models for business intelligence and data analysis.

### Database Integration

Connecting AI models directly to structured databases for real-time insights.

---

## Use Cases

- Business Intelligence
- Self-Service Analytics
- Data Exploration
- Reporting Automation
- Educational SQL Learning
- Database Chatbots
- Enterprise Data Assistants

---

## Future Enhancements

- Query visualisation and charts
- PostgreSQL support
- Export results to CSV
- Multi-database connections
- Query validation and guardrails
- Role-based access control
- Semantic caching
- Dashboard generation

---

## Limitations

- Complex analytical queries may require manual optimisation.
- Accuracy depends on database schema clarity.
- Requires a valid Groq API key.
- Generated SQL should be reviewed before use in production environments.

---

## Learning Outcomes

This project demonstrates hands-on experience with:

- LangChain
- LLM Applications
- Agentic AI
- Text-to-SQL Systems
- Groq API
- SQLAlchemy
- SQLite
- MySQL
- Streamlit
- Prompt Engineering

---

## Disclaimer

This project is intended for educational and demonstration purposes. Generated SQL queries should be reviewed before being executed in production environments.

---

⭐ If you found this project useful, consider giving the repository a star.
