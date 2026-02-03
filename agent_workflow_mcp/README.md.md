n8n AI Router Agent Workflow (with MCP)

This project implements an AI Router Agent in n8n that routes user messages to different tools using Model Context Protocol (MCP). The workflow analyzes user intent and decides whether to call an MCP tool (Weather, Task, Calendar) or return a normal assistant response.

🧠 How It Works

The workflow receives a chat-style message through a Webhook trigger. The message is passed to an AI Agent node, which uses an LLM to understand the user’s intent. Based on this intent, the agent routes the request to the appropriate MCP tool. If no tool is required, the agent responds directly using the LLM. Strict validation rules ensure that MCP tools are called only with valid and complete arguments.

🔀 Routing Examples

"weather delhi" → MCP Weather Tool

"add buy milk task" → MCP Task Tool

"schedule meeting tomorrow" → MCP Calendar Tool

"summarize my day" → NONE (normal assistant response)

🧰 Tools Used

n8n – Workflow automation

LLM (OpenRouter / OpenAI / compatible) – Intent detection

MCP Weather Tool – Fetches weather data

MCP Task Tool – Manages tasks

MCP Calendar Tool – Handles calendar events

📂 Project Structure (Recommended)
n8n-ai-router-agent/
│
├── workflows/
│   └── ai-router-workflow.json     # Main n8n workflow
│
├── mcp-tools/
│   ├── weather.mcp.json            # MCP Weather tool
│   ├── task.mcp.json               # MCP Task tool
│   └── calendar.mcp.json           # MCP Calendar tool
│
├── prompts/
│   └── system-prompt.txt           # AI routing & MCP rules
│
└── README.md

🛡️ MCP Tool Execution Rules

MCP tools are called only after intent is confirmed

Required parameters must be present before execution

Empty payloads ({} or []) are never sent

Clarification questions are asked when input is incomplete

Intent is always converted into valid MCP-compatible JSON

✅ Example Flow

User sends a message to the webhook

AI Agent detects intent using LLM

Required parameters are validated

Relevant MCP tool is executed (if needed)

Response is returned to the user