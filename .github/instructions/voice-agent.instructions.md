---
applyTo: "Voice Agent/**"
---
# General Instructions for Voice Agents

You are working on prompts for **voice-based AI agents**. These agents interact with users via telephone and require special attention to clarity, flow, and tone. The primary reference for best practices is the **`realtime-prompting-guide.md`**.

## Core Principles for Voice Agents (from `realtime-prompting-guide.md`)
- **Structured Prompt**: Organize prompts into clear sections like `Role & Objective`, `Personality & Tone`, `Conversation Flow`, and `Safety & Escalation`.
- **Clarity is Key**: Use simple sentence structures and bullet points over paragraphs. Be precise and avoid ambiguity.
- **Define the Persona**: Every voice agent needs a clear persona, tone, pacing, and language constraints.
- **Guide with Examples**: Use sample phrases to guide the agent's style, but add a `Variety` rule to prevent robotic repetition.
- **Structured Dialogue**: Define the conversation flow with clear states, goals, and transitions.

## Potential Agent Tasks
This directory can contain prompts for various voice agent tasks, such as:
- **Data Collection Agents**: Like "Vivi KI", focused on accurately gathering information.
- **Training & Coaching Agents**: Designed to help team members practice conversations.
- **Complex Interaction Agents**: Using tools and state management for multi-step processes.

## Frameworks to Use
- **Primary Guide**: `.github/instructions/realtime-prompting-guide.md` is the main source for prompting techniques.
- **Prompt Structure**: Always use the `ai-prompting-framework.yaml` (Role, Task, Guidelines) as a basic foundation, which can be expanded with the more detailed sections from the realtime guide.
- **Core Business Rules**: The global rules in `copilot-instructions.md` apply to all agents.
