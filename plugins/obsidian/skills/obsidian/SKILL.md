---
name: obsidian
description: Work with an Obsidian vault through the official Obsidian CLI — read, create, append to, search, rename and move notes, and work with daily notes, tasks, tags and properties. Use when the user asks to do something in their Obsidian vault, especially renaming or moving notes, where the CLI keeps links intact.
---

# Obsidian CLI

The `obsidian` command drives the running Obsidian app from a terminal. Changes go
through Obsidian itself, so they behave like edits made in the app. For example, a
renamed or moved note has its links updated across the vault.

## Before you start

- The Obsidian app must be running. The CLI talks to it and does nothing by itself.
- The CLI must be enabled under Obsidian **Settings → General → Command line interface**.
  If `obsidian` is "command not found", ask the user to enable it and restart their terminal.

## What it can do

- Read, create, and append to notes
- Search the vault
- Rename and move notes, with links updated
- Open and add to daily notes
- List and update tasks, tags, properties, and backlinks

## How

Don't guess at syntax. Look it up when you need it:

```bash
obsidian help              # list every command
obsidian help <command>    # parameters for one command
```

Parameters are usually written as `key=value`. Quote any value that contains spaces.
If the user has more than one vault, check `help` for how to target a specific one.

For anything `help` doesn't cover, see Obsidian's documentation at
https://help.obsidian.md (search for "CLI").

## Guidance

- For rename and move, use the CLI rather than `mv` or other file tools, because plain
  file operations leave broken links behind.
- Plain reads and searches of the Markdown files are fine to do with normal file tools
  when Obsidian isn't running.
- Before bulk operations, list what will change and confirm with the user.
