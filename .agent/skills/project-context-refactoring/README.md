# project-context-refactoring Skill

## Overview
This skill automatically refactors large documentation files in the project-context/ directory by splitting them into modular subdocuments when they exceed 300 lines. It creates a structured directory with a router file for better maintainability and navigation.

## Purpose
- Maintain documentation files at a manageable size
- Improve documentation navigation and discoverability
- Create a consistent structure across project documentation
- Make it easier to find and update specific documentation sections

## When to Use
Use this skill when:
- Documentation files in project-context/ exceed 300 lines
- You want to improve documentation structure and organization
- Files become too large and difficult to navigate
- You need to split monolithic documentation into focused topics

## What It Does
1. Scans all markdown files in project-context/ directory
2. Identifies files exceeding 300 lines
3. Analyzes file structure and logical sections
4. Creates subdirectories for each large file
5. Splits content into focused subdocuments
6. Transforms original files into router files with navigation
7. Updates context-router.md with new structure
8. Validates that all content is preserved

## Output Format
For a file like project-context/api/api-integrations.md:
- Creates directory: project-context/api/api-integrations/
- Creates subdocuments: app-store-connect.md, browserstack.md, etc.
- Transforms original file into router with format:
```
## {{ROUTE_NAME}}
{{ROUTE_DESCRIPTION}}
Location: project-context/{{relative-path}}/{{filename}}.md
```

## Constraints
- Only refactors files exceeding 300 lines
- Never deletes original content
- Preserves all formatting and structure
- Uses kebab-case for filenames
- Keeps subdocuments under 300 lines when possible
- Does not refactor context-router.md itself

## How to Apply
In your Agent interface, write:
```
Apply skill project-context-refactoring to refactor my project documentation
```

Or more specifically:
```
Use project-context-refactoring skill to analyze and refactor large files in project-context/
```

## Files Generated
- SKILL.md: Main skill definition with instructions and examples