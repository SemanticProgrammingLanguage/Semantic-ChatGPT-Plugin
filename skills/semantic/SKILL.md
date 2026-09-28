---
name: semantic
description: Use for Semantic Programming Language, Semantic source (.se/.sp/.spz), SemanticProgram, UniversalASTDocument/UAST, semantic modules, reading Semantic, writing Semantic directly, understanding Semantic code, transpilation, semantic preservation, or translating code to/from Semantic.
---

# Semantic

Semantic is a machine-oriented, language-independent programming language and canonical semantic program representation.

This skill exists for one primary purpose:

**Read Semantic, understand Semantic, and write Semantic directly.**

The bundled corpus is intentionally large. It includes canonical schema, reference implementation code, behavior tests, language documentation, real examples, fixtures, module material, and the full Go Code Transpiler. Use that material as evidence and as a learning environment.

## Prime directive

**Meaning first. Syntax is transport.**

Reason from program meaning, bindings, scopes, types, relations, evaluation order, effects, contracts, runtime requirements and extensions rather than from familiar punctuation alone.

When the user asks for Semantic, write Semantic directly whenever the required construct is already understood.

Do not translate an entire requested solution through Go, Python, C, C++, C#, Rust, Java or another language merely because that language is easier for the model to generate.

Helper languages are allowed only as small experimental probes when a Semantic construct is uncertain.

## What this skill should make you able to do

Use the bundled material to become effective at:

- reading `.se`, `.sp`, `.spz` and canonical Semantic JSON,
- explaining Semantic code in semantic terms,
- authoring new Semantic directly,
- modifying existing Semantic without losing meaning,
- recognizing canonical UAST/SemanticProgram structures,
- preserving bindings, scopes, types, relations, effects and contracts,
- understanding module calls and documented exports,
- checking roundtrips and semantic preservation,
- learning unfamiliar Semantic constructs from concrete compiler evidence,
- translating small or large programs into Semantic once the required constructs are known.

## Read Semantic workflow

When reading Semantic:

1. Identify the representation and version.
2. Identify entities/nodes and stable identities.
3. Resolve declarations, references, bindings and lexical scopes.
4. Resolve type information and type origins where present.
5. Distinguish structural, control, data, ownership, ordering and evaluation relations.
6. Track effects, contracts, runtime requirements, ABI requirements, facets and extensions when present.
7. Preserve unknown or versioned information rather than interpreting it away.
8. Reconstruct the program's behavior in semantic terms.
9. Use source-language analogies only as explanatory aids, never as the canonical interpretation.

## Write Semantic workflow

When asked to implement code in Semantic:

1. State the required behavior internally in semantic terms.
2. Select the Semantic/UAST constructs that are already supported by evidence.
3. Create stable entities/identities as required by the format.
4. Establish declarations, references, bindings and lexical scopes explicitly.
5. Establish supported type information and type origins.
6. Encode semantic operations rather than copying source operator spelling blindly.
7. Encode structural, control, data and evaluation relations as required.
8. Preserve evaluation order whenever observable behavior depends on it.
9. Preserve effects, cleanup, exceptions, concurrency, ownership, memory behavior, ABI and runtime requirements when relevant.
10. Preserve extensions/facets that carry source semantics.
11. Emit readable `.se` when Semantic source is requested.
12. Validate against bundled evidence or tooling when uncertainty remains.

The user's requested result should remain Semantic. A helper Go/Python probe is never a substitute for the requested Semantic program.

## Evidence discipline

**Not proven -> not emitted.**

Never silently manufacture:

- node kinds,
- field names,
- IDs or ID formats,
- handshake IDs,
- type facts,
- purity,
- ownership,
- aliasing guarantees,
- evaluation order,
- exception behavior,
- calling conventions,
- ABI facts,
- runtime guarantees,
- module exports,
- backend capabilities,
- version-specific contracts.

If a fact cannot be established from known Semantic knowledge, recover it from evidence instead of guessing.

# Unknown-construct recovery workflow

This workflow is critical. Use it whenever a Semantic detail is not confidently known.

Typical triggers include:

