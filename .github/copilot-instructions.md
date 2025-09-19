
# Copilot Instructions for AI Coding Agents

This codebase is organized for AI-driven voice and conversation agents, with a focus on customer support automation for "Endlich zu Hause Finanzierungen GmbH".

## 1. Workspace Structure
- `Docs/`: Contains business and feature documentation in AI-friendly YAML formats. Key files:
  - `social-proof-types.yaml`: Complete framework for 5 types of social proof implementation
  - `post-types-framework.yaml`: 6 fundamental post types for content strategy
  - `ai-prompting-framework.yaml`: Complete LeadConnector AI prompting framework with elements, best practices, and advanced techniques
  - `bot-goals-framework.yaml`: Detailed Bot Goals feature framework with step-by-step setup and multiple bot support
  - `conversation-ai-v3-setup.md`: Form-based AI setup guide (legacy markdown)
- `Voice Agent/`: Main source folder for agent logic. The key file is `Vivi KI Voice AI`, which contains agent role, objectives, and call flow scripts.
- `Conversation Agent/`: Reserved for future conversation AI expansion

## 2. Agent Logic & Call Flow
- The file `Voice Agent/Vivi KI Voice AI` defines the agent's role, objectives, and strict call handling rules:
	- Always gather caller name and reason for call.
	- Confirm names by spelling out each character ("That's John, J O H N, right?").
	- If caller's query matches a tool trigger, use the tool immediately.
	- If not, assure a callback and do not suggest external sources.
	- Never ask for extra details or repeat sentences verbatim.
	- Only use information provided in prompts or tool instructions—do not infer or add details.

## 3. Developer Workflows
- No build/test scripts or package manifests detected. If you add code, document new workflows in `README.md` or a dedicated setup file.
- For Python/Node.js, use standard environment setup unless project-specific instructions are found in `Voice Agent/Vivi KI Voice AI`.

## 4. Patterns & Conventions
- Modular organization by agent type or feature is expected.
- Use descriptive naming aligned with business documentation.
- Summarize external API endpoints and authentication flows in code comments when integrating.

## 5. Integration Points
- Business logic and content strategy patterns are documented in structured YAML files in `Docs/`
- All documentation optimized for machine parsing and AI agent consumption
- Reference structured files for content strategy, social proof implementation, and customer psychology frameworks
- LeadConnector platform integration guidelines in YAML format for consistent data structure
- YAML-first approach ensures consistent, parseable, and machine-optimized documentation

## 6. Updating Instructions
- If you discover new conventions, workflows, or integration patterns, update this file and notify maintainers.

---

For questions or missing context, request feedback from the user to clarify project-specific practices.
