# KI Agents Repository

Configuration-as-code for the voice agents, coaching simulations, and prompting frameworks that power "Endlich zu Hause Finanzierungen GmbH". Every file is written so AI systems can apply the guidance without additional interpretation.

## 🚀 Direkter Zugang zu den Prompts

**Für Voice Agents (Telefon/Anrufe):**
- 🎯 [**Vivi KI Voice Agent** - Hauptprompt für Telefonannahme](Voice%20Agent/Vivi%20KI%20Voice%20AI.md)
- 🏋️ [**Finanzberater Coach** - Training & Simulation](Voice%20Agent/Finanzberater%20Coach%20AI.md)

**Für Conversation Agents (Chat/Text):**
- 💬 [**Vivi KI Conversation Agent** - Hauptprompt für Text-Chat](Conversation%20Agent/Vivi%20KI%20Conversation%20AI)

**Knowledge Base & Frameworks:**
- 📚 [**Vivi KI Knowledge Base** - Wissenssammlung](Knowledge%20Base/Kunden/Vivi%20KI%20Knowledge.md)
- 🛠️ [**AI Prompting Framework** - Technische Anleitung](Docs/ai-prompting-framework.yaml)
- 📋 [**Conversation AI Guide** - Setup-Anleitung](Docs/Conversation%20AI%20Guide)

> **💡 Tipp:** Klicke einfach auf die Links oben, um direkt zu den gewünschten Prompt-Texten zu gelangen. Du kannst die Inhalte kopieren und in dein System einfügen.

## Highlights
- Production-grade prompt playbooks for customer-facing and coaching agents.
- Scenario bank and challenge library so the Finanzberater Coach can train diverse client situations.
- Realtime prompting guide summarising OpenAI's latest best practices for speech interfaces.
- Conversation AI V3 implementation with three-field structure (Personality, Goal, Additional Information).
- Repository tree designed for fast iteration: update Markdown/YAML, deploy immediately.

## Quick Start

### Für Einsteiger (ohne GitHub-Kenntnisse)
1. **Klicke direkt auf die Links im "🚀 Direkter Zugang" Bereich oben**
2. **Kopiere den gewünschten Prompt-Text** aus der geöffneten Datei
3. **Füge ihn in dein AI-System ein** (ChatGPT, LeadConnector, etc.)

### Für Entwickler
1. **Review Vivi KI Voice Agent** – [`Voice Agent/Vivi KI Voice AI.md`](Voice%20Agent/Vivi%20KI%20Voice%20AI.md) contains the operational prompt for the message-taking assistant.
2. **Check Vivi KI Conversation Agent** – [`Conversation Agent/Vivi KI Conversation AI`](Conversation%20Agent/Vivi%20KI%20Conversation%20AI) shows the V3 three-field implementation for text-based interactions.
3. **Explore the Finanzberater Masterclass** – [`Voice Agent/Finanzberater Coach AI.md`](Voice%20Agent/Finanzberater%20Coach%20AI.md) packs the simulation cycle, feedback scoring, and scenario templates.
4. **Check the prompting frameworks** – documentation in [`Docs/`](Docs/) captures reusable rules, merge fields, and realtime prompting guidance.

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
│   ├── Conversation AI Guide
│   ├── merge-fields.md
│   ├── post-types-framework.yaml
│   ├── realtime-prompting-guide.md
│   └── social-proof-types.yaml
├── Voice Agent/
│   ├── Finanzberater Coach AI.md
│   ├── Vivi KI Voice AI.md
│   └── Vivi KI Voice AI (FULL BACKUP).md
├── Conversation Agent/
│   └── Vivi KI Conversation AI
└── Knowledge Base/
    ├── Kunden/
    │   └── Vivi KI Knowledge.md
    └── Partner/
```

## Agent Playbooks

### Voice Agents
- **Vivi KI Voice** – Professional front-office assistant focused solely on structured data capture for callbacks. Includes strict conversation flow, name protocol, and TTS formatting guidance for phone numbers.
- **Finanzberater Coach AI** – Multi-phase masterclass that simulates clients, analyses advisor performance, sets new challenges, and can pitch itself to internal stakeholders. Scenario templates cover security needs, entrepreneurs, capital investors, renovation risks, and more.

### Conversation Agents (Text-Based)
- **Vivi KI Conversation** – Text-based version using Conversation AI V3 structure with three fields: Personality (agent character and tone), Goal (primary objectives and flow), and Additional Information (safety rules and constraints).

## Documentation & Frameworks
- **Prompting Fundamentals** – [`Docs/ai-prompting-framework.yaml`](Docs/ai-prompting-framework.yaml) and [`Docs/bot-goals-framework.yaml`](Docs/bot-goals-framework.yaml) define global prompting principles and measurable agent goals, updated for Conversation AI V3.
- **Realtime Voice Best Practices** – [`Docs/realtime-prompting-guide.md`](Docs/realtime-prompting-guide.md) condenses OpenAI's realtime API guidance into actionable checklists.
- **Marketing & Social Proof** – [`Docs/post-types-framework.yaml`](Docs/post-types-framework.yaml) and [`Docs/social-proof-types.yaml`](Docs/social-proof-types.yaml) capture the core content archetypes used across campaigns.
- **Merge Fields Reference** – [`Docs/merge-fields.md`](Docs/merge-fields.md) lists GoHighLevel merge fields for consistent CRM sync.

## Conversation AI V3 Structure
Current conversation agents use a three-field configuration:
- **Personality**: Agent character, tone, background, and behavioral guidelines
- **Goal**: Primary objectives, success criteria, and conversation flow
- **Additional Information**: Safety rules, escalation procedures, tool usage, and examples

This structure maps to the classic prompting framework (Role → Personality, Task → Goal, Guidelines → Additional Information) while optimizing for the LeadConnector interface.

## 📋 Wie verwende ich diese Prompts?

### Schritt 1: Prompt kopieren
- Klicke auf einen der direkten Links oben
- Markiere den gesamten Text der Datei (Strg+A oder Cmd+A)
- Kopiere den Text (Strg+C oder Cmd+C)

### Schritt 2: In dein System einfügen
**Für Conversation AI V3 (LeadConnector):**
- **Personality Feld:** Alles aus dem "Personality:" Bereich
- **Goal Feld:** Alles aus dem "Goal:" Bereich  
- **Additional Information Feld:** Alles aus dem "Additional Information:" Bereich

**Für andere AI-Systeme:**
- Füge den kompletten Prompt-Text ein
- Passe bei Bedarf die Namen und Unternehmensdaten an

### Schritt 3: Testen
- Führe einen Testlauf durch
- Prüfe, ob der Agent wie gewünscht reagiert
- Bei Bedarf kleine Anpassungen vornehmen

## Workflow & Collaboration
- Treat each prompt as code: make atomic changes, review diffs, and keep backups in respective directories when experimenting.
- Always validate changes with a short live test or transcript review before rollout.
- Document new scenarios, challenges, or safety rules directly in the relevant files so agents inherit the behaviour instantly.
- For conversation agents: Test each field modification independently to identify impact on performance.

## Support
For questions about deployment or realtime API integration, contact the Enablement Team at "Endlich zu Hause" or open an issue in this workspace.