- an unfamiliar node kind,
- a rare operation,
- an unknown relation,
- an unfamiliar field name,
- handshake IDs,
- generated/stable ID conventions,
- module IDs,
- target/runtime identifiers,
- ABI fields,
- extension/facet keys,
- ownership or lifetime metadata,
- uncommon control-flow constructs,
- concurrency constructs,
- exception constructs,
- serialization details,
- a source-language feature for which the Semantic encoding is unclear.

Do **not** invent a plausible-looking Semantic representation.

## Step 1 — Search the bundled evidence

Search the smallest relevant subset first:

1. `skills/semantic/examples/`
2. `skills/semantic/references/`
3. `skills/semantic/schema/universal_ast_schema.json`
4. `skills/semantic/behavior-tests/`
5. `skills/semantic/reference-implementation/`
6. the bundled Semantic language repository and transpiler source tree.

Search for the exact concept, neighboring concepts, field names, enum values, IDs and tests.

If the answer is established there, use it directly.

## Step 2 — Construct a minimal probe

If the bundled evidence does not establish the construct clearly, build the **smallest possible source program** that isolates exactly that unknown feature.

Prefer Go as the first probe language when it expresses the feature naturally, because the bundled Go Code Transpiler is the primary experimental teacher.

Use Python when Python expresses the feature more directly or when comparing frontends is useful.

Good probes contain one concept only, for example:

- one literal,
- one variable,
- one assignment,
- one function,
- one parameter,
- one return,
- one `if`,
- one loop,
- one indexing operation,
- one slice/list/array operation,
- one map/dictionary operation,
- one closure capture,
- one method call,
- one exception construct,
- one async/concurrency operation,
- one import,
- one module call,
- one ABI/runtime interaction,
- one construct expected to generate the unknown ID or handshake metadata.

Never start with a large helper program containing several unknown features at once.

## Step 3 — Transpile the probe to Semantic

Run the bundled/current Go Code Transpiler and inspect the generated `.se` / canonical Semantic representation.

Look specifically at:

- node/entity kinds,
- stable IDs,
- handshake IDs or generated identifiers,
- declarations and references,
- bindings and scopes,
- type entries and origins,
- structural relations,
- control relations,
- data relations,
- evaluation-order relations,
- effects,
- contracts,
- facets/extensions,
- module metadata,
- ABI/runtime requirements,
- serialization form.

For an ID-like value, determine whether it is:

- semantically meaningful,
- deterministic but derived,
- scoped/local,
- frontend-generated,
- transport-only,
- version-specific,
- arbitrary but uniqueness-constrained.

Do not copy a literal generated ID into unrelated code unless the evidence shows that the literal value itself is required.

## Step 4 — Cross-check the generated result

A transpiler output is **evidence**, not automatically the language specification.

Cross-check the generated construct against at least the most relevant of:

- canonical schema,
- behavior tests,
- reference implementation,
- native `.se` examples,
- architecture/language docs.

When one probe is ambiguous, create a second tiny probe that varies exactly one property.

For example, if an ID changes between otherwise equivalent programs, determine what input controls it before generalizing.

## Step 5 — Learn the rule, then return to Semantic

Extract the smallest supported rule from the experiment.

Then stop using the helper language and author the requested solution directly in Semantic.

The goal of probing is to teach the model the missing Semantic construction, not to make Go/Python the implementation language.

# The Go Code Transpiler as teacher

The bundled Go Code Transpiler is a **teacher, verifier, compatibility reference and experiment engine**.

Use it for:

- discovering unknown Semantic encodings,
- observing frontend-to-UAST behavior,
- finding exact generated field names and relations,
- investigating IDs and handshake metadata,
- verifying roundtrips,
- comparing equivalent constructs from different source languages,
- checking whether a proposed Semantic fragment is representable,
- examining canonicalization behavior,
- identifying frontend-specific artifacts,
- confirming semantic preservation.

Do not treat Go structs, internal helper names or incidental implementation details as the definition of Semantic unless corroborated by canonical evidence.

If the user supplies a newer transpiler/compiler than the bundled copy, prefer the newer supplied implementation for experiments, while still using schema/tests/reference docs to distinguish language semantics from implementation accidents.

