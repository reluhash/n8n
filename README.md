# n8n AI Router Agent Workflow

This project uses an AI Agent inside n8n to route user messages to different tools such as:

- Weather tool
- Task tool
- Calendar tool
- Normal Assistant (NONE)

## 🧠 How It Works

The workflow reads a chat-like message from a webhook input.
Then the AI Agent decides what the user is asking for and routes to the correct tool.

Example inputs:

- "weather delhi" → Weather
- "add buy milk task" → Task
- "schedule meeting tomorrow" → Calendar
- "summarize my day" → NONE (normal LLM reply)

## 🧰 Tools Used

- n8n (workflow automation)
- LLM (via OpenRouter / OpenAI / etc)
- Weather API
- Task Tool (internal)
- Calendar Tool (internal)

## 📂 Project Structure (Recommended)

