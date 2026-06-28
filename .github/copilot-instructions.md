# AI Agent Instructions: gm-exec

## Big Picture

This repository implements `gm-exec`, an MCP-oriented code execution tool with multi-language support, CLI entrypoints, and background task handling.

Common change areas include:

- MCP server behavior
- runner lifecycle and isolation
- background execution semantics
- language/runtime support
- CLI/API compatibility
- publish and packaging workflows

## Design Maturity Baseline

Before implementation gets deep, use a lightweight design pass for:

- protocol or tool-surface changes
- task model / background execution redesign
- runner lifecycle or isolation changes
- security boundary changes
- compatibility-breaking CLI behavior changes
- major packaging or publish-flow changes

Start with:

- `docs/DESIGN_MATURITY_BASELINE.md`

## External Design References

External system-design resources such as ByteByteGo may be used as **reference-only** study material.

- keep repository documentation, diagrams, and design notes original
- do not copy/adapt restricted third-party material into this repository
- translate concepts into repo-specific trade-offs and behavior guarantees

## Implementation Rules

- preserve backward compatibility unless a breaking change is intentional and documented
- define timeout, backgrounding, and failure semantics explicitly
- document security implications for code execution and task isolation changes
- include rollback or compatibility notes for risky behavior changes
