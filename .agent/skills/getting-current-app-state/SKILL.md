---
name: getting-current-app-state
description: Create or refresh a concise current-state.md that captures the real current project behavior, APIs, configuration, storage, and known gaps. Use when the user asks for current app state, project status, system snapshot, or planning baseline.
---

# Goal
Produce a clear, concise, and reliable `current-state.md` file that reflects the actual implemented state of the project.

# Instructions
1. Confirm scope:
   - Default output path is repository root: `current-state.md`.
   - If the user provides another path or filename, follow that.
2. Gather source-of-truth context:
   - Read `context-router.md`.
   - Read only the mapped files required for the current-state summary.
   - Inspect real code paths for backend entrypoints, frontend behavior, storage, and config.
3. Validate implemented behavior from code:
   - Verify active API endpoints and payload shapes in backend code.
   - Verify frontend flows (forms, fetch calls, loading/error states).
   - Verify storage model (files/directories/env overrides).
4. Write `current-state.md` with practical sections:
   - Summary
   - Implemented functionality
   - Backend API
   - Data and storage
   - Frontend behavior
   - Configuration
   - Repository structure (relevant paths)
   - Current limitations / not implemented yet
5. Keep output concise:
   - Prefer short bullets and short examples.
   - Include only what is implemented or directly inferred from code.
6. Verify before finalizing:
   - Ensure the file is usable as a planning baseline for future features.
   - Ensure terminology matches code and docs.

# Examples
User request: "Create current state file so I can plan next tasks."
Agent action:
1. Read `context-router.md` and mapped docs.
2. Verify backend/frontend behavior in code.
3. Create `current-state.md` with API contracts, storage, config, and gaps.

User request: "Refresh current-state.md after registration feature."
Agent action:
1. Re-check changed backend/frontend files and relevant project-context docs.
2. Update `current-state.md` to include registration behavior and constraints.

# Constraints
- Do not invent features, endpoints, or architecture that are not in code or mapped docs.
- Do not include unnecessary narrative, long prose, or speculative implementation details.
- Do not use bold formatting.
- Do not use table formatting.
- Do not overwrite a different target file unless the user asked for that path.
- Keep the file focused on present state, not full roadmap design.