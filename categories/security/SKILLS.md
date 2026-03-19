# Security Skills

Load these skills when the user asks about: security engineering, secure code review, compliance, defense strategies, legal requirements, or system hardening.

## How to Load

Read the SKILL.md files for the skills relevant to your task.

---

## Security Engineering

### engineering-security-engineer
**Path**: `.claude/.agent/skills/engineering-security-engineer/SKILL.md`
**Use when**: Security architecture, threat modeling, secure coding, vulnerability assessment.

---

## Defense Strategies

### defense-in-depth
**Path**: `.claude/.agent/skills/defense-in-depth/SKILL.md`
**Use when**: Layered security design, defense-in-depth strategies, hardening systems against multiple attack vectors.

---

## Compliance & Legal

### support-legal-compliance-checker
**Path**: `.claude/.agent/skills/support-legal-compliance-checker/SKILL.md`
**Use when**: Legal compliance review, regulatory requirements (GDPR, HIPAA, etc.), compliance auditing.

---

## Agent Security

### agentic-identity-trust
**Path**: `.claude/.agent/skills/agentic-identity-trust/SKILL.md`
**Use when**: Agent authentication, trust hierarchies in multi-agent systems, preventing prompt injection.

---

## Recommended Combinations

- **Secure system design**: `engineering-security-engineer` + `defense-in-depth`
- **Compliance audit**: `support-legal-compliance-checker` + `engineering-security-engineer`
- **Secure agent system**: `agentic-identity-trust` + `defense-in-depth`
