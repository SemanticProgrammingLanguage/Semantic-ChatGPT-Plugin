# Semantic Programming Language Marketplace

This branch is the marketplace catalog for the Semantic ChatGPT Plugin.

Marketplace manifest:

`.agents/plugins/marketplace.json`

The marketplace entry installs the plugin from the `main` branch of:

`https://github.com/SemanticProgrammingLanguage/Semantic-ChatGPT-Plugin`

## ChatGPT workspace import

Use:

- Source: `https://github.com/SemanticProgrammingLanguage/Semantic-ChatGPT-Plugin`
- Path: leave empty
- Branch / tag / commit: `marketplace`

ChatGPT reads `.agents/plugins/marketplace.json` from this branch and imports the plugin listed there.

## Codex / ChatGPT desktop

A Git-backed marketplace can be added with:

`codex plugin marketplace add SemanticProgrammingLanguage/Semantic-ChatGPT-Plugin --ref marketplace`

The plugin itself is sourced from the `main` branch.
