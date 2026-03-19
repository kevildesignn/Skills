# Testing & QA Skills

Load these skills when the user asks about: writing tests, test-driven development, accessibility auditing, API testing, performance testing, QA workflows, or avoiding testing anti-patterns.

## How to Load

Read the SKILL.md files for the skills relevant to your task.

---

## Test-Driven Development

### test-driven-development
**Path**: `.claude/.agent/skills/test-driven-development/SKILL.md`
**Use when**: Red-green-refactor TDD workflow, writing tests before implementation.

### test-driven-development--obra-superpowers
**Path**: `.claude/.agent/skills/test-driven-development--obra-superpowers/SKILL.md`
**Use when**: Enhanced TDD with Obra Superpowers workflow integration.

### test-driven-development--obra-superpowers-skills
**Path**: `.claude/.agent/skills/test-driven-development--obra-superpowers-skills/SKILL.md`
**Use when**: Skills-augmented TDD approach.

---

## Test Quality & Anti-Patterns

### testing-anti-patterns
**Path**: `.claude/.agent/skills/testing-anti-patterns/SKILL.md`
**Use when**: Identifying and fixing bad test patterns, improving test reliability.

### testing-anti-patterns--obra-superpowers-skills
**Path**: `.claude/.agent/skills/testing-anti-patterns--obra-superpowers-skills/SKILL.md`
**Use when**: Enhanced anti-pattern detection with additional context.

### testing-reality-checker
**Path**: `.claude/.agent/skills/testing-reality-checker/SKILL.md`
**Use when**: Validating that tests actually test what they claim to test.

### testing-evidence-collector
**Path**: `.claude/.agent/skills/testing-evidence-collector/SKILL.md`
**Use when**: Gathering evidence of test coverage, test outcomes, and quality metrics.

---

## Specialized Testing

### testing-accessibility-auditor
**Path**: `.claude/.agent/skills/testing-accessibility-auditor/SKILL.md`
**Use when**: Auditing for WCAG compliance, screen reader testing, a11y validation.

### testing-api-tester
**Path**: `.claude/.agent/skills/testing-api-tester/SKILL.md`
**Use when**: API endpoint testing, contract testing, integration test design.

### testing-performance-benchmarker
**Path**: `.claude/.agent/skills/testing-performance-benchmarker/SKILL.md`
**Use when**: Performance benchmarks, load testing, profiling, optimization validation.

---

## Web Application Testing

### webapp-testing
**Path**: `.claude/.agent/skills/webapp-testing/SKILL.md`
**Use when**: End-to-end web testing, browser automation, UI test flows.

### webapp-testing--anthropics-skills
**Path**: `.claude/.agent/skills/webapp-testing--anthropics-skills/SKILL.md`
**Use when**: Anthropic-curated web app testing patterns.

---

## Testing Tooling & Analysis

### testing-test-results-analyzer
**Path**: `.claude/.agent/skills/testing-test-results-analyzer/SKILL.md`
**Use when**: Analyzing test output, identifying flaky tests, interpreting CI results.

### testing-tool-evaluator
**Path**: `.claude/.agent/skills/testing-tool-evaluator/SKILL.md`
**Use when**: Evaluating and choosing testing frameworks, tools, or libraries.

### testing-workflow-optimizer
**Path**: `.claude/.agent/skills/testing-workflow-optimizer/SKILL.md`
**Use when**: Improving test pipeline speed, parallelization, test organization.

---

## Subagent-Based Testing

### testing-skills-with-subagents
**Path**: `.claude/.agent/skills/testing-skills-with-subagents/SKILL.md`
**Use when**: Running tests via multiple parallel subagents.

### testing-skills-with-subagents--obra-superpowers-skills
**Path**: `.claude/.agent/skills/testing-skills-with-subagents--obra-superpowers-skills/SKILL.md`
**Use when**: Enhanced subagent testing with skills context.

---

## Recommended Combinations

- **New feature TDD**: `test-driven-development` + `testing-anti-patterns`
- **API service**: `testing-api-tester` + `test-driven-development`
- **Accessible UI**: `testing-accessibility-auditor` + `webapp-testing`
- **CI optimization**: `testing-workflow-optimizer` + `testing-test-results-analyzer`
- **Full QA audit**: `testing-reality-checker` + `testing-evidence-collector` + `testing-anti-patterns`