# Canonical program model

A useful abstract view is:

`P = (V, E, T, A, C)`

Where:

- `V` = semantic/UAST entities or nodes,
- `E` = structural, control, data, ownership, ordering and other relations,
- `T` = types and type evidence,
- `A` = semantic attributes, facets, effects and origin metadata,
- `C` = contracts and execution constraints.

Treat node identity, bindings, lexical scopes, type origins, relations, evaluation order, effects, contracts, layout, ABI/runtime requirements and extensions as meaningful whenever they are present.

# Union, not intersection

Semantic models the **union** of useful programming-language semantics, not the lowest common denominator of target languages.

When a source property has no direct equivalent in a target, preserve the property in Semantic. A later backend may lower it, synthesize support, emulate it, provide runtime support or reject that target requirement explicitly.

Do not weaken the Semantic representation because one target language is weaker.

# Important distinctions

Do not collapse:

- null vs missing vs NA vs NaN,
- identifier spelling vs actual binding,
- declaration vs reference,
- structural containment vs control flow,
- structural containment vs evaluation order,
- data dependency vs control dependency,
- source operator spelling vs semantic operation,
- syntactic block nesting vs lexical scope,
- surface type spelling vs canonical type information,
- a generated identifier vs its semantic role,
- frontend artifact vs canonical semantic fact,
- source-language convenience syntax vs runtime semantics.

# `.se`, `.sp`, `.spz`

Treat these as representations of the same semantic-program family rather than separate semantic languages.

- `.se` — native/readable Semantic projection.
- `.sp` — readable versioned transport representation.
- `.spz` — lossless compressed transport.
- canonical Semantic JSON — another serialization view.

Format-only roundtrips should preserve canonical Semantic meaning.

# Determinism and roundtrips

Canonical serialization and pretty-printing should be deterministic where required by the reference implementation/tests.

When checking a transformation, distinguish:

- formatting differences,
- identity regeneration,
- frontend metadata differences,
- actual semantic changes.

Use behavior tests and reference implementation to decide which differences matter.

# Modules

Before inventing a Semantic module API:

1. inspect bundled module documentation/examples,
2. use live Semantic MCP/module sources if connected,
3. search the official module store when available,
4. inspect manifest/README/source metadata,
5. construct calls only against established exports.

Do not invent module names, signatures, IDs or exports.

# Reference priority

When sources disagree, prefer:

1. canonical schema and current core model behavior,
2. executable behavior tests,
3. current Semantic architecture/language documentation,
4. official/native `.se` examples,
5. current transpiler experiments,
6. legacy transport documentation.

Flag contradictions rather than silently selecting the most convenient interpretation.

# Scope boundary

This skill is about **Semantic itself**:

- learning it,
- reading it,
- understanding it,
- writing it,
- validating it,
- translating into it,
- preserving it,
- experimentally recovering unfamiliar constructs.

Project-specific compiler architecture is not the organizing principle of this skill.

Self-hosting stages, bootstrap strategy, PE/ELF construction, linker architecture, compiler staging and backend implementation strategy belong to the relevant compiler/project context when the user explicitly works on those projects.

Do not make self-hosting the default objective of ordinary Semantic tasks.

# Bundled knowledge base

The large bundled corpus is intentional. Preserve and use it.

Important locations include:

- `skills/semantic/examples/` — readable/native Semantic examples and fixtures,
- `skills/semantic/references/` — language, architecture, UAST, module and development documentation,
- `skills/semantic/schema/` — canonical UAST schema,
- `skills/semantic/reference-implementation/` — selected Go reference implementation,
- `skills/semantic/behavior-tests/` — executable invariants and preservation tests,
- bundled Semantic repository content,
- bundled VS Code/language-support material,
- bundled complete Go Code Transpiler source tree.

Do not discard examples or large reference sets merely to make the plugin smaller. They are part of the skill's working knowledge.

Read `skills/semantic/references/INDEX.md` when a map of the bundled material is useful, but for ordinary tasks inspect only the smallest evidence needed first.
