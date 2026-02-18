---
name: current-state-updater
description: Update current-state.md with clear, concise summaries of new user-facing capabilities. Use when the user asks to refresh or update current-state.md after implementing features.
---

# Goal
Update current-state.md so it accurately reflects the latest user-facing capabilities in product-focused language.

# Instructions
1. Open current-state.md and identify the sections impacted by the latest changes.
2. Add or adjust only the minimal lines needed to reflect the new user capability.
3. Keep wording concise, user-focused, and scoped to what changed.
4. Group new capabilities under the appropriate "What Users Can Do Today" subsection.
5. Update version in Summary if version changed.
6. Add version entry to Version History section if significant feature was added.
7. Avoid restating unchanged capabilities; focus only on deltas.

# Examples
User request: "Update current-state.md for the last changes."
Expected action:
1. Add a short bullet describing the new user capability in the relevant subsection.
2. Update version number if changed.

User request: "Update current state after search feature."
Expected action:
1. Add "Search tasks across all columns" to View and Organize Tasks section.
2. Add version history entry if major feature.

# Constraints
- Do not edit files other than current-state.md unless the user explicitly asks.
- Do not add technical implementation details (no component names, service names, or code structure).
- Do not use bold formatting or tables.
- Keep entries short, clear, and user-focused.