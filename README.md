# Kaira - Personal AI Assistant

## Overview

Kaira is a sophisticated personal AI assistant built using n8n workflows, leveraging OpenRouter's LLM capabilities and a modular agent architecture. It features natural language processing, persistent memory, scheduled automations, and multi-channel input processing via Telegram.

## Architecture

Kaira employs a multi-agent architecture with specialized components orchestrated by a central Manager Agent:

```
                   ┌─────────────┐
                   │ Telegram    │
                   │ Interface   │
                   └──────┬──────┘
                          │
                          ▼
┌──────────────┐    ┌─────────────┐    ┌───────────────┐
│ Input        │    │ Memory      │    │ OpenRouter    │
│ Processing   │◄───┤ Buffer      │◄───┤ LLM           │
└──────┬───────┘    └─────────────┘    └───────────────┘
       │                   ▲
       ▼                   │
┌──────────────┐    ┌─────────────┐
│ Manager      │◄───┤ Scheduled   │
│ Agent        │    │ Triggers    │
└──────┬───────┘    └─────────────┘
       │
       ▼
┌─────────────────────────────────────────────┐
│                                             │
│  ┌─────────┐ ┌────────┐ ┌───────────┐       │
│  │Calendar │ │Email   │ │Research   │       │
│  │Agent    │ │Agent   │ │Agent      │ ...   │
│  └─────────┘ └────────┘ └───────────┘       │
│                                             │
│              Specialized Agents             │
└─────────────────────────────────────────────┘
```

## Key Features

- **Natural Language Processing**: Powered by OpenRouter LLMs for human-like conversations
- **Multi-Agent System**: Specialized agents for calendar, email, research, portfolio management
- **Memory Management**: Persistent context tracking across conversations
- **Multi-Channel Input**: Process text, voice messages, and documents
- **Scheduled Automations**: Daily briefings and weekly team management reports
- **Telegram Integration**: User-friendly interface accessible from mobile and desktop

## Technical Implementation

### Core Components

- **Manager Agent**: Orchestrates workflow and delegates tasks to specialized agents
- **Memory Buffer**: Maintains conversation context and user preferences
- **Specialized Agents**:
  - Calendar Agent: Manages appointments and reminders
  - Email Agent: Handles email communication
  - Research Agent: Performs web research and information gathering
  - Portfolio Agent: Tracks and reports on financial investments
  - Memory Base: Stores and retrieves personal information and preferences

### Workflow Architecture

The n8n workflow implements:

1. **Input Processing**: Routes different types of Telegram inputs (text, voice, documents)
2. **Context Management**: Maintains conversation history with window buffer memory
3. **Task Delegation**: Routes tasks to appropriate specialized agents
4. **Scheduled Triggers**: Automates daily briefings and weekly reports
5. **Response Generation**: Formats responses and sends them back via Telegram

## Future Development

- Voice interface integration
- Web dashboard for configuration
- Expanded tool integration (smart home, productivity apps)
- Fine-tuned custom LLM for improved personality and response quality

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Contact

For questions or collaboration opportunities:
- GitHub: [your-github-username](https://github.com/your-github-username)
- LinkedIn: [your-linkedin-profile](https://linkedin.com/in/your-linkedin-profile)

---

*Kaira: Your intelligent, proactive AI assistant*
