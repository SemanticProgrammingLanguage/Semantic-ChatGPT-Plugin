# Using the Code Transpiler as a Semantic teacher

The full Code Transpiler is intentionally not embedded in this upload package.

When the user supplies it in a chat or exposes it through MCP, use it experimentally:

1. Write the smallest source program that isolates one semantic concept.
2. Transpile that source to Semantic.
3. Inspect:
   - node kinds and stable IDs,
   - type entries and origins,
   - scope/binding structure,
   - relations,
   - evaluation semantics,
   - effects/contracts/extensions,
   - runtime/ABI demands.
4. Compare against the canonical schema and behavior tests.
5. Generalize only what is invariant across more than one useful example.
6. Write the next program directly in Semantic.
7. Use transpilation only to verify uncertain details.

Do not memorize accidental implementation artifacts as language laws.
