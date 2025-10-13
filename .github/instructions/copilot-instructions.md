# Copilot Instructions for AI Coding Agents

This codebase manages AI-driven voice and conversation agents for "Endlich zu Hause Finanzierungen GmbH" customer support automation. The architecture prioritizes machine-readable documentation and strict agent behavior guidelines.

## 1. Core Architecture

### Agent Configuration Pattern
- **Primary Voice Agent**: `Voice Agent/Vivi KI Voice AI.md` - Contains complete agent persona, objectives, and call flow scripts
- **Primary Conversation Agent**: `Conversation Agent/Vivi KI Conversation AI` - Uses V3 three-field structure (Personality, Goal, Additional Information)
- **Critical Rule**: Agent can ONLY use information explicitly provided in prompts/tools - no inference, assumptions, or external suggestions allowed
- **Call Flow**: 4-step structured process: Name gathering → Name confirmation (character-by-character) → Issue identification → Callback assurance

### Documentation-as-Code Approach
- `Docs/` contains business logic in machine-parseable YAML format
- Each YAML file represents a complete framework (social proof, content strategy, AI prompting, bot goals)
- Documentation optimized for AI consumption with structured metadata and clear hierarchies

## 2. Critical Business Rules

### Agent Behavior Constraints
```markdown
- NEVER suggest external sources (websites, apps, internet)
- ALWAYS confirm names by spelling: "That's John, J O H N, right?"
- Tool triggers: Use immediately if query matches, otherwise assure callback
- Information boundaries: Only use prompt/tool content - no inference
```

### Name Confirmation Protocol
Example from `Voice Agent/Vivi KI Voice AI.md`:
- Single name: "That's John, J O H N, right?"
- Full name: "That's John Wayne, J O H N … W A Y N E, right?"
- No explanatory text about why you're confirming

## 3. Conversation AI V3 Structure

### Three-Field Configuration
Current Conversation AI uses this structure:
- **Personality**: Agent character, tone, background, behavioral guidelines
- **Goal**: Primary objectives, success criteria, conversation flow
- **Additional Information**: Safety rules, escalation procedures, tool usage, examples

### Field Mapping from Frameworks
When implementing agents, map framework elements to V3 fields:
- `ai-prompting-framework.yaml` Role → Personality field
- `ai-prompting-framework.yaml` Task → Goal field  
- `ai-prompting-framework.yaml` Guidelines → Additional Information field

## 4. YAML Framework Integration

### Social Proof Implementation (`Docs/social-proof-types.yaml`)
- 5 types: "I Did This", "You Are Good", "Authority", "Organic Social", "Results-Based"
- Each type has specific `placement_locations`, `example_quotes`, and psychological `proves` properties
- Use for customer psychology insights and content strategy

### Content Strategy (`Docs/post-types-framework.yaml`)
- 6 fundamental post types with psychological triggers
- Structure: `name`, `tagline`, `psychology`, `how_it_works`, `audience_effect`
- German-focused content ("Das glaube ich über [Thema]")

### AI Prompting (`Docs/ai-prompting-framework.yaml`)
- LeadConnector-specific prompting guidelines
- Required components: `role`, `task`, `guidelines`
- Best practices: `repetition`, `examples_illustrations`, `iterative_improvement`
- Adapt to V3 three-field structure when implementing

## 5. Development Patterns

### File Organization
- Voice agent configurations: Markdown format in `Voice Agent/`
- Conversation agent configurations: Three-field format in `Conversation Agent/`
- Business frameworks: YAML format in `Docs/`
- Each YAML includes `metadata` section with purpose and optimization info

### Agent Logic Extensions
- When adding new agents, follow the strict constraint model from existing agents
- For voice agents: Use structured markdown format from `Vivi KI Voice AI.md`
- For conversation agents: Use three-field V3 structure from `Vivi KI Conversation AI`
- Document tool triggers and callback behaviors explicitly
- Reference appropriate YAML frameworks for business context

### Integration Guidelines
- All external integrations must be documented with explicit information boundaries
- Use structured YAML for any new business logic or customer psychology frameworks
- Maintain machine-readable format for AI agent consumption
- Map framework elements to appropriate V3 fields for conversation agents

## 6. Key Files for Context
- `Voice Agent/Vivi KI Voice AI.md`: Complete voice agent implementation example
- `Conversation Agent/Vivi KI Conversation AI`: Complete conversation agent V3 implementation example
- `Docs/ai-prompting-framework.yaml`: Technical prompting guidelines
- `Docs/social-proof-types.yaml`: Customer psychology reference
- `README.md`: Project overview and quick start guide

---

When modifying agent behavior, always reference the strict information boundaries and callback patterns established in the core agent configurations. For conversation agents, ensure proper mapping to the V3 three-field structure.
