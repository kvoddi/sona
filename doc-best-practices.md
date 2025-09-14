# Infrastructure Platform Documentation Best Practices

## Purpose & Scope

This document establishes documentation standards for all infrastructure platforms within our Platform Engineering organization. It provides a structured approach to creating, organizing, and maintaining technical documentation that serves our diverse audience of developers, SREs, platform engineers, and new team members.

## Documentation Framework

### Our Chosen Approach

We have adopted the **Diátaxis framework** as our documentation standard. While various documentation frameworks exist (such as DITA, Information Mapping, and others), we've selected Diátaxis for its clarity and proven effectiveness in technical documentation. Any documentation framework can succeed when its principles are consistently applied—the key is choosing one and adhering to its methodology. For our organization, that framework is Diátaxis.

### Why a Framework Matters

- **Consistency**: Users know where to find specific types of information
- **Completeness**: Ensures all aspects of a platform are documented
- **Efficiency**: Writers know exactly what type of content to create
- **Maintainability**: Clear boundaries prevent documentation overlap and conflicts

## The Diátaxis Framework

Diátaxis organizes documentation into four distinct quadrants based on two axes:
- **Practical vs. Theoretical**: Is the user doing something or learning something?
- **Acquisition vs. Application**: Is the user learning for the first time or applying existing knowledge?

### The Four Documentation Types

```
        Practical Work              Theoretical Knowledge
       (doing things)               (learning things)
    ┌─────────────────┬─────────────────┐
    │                 │                 │
    │   TUTORIALS     │   EXPLANATION   │  Learning
    │   Learning by   │   Understanding │  (acquisition)
    │   doing         │   theory        │
    │                 │                 │
    ├─────────────────┼─────────────────┤
    │                 │                 │
    │   HOW-TO GUIDES │   REFERENCE     │  Working
    │   Solving       │   Information   │  (application)
    │   problems      │   lookup        │
    │                 │                 │
    └─────────────────┴─────────────────┘
```

## 1. Tutorials (Learning-Oriented)

### Purpose
Tutorials are **learning experiences** that take a beginner through their first successful interaction with the platform. They build confidence and familiarity.

### Characteristics
- **Guided journey** from start to finish
- **Guaranteed success** - must work for everyone
- **Minimal explanations** - focus on doing, not understanding
- **Concrete and specific** - exact steps, not options

### Best Practices
- Start with the simplest possible "Hello World" equivalent
- Provide exact commands, configurations, and expected outputs
- Test with someone unfamiliar with the platform
- Keep scope narrow - teach one thing well
- Include prerequisites explicitly
- Provide a clean-up section

### Example Structure
```markdown
# Getting Started with [Platform Name]

## Prerequisites
- List exact versions and requirements
- Include how to verify prerequisites

## Step 1: Initial Setup
[Exact commands with expected output]

## Step 2: First Deployment
[Exact commands with expected output]

## What You've Learned
- Brief summary of accomplishments

## Clean Up
- Commands to reset environment
```

## 2. How-To Guides (Task-Oriented)

### Purpose
How-to guides provide **practical steps** to solve specific real-world problems. They assume basic familiarity with the platform.

### Characteristics
- **Problem-focused** - addresses a specific need
- **Flexible** - may offer alternatives
- **Assumes knowledge** - not for beginners
- **Results-oriented** - gets something done

### Best Practices
- Title should complete: "How to..."
- State the goal upfront
- List prerequisites and assumptions
- Provide options when multiple approaches exist
- Include troubleshooting for common issues
- Keep explanations minimal
- Focus on the task, not the theory

### Example Structure
```markdown
# How to [Specific Task]

## Goal
What this guide accomplishes

## Prerequisites
- Required access/permissions
- Assumed knowledge
- Required tools/versions

## Option A: [Approach Name]
### When to use this approach
### Steps
### Considerations

## Option B: [Alternative Approach]
### When to use this approach
### Steps
### Considerations

## Troubleshooting
### Common Issue 1
### Common Issue 2

## Related Tasks
- Links to similar how-to guides
```

## 3. Reference (Information-Oriented)

### Purpose
Reference documentation provides **factual, descriptive information** for lookup when needed. It's the source of truth for technical details.

### Characteristics
- **Descriptive** - states facts, not instructions
- **Structured** - consistent, predictable organization
- **Comprehensive** - covers all features/options
- **Neutral** - no opinions or recommendations

### Best Practices
- Use consistent structure across all reference docs
- Include all parameters, options, and configurations
- Provide clear descriptions without tutorials
- Use tables for structured data
- Keep examples minimal and illustrative
- Version clearly - what version does this describe?
- Auto-generate when possible from code/configuration

