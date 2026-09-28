# Semantic FULL 0.6.0

A full-size Semantic knowledge plugin designed to let ChatGPT **read, understand, learn and write Semantic directly**.

The large bundled knowledge base is intentionally retained: examples, fixtures, behavior tests, canonical schema, reference implementation, language and UAST documentation, module material, Semantic repository content, VS Code/language support, and the complete Go Code Transpiler.

## Learning fallback

When an unfamiliar Semantic construct cannot be established from the bundled corpus, the skill may create a minimal Go or Python probe and translate it with the Go Code Transpiler. This is specifically useful for obscure nodes, relations, fields, handshake IDs, generated IDs, ABI/runtime metadata and uncommon language features. The generated Semantic is then cross-checked against schema/tests/reference evidence. Once the construct is understood, the requested solution is authored directly in Semantic.

The helper language is a microscope, not the implementation target.

## Scope

The general skill is centered on Semantic itself. Self-hosting, bootstrap stages, PE/ELF construction and linker/backend strategy remain project-specific topics rather than the default purpose of the plugin.
