# main.json — Central Logic Controller

This is the core controller of the entire voice and chat-based AI assistant.

It receives user input (via Telegram or voice), analyzes the intent, and routes the request to the appropriate module:

- For email tasks → it calls `email.json`
- For scheduling or calendar events → it triggers `calendar.json`
- For anything related to contacts → it invokes `contact.json`
- For general understanding → it sends the prompt to an AI model (like GPT-3.5 or Mistral)

## Key Components
- Telegram or voice-based trigger
- Intent recognition logic (Switch or If nodes)
- Optional context memory
- AI integration (OpenAI, Together.ai, etc.)
- `Execute Workflow` nodes to delegate tasks to sub-agents

It acts as the brain of the system, coordinating all actions and decisions.