### Example Structure
```markdown
# [Component] Reference

## Overview
Brief factual description

## Configuration Parameters

| Parameter | Type | Required | Default | Description |
|-----------|------|----------|---------|-------------|
| param_1   | string | Yes | - | Description |
| param_2   | integer | No | 10 | Description |

## API Endpoints

### GET /endpoint
- **Purpose**: 
- **Parameters**:
- **Response**:
- **Status Codes**:

## Environment Variables

| Variable | Required | Default | Description |
|----------|----------|---------|-------------|

## File Formats
[Schemas, structures, examples]

## Limits and Quotas
[System boundaries and constraints]
```

## 4. Explanation (Understanding-Oriented)

### Purpose
Explanations provide **context and deeper understanding** of concepts, architecture, and design decisions. They answer "why" questions.

### Characteristics
- **Conceptual** - discusses ideas, not actions
- **Alternative perspectives** - multiple viewpoints
- **Making connections** - relates concepts
- **Background** - history and context

### Best Practices
- Start with the big picture
- Use diagrams and visualizations
- Discuss trade-offs and alternatives
- Explain design decisions and rationale
- Connect to broader concepts
- Include historical context when relevant
- Avoid step-by-step instructions

### Example Structure
```markdown
# Understanding [Concept/Architecture]

## Overview
High-level introduction to the concept

## Core Concepts
### Concept 1
- What it is
- Why it matters
- How it relates to other concepts

### Concept 2
[Similar structure]

## Architecture Patterns
[Diagrams and explanations]

## Design Decisions
### Why We Chose [Approach]
- Alternatives considered
- Trade-offs
- Rationale

## Common Misconceptions
Address frequent misunderstandings

## Further Reading
Links to deeper resources
```

## Writing Best Practices

### General Principles

1. **Write for Your Reader**
   - Assume technical competence but not platform expertise
   - Define acronyms on first use
   - Link to prerequisites rather than explaining basics

2. **Be Concise**
   - Get to the point quickly
   - Use bullet points for lists
   - Break up long paragraphs

3. **Be Precise**
   - Use exact version numbers
   - Specify exact commands
   - Include full error messages

4. **Be Consistent**
   - Use standard terminology throughout
   - Maintain consistent formatting
   - Follow naming conventions

5. **Make It Scannable**
   - Use descriptive headings
   - Include a table of contents for long documents
   - Highlight important warnings or notes
   - Use code blocks for commands and configuration

### Documentation Quality Checklist

Before publishing any documentation, verify:

- [ ] **Accuracy**: All commands and configurations tested and working
- [ ] **Completeness**: All necessary information included
- [ ] **Clarity**: Free of jargon, ambiguity, and assumptions
- [ ] **Currency**: Versions and dates clearly marked
- [ ] **Accessibility**: Follows accessibility guidelines
- [ ] **Findability**: Proper titles, metadata, and search terms
- [ ] **Reviewability**: Peer reviewed by subject matter expert
- [ ] **Maintainability**: Owner identified and update process clear

### Version Control for Documentation

1. **Documentation as Code**
   - Store in version control (Git)
   - Use pull requests for reviews
   - Tag releases with platform versions

2. **Clear Versioning**
   - Document which platform version applies
   - Maintain version compatibility matrix
   - Archive outdated documentation appropriately

3. **Change Management**
   - Include documentation updates in definition of done
   - Review documentation during platform changes
   - Maintain changelog for significant updates

## Anti-Patterns to Avoid

### Common Pitfalls

1. **Tutorial Sprawl**: Don't explain everything in tutorials
2. **Reference Overload**: Don't include how-to instructions in reference
3. **Explanation Confusion**: Don't mix practical steps with theory
4. **How-To Theory**: Don't explain why in how-to guides

### Documentation Smells

- Multiple documents covering the same topic differently
- Outdated examples that no longer work
- Missing documentation for critical features
- Inconsistent terminology across documents
- Circular references without clear starting points
- "TODO" sections in published documentation
- Screenshots of text that should be copyable
- Assumptions about reader's environment

## Quick Reference

### When to Write What

| If you need to... | Write a... |
|-------------------|------------|
| Onboard a new user | Tutorial |
| Show first-time setup | Tutorial |
| Solve a specific problem | How-To Guide |
| Complete a common task | How-To Guide |
| List all configuration options | Reference |
| Document API specifications | Reference |
| Explain architecture | Explanation |
| Discuss design decisions | Explanation |
| Provide background context | Explanation |

## Conclusion

Effective documentation is crucial for platform adoption and operational excellence. By following the Diátaxis framework and these best practices, we ensure our documentation serves its users effectively while remaining maintainable and consistent.

Remember: Good documentation is not about writing more—it's about writing the right type of content for the right purpose in the right place.

---

*Document Version: 1.0*  
*Last Updated: [DATE]*  
*Owner: Platform Engineering Architecture*  
*Review Cycle: Quarterly*