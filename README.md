# KI Agents Repository

Configuration-as-code for the voice agents, coaching simulations, and prompting frameworks that power "Endlich zu Hause Finanzierungen GmbH". Every file is written so AI systems can apply the guidance without additional interpretation.

## Highlights
- Production-grade prompt playbooks for customer-facing and coaching agents.
- Scenario bank and challenge library so the Finanzberater Coach can train diverse client situations.
- Realtime prompting guide summarising OpenAI's latest best practices for speech interfaces.
- Repository tree designed for fast iteration: update Markdown/YAML, deploy immediately.

## Quick Start
1. **Review Vivi KI** – `Voice Agent/Vivi KI Voice AI.md` contains the operational prompt for the message-taking assistant.
2. **Explore the Finanzberater Masterclass** – `Voice Agent/Finanzberater Coach AI.md` packs the simulation cycle, feedback scoring, and scenario templates.
3. **Check the prompting frameworks** – documentation in `Docs/` captures reusable rules, merge fields, and realtime prompting guidance.

## Repository Structure
```
KI Agents/
├── .github/
│   └── instructions/
│       ├── conversation-agent.instructions.md
│       ├── copilot-instructions.md
│       └── voice-agent.instructions.md
├── Docs/
│   ├── ai-prompting-framework.yaml
│   ├── bot-goals-framework.yaml
│   ├── merge-fields.md
│   ├── post-types-framework.yaml
│   ├── realtime-prompting-guide.md
│   └── social-proof-types.yaml
├── Voice Agent/
│   ├── Finanzberater Coach AI.md
│   ├── Vivi KI Voice AI.md
│   └── Vivi KI Voice AI (FULL BACKUP).md
└── Conversation Agent/ (placeholder for future text agents)
```

## Voice Agent Playbooks
- **Vivi KI** – Professional front-office assistant focused solely on structured data capture for callbacks. Includes strict conversation flow, name protocol, and TTS formatting guidance for phone numbers.
- **Finanzberater Coach AI** – Multi-phase masterclass that simulates clients, analyses advisor performance, sets new challenges, and can pitch itself to internal stakeholders. Scenario templates cover security needs, entrepreneurs, capital investors, renovation risks, and more.

## Documentation & Frameworks
- **Prompting Fundamentals** – `Docs/ai-prompting-framework.yaml` and `Docs/bot-goals-framework.yaml` define global prompting principles and measurable agent goals.
- **Realtime Voice Best Practices** – `Docs/realtime-prompting-guide.md` condenses OpenAI's realtime API guidance into actionable checklists.
- **Marketing & Social Proof** – `Docs/post-types-framework.yaml` and `Docs/social-proof-types.yaml` capture the core content archetypes used across campaigns.
- **Merge Fields Reference** – `Docs/merge-fields.md` lists GoHighLevel merge fields for consistent CRM sync.

## Workflow & Collaboration
- Treat each prompt as code: make atomic changes, review diffs, and keep backups in `Voice Agent/` when experimenting.
- Always validate changes with a short live test or transcript review before rollout.
- Document new scenarios, challenges, or safety rules directly in the relevant Markdown file so agents inherit the behaviour instantly.

## Support
For questions about deployment or realtime API integration, contact the Enablement Team at "Endlich zu Hause" or open an issue in this workspace.
