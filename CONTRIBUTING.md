# Contributing to Statlib

Thank you for contributing to Statlib. Please open an issue before beginning a large formalization
or architectural change so that ownership and dependencies can be agreed in advance.

## Development requirements

- Use the Lean and Mathlib versions pinned by `lean-toolchain` and `lakefile.lean`.
- Place declarations in the subject-owned module described in `ARCHITECTURE.md`.
- Reuse existing Statlib and Mathlib declarations before adding new infrastructure.
- Do not introduce `sorry`, `axiom`, `admit`, or `native_decide`.
- Keep builds free of warning and info messages; remove unused parameters instead of hiding them.
- Preserve the copyright and author attribution of migrated files.

## Before submitting a change

Run the whole-library verification from the repository root:

```bash
LEAN_NUM_THREADS=$(nproc) lake build
```

Describe the mathematical result, its source, the owning module, and any API decisions in the pull
request. New modules should include a Mathlib-style file header and module docstring.
