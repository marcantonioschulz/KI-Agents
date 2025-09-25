# Realtime Prompting Guide

This guide distills OpenAI's realtime prompting recommendations so voice agents stay responsive, natural, and precise.

## Overview
- GPT Realtime delivers high-fidelity speech-to-speech conversations with stronger tool usage, instruction following, and expressive delivery.
- The goal is to reduce latency, avoid chained prompts, and keep responses human sounding.
- Structure your system prompts so the model can navigate them like a playbook.

## General Tips
- Iterate relentlessly; small wording adjustments can unlock large behavioral gains.
- Prefer short bullets over long paragraphs to make rules scannable.
- Lead with examples; the model mirrors sample phrases closely.
- Pin the output language explicitly if the model drifts.
- Use a "Variety" rule to curb repetitive acknowledgements.
- Convert abstract guardrails into natural-language rules (e.g., "IF MORE THAN THREE FAILURES THEN ESCALATE").

## Prompt Structure Blueprint
Keep prompts modular so you can edit individual sections without breaking the rest.

```
# Role & Objective         — who you are and what success means
# Personality & Tone       — voice, pacing, verbosity
# Context                  — retrieved knowledge or CRM data
# Reference Pronunciations — phonetic guides for tricky words
# Tools                    — names, triggers, preambles
# Instructions / Rules     — do's, don'ts, escalation logic
# Conversation Flow        — ordered phases with goals & exits
# Safety & Escalation      — fallback behaviors and handoff criteria
```

## Role & Objective
- Pin the agent's identity and the definition of "done" in the first section.
- Tailor the wording to your domain (e.g., empathetic coach, compliance-focused expert).
- Example: `You are a French-Canadian customer support bot. Answer in Quebec French.`

## Personality, Tone & Pace
- Define personality, tone, and default response length separately.
- For multi-emotion behaviors, list the mood sequence explicitly.
- To speed up speech, combine shorter sentences with pacing cues instead of relying on the `speed` parameter alone.
- Sample instruction:
  - Personality: "Friendly, calm, approachable expert."
  - Tone: "Warm, concise, confident."
  - Length: "1–2 sentences per turn." 
  - Pacing: "Use brief pauses (`...`) after key digits or product names."

## Language Control
- Force a target language when the model might switch mid-call.
- Example: `Antworte ausschließlich auf Deutsch. Wenn du einen fremdsprachigen Begriff zitierst, erkläre ihn auf Deutsch.`

## Reducing Repetition
- Add a dedicated "Variety" rule: "Vermeide identische Formulierungen für Bestätigungen; nutze mindestens drei Varianten."
- Provide two or three alternative sample responses the model can rotate through.

## Reference Pronunciations
- List tricky brand names, towns, or abbreviations with simple phonetic hints.
- Example: `"LeadConnector" – sprich „LIED-Ko-nnek-tor“.`
- For alphanumeric IDs, specify digit-by-digit pronunciation and ask callers to confirm.

## Instructions Quality Checklist
Before shipping a prompt revision, confirm:
- Role, objective, and tone are defined in separate sections.
- Every rule is actionable (no vague "be better" statements).
- Safety, compliance, and escalation paths are explicit.
- Tool usage covers triggers *and* the expected spoken preamble.
- Output format expectations (summary, score, closing) are defined.

## Tools & Tool Calls
- Document each tool with: purpose, input schema, mandatory preamble, and whether confirmation is required.
- Note when to call a tool proactively versus on request.
- If the agent must narrate tool usage, include the exact phrasing (e.g., "Einen Moment, ich prüfe das im System...").

## Conversation Flow Patterns
- Lay out phases with clear goals, entry, and exit conditions.
- Provide example dialogues for each phase so the agent understands pacing.
- For advanced flows, describe the states like a miniature state machine (e.g., `Greeting → Discover → Diagnose → Resolve → Close`).
- Include sample phrases to model empathy, clarification, and closing language.

## Safety & Escalation
- Define what counts as abuse, how to pause or end the call, and how to promise follow-up.
- Give fallback scripts for unclear or low-quality audio (e.g., request repetition up to twice, then schedule callback).
- Clarify when to escalate to a human versus when to provide a neutral closing.

## Putting It Together
When iterating on voice prompts:
1. Update one section at a time and test in production-like conditions.
2. Log turn-by-turn transcripts to spot breakdowns quickly.
3. Annotate failures with the rule or example that should be refined.
4. Keep a backup of major prompt versions so you can roll back quickly.

A disciplined structure plus scenario-driven examples ensure your realtime agents sound natural, stay on brand, and handle complex tool workflows reliably.
