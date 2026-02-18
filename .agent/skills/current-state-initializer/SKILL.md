---
name: current-state-initializer
description: Create or refresh a concise current-state.md that captures what users can do today, key features, data storage approach, and current limitations. Use when the user asks for current app state, project status, or planning baseline.
---

# Goal
Produce a clear, concise, and product-focused `current-state.md` file that reflects the actual implemented capabilities of the project from a user perspective.

# Instructions
1. Confirm scope:
   - Default output path is repository root: `current-state.md`.
   - If the user provides another path or filename, follow that.
2. Gather source-of-truth context:
   - Read `context-router.md`.
   - Read only the mapped files in `project-context/product/` for feature context.
   - Check version file for current version number.
3. Write `current-state.md` with product-focused sections:
   - Summary (what the app is, current version)
   - What Users Can Do Today (capabilities grouped by user workflow)
   - Data Storage (simple explanation of where data lives)
   - Current Limitations (what is not yet available)
   - Version History (brief changelog of recent versions)
4. Keep output concise and user-focused:
   - Prefer short bullets describing user-facing capabilities.
   - Avoid technical implementation details (no service names, component names, internal types).
   - Focus on what users can do, not how the code works.
5. Verify before finalizing:
   - Ensure the file reads like product documentation, not technical specification.
   - Ensure terminology is user-friendly.

# Examples
User request: "Create current state file so I can plan next tasks."
Agent action:
1. Read `context-router.md` and product docs.
2. Create `current-state.md` with user capabilities, storage summary, and gaps.

User request: "Refresh current-state.md after task creation feature."
Agent action:
1. Re-check relevant product documentation.
2. Update `current-state.md` to include new user capability in appropriate section.

# Constraints
- Do not invent features that are not implemented.
- Do not include technical details like service names, component architecture, or internal types.
- Do not use bold formatting.
- Do not use table formatting.
- Keep the file focused on product capabilities, not code structure.