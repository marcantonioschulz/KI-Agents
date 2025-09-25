# KI Agents Repository

This repository contains the configuration and documentation for AI-driven voice and conversation agents for "Endlich zu Hause Finanzierungen GmbH" customer support automation. The architecture is designed for machine-readability, ensuring that AI agents can directly consume business logic and operational guidelines.

## 🚀 Quick Start

1.  **Explore the Core Voice Agent**: Review [`Voice Agent/Vivi KI Voice AI.md`](Voice Agent/Vivi KI Voice AI.md) to understand the primary customer support agent's persona, rules, and structured call flow.
2.  **Discover the Coaching Agent**: See [`Voice Agent/Finanzberater Coach AI.md`](Voice Agent/Finanzberater Coach AI.md) for an advanced agent designed to train financial advisors in communication skills.
3.  **Consult Business Frameworks**: The `Docs/` directory contains the core business logic in machine-readable YAML files, covering everything from AI prompting techniques to customer psychology.

## 📁 Repository Structure

```
KI Agents/
├── .github/
│   ├── instructions/
│   │   ├── conversation-agent.instructions.md # Rules for text-based chatbots
│   │   ├── copilot-instructions.md            # GLOBAL AI coding agent guidelines
│   │   └── voice-agent.instructions.md        # Rules for voice-based agents
├── Docs/
│   ├── ai-prompting-framework.yaml    # Best practices for AI prompting
│   ├── bot-goals-framework.yaml       # Goal-tracking for conversation AI
│   ├── merge-fields.md                # Reference for GoHighLevel merge fields
│   ├── post-types-framework.yaml      # 6 fundamental content post types
│   ├── realtime-prompting-guide.md    # Advanced guide for realtime voice AI
│   └── social-proof-types.yaml        # 5 types of social proof framework
├── Voice Agent/
│   ├── Finanzberater Coach AI.md      # Advanced communication coaching agent
│   ├── Vivi KI Voice AI.md            # Main agent for customer data collection
│   └── Vivi KI Voice AI (FULL BACKUP).md # Backup of a previous version
└── Conversation Agent/                # (Future expansion for text-based agents)
```

## 📋 Agent Capabilities

### Voice Agents (`Voice Agent/`)
-   **Vivi KI**: A professional virtual assistant whose sole purpose is to collect caller information for a qualified callback. It operates with strict rules, a defined conversation flow, and does not solve problems directly.
-   **Finanzberater Coach AI**: An expert communication coach that simulates client conversations to train financial advisors. It uses advanced methodologies like SPIN Selling and the "Five Whys" in a `Simulate -> Analyze -> Challenge` cycle.

### Business Intelligence (`Docs/`)
-   **AI Prompting & Goals**: Technical setup and best practices for LeadConnector are defined in [`Docs/ai-prompting-framework.yaml`](Docs/ai-prompting-framework.yaml) and [`Docs/bot-goals-framework.yaml`](Docs/bot-goals-framework.yaml).
-   **Customer Psychology**: Frameworks for building trust and creating content are available in [`Docs/social-proof-types.yaml`](Docs/social-proof-types.yaml) and [`Docs/post-types-framework.yaml`](Docs/post-types-framework.yaml).

## 🔧 For Developers & AI Agents

### Agent Development Guidelines
-   **Global Rules**: All development must adhere to the master guidelines in [`.github/instructions/copilot-instructions.md`](.github/instructions/copilot-instructions.md).
-   **Voice Agents**: Follow the specific rules in [`.github/instructions/voice-agent.instructions.md`](.github/instructions/voice-agent.instructions.md).
-   **Core Principles**:
    -   Agents must only use information provided in prompts or tools (no inference).
    -   Agents must never suggest external sources; always assure a team callback.
    -   Name confirmation must be done by spelling each character.

### Workflow
-   This is a configuration-as-code repository. No build or test scripts are required.
-   Changes are made by directly editing the Markdown and YAML files.
-   All documentation is optimized for AI consumption.