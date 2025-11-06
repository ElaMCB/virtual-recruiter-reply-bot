# AI Recruiter Response Agent

An autonomous agent that handles job recruiter communications across multiple channels (Email, SMS, Voice).

## 🎯 Features

- **Email Automation**: Automatically read and respond to recruiter emails
- **SMS Handling**: Process and reply to text messages from recruiters
- **State Management**: Track conversation context across all interactions
- **LLM-Powered Responses**: Generate professional, context-aware replies
- **Multi-Channel Support**: Unified handling of email, SMS, and future voice integration

## 💰 100% Free Implementation

This project uses only free services:
- ✅ Gmail API (free, unlimited)
- ✅ Local LLM via Ollama (free, runs on your machine)
- ✅ Email-to-SMS gateways (free alternative to Twilio)
- ✅ Python with free hosting options

## 🚀 Quick Start

### Prerequisites

1. Python 3.9+
2. Gmail account with API access
3. Ollama installed (for local LLM)

### Installation

```bash
# Install dependencies
pip install -r requirements.txt

# Install Ollama (for local LLM)
# Visit: https://ollama.ai/download

# Pull a model
ollama pull llama2
```

### Configuration

1. Set up Gmail API credentials (see `docs/gmail_setup.md`)
2. Copy `.env.example` to `.env` and fill in your details
3. Configure your profile in `config/profile.yaml`

### Running

```bash
# Start the agent
python main.py

# Run in background
python main.py --daemon
```

## 📁 Project Structure

```
ai-recruiter-agent/
├── agents/
│   ├── email_agent.py      # Email handling
│   ├── sms_agent.py         # SMS handling
│   └── voice_agent.py       # Future voice handling
├── core/
│   ├── orchestrator.py      # Central coordinator
│   ├── state_manager.py     # Conversation state tracking
│   └── llm_processor.py     # LLM response generation
├── config/
│   ├── profile.yaml         # Your professional profile
│   └── prompts.yaml         # System prompts
├── utils/
│   ├── gmail_helper.py      # Gmail API wrapper
│   └── logger.py            # Logging utilities
├── data/
│   └── conversations.db     # SQLite database for state
├── main.py                  # Entry point
├── requirements.txt
└── .env.example
```

## ⚠️ Legal & Ethical Considerations

- Agent identifies itself when necessary
- All interactions are logged for your review
- Option to escalate to human at any time
- Respects STOP/unsubscribe requests
- Does not make final commitments without approval

## 🔄 How It Works

1. **Monitor**: Agent checks email/SMS periodically
2. **Parse**: Extracts key information (company, role, requirements)
3. **Decide**: Determines appropriate response based on your profile
4. **Generate**: Creates professional reply using LLM
5. **Send**: Dispatches response via appropriate channel
6. **Track**: Updates conversation state for context

## 📊 Conversation Stages

- `initial_contact`: First message from recruiter
- `information_gathering`: Getting details about role
- `screening`: Answering qualification questions
- `negotiation`: Discussing compensation/benefits
- `scheduling`: Arranging interviews
- `escalation`: Requires human intervention

## 🛠️ Advanced Configuration

See `docs/` folder for:
- Gmail API setup guide
- SMS integration options
- Custom prompt engineering
- Voice integration (future)

## 🤝 Contributing

This is a personal project but feel free to adapt for your needs!

## 📝 License

MIT License - Use freely for personal job search automation

