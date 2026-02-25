# Codex Migration Wrap-Up

This document closes the migration batches for Codex compatibility and unified n8n-mcp tool naming.

## Completed batches

- Batch A: `mcp-tools` + `workflow-patterns`
- Batch B: `node-configuration` + `validation-expert`
- Batch C: `code-javascript` + `code-python` + `expression-syntax`

See:

- `docs/EVALUATION_BATCH_A.md`
- `docs/EVALUATION_BATCH_B.md`
- `docs/EVALUATION_BATCH_C.md`

## Final consistency checks

1. **Legacy tool terms**
   - No remaining references to deprecated names in active docs/skills:
     - `get_node_essentials`
     - `get_node_info`
     - `validate_node_operation`
     - `validate_node_minimal`

2. **Evaluation schema consistency**
   - `evaluations/**` uses `"skills": [ ... ]` consistently.

3. **Unified API guidance**
   - Discovery/config inspection: `get_node` with `detail: "standard"` by default.
   - Deep schema/debug: `get_node` with `detail: "full"` when needed.
   - Validation: `validate_node` with explicit `mode`/`profile`.

## Outcome

The repository is now aligned on Codex-first installation, skill metadata/routing, evaluation fixtures, and unified n8n-mcp terminology.
