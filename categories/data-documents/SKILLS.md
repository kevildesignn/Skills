# Data & Documents Skills

Load these skills when the user asks about: working with Excel/CSV, PDFs, Word docs, PowerPoint, data pipelines, analytics reports, or document generation.

## How to Load

Read the SKILL.md files for the skills relevant to your task.

---

## Spreadsheets

### xlsx
**Path**: `.claude/.agent/skills/xlsx/SKILL.md`
**Use when**: Reading, writing, or manipulating Excel/XLSX files.

### xlsx--anthropics-skills
**Path**: `.claude/.agent/skills/xlsx--anthropics-skills/SKILL.md`
**Use when**: Anthropic-curated XLSX handling patterns.

---

## Documents

### docx
**Path**: `.claude/.agent/skills/docx/SKILL.md`
**Use when**: Reading, writing, or generating Word/DOCX documents.

### docx--anthropics-skills
**Path**: `.claude/.agent/skills/docx--anthropics-skills/SKILL.md`
**Use when**: Anthropic-curated DOCX handling.

### pdf
**Path**: `.claude/.agent/skills/pdf/SKILL.md`
**Use when**: PDF reading, generation, or extraction.

### pdf--anthropics-skills
**Path**: `.claude/.agent/skills/pdf--anthropics-skills/SKILL.md`
**Use when**: Anthropic-curated PDF handling.

---

## Presentations

### pptx
**Path**: `.claude/.agent/skills/pptx/SKILL.md`
**Use when**: Creating or modifying PowerPoint/PPTX presentations.

### pptx--anthropics-skills
**Path**: `.claude/.agent/skills/pptx--anthropics-skills/SKILL.md`
**Use when**: Anthropic-curated PPTX patterns.

---

## Data Analytics & Reporting

### data-analytics-reporter
**Path**: `.claude/.agent/skills/data-analytics-reporter/SKILL.md`
**Use when**: Generating analytics reports, data visualization, metrics summaries.

### data-consolidation-agent
**Path**: `.claude/.agent/skills/data-consolidation-agent/SKILL.md`
**Use when**: Merging multiple data sources, deduplication, data unification.

### sales-data-extraction-agent
**Path**: `.claude/.agent/skills/sales-data-extraction-agent/SKILL.md`
**Use when**: Extracting structured sales data from documents or raw sources.

### report-distribution-agent
**Path**: `.claude/.agent/skills/report-distribution-agent/SKILL.md`
**Use when**: Automating report generation and distribution workflows.

### support-analytics-reporter
**Path**: `.claude/.agent/skills/support-analytics-reporter/SKILL.md`
**Use when**: Support/customer service metrics reporting.

### support-executive-summary-generator
**Path**: `.claude/.agent/skills/support-executive-summary-generator/SKILL.md`
**Use when**: Generating executive summaries from data or reports.

---

## Recommended Combinations

- **Data report**: `data-analytics-reporter` + `xlsx` or `pdf`
- **Business presentation**: `pptx` + `data-analytics-reporter`
- **Sales pipeline**: `sales-data-extraction-agent` + `data-consolidation-agent`
- **Executive briefing**: `support-executive-summary-generator` + `report-distribution-agent`
