# MCP & Plugin Development Skills

Load these skills when the user asks about: building MCP servers, Claude plugins, hooks, plugin structure, CLI tools for MCP, or extending Claude Code functionality.

## How to Load

Read the SKILL.md files for the skills relevant to your task.

---

## MCP Server Building

### mcp-builder
**Path**: `.claude/.agent/skills/mcp-builder/SKILL.md`
**Use when**: Building a new MCP server from scratch — tool definitions, resource handling.

### mcp-builder--anthropics-skills
**Path**: `.claude/.agent/skills/mcp-builder--anthropics-skills/SKILL.md`
**Use when**: Anthropic-curated MCP building patterns.

---

## MCP CLI & Integration

### mcp-cli
**Path**: `.claude/.agent/skills/mcp-cli/SKILL.md`
**Use when**: Using MCP CLI tools, managing MCP servers via command line.

### mcp-cli--obra-superpowers-lab
**Path**: `.claude/.agent/skills/mcp-cli--obra-superpowers-lab/SKILL.md`
**Use when**: Lab-enhanced MCP CLI workflows.

### mcp-integration
**Path**: `.claude/.agent/skills/mcp-integration/SKILL.md`
**Use when**: Integrating MCP servers into Claude workflows, connecting tools.

### mcp-integration--anthropics-claude-code
**Path**: `.claude/.agent/skills/mcp-integration--anthropics-claude-code/SKILL.md`
**Use when**: MCP integration within Claude Code — Anthropic's patterns.

---

## Plugin Architecture

### plugin-structure
**Path**: `.claude/.agent/skills/plugin-structure/SKILL.md`
**Use when**: Designing plugin architecture, plugin file structure, plugin conventions.

### plugin-structure--anthropics-claude-code
**Path**: `.claude/.agent/skills/plugin-structure--anthropics-claude-code/SKILL.md`
**Use when**: Claude Code-specific plugin structure patterns.

### plugin-settings
**Path**: `.claude/.agent/skills/plugin-settings/SKILL.md`
**Use when**: Plugin configuration, settings UI, user preferences for plugins.

### plugin-settings--anthropics-claude-code
**Path**: `.claude/.agent/skills/plugin-settings--anthropics-claude-code/SKILL.md`
**Use when**: Claude Code plugin settings patterns.

---

## Hooks

### hook-development
**Path**: `.claude/.agent/skills/hook-development/SKILL.md`
**Use when**: Building Claude Code hooks — pre/post tool call hooks, event handlers.

### hook-development--anthropics-claude-code
**Path**: `.claude/.agent/skills/hook-development--anthropics-claude-code/SKILL.md`
**Use when**: Anthropic-curated hook development patterns.

---

## Recommended Combinations

- **New MCP server**: `mcp-builder` + `plugin-structure`
- **Full plugin**: `plugin-structure` + `plugin-settings` + `hook-development`
- **Claude Code extension**: `hook-development--anthropics-claude-code` + `mcp-integration--anthropics-claude-code`
