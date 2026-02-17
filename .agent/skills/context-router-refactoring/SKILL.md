---
name: context-router-refactoring
description: Automatically refactors large documentation files (>300 lines) in project-context/ into structured directories with router files. Use when documentation files become too large and need to be split for better maintainability.
---

# Goal
Refactor large documentation files in project-context/ by splitting them into modular subdocuments when they exceed 300 lines, creating a router file with standardized navigation format.

# Instructions
1. Scan Documentation Files:
    - Recursively scan all markdown files in project-context/ directory
    - Count lines in each file to identify files exceeding 300 lines
    - Create a list of files that need refactoring
2. Analyze File Structure:
    - For each file exceeding 300 lines, analyze its content structure
    - Identify logical sections (typically marked by ## headings)
    - Plan how to split content into separate focused documents
3. Create Directory Structure:
    - For file project-context/path/to/document.md, create directory project-context/path/to/document/
    - Keep the original file project-context/path/to/document.md as the router file
4. Split Content into Subdocuments:
    - Create individual markdown files in the new subdirectory
    - Each file should represent a logical section from the original document
    - Use descriptive kebab-case filenames that reflect the content
    - Preserve all original content, headings, and formatting
5. Transform Original File into Router:
    - Replace the original file content with route definitions
    - Use the standardized format for each route:
      ```
      ## {{ROUTE_NAME}}
      {{ROUTE_DESCRIPTION}}
      Location: project-context/{{relative-path}}/{{filename}}.md
      ```
    - Keep route names clear and descriptive
    - Add brief descriptions that help users understand what each subdocument contains
6. Update context-router.md:
    - Update the corresponding entry in context-router.md
    - Change the description to indicate it's now a router file
    - Ensure the location path is still correct
7. Validate Refactoring:
    - Verify all content from original file is preserved in subdocuments
    - Check that all links and references still work
    - Ensure consistent formatting across all new files
8. Report Results:
    - List all files that were refactored
    - Show the new directory structure created
    - Confirm updates to context-router.md

# Examples
Example 1: Refactoring a large API integration file
> User Request: "Refactor project-context documentation"
>
> Agent Action:
> 1. Scans project-context/ and finds project-context/api/api-integrations.md with 522 lines
> 2. Analyzes content and identifies sections: App Store Connect, BrowserStack, Firebase, TestFlight
> 3. Creates directory project-context/api/api-integrations/
> 4. Creates files:
>    - project-context/api/api-integrations/app-store-connect.md
>    - project-context/api/api-integrations/browserstack.md
>    - project-context/api/api-integrations/firebase.md
>    - project-context/api/api-integrations/testflight.md
> 5. Transforms project-context/api/api-integrations.md into router:
>    ```markdown
>    ## App Store Connect Integration
>    API integration for managing iOS app releases and metadata on App Store Connect.
>    Location: project-context/api/api-integrations/app-store-connect.md
>    
>    ## BrowserStack Integration
>    Automated testing integration with BrowserStack for cross-device testing.
>    Location: project-context/api/api-integrations/browserstack.md
>    ```
> 6. Updates context-router.md entry for "API integrations"
> 7. Reports: "Refactored 1 file: api-integrations.md split into 4 subdocuments"

Example 2: Refactoring pipeline documentation
> User Request: "Refactor project-context documentation"
>
> Agent Action:
> 1. Finds project-context/pipelines/mobile-ios-app.md with 450 lines
> 2. Identifies sections: Build Process, Testing, Code Signing, Distribution
> 3. Creates project-context/pipelines/mobile-ios-app/ directory
> 4. Splits content into focused files
> 5. Updates the router file with proper navigation
> 6. Updates context-router.md

# Constraints
- Never delete or lose original content - all content must be preserved in subdocuments
- Only refactor files that exceed 300 lines
- Do not refactor files that are already router files (contain only route definitions)
- Always maintain the same heading hierarchy in subdocuments
- Use kebab-case for all new filenames
- Always update context-router.md after refactoring
- Do not refactor context-router.md itself
- Preserve all code blocks, formatting, and markdown structure
- Each subdocument should be self-contained and focused on one topic
- Route descriptions in router files should be concise (1-2 sentences)
- Always backup original content before starting refactoring
- Do not use bold formatting in generated documentation
- Do not use table formatting in generated documentation
- Keep router files clear and concise
- Subdocument filenames should not exceed 50 characters
- Each subdocument should ideally be under 300 lines itself