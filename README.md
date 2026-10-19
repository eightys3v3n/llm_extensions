# llm_extensions

A Claude Code plugin marketplace. Each plugin lives in its own folder under `plugins/`.

| Plugin | What it does |
| --- | --- |
| [obsidian](plugins/obsidian) | Work with an Obsidian vault through the official Obsidian CLI |

## Install

```bash
claude plugin marketplace add "<path or git URL of this repo>"
claude plugin install obsidian@llm-extensions
```

## Layout

```
.claude-plugin/marketplace.json   # lists every plugin in this repo
plugins/<name>/
  .claude-plugin/plugin.json      # plugin manifest
  skills/<skill>/SKILL.md         # optional: skills
  commands/  agents/  hooks/      # optional: other extension types
```

## Adding a plugin

1. Create `plugins/<name>/.claude-plugin/plugin.json` and add the plugin's content.
2. Add an entry for it to `plugins` in `.claude-plugin/marketplace.json`.
3. Run `claude plugin validate .` from the repo root.
