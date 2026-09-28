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
## Install Semantic from the Plugin Marketplace

1. Open ChatGPT and go to **Plugins**.
2. Select **Add marketplace**.
3. Enter this repository:

https://github.com/SemanticProgrammingLanguage/Semantic-ChatGPT-Plugin

4. For **Branch / tag / commit**, enter:

marketplace

5. Leave **Path** empty.
6. Add/import the marketplace.
7. Open the newly added marketplace.
8. Find **Semantic** or **Semantic Test** and click **Install**.

Alternatively, if you are using Codex or the ChatGPT desktop plugin workflow, you can add the marketplace with:

codex plugin marketplace add SemanticProgrammingLanguage/Semantic-ChatGPT-Plugin --ref marketplace

After the marketplace has been added, install the Semantic plugin from the marketplace list.
