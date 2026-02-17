---
name: context-router-actualizer
description: Use this skill to actualize context-router.md routes and project-context/ documentation by diving into the codebase, identifying missing routes, updating existing docs, and ensuring documentation accurately reflects implementation.
---

# Goal
Maintain accurate and complete project documentation by actualizing context-router.md routes and project-context/ files to match the current codebase implementation.

# When to use
Use this skill when:
- Documentation may be outdated after code changes
- New features or modules have been added that lack documentation
- Routes in context-router.md need verification against actual files
- project-context/ docs need synchronization with implementation
- User requests documentation review or actualization

# Instructions
1. Dive into the application codebase
- Read current `project-context/` files to understand documented context
- Read codebase directories structure and key implementation files
- Identify major features, services, components, and workflows
- Check for implemented functionality that may not be documented
- Review configuration files and environment variables

2. Review existing context-router.md
- Load context-router.md from repository root
- Extract all route entries in "Project context map" section
- Verify each route points to an existing file
- Identify any route descriptions that may be outdated

3. Verify project-context/ file accuracy
- Read each file referenced in context-router.md routes
- Compare documented behavior against actual implementation
- Identify missing, incomplete, or outdated sections
- Check for new code patterns or services not covered

4. Identify missing logical routes
- Look for major features or workflows in code without corresponding routes
- Consider these common route categories:
  - Product flows (user journeys, workflows)
  - Architecture components (services, state management, data models)
  - API or integration patterns
- Do NOT create routes for routes themselves
- Keep routes focused on concrete functionality or concepts

5. Update context-router.md
- Add new routes for undocumented features or workflows
- Update route descriptions to match current implementation
- Fix any broken file paths
- Maintain consistent route naming and structure
- Preserve required sections and format constraints
- Keep descriptions clear, concise, and factual

6. Update or create project-context/ files
- For outdated files: update sections to reflect current implementation
- For missing files: create with accurate content based on code analysis
- Follow existing documentation style and structure
- Include only verified information from codebase
- Keep content clear, concise, and maintainable
- Use consistent section headers across similar doc types

7. Ensure documentation clarity
- Remove ambiguous or speculative language
- Replace vague descriptions with specific implementation details
- Ensure code examples or file paths are current and valid
- Verify terminology matches actual code identifiers
- Keep formatting simple (no bold, no tables in context-router.md)

8. Validate completeness
- Confirm all routes in context-router.md resolve to existing files
- Confirm major application features have corresponding documentation
- Confirm each project-context/ file has clear purpose and accurate content
- Confirm no duplicate or redundant routes exist

# Output expectations
After running this skill, the repository should have:
- context-router.md with accurate routes matching implementation
- All referenced project-context/ files exist and contain current information
- New routes added for previously undocumented features
- Updated docs reflecting code changes since last documentation pass
- Clear, concise, and maintainable documentation structure

# Constraints
- Do not modify source code or application files
- Do not remove routes that are still relevant
- Do not add routes for documentation files themselves
- Do not create nested or circular documentation references
- Keep context-router.md format rules intact (no bold, no tables)
- Preserve mandatory constraints section in context-router.md
- Only document what is actually implemented in code
- Do not add speculative or planned features to documentation

# Difference from context-router-initializer
- context-router-initializer: creates initial documentation structure from scratch
- context-router-actualizer: updates and maintains existing documentation to match code reality