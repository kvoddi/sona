# Documentation Quick Reference Cards

## Card 1: Diátaxis Quick Guide

### What Type of Documentation Should I Write?

| If you need to... | Write a... | Key Characteristics |
|-------------------|------------|---------------------|
| **Teach a beginner** | **TUTORIAL** | • Step-by-step<br>• Guaranteed success<br>• Learning by doing<br>• "Getting Started with..." |
| **Solve a problem** | **HOW-TO** | • Task-focused<br>• Assumes knowledge<br>• Multiple approaches<br>• "How to..." |
| **Look up information** | **REFERENCE** | • Factual<br>• Structured<br>• Comprehensive<br>• API docs, configs |
| **Understand concepts** | **EXPLANATION** | • Theoretical<br>• Background<br>• Design decisions<br>• "Understanding..." |

### Quick Test: Am I Writing the Right Type?

**Tutorials**
- ✅ Can a beginner follow this exactly?
- ✅ Will it work every time?
- ❌ No options or alternatives

**How-To Guides**
- ✅ Does it solve a specific problem?
- ✅ Can readers adapt it to their needs?
- ❌ No lengthy explanations

**Reference**
- ✅ Just the facts
- ✅ Complete information
- ❌ No instructions or opinions

**Explanation**
- ✅ Answers "why" questions
- ✅ Discusses concepts
- ❌ No step-by-step instructions

---

## Card 2: Where to Document

### Platform Decision Tree

```
What are you documenting?
├─> Technical platform docs? → Docusaurus
├─> Code/configs? → GitLab
├─> Official policy? → Policy Hub
├─> Corporate/HR? → SharePoint
└─> Team/project work? → Confluence
```

### Quick Platform Guide

| Platform | Use For | Don't Use For |
|----------|---------|---------------|
| **Docusaurus** | • User guides<br>• API docs<br>• Architecture | • Meeting notes<br>• Drafts |
| **Confluence** | • Project docs<br>• Team wikis<br>• RFCs | • Final tech docs<br>• Code |
| **GitLab** | • READMEs<br>• Code docs<br>• CI/CD docs | • User guides<br>• Policies |
| **SharePoint** | • HR docs<br>• Forms<br>• Presentations | • Tech docs<br>• Code |
| **Policy Hub** | • Policies<br>• Standards<br>• Compliance | • How-tos<br>• Code |

---

## Card 3: Documentation Checklist

### Before You Write
- [ ] Identify the Diátaxis type (Tutorial/How-To/Reference/Explanation)
- [ ] Choose the right platform
- [ ] Check if documentation already exists
- [ ] Define your audience
- [ ] Gather technical details

### While Writing
- [ ] Follow the Diátaxis structure for your type
- [ ] Use clear, descriptive headings
- [ ] Include all prerequisites
- [ ] Test all commands/code
- [ ] Add examples where helpful
- [ ] Keep language simple and direct

### Before Publishing
- [ ] Technical review completed
- [ ] All links work
- [ ] Metadata added (owner, date, version)
- [ ] No sensitive information exposed
- [ ] Spell check passed
- [ ] Peer reviewed

### After Publishing
- [ ] Announce to relevant teams
- [ ] Add to documentation index
- [ ] Monitor initial feedback
- [ ] Schedule quarterly review

---

## Card 4: Documentation Owner Responsibilities

### As a Document Owner, You Must:

**Weekly**
- Monitor feedback and questions
- Fix critical errors immediately

**Monthly**
- Review for accuracy
- Update based on platform changes
- Check all links

**Quarterly**
- Comprehensive review
- Update version information
- Validate all examples
- Review user feedback

**On Platform Release**
- Update affected documentation
- Test all examples
- Update version compatibility
- Communicate changes

### Escalation Path
1. **Day 1**: Document Owner responds
2. **Day 2**: Platform Owner involved
3. **Day 3**: Platform Engineering Lead
4. **Weekly**: Architecture Review Board

---

## Card 5: Writing Best Practices

### The Golden Rules

**BE CLEAR**
- Define acronyms on first use
- Use simple language
- One idea per paragraph

**BE PRECISE**
- Exact version numbers
- Full commands
- Complete error messages

**BE CONSISTENT**
- Standard terminology
- Same formatting
- Naming conventions

**BE SCANNABLE**
- Descriptive headings
- Bullet points for lists
- Code blocks for commands
- Bold key information

### Common Anti-Patterns to Avoid

❌ **Don't Mix Types**
- Tutorials with deep explanations
- How-tos with theory
- Reference with instructions

❌ **Don't Assume**
- Reader's environment
- Previous knowledge
- Access levels

❌ **Don't Forget**
- Version information
- Prerequisites
- Clean-up steps

❌ **Don't Create**
- Duplicate documentation
- Circular references
- Dead links

---

## Card 6: Metrics & Success

### What We Measure

**Usage**
- Page views
- Search success rate
- Time on page

**Quality**
- Coverage %
- Update frequency
- Error reports

**Impact**
- Support ticket reduction
- User satisfaction
- Time to productivity

### Success Targets

| Metric | Target |
|--------|---------|
| Feature Coverage | 90% |
| Quarterly Reviews | 95% |
| User Satisfaction | 4/5 |
| Support Reduction | 30% |
| Find Time | < 2 min |

### Red Flags
🚩 No updates in 6 months
🚩 High bounce rate
🚩 Repeated support tickets
🚩 Failed searches
🚩 User complaints

---

## Card 7: Migration Guide

### Moving Documentation

| From → To | When |
|-----------|------|
| Confluence → Docusaurus | Tech docs are final |
| Confluence → Policy Hub | Process becomes policy |
| GitLab Wiki → Docusaurus | Scope expands beyond repo |
| SharePoint → Docusaurus | Tech docs misplaced |

### Migration Steps
1. **Audit** existing content
2. **Categorize** by Diátaxis type
3. **Convert** to new format
4. **Review** for accuracy
5. **Redirect** old locations
6. **Archive** old content
7. **Update** all references

---

## Card 8: Emergency Updates

### When to Update Immediately

🚨 **Critical Issues**
- Security vulnerabilities
- Data loss risks
- Breaking changes
- Major errors

### Fast Track Process
1. Make changes immediately
2. Tag as "URGENT"
3. Get any available reviewer
4. Deploy within 1 hour
5. Full review within 48 hours
6. Document lessons learned

### Who to Contact
- **Technical Emergency**: Platform On-Call
- **Documentation System**: Platform Owner
- **Can't reach anyone**: Team Lead

---

## Print-Ready Format

*These cards are designed to be:*
- *Printed as desk references*
- *Shared in Slack*
- *Bookmarked for quick access*
- *Used in onboarding*

*Keep them handy for daily documentation work!*