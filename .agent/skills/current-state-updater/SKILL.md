---
name: current-state-updater
description: Update current_state.md with clear, concise summaries of the most recent changes. Use when the user asks to refresh or update current_state.md.
---

# Goal
Update current_state.md so it accurately and concisely reflects the latest implemented changes.

# Instructions
1. Open current_state.md and identify the sections impacted by the latest changes.
2. Add or adjust only the minimal lines needed to reflect the new behavior or files.
3. Keep wording concise, factual, and scoped to what changed.
4. If new files were added, list them under the relevant section (usually Frontend behavior or Repository structure).
5. Avoid restating unchanged behavior; focus only on deltas from the previous state.

# Examples
User request: "Update current_state.md for the last changes."
Expected action:
1. Add a short bullet describing the new behavior in the relevant section.
2. Add new files to the file list if applicable.

# Constraints
Do not edit files other than current_state.md unless the user explicitly asks.
Do not add verbose explanations; keep entries short and clear.
Do not use bold formatting or tables in the skill file.
