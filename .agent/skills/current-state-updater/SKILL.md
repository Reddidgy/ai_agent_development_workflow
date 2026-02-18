---
name: current-state-updater
description: Perform comprehensive research of project documentation and update current-state.md with accurate, user-facing capabilities. Use when the user asks to refresh or update current-state.md.
---

# Goal
Update current-state.md so it accurately reflects the latest user-facing capabilities in product-focused language after comprehensive project research.

# Research Phase (MANDATORY)
Before making any changes, gather full context by reading `project-context/` and all relevant documentation of the project!

# Update Phase
After research, update current-state.md:

1. Compare researched capabilities against current-state.md content.
2. Identify missing, outdated, or inaccurate user-facing capabilities.
3. Update version in Summary section if changed.
4. Add new capabilities under appropriate "What Users Can Do Today" subsection.
5. Remove or correct outdated limitations.
6. Add version history entry for significant features since last documented version.
7. Keep wording concise, user-focused, and scoped to actual capabilities.

# Examples
User request: "Update current-state.md for the last changes."
Expected action:
1. Read all documentation sources listed in Research Phase.
2. Compare against current-state.md.
3. Add bullets describing new user capabilities in relevant subsections.
4. Update version number and history.

User request: "Update current state after search feature."
Expected action:
1. Read task-search-workflow.md and implemented-features.md.
2. Add "Search tasks across all columns with title-priority ranking" to View and Organize Tasks.
3. Add version history entry.

# Constraints
- MUST complete Research Phase before making any edits.
- Do not edit files other than current-state.md unless explicitly asked.
- Do not add technical implementation details (no component names, service names, or code structure).
- Do not use bold formatting or tables.
- Keep entries short, clear, and user-focused.
- Ensure all documented capabilities are actually implemented (verified via implemented-features.md).