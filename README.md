# Cursor Rules Library

A centralized repository of modular rules and instructions for AI assistants (Cursor and others) in a unified format.

## Purpose
- Version control and code review of rules through GitHub
- Reusable and connectable as Git submodule or via CI
- Modular loading of only necessary rules based on project context

## Repository Structure
.cursorrules # Entry point, references rule modules
.cursor/rules/
├── core/ # Core behavior (always)
├── context/ # MVP/Production, languages
├── frontend/ # React, TypeScript, UI
├── backend/ # Flask, Python, MongoDB, Java, Node.js
├── architecture/ # Design discussion and implementation
├── testing/ # Testing strategies
├── legacy/ # Legacy code handling
└── integration/ # CI/CD, GitHub Issues, tools
AGENTS.md # Instructions for any AI agents
README.md # Repository description and connection
README-ru.md # Russian version of README
CONTRIBUTING.md # Contribution guidelines
CONTRIBUTING-ru.md # Russian version of contributing guidelines

text

## Quick Start

### Adding to Project
1. Add repository as submodule:
git submodule add https://github.com/your-org/cursor-rules-library .cursor/rules

text

2. Create `.cursorrules` file in project root:
include:
- .cursor/rules/core/.mdc
- .cursor/rules/context/.mdc
- .cursor/rules/frontend/.mdc
- .cursor/rules/backend/.mdc
- .cursor/rules/testing/.mdc
- .cursor/rules/architecture/.mdc
- .cursor/rules/legacy/.mdc
- .cursor/rules/integration/.mdc
hierarchy:
- core
- context
- frontend
- backend
- architecture
- testing
- legacy
- integration

text

3. Restart agent - rules will load automatically.

## Contributing
See [CONTRIBUTING.md](CONTRIBUTING.md) for contribution guidelines.

---

*Maintained by your development team.*
