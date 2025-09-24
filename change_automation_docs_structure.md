# Change Management Automation Framework - Documentation Structure

## Docusaurus Directory Structure

```
docs/
├── change-management-automation/
│   ├── _category_.json
│   ├── overview/
│   │   ├── _category_.json
│   │   ├── architecture-overview.md
│   │   ├── integration-landscape.md
│   │   └── compliance-overview.md
│   │
│   ├── explanations/                    # Diátaxis: Understanding-oriented
│   │   ├── _category_.json
│   │   ├── why-change-automation.md
│   │   ├── risk-mitigation-strategy.md
│   │   ├── regulatory-compliance.md
│   │   ├── rollback-philosophy.md
│   │   └── security-by-design.md
│   │
│   ├── tutorials/                       # Diátaxis: Learning-oriented
│   │   ├── _category_.json
│   │   ├── getting-started/
│   │   │   ├── your-first-automated-change.md
│   │   │   ├── setting-up-compliance-checks.md
│   │   │   └── configuring-health-monitoring.md
│   │   ├── advanced/
│   │   │   ├── complex-rollback-scenarios.md
│   │   │   ├── multi-environment-deployments.md
│   │   │   └── emergency-change-walkthrough.md
│   │   └── team-onboarding/
│   │       ├── developer-certification.md
│   │       ├── ops-team-training.md
│   │       └── manager-dashboard-tour.md
│   │
│   ├── how-to-guides/                   # Diátaxis: Problem-oriented
│   │   ├── _category_.json
│   │   ├── framework-implementation/
│   │   │   ├── deploy-change-automation.md
│   │   │   ├── configure-servicenow-integration.md
│   │   │   ├── setup-compliance-pipeline.md
│   │   │   └── implement-rollback-triggers.md
│   │   ├── operational-procedures/
│   │   │   ├── handle-failed-changes.md
│   │   │   ├── execute-emergency-rollback.md
│   │   │   ├── manage-change-conflicts.md
│   │   │   └── escalate-critical-issues.md
│   │   ├── troubleshooting/
│   │   │   ├── common-automation-failures.md
│   │   │   ├── compliance-check-errors.md
│   │   │   ├── rollback-mechanism-issues.md
│   │   │   └── health-check-false-positives.md
│   │   └── maintenance/
│   │       ├── update-compliance-rules.md
│   │       ├── tune-rollback-thresholds.md
│   │       └── maintain-health-check-library.md
│   │
│   ├── reference/                       # Diátaxis: Information-oriented
│   │   ├── _category_.json
│   │   ├── apis/
│   │   │   ├── change-automation-api.md
│   │   │   ├── compliance-api.md
│   │   │   ├── rollback-api.md
│   │   │   └── health-check-api.md
│   │   ├── configurations/
│   │   │   ├── ansible-playbook-standards.md
│   │   │   ├── terraform-module-reference.md
│   │   │   ├── compliance-rule-library.md
│   │   │   └── health-check-specifications.md
│   │   ├── integrations/
│   │   │   ├── servicenow-webhook-specs.md
│   │   │   ├── monitoring-tool-connectors.md
│   │   │   ├── gitlab-ci-integration.md
│   │   │   └── notification-channels.md
│   │   ├── templates/
│   │   │   ├── change-request-templates.md
│   │   │   ├── rollback-plan-templates.md
│   │   │   ├── risk-assessment-forms.md
│   │   │   └── post-implementation-reviews.md
│   │   └── metrics/
│   │       ├── change-success-metrics.md
│   │       ├── compliance-kpis.md
│   │       ├── rollback-statistics.md
│   │       └── operational-risk-indicators.md
│   │
│   └── governance/                      # Banking-specific governance
│       ├── _category_.json
│       ├── policies/
│       │   ├── change-management-policy.md
│       │   ├── emergency-change-policy.md
│       │   ├── rollback-governance.md
│       │   └── access-control-policy.md
│       ├── procedures/
│       │   ├── change-approval-workflows.md
│       │   ├── risk-assessment-procedures.md
│       │   ├── audit-trail-requirements.md
│       │   └── incident-response-procedures.md
│       ├── compliance/
│       │   ├── regulatory-mapping.md
│       │   ├── audit-preparation.md
│       │   ├── control-testing.md
│       │   └── exception-management.md
│       └── reporting/
│           ├── executive-dashboards.md
│           ├── operational-reports.md
│           ├── compliance-reports.md
│           └── risk-reports.md

# Static Assets
static/
├── img/
│   └── change-automation/
│       ├── architecture-diagrams/
│       ├── workflow-diagrams/
│       ├── integration-maps/
│       └── dashboard-screenshots/
└── files/
    └── change-automation/
        ├── templates/
        ├── sample-configs/
        └── policy-documents/
```

## Document Categorisation by Diátaxis Framework

### Tutorials (Learning-oriented)
- Step-by-step learning experiences
- Confidence-building exercises  
- Practical skill development
- Progressive complexity

### How-to Guides (Problem-oriented)
- Specific problem solutions
- Practical steps to achieve goals
- Operational procedures
- Troubleshooting guides

### Reference (Information-oriented)
- Technical specifications
- API documentation
- Configuration options
- Template libraries

### Explanations (Understanding-oriented)
- Architectural decisions
- Design philosophy
- Risk management approach
- Regulatory context

## Governance Structure
- **Policies**: High-level governance documents
- **Procedures**: Detailed operational processes  
- **Compliance**: Regulatory and audit materials
- **Reporting**: Metrics, dashboards, and analytics

This structure ensures comprehensive coverage while maintaining the modularity and discoverability that Diátaxis promotes.