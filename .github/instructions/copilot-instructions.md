
# Copilot Instructions for AI Coding Agents

This codebase manages AI-driven voice and conversation agents for "Endlich zu Hause Finanzierungen GmbH" customer support automation. The architecture prioritizes machine-readable documentation and strict agent behavior guidelines.

## 1. Core Architecture

### Agent Configuration Pattern
- **Primary Agent**: `Voice Agent/Vivi KI Voice AI.md` - Contains complete agent persona, objectives, and call flow scripts
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

## 3. YAML Framework Integration

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

## 4. Development Patterns

### File Organization
- Agent configurations: Markdown format in `Voice Agent/`
- Business frameworks: YAML format in `Docs/`
- Each YAML includes `metadata` section with purpose and optimization info

### Agent Logic Extensions
- When adding new agents, follow the strict constraint model from `Vivi KI Voice AI.md`
- Document tool triggers and callback behaviors explicitly
- Reference appropriate YAML frameworks for business context

### Integration Guidelines
- All external integrations must be documented with explicit information boundaries
- Use structured YAML for any new business logic or customer psychology frameworks
- Maintain machine-readable format for AI agent consumption

## 5. Key Files for Context
- `Voice Agent/Vivi KI Voice AI.md`: Complete agent implementation example
- `Docs/ai-prompting-framework.yaml`: Technical prompting guidelines
- `Docs/social-proof-types.yaml`: Customer psychology reference
- `README.md`: Project overview and quick start guide

---

When modifying agent behavior, always reference the strict information boundaries and callback patterns established in the core voice agent configuration.
