# Support & Operations Skills

Load these skills when the user asks about: customer support, finance tracking, infrastructure maintenance, analytics reporting, executive summaries, or internal operations.

## How to Load

Read the SKILL.md files for the skills relevant to your task.

---

## Customer Support

### support-support-responder
**Path**: `.claude/.agent/skills/support-support-responder/SKILL.md`
**Use when**: Drafting support responses, handling customer issues, support ticket management.

---

## Finance

### support-finance-tracker
**Path**: `.claude/.agent/skills/support-finance-tracker/SKILL.md`
**Use when**: Tracking finances, expense reporting, budget management, financial summaries.

---

## Infrastructure

### support-infrastructure-maintainer
**Path**: `.claude/.agent/skills/support-infrastructure-maintainer/SKILL.md`
**Use when**: Infrastructure maintenance tasks, system health checks, operational runbooks.

---

## Analytics & Reporting

### support-analytics-reporter
**Path**: `.claude/.agent/skills/support-analytics-reporter/SKILL.md`
**Use when**: Support metrics, ticket analytics, customer satisfaction reporting.

### support-executive-summary-generator
**Path**: `.claude/.agent/skills/support-executive-summary-generator/SKILL.md`
**Use when**: Generating executive-level summaries of operations, support, or business data.

### data-analytics-reporter
**Path**: `.claude/.agent/skills/data-analytics-reporter/SKILL.md`
**Use when**: Broader analytics reporting beyond support — product, business, or engineering metrics.

### report-distribution-agent
**Path**: `.claude/.agent/skills/report-distribution-agent/SKILL.md`
**Use when**: Automating distribution of regular reports to stakeholders.

---

## Sales & Data

### sales-data-extraction-agent
**Path**: `.claude/.agent/skills/sales-data-extraction-agent/SKILL.md`
**Use when**: Extracting and structuring sales data from various sources.

### data-consolidation-agent
**Path**: `.claude/.agent/skills/data-consolidation-agent/SKILL.md`
**Use when**: Merging and deduplicating data from multiple sources.

---

## Recommended Combinations

- **Ops dashboard**: `support-analytics-reporter` + `data-analytics-reporter` + `support-executive-summary-generator`
- **Finance report**: `support-finance-tracker` + `support-executive-summary-generator`
- **Support ops**: `support-support-responder` + `support-analytics-reporter`
- **Sales pipeline**: `sales-data-extraction-agent` + `data-consolidation-agent`
