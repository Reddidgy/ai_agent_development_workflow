# context-router-actualizer

## Purpose
Maintains project documentation accuracy by actualizing context-router.md routes and project-context/ files to match current codebase implementation.

## When to use
- After implementing new features that need documentation
- When documentation may be outdated
- To verify routes point to correct files
- To discover and document undocumented features
- User explicitly requests documentation actualization

## How it works
1. Dives into source code to understand current implementation
2. Reviews context-router.md routes for accuracy
3. Verifies project-context/ files match code reality
4. Identifies missing routes for undocumented features
5. Updates context-router.md with new/corrected routes
6. Updates or creates project-context/ documentation files
7. Ensures clarity, accuracy, and completeness

## Key differences from context-router-initializer
- initializer: Creates documentation structure from scratch
- actualizer: Updates existing documentation to match code changes

## Output
- Accurate routes in context-router.md
- Up-to-date project-context/ files
- New routes for previously undocumented features
- Clear, concise, maintainable documentation

## Usage pattern
When user says:
- "Actualize the documentation"
- "Update context router"
- "Review and fix documentation"
- "I added X feature, update docs"

Agent should:
1. Apply this skill
2. Read relevant source code
3. Update context-router.md and project-context/ files
4. Report what was actualized

## Related skills
- `.agents/skills/context-router-initializer` - Initial setup
- `.agents/skills/current-state-updater` - Updates current_state.md
- `.agents/skills/getting-current-app-state` - Retrieves current state