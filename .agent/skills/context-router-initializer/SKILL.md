---
name: context-router-initializer
description: Use this skill to initialize project context documentation by creating context-router.md and the project-context/ source-of-truth document set for any repository type.
---

# Goal
Create and initialize a consistent documentation foundation centered on `context-router.md` for any project type (full-stack app, backend-only, frontend-only, pipeline/data repo, infra/ansible repo).

# When to use
Use this skill when a repository does not yet have standardized project-context docs, or when older docs must be migrated to the context-router structure.

# Instructions
0. You MUST dive into the project and codebase
1. Detect repository shape and type
- Inspect top-level directories and key files to identify applicable areas:
  - Product/app docs
  - Architecture/docs
  - API/docs
  - Infra/deployment docs
- Keep one unified structure regardless of project type. If an area is not applicable, keep the section and mark as `N/A`.

2. Ensure canonical folder structure exists
- Create (if missing):
  - `project-context/product/`
  - `project-context/architecture/`
  - `project-context/api/`
- Create base files if missing:
  - `project-context/product/application-overview.md`
  - `project-context/product/implemented-features.md`
  - `project-context/architecture/technology-stack.md`
  - `project-context/architecture/project-structure.md`
  - `project-context/architecture/ui-objects.md`
  - `project-context/api/api-specification.md`

3. Create or update `context-router.md`
- Make `context-router.md` the entry point and source of truth pointer document.
- Enforce this exact high-level section order:
  1) context-router Purpose
  2) How to use this router
  3) Role and mission
  4) Mandatory constraints
  5) Project context map
  6) Response output format
  7) Current goal
- Keep wording concise and instruction-first.

4. Populate the project context map
- Always include these entries and paths:
  - Product overview and goals -> `project-context/product/application-overview.md`
  - Feature status -> `project-context/product/implemented-features.md`
  - Technology stack -> `project-context/architecture/technology-stack.md`
  - Repository layout -> `project-context/architecture/project-structure.md`
  - Frontend UI objects -> `project-context/architecture/ui-objects.md`
  - Backend API contract -> `project-context/api/api-specification.md`
- If a section does not apply to the repo type, keep the map entry and mark target file content as `N/A` with short reason.

5. Migrate from legacy docs when present
- Preserve useful constraints and architecture rules.
- Delete only explicitly deprecated bootstrap files after migration is complete.

6. Fill base files with minimal useful content
- `application-overview.md`: mission, target users, value, MVP scope.
- `implemented-features.md`: shipped features and current status.
- `technology-stack.md`: runtime, framework, storage, tooling.
- `project-structure.md`: top-level tree and ownership boundaries.
- `ui-objects.md`: screens/components, or `N/A` if no UI.
- `api-specification.md`: endpoints/contracts, or `N/A` if no API.

7. Verify
- Confirm `context-router.md` exists and references only valid paths.
- Confirm all mapped files exist.
- Confirm content has no tables and no bold formatting in `context-router.md`.
- Confirm instructions are clear for future routing.

# Required `context-router.md` baseline template
Use this baseline and adapt only the `Current goal` section to the active task:

You can use `.agent/skills/context-router-initializer/examples/web-app-context-router.md` for refference, but ensure the final `context-router.md` is related to the actual project!

# Constraints
- Do not fail if some source docs are missing; initialize with `TBD` or `N/A`.
- Keep `context-router.md` concise and deterministic.
- Do not introduce project-specific assumptions unless verified from repository files.

If user doesn't have any code we must just provide proper structure and instructions in `context-router.md` to fill it later.