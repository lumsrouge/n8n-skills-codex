# Codex Migration Evaluation - Batch A

Scope: `n8n-mcp-tools-expert` and `n8n-workflow-patterns`

## What was checked

- Reviewed evaluation scenarios in:
  - `evaluations/mcp-tools/*.json`
  - `evaluations/workflow-patterns/*.json`
- Compared expected behavior against current skill content in:
  - `skills/n8n-mcp-tools-expert/SKILL.md`
  - `skills/n8n-workflow-patterns/SKILL.md`

## Findings

### 1) High-impact mismatch fixed

`evaluations/mcp-tools` still referenced pre-unified tool names (`get_node_essentials`, `get_node_info`, `validate_node_operation`) while skills now teach unified APIs (`get_node`, `validate_node`).

Updated these files to match current tool model:

- `evaluations/mcp-tools/eval-001-tool-selection.json`
- `evaluations/mcp-tools/eval-002-nodetype-format.json`
- `evaluations/mcp-tools/eval-003-validation-workflow.json`
- `evaluations/mcp-tools/eval-004-essentials-vs-info.json`

### 2) Workflow-pattern eval set

`evaluations/workflow-patterns` remains structurally aligned with the skill and did not require schema/tool-name changes in this batch.

## Next recommended batch

Run the same migration pass for:

- `evaluations/node-configuration`
- `evaluations/validation-expert`
- then `evaluations/code-javascript`, `evaluations/code-python`, `evaluations/expression-syntax`

These sets still include older tool naming in places and should be normalized to unified API terminology.
