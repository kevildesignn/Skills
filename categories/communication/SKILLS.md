# Communication Skills

Load these skills when the user asks about: sending Slack messages, creating Slack GIFs, writing internal communications, or managing team announcements.

## How to Load

Read the SKILL.md files for the skills relevant to your task.

---

## Slack

### slack-messaging
**Path**: `.claude/.agent/skills/slack-messaging/SKILL.md`
**Use when**: Drafting or sending Slack messages, formatting for Slack, channel strategy.

### slack-messaging--obra-superpowers-lab
**Path**: `.claude/.agent/skills/slack-messaging--obra-superpowers-lab/SKILL.md`
**Use when**: Lab-enhanced Slack messaging with automation.

### slack-gif-creator
**Path**: `.claude/.agent/skills/slack-gif-creator/SKILL.md`
**Use when**: Creating or finding GIFs for Slack reactions, celebrations, announcements.

### slack-gif-creator--anthropics-skills
**Path**: `.claude/.agent/skills/slack-gif-creator--anthropics-skills/SKILL.md`
**Use when**: Anthropic-curated Slack GIF patterns.

---

## Internal Communications

### internal-comms
**Path**: `.claude/.agent/skills/internal-comms/SKILL.md`
**Use when**: Writing internal announcements, all-hands updates, team newsletters.

### internal-comms--anthropics-skills
**Path**: `.claude/.agent/skills/internal-comms--anthropics-skills/SKILL.md`
**Use when**: Anthropic-curated internal comms writing.

---

## Recommended Combinations

- **Team announcement**: `internal-comms` + `slack-messaging`
- **Celebratory message**: `slack-messaging` + `slack-gif-creator`
- **Company update**: `internal-comms--anthropics-skills` + `support-executive-summary-generator`
