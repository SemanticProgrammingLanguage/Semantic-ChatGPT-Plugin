# Semantic skill reference index

This package intentionally embeds the maximum useful *knowledge* while leaving out the very large full transpiler and generated multi-megabyte Semantic bundles.

## Recommended reading order

1. `MACHINE_LANGUAGE_PHILOSOPHY.md`
2. `SEMANTIC_PROGRAM.md` / `root-SEMANTIC_PROGRAM.md`
3. `UNIVERSAL_CANONICAL_ARCHITECTURE.md` or canonical architecture documents
4. `FRONTEND_UAST_CONTRACT.md`
5. `SP_LANGUAGE.md`
6. `SEMANTIC_MODULE_SYSTEM.md`
7. schema: `../schema/universal_ast_schema.json`
8. selected implementation
9. behavior tests
10. examples

## Documentation included

- CROSSTL_DESIGN.md
- EXTSEM_UASF_MATRIX.md
- FRONTEND_UAST_CONTRACT.md
- IMPLEMENTATION_MATRIX.md
- MACHINE_LANGUAGE_PHILOSOPHY.md
- MLCPD_INPUT_CONTRACT.md
- NATIVE_SEMANTIC_PIPELINE.md
- SEMANTIC_DEVELOPMENT.md
- SEMANTIC_FRONTEND_V2.md
- SEMANTIC_MODULE_SYSTEM.md
- SEMANTIC_PROGRAM.md
- SFGC.md
- SFPC.md
- SP_LANGUAGE.md
- THIRD_PARTY_NOTICES.md
- TRANSPILER_AS_TEACHER.md
- UAST_CANONICAL_CAPABILITY_COVERAGE.md
- UAST_CORPUS_MATRIX.md
- UAST_MIGRATION_STATUS.md
- UNIVERSAL_CANONICAL_ARCHITECTURE.md
- language-configuration.json
- root-FRONTEND_UAST_CONTRACT.md
- root-IMPLEMENTATION_MATRIX.md
- root-README.md
- root-SEMANTIC_DEVELOPMENT.md
- root-SEMANTIC_FRONTEND_V2.md
- root-SEMANTIC_PROGRAM.md
- root-UAST_MIGRATION_STATUS.md
- root-Universal-Code-Transpiler-Canonical-Architecture.md
- semantic-examples-README.md
- semantic-language-repository-README.md
- semantic.tmLanguage.json
- vscode-extension-README.md

## Selected canonical implementation files

- runtime_uast.go
- runtime_uast_primitives.go
- semantic_behavior.go
- semantic_closure.go
- semantic_document.go
- semantic_executable_closure.go
- semantic_feature_space.go
- semantic_module.go
- semantic_module_embedding.go
- semantic_module_resolver.go
- semantic_native_pipeline.go
- semantic_package_import.go
- semantic_program.go
- semantic_source.go
- semantic_sp.go
- semantic_validation.go
- semantic_walk.go
- uast_capability.go
- uast_contracts.go
- uast_direct.go
- uast_direct_lowering.go
- uast_emission_contracts.go
- uast_emission_recipes.go
- uast_evidence.go
- uast_execution_primitives.go
- uast_execution_registry.go
- uast_extended_contracts.go
- uast_function_flow.go
- uast_preservation_analysis.go
- uast_structure_projection.go
- uast_target_codegen.go

## Behavior tests

- semantic_behavior_test.go
- semantic_closure_test.go
- semantic_document_test.go
- semantic_entry_roundtrip_test.go
- semantic_executable_closure_test.go
- semantic_integrity_test.go
- semantic_module_test.go
- semantic_native_pipeline_test.go
- semantic_program_test.go
- semantic_project_link_test.go
- semantic_sp_test.go
- uast_backend_canonical_test.go
- uast_canonical_coverage_test.go
- uast_contracts_test.go
- uast_direct_execution_test.go
- uast_direct_lowering_test.go
- uast_emission_recipes_test.go
- uast_function_flow_test.go
- uast_target_legalization_test.go

## Why tests are included

Tests provide machine-readable examples of required invariants such as:
- lossless Semantic roundtrips,
- deterministic readable serialization,
- preservation of contract planes,
- closure behavior,
- module embedding/resolution,
- executable closure,
- direct lowering,
- target legalization,
- canonical coverage and preservation.

Use them as normative evidence when prose is ambiguous.

## Bundled full transpiler

The complete Code Transpiler is bundled at:

`../../../transpiler/Code-Transpiler-main/`

Use it as a reference implementation and experimental teacher.

Important:
- The transpiler is not the definition of Semantic.
- Prefer canonical schema/tests/core model for language truth.
- When uncertain, inspect the relevant frontend/backend/transformation path in the transpiler.
- Generated large `.se` bundles inside the transpiler are valuable real-world examples of Semantic output.
