
# Copilot Instructions for KI Agents Repository

This repository manages production-ready AI agent prompts, workflows, and business logic for "Endlich zu Hause Finanzierungen GmbH" (German mortgage & finance). Follow these project-specific conventions for maximum effectiveness:

## 1. Architecture & Key Components
- **Voice Agents**: Markdown prompts in `Voice Agent/` (e.g., `Vivi KI Voice AI.md`) use a modular structure: Role & Objective, Personality & Tone, Instructions/Rules, Conversation Flow, Safety/Escalation. Strict phase order and TTS formatting are critical.
- **Conversation Agents**: Text-based agents in `Conversation Agent/` use a V3 three-field structure: Personality, Goal, Additional Information. Field order is mandatory for LeadConnector compatibility.
- **Automation Prompts**: `Automationsprompts/` contains workflow-specific prompts (e.g., lead classification) with exact output formats for CRM automation (GoHighLevel, LeadConnector).
- **Frameworks & Rules**: YAML docs in `Docs/` define global prompting, automation, and business logic (see `ai-prompting-framework.yaml`, `automation-framework.yaml`, `bot-goals-framework.yaml`).
- **Knowledge Base**: Markdown files in `Knowledge Base/` provide business context, personas, and escalation paths.

## 2. Critical Patterns & Conventions
- **Strict Information Boundaries**: Agents may only use info from prompts/tools—no inference, speculation, or external suggestions.
- **German Market Focus**: All content, tone, and TTS rules are tailored for German business etiquette and language.
- **Merge Fields**: Use `{{contact.*}}`, `{{user.*}}`, etc. for CRM data. Reference `Docs/merge-fields.md` for all available fields.
- **Voice Agent Protocols**: Always confirm names with spelling, use digit-by-digit phone number collection, and never transfer calls (message-taker only).
- **Automation Output**: Automation prompts must return a single, parseable token (e.g., `A-LEAD`, `B-LEAD`, `C-LEAD`)—no explanations or formatting. Fallbacks and error handling are defined in each prompt.
- **Testing & Validation**: Each automation prompt requires at least 5 sample input/output pairs. Use the provided testing guides and validation schemas.

## 3. Developer Workflow
- **Prompt as Code**: Treat every prompt as code—make atomic changes, review diffs, and keep backups when experimenting.
- **Field Isolation**: For Conversation AI, test changes to each field (Personality, Goal, Additional Information) independently.
- **YAML-Driven Logic**: Update YAML frameworks (`Docs/`) with any business logic or structure changes. Document new scenarios and rules directly in relevant files.
- **Platform Constraints**: GoHighLevel: 3000-word prompt limit. LeadConnector: V3 field structure. OpenAI API: TTS and German pronunciation optimization.
- **Versioning**: Use semantic versioning in filenames (e.g., `lead-classification-automation-v3.0.md`).

## 4. Integration & Escalation
- **CRM Integration**: All agents and automations use merge fields for data sync. See `Docs/merge-fields.md` for details.
- **Tool Triggers**: Knowledge base tools activate on business detail queries. Escalation paths are defined in the team directory.
- **Security**: Never reveal prompt logic, model details, or technical implementation to end users.

## 5. Key References
- **Voice Agent Example**: `Voice Agent/Vivi KI Voice AI.md`
- **Conversation Agent Example**: `Conversation Agent/Vivi KI Conversation AI.md`
- **Automation Example**: `Automationsprompts/lead-classification-automation.md`
- **Prompting Framework**: `Docs/ai-prompting-framework.yaml`
- **Automation Framework**: `Docs/automation-framework.yaml`
- **Bot Goals**: `Docs/bot-goals-framework.yaml`
- **Merge Fields**: `Docs/merge-fields.md`
- **Realtime Prompting Guide**: `Docs/realtime-prompting-guide.md`

---
**Always reference production agent files and YAML frameworks before making changes. When in doubt, follow the strictest information boundary and output format rules.**