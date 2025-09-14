# Documentation Platform Selection Guide

## Purpose

This guide helps teams determine the appropriate platform for different types of documentation. While formal governance is still evolving, this document provides practical guidance to reduce documentation fragmentation and improve discoverability.

## Current State

Our organization currently uses multiple documentation platforms, each with different strengths and use cases. Without clear guidelines, teams often struggle with where to document, leading to:
- Duplicate documentation across platforms
- Difficulty finding information
- Inconsistent user experience
- Maintenance overhead

This guide provides a decision framework to help teams make consistent choices about documentation placement.

## Available Platforms

### Platform Overview

| Platform | Primary Purpose | Best For | Avoid For |
|----------|----------------|----------|-----------|
| **Docusaurus** | Technical product documentation | Developer docs, APIs, technical guides | Temporary content, discussions |
| **Confluence** | Collaboration and knowledge sharing | Project docs, meeting notes, team wikis | Source code, API references |
| **GitLab** | Code-adjacent documentation | README files, contribution guides, code comments | Non-technical documentation |
| **SharePoint** | Corporate documents and policies | HR docs, policies, forms, presentations | Technical documentation |
| **Internal Policy Hub** | Governance and compliance | Official policies, standards, procedures | Technical how-tos, code |

## Decision Framework

### Primary Decision Tree

```
Start Here: What type of content are you documenting?
│
├─> Is it technical documentation about a platform/product?
│   │
│   ├─> Is it user-facing technical documentation?
│   │   └─> ✅ Docusaurus (tutorials, how-tos, references, explanations)
│   │
│   └─> Is it code or directly related to code?
│       └─> ✅ GitLab (README, CONTRIBUTING, inline docs)
│
├─> Is it organizational or policy documentation?
│   │
│   ├─> Is it an official policy, standard, or compliance document?
│   │   └─> ✅ Internal Policy Hub
│   │
│   └─> Is it a general corporate document (HR, admin, forms)?
│       └─> ✅ SharePoint
│
└─> Is it project or team collaboration content?
    │
    ├─> Is it temporary or discussion-based?
    │   └─> ✅ Confluence (meeting notes, project plans, RFCs)
    │
    └─> Will it eventually become formal documentation?
        └─> ✅ Start in Confluence → Migrate to appropriate platform
```

## Detailed Platform Guidelines

### Docusaurus - Technical Documentation Platform

**Use Docusaurus for:**
- Infrastructure platform documentation (following Diátaxis framework)
- API documentation and references
- Technical tutorials and how-to guides
- Architecture explanations and diagrams
- Integration guides
- Troubleshooting guides
- Technical FAQs
- Release notes and changelogs

**Characteristics:**
- Version controlled
- Developer-friendly (Markdown)
- Searchable
- Public or internal facing
- Long-lived content
- Structured navigation

**Do NOT use for:**
- Meeting minutes
- Project planning documents
- Temporary or draft content
- Non-technical policies
- Team discussions

### Confluence - Collaboration Hub

**Use Confluence for:**
- Project documentation and plans
- Meeting notes and decisions
- Team wikis and knowledge bases
- RFC (Request for Comments) documents
- Sprint retrospectives
- Onboarding checklists (non-technical)
- Process workflows
- Draft documentation before formalization
- Cross-team collaboration documents

**Characteristics:**
- Easy collaborative editing
- Rich formatting options
- Comments and discussions
- Page hierarchy
- Temporary to semi-permanent content

**Do NOT use for:**
- Final technical documentation (move to Docusaurus)
- Source code (use GitLab)
- Official policies (use Internal Policy Hub)
- Long-term technical references

### GitLab - Code Repository Documentation

**Use GitLab for:**
- README files
- CONTRIBUTING guidelines
- LICENSE information
- Code comments and documentation
- CI/CD pipeline documentation
- Docker/Kubernetes manifests with comments
- Configuration file documentation
- Issue and merge request templates
- Code review guidelines

**Characteristics:**
- Lives with the code
- Version controlled with code
- Markdown support
- Developer workflow integrated
- Branch-specific documentation

**Do NOT use for:**
- Extensive user documentation (use Docusaurus)
- Non-code related documentation
- Corporate policies
- Meeting notes

### SharePoint - Corporate Documentation

**Use SharePoint for:**
- HR policies and procedures
- Administrative forms and templates
- Department presentations
- Training materials (non-technical)
- Organizational charts
- Business continuity plans
- Corporate communications
- Budget and financial documents
- Legal documents and contracts

**Characteristics:**
- Microsoft Office integration
- Corporate access controls
- Document libraries
- Workflow capabilities
- Non-technical audience

**Do NOT use for:**
- Technical documentation
- Code or configurations
- Developer guides
- API documentation

### Internal Policy Hub - Governance Platform

**Use Internal Policy Hub for:**
- Information security policies
- Compliance standards (SOC2, ISO, etc.)
- Regulatory requirements
- Audit procedures
- Risk management documentation
- Data governance policies
- Change management procedures
- Service level agreements (SLAs)
- Disaster recovery plans

**Characteristics:**
- Formal approval workflows
- Audit trail
- Version control with approval history
- Compliance tracking
- Policy attestation

**Do NOT use for:**
- Technical how-to guides
- Team collaboration
- Code documentation
- Informal processes

## Migration Scenarios

### When to Migrate Documentation

| From | To | When |
|------|-----|------|
| Confluence | Docusaurus | Technical documentation is finalized and ready for users |
| Confluence | Internal Policy Hub | Process becomes official policy |
| GitLab Wiki | Docusaurus | Documentation scope expands beyond single repository |
| SharePoint | Docusaurus | Technical documentation was misplaced |
| Confluence | SharePoint | Project documents become corporate archives |

### Migration Process

1. **Identify** content that belongs elsewhere
2. **Prepare** content for new platform format
3. **Migrate** with proper formatting and structure
4. **Redirect** from old location to new
5. **Archive** or delete old content
6. **Update** all references and links

## Special Cases

### Cross-Platform Documentation

Some documentation may legitimately exist in multiple places:

| Content Type | Primary Location | Secondary Location | Reason |
|--------------|-----------------|-------------------|---------|
| API Getting Started | Docusaurus | GitLab README | Developers expect README |
| Security Policies | Internal Policy Hub | Docusaurus (summary) | Developers need awareness |
| Architecture Decisions | Docusaurus | Confluence (discussion) | Discussion → Documentation |
| Runbooks | Docusaurus | GitLab (scripts) | Documentation + Implementation |

### Handling Ambiguity

When uncertain about placement:

1. **Consider the primary audience**
   - Developers → Docusaurus or GitLab
   - Business users → SharePoint or Confluence
   - Compliance/Audit → Internal Policy Hub

2. **Consider the content lifecycle**
   - Temporary → Confluence
   - Long-lived → Docusaurus or Policy Hub
   - Archived → SharePoint

3. **Consider the update frequency**
   - Frequent updates → GitLab or Confluence
   - Stable content → Docusaurus or Policy Hub
   - Historical record → SharePoint

4. **When still uncertain**
   - Start in Confluence
   - Gather feedback
   - Move to appropriate platform once clear

## Search and Discovery

### Making Documentation Findable

Regardless of platform:

1. **Use descriptive titles** that include key search terms
2. **Add metadata** (tags, categories, labels) where available
3. **Create cross-references** between related documents
4. **Maintain a central index** of where different documentation lives
5. **Use consistent naming conventions** across platforms

### Central Documentation Index

Consider maintaining a simple index in Confluence or Docusaurus:

```markdown
# Documentation Index

## Platform Documentation
- **OpenShift**: [Docusaurus - OpenShift Docs]
- **Vault**: [Docusaurus - Vault Docs]
- **VMware**: [Docusaurus - VMware Docs]

## Policies and Standards
- **Security Policies**: [Internal Policy Hub]
- **Development Standards**: [Internal Policy Hub]

## Team Resources
- **Onboarding**: [Confluence - New Hire Wiki]
- **Meeting Notes**: [Confluence - Team Space]

## Code and Scripts
- **Automation Scripts**: [GitLab - infrastructure-automation]
- **CI/CD Templates**: [GitLab - pipeline-templates]
```

## Common Anti-Patterns

### What NOT to Do

1. **Don't duplicate** - Avoid maintaining the same content in multiple places
2. **Don't use email** - Documentation in email is lost immediately
3. **Don't use chat** - Slack/Teams is for discussion, not documentation
4. **Don't use personal drives** - Documentation must be team-accessible
5. **Don't mix platforms** - Keep related documentation together
6. **Don't forget to redirect** - Always leave pointers when moving content

## Quick Decision Matrix

| I need to document... | Platform | Why |
|----------------------|----------|-----|
| How to deploy to our platform | Docusaurus | Technical user guide |
| Team retrospective notes | Confluence | Team collaboration |
| Deployment script | GitLab | Lives with code |
| HR leave policy | SharePoint | Corporate document |
| Data retention policy | Internal Policy Hub | Compliance requirement |
| Architecture design | Docusaurus | Technical explanation |
| Project timeline | Confluence | Project management |
| API endpoint reference | Docusaurus | Technical reference |
| Budget spreadsheet | SharePoint | Business document |
| Security standards | Internal Policy Hub | Official policy |

## Future Considerations

### Platform Consolidation

While we currently use multiple platforms, consider future consolidation:
- Reduce platform sprawl
- Improve search capabilities
- Simplify access management
- Reduce licensing costs

### Evaluation Criteria for Platform Changes

Before adding new platforms or consolidating:
1. Does it solve a real gap?
2. Will it reduce complexity?
3. Is there user demand?
4. Can we migrate existing content?
5. Is it sustainable long-term?

## Getting Help

### Platform Support Contacts

- **Docusaurus**: Platform Engineering Team
- **Confluence**: IT Collaboration Team
- **GitLab**: DevOps Team
- **SharePoint**: Corporate IT
- **Internal Policy Hub**: Governance Team

### Documentation Questions

If you're unsure where to document:
1. Check this guide
2. Ask in #documentation Slack channel
3. Consult with your team lead
4. Default to Confluence and refine later

## Conclusion

Choosing the right documentation platform ensures information is discoverable, maintainable, and valuable. While we work with multiple platforms, following these guidelines will reduce fragmentation and improve the documentation experience for everyone.

Remember: **It's better to document in the "wrong" place than not document at all.** You can always migrate later.

---

*Document Version: 1.0*  
*Last Updated: [DATE]*  
*Owner: Platform Engineering Architecture*  
*Review Cycle: Semi-Annual*