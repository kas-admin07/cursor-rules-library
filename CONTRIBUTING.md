# Contributing to Cursor Rules Library

We welcome contributions! Please follow these steps to add or update rules:

## Steps
1. Fork the repository and create a new branch for your changes.
2. Add or update `.mdc` rule files under the appropriate folder in `.cursor/rules/`.
3. For any rule file `rule-name.mdc`, provide a Russian translation as `rule-name-ru.mdc` with identical structure.
4. Ensure both files have matching `description`, `globs`, and `alwaysApply` values.
5. Commit with a clear message, e.g., `Add testing-strategies rule (EN & RU)`.
6. Open a Pull Request against `main`.
7. Include in your PR description:
   - Summary of changes
   - Affected modules (core, frontend, backend, etc.)
   - Any conflicts or deprecations

## Review Process
- Maintainers will check:
  - Correct file naming (`*.mdc` and `*-ru.mdc`)
  - Bilingual content consistency
  - Proper frontmatter fields
  - Valid and invalid examples included
- PRs should pass CI checks (linter, markdown validation).

## Bilingual Rule Files
- `example-rule.mdc` — English
- `example-rule-ru.mdc` — Russian

Ensure that English and Russian versions remain synchronized.

## Rule File Format
Each rule file must follow this structure:

description: "Detailed description when to apply this rule"
globs: *.tsx, *.ts (or leave blank)
alwaysApply: true/false

Rule Title
Critical Rules
Actionable rule 1

Actionable rule 2

Actionable rule 3

Examples
<example> ✅ Valid implementation </example> <example type="invalid"> ❌ Invalid implementation </example> ```
Thank you for improving Cursor Rules Library!
