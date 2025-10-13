---
applyTo: "Conversation Agent/**"
---
# General Instructions for Conversation Agents

You are working on prompts for **text-based conversation agents** (chatbots). These agents are generally more interactive than voice agents and are designed to guide users toward specific goals.

## Core Principles for Conversation Agents
- **Goal-Oriented Design**: Every conversation should have a clear purpose. This could be lead qualification, appointment booking, customer support, or user onboarding. Define the goal at the start of the prompt.
- **Interactivity**: Leverage text-based features like buttons, quick replies, and links to make the conversation efficient and user-friendly.
- **Flexible Flow**: Unlike rigid voice scripts, chatbot conversations can be more dynamic. The prompt should account for different user paths and questions, always guiding the user back to the primary goal.
- **Persona and Tone**: Define a consistent persona. Is the agent purely functional, or should it be more conversational and brand-aligned?

## Conversation AI V3 Structure
The current Conversation AI uses a **three-field structure**:
- **Personality**: Define the agent's character, tone, background, and behavioral guidelines
- **Goal**: Specify the primary objective and success criteria for conversations
- **Additional Information**: Include supporting details, escalation rules, and supplementary instructions

## Potential Agent Tasks
This directory can contain prompts for various chatbot tasks, such as:
- **Lead Qualification Bots**: Asking questions to determine if a user is a good fit.
- **Appointment Booking Bots**: Integrating with calendars to schedule meetings.
- **FAQ & Support Bots**: Answering common questions and creating support tickets.

## Frameworks to Use
- **Bot Goals**: The `bot-goals-framework.yaml` is the primary guide for defining what an agent should achieve.
- **Prompt Structure**: Use the `ai-prompting-framework.yaml` (Role, Task, Guidelines) to structure all prompts, adapted to the V3 three-field format.
- **Psychological Context**: For marketing or sales-focused bots, consider using principles from `social-proof-types.yaml` and `post-types-framework.yaml` to build trust.
- **Core Business Rules**: The global rules in `copilot-instructions.md` apply here as well.

## V3 Field Mapping
When creating conversation agents, map the framework elements to V3 fields:
- **Personality Field**: Role definition, persona, tone, behavioral constraints
- **Goal Field**: Primary objectives, success metrics, conversation flow
- **Additional Information Field**: Safety rules, escalation procedures, tool usage, examples
