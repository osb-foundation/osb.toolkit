# AGENTS.md — OSB Toolkit

This file guides coding agents working in the `osb.toolkit` repository.

## Project Identity

**OSB Toolkit** is a minimal GUI toolkit for OSB (Operating System Basic) freestanding programs. It provides window management, controls, graphics primitives, and desktop/input handling for building interactive text-mode applications.

## Code Policy

1. **Implementation Language**
   - Use **C#** for toolkit logic and UI components.

2. **Freestanding Constraints**
   - No BCL convenience, no GC allocations, no exceptions for normal control flow.
   - Fixed/stack buffers where appropriate.
   - Deterministic, bounded behavior over convenience frameworks.
   - Preserve freestanding safety: no managed heap allocation.

3. **Design Principles**
   - Keep components small and focused.
   - Minimize dependencies between modules.
   - Prefer explicit, simple control flow.

## Architecture

The toolkit is organized into focused modules:

- **App** - Application lifecycle
- **Control** - Base control class
- **Desktop** - Desktop/window management
- **Graphics** - Drawing primitives
- **Paint** - Paint operations
- **Types** - Common types
- **Window** - Window management

## Build and Validation

```bash
dotnet build
```

## Change Workflow for Agents

1. Inspect relevant files first.
2. Keep edits targeted.
3. Do not break compatibility with dependent projects (like osb.xwin).
4. Check file lengths before finishing (no file may exceed 400 lines).

## Non-Goals and Cautions

- Do not introduce BCL dependencies.
- Do not use exceptions for ordinary control flow.
- Do not break API compatibility with existing users of the toolkit.

## Documentation Anchors

- `README.md`: High-level project/user documentation.