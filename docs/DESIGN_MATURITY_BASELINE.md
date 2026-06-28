# gm-exec Design Maturity Baseline

**Purpose:** Provide a lightweight design standard for major behavioral or architectural changes in `gm-exec`.

## Use this before

- changing MCP protocol surface or tool contracts
- redesigning task timeout/background semantics
- changing runner lifecycle behavior
- adding/removing runtime support
- changing publish/distribution behavior
- introducing breaking CLI or server behavior

## Minimum design checklist

### 1) Scope

- What user-visible behavior changes?
- Who is affected: MCP clients, CLI users, package consumers?
- What is explicitly out of scope?

### 2) Behavioral contract

Document expected behavior for:

- foreground execution
- background handoff
- status polling
- task cleanup
- failure and timeout reporting

### 3) Compatibility

- Is this backward compatible?
- If not, what breaks and how is it communicated?
- Are docs/examples/tests updated accordingly?

### 4) Safety and security

- What code execution boundary is assumed?
- What isolation guarantees exist?
- What new abuse or escape paths could this change create?

### 5) Validation and rollback

Define:

- the test cases that prove the behavior
- how to verify no regression in existing CLI/MCP flows
- how to revert if the new behavior is unsafe or confusing

## External references

External system-design resources such as ByteByteGo are reference-only here. Keep repository design notes and diagrams original and specific to `gm-exec`.
