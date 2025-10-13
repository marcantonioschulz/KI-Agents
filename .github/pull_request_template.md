## 🎯 Pull Request Summary
<!-- Brief description of what this PR accomplishes -->

### Changes Made
- 
- 
- 

### Related Issues
<!-- Link to any related GitHub issues -->
Fixes #(issue number)
Relates to #(issue number)

## 🤖 Agent Changes
### Affected Agents
- [ ] Voice Agent (Vivi KI Voice AI)
- [ ] Conversation Agent (Vivi KI Conversation AI)
- [ ] Coaching Agent (Finanzberater Coach AI)
- [ ] Framework/Documentation only
- [ ] New agent: ___________

### Type of Change
- [ ] Bug fix (non-breaking change that fixes an issue)
- [ ] New feature (non-breaking change that adds functionality)
- [ ] Breaking change (fix or feature that would cause existing functionality to not work as expected)
- [ ] Documentation update
- [ ] Framework/configuration improvement
- [ ] Security enhancement

## 🧪 Testing Checklist

### Voice Agent Testing (if applicable)
- [ ] German TTS pronunciation tested and sounds natural
- [ ] Phone number pronunciation clear (digit-by-digit)
- [ ] All 4 conversation phases work correctly (Greeting → Identification → Discovery → Finalization)
- [ ] Name spelling confirmation works properly
- [ ] Information boundary enforcement tested (no external suggestions)
- [ ] Security deflection responses work for meta-queries
- [ ] Callback promises are appropriate (24 hours max)

### Conversation Agent Testing (if applicable)
- [ ] V3 three-field structure correctly implemented (Personality/Goal/Additional Information)
- [ ] CRM merge field variables work properly (e.g., `{{contact.last_name}}`)
- [ ] Goal achievement measurable and testable
- [ ] Information boundaries enforced (no inference or assumptions)
- [ ] Escalation procedures clearly defined
- [ ] LeadConnector compatibility verified

### Framework/Documentation Testing (if applicable)
- [ ] YAML files validate and parse correctly
- [ ] Metadata sections complete and accurate
- [ ] Machine-readable format maintained
- [ ] Cross-references to other files accurate
- [ ] Examples are realistic and anonymized
- [ ] German language accuracy verified (if applicable)

### Security Testing (Required for all PRs)
- [ ] No sensitive customer data or real information in examples
- [ ] Prompt injection attacks tested and mitigated
- [ ] Information boundary violations tested and prevented
- [ ] Security deflection responses appropriate
- [ ] Compliance with financial services regulations maintained

## 📋 Code Quality Checklist

### Documentation Standards
- [ ] All changes documented appropriately
- [ ] Examples include realistic but anonymized data
- [ ] Comments explain complex logic or business rules
- [ ] German language content reviewed for accuracy
- [ ] English language content clear and professional

### Configuration Standards
- [ ] Agent prompts follow established structure patterns
- [ ] Framework elements properly mapped to V3 fields (if applicable)
- [ ] Business context accurately reflected
- [ ] Team escalation procedures correctly defined
- [ ] Merge field usage consistent with CRM integration

### File Organization
- [ ] Files placed in correct directories
- [ ] Naming conventions followed consistently
- [ ] No duplicate or conflicting configurations
- [ ] Backup files removed or appropriately stored
- [ ] Related files updated for consistency

## 🔒 Security & Compliance Review

### Information Handling
- [ ] Customer data protection maintained
- [ ] Financial information handling appropriate
- [ ] Privacy regulations (GDPR) compliance verified
- [ ] Business confidentiality respected

### Agent Behavior
- [ ] No external resource suggestions (websites, apps, etc.)
- [ ] No inference beyond provided information
- [ ] Appropriate escalation to human agents
- [ ] Professional tone and German business culture alignment

## 🎨 User Experience Verification

### Conversation Quality
- [ ] Natural dialogue flow maintained
- [ ] Professional yet approachable tone
- [ ] Clear and actionable responses
- [ ] Appropriate use of German formality (Sie/Du)
- [ ] Consistent brand voice

### Technical Performance  
- [ ] Response times appropriate for real-time interaction
- [ ] Error handling graceful and user-friendly
- [ ] Edge cases considered and handled
- [ ] Integration points tested and functional

## 📚 Additional Context
<!-- Any additional information that reviewers should know -->

### Business Impact
<!-- How does this change impact business operations? -->

### Migration Notes
<!-- Any breaking changes or migration steps needed? -->

### Future Considerations
<!-- What should be considered in future iterations? -->

## 👥 Reviewer Guidelines
<!-- Instructions for reviewers -->

### Focus Areas for Review
- [ ] Technical accuracy of agent configurations
- [ ] Business logic alignment with company procedures
- [ ] Security and compliance adherence
- [ ] German language accuracy and cultural appropriateness
- [ ] Integration compatibility with existing systems

### Testing Recommendations
- [ ] Test with real-world scenarios from the knowledge base
- [ ] Verify information boundary enforcement
- [ ] Check TTS output quality (for voice agents)
- [ ] Validate V3 structure implementation (for conversation agents)

---

**Reviewer Checklist:**
- [ ] Code/configuration reviewed for quality and standards
- [ ] Testing checklist items verified
- [ ] Security implications assessed
- [ ] Documentation adequate and accurate
- [ ] Ready for deployment to production environment