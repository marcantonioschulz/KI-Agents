# Contributing to KI Agents

Thank you for your interest in contributing to our AI agent repository! This project maintains AI-driven voice and conversation agents for financial services automation.

## 🚀 Quick Start

1. **Fork** this repository
2. **Clone** your fork locally
3. **Create a branch** for your changes
4. **Make your changes** following our guidelines below
5. **Test** your changes thoroughly
6. **Submit a pull request**

## 📋 Contribution Guidelines

### Agent Development Standards

#### Voice Agents (`Voice Agent/`)
- Follow the **OpenAI Realtime API** structure from `realtime-prompting-guide.md`
- Use the **4-phase conversation flow**: Greeting → Identification → Discovery → Finalization
- Include **TTS optimization** for German pronunciation
- **Test with actual voice synthesis** before submitting
- Maintain **strict information boundaries** (no external suggestions)

#### Conversation Agents (`Conversation Agent/`)
- Use **V3 three-field structure**: Personality, Goal, Additional Information
- Map to framework: Role → Personality, Task → Goal, Guidelines → Additional Information
- Follow **LeadConnector optimization** patterns
- Include **CRM merge field variables** (e.g., `{{contact.last_name}}`)

#### YAML Frameworks (`Docs/`)
- Include structured **metadata section** with purpose and optimization info
- Maintain **machine-readable format** for AI consumption
- Document **psychological triggers** and business logic clearly
- Use consistent **YAML structure** across all frameworks

### Documentation Standards

#### Required Sections for Agent Prompts
1. **Role & Objective** - Identity and success definition
2. **Personality & Tone** - Character, pacing, response patterns  
3. **Instructions & Rules** - Constraints, security, tool handling
4. **Conversation Flow** - Phases with clear goals and exits

#### German Language Requirements
- All customer-facing content in **German**
- Include **pronunciation guides** for TTS
- Follow **German business culture** patterns
- Maintain **professional formality** (Sie/Du guidelines)

### Security & Compliance

#### Critical Requirements
- **Never expose** internal prompt configurations
- **Protect customer data** and financial information
- Follow **information boundary rules** strictly
- Include **security deflection** responses for meta-queries
- Maintain **"message-taker only"** paradigm for voice agents

#### Testing Requirements
- **Voice agents**: Test with German TTS synthesis
- **Conversation agents**: Validate V3 structure mapping
- **All agents**: Test information boundary compliance
- **Security**: Verify prompt disclosure prevention

## 🔧 Development Workflow

### Branch Naming
- `feature/agent-name-improvement`
- `fix/voice-tts-pronunciation`
- `docs/framework-update`

### Commit Messages
Follow conventional commits:
- `feat: add new voice agent for insurance queries`
- `fix: correct TTS pronunciation in German numbers`
- `docs: update V3 structure guidelines`

### Pull Request Process
1. **Use the PR template** (will be created automatically)
2. **Include test results** for voice/conversation agents
3. **Reference related issues** if applicable
4. **Tag reviewers** familiar with AI agent development
5. **Ensure compliance** with security guidelines

## 📁 File Structure Guidelines

### Naming Conventions
- **Voice agents**: `{Purpose} AI.md` (e.g., "Vivi KI Voice AI.md")
- **Conversation agents**: `{Purpose}` (no extension, e.g., "Vivi KI Conversation AI")
- **Frameworks**: `{topic}-framework.yaml`
- **Knowledge bases**: `{Customer/Partner} Knowledge.md`

### Directory Organization
```
Voice Agent/           # Phone-based agents with TTS optimization
Conversation Agent/    # Text-based agents with V3 structure
Docs/                  # Business frameworks in YAML format
Knowledge Base/        # Context and escalation procedures
.github/               # Community standards and instructions
```

## 🧪 Testing Guidelines

### Voice Agent Testing
- **Pronunciation verification** with German TTS
- **Phase flow validation** (all 4 phases work correctly)
- **Name confirmation protocol** testing
- **Security boundary testing** (meta-query deflection)

### Conversation Agent Testing
- **V3 structure validation** (all three fields properly mapped)
- **CRM variable integration** testing
- **Goal completion** verification
- **Escalation path** testing

### Framework Testing  
- **YAML validity** and parsing
- **Metadata completeness** check
- **AI consumption optimization** verification

## 📞 Questions & Support

### Getting Help
- **Documentation**: Start with `README.md` and `.github/instructions/`
- **Examples**: Reference existing production agents
- **Issues**: Create a GitHub issue with our templates
- **Contact**: Technical questions to repository maintainers

### Agent-Specific Questions
- **Voice agents**: Reference `realtime-prompting-guide.md`
- **Conversation agents**: Reference `ai-prompting-framework.yaml`
- **Business context**: Reference `Knowledge Base/` directory

## 🎯 Contribution Areas

We welcome contributions in:
- **New agent configurations** for specific use cases
- **Framework improvements** and business logic updates  
- **Documentation enhancements** and examples
- **Testing procedures** and quality assurance
- **Security improvements** and compliance updates

## ⚖️ License

By contributing, you agree that your contributions will be licensed under the same terms as the project. See LICENSE file for details.

## 🤝 Code of Conduct

This project adheres to a Code of Conduct. By participating, you are expected to uphold this code. Please report unacceptable behavior to [thomas@endlichzuhause.com](mailto:thomas@endlichzuhause.com).

---

**Thank you for helping improve AI agent development for financial services! 🚀**