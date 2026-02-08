---
name: main-system-prompt-initializer
description: Use this skill to initialize the main project documentation (system_prompt.md) by consolidating information from temporary setup files (about_system_prompt.md, some_information_about_project.md) and establishing the initial project structure section.
---

# Goal
Automate the initialization of `system_prompt.md` by importing project specifics from `some_information_about_project.md`, and setting up basic project sections, ensuring a clean and centralized documentation source.

# Instructions
1.  Read Source Information:
    -   Check for the existence of `some_information_about_project.md`. If present, read its entire content to extract:
        -   Project MVP description.
        -   Target audience / USP.
        -   Key features or capabilities.

2.  Update `system_prompt.md` Content:
    -   Application Overview: Replace "To be filled" with the Project MVP description and key features extracted from `some_information_about_project.md`. ensuring formatting is clean (lists/paragraphs, no bold/tables).
    -   Technology Stack: If specific stack info (e.g., Python, Flask) is known or inferable from context, update this section. Otherwise, leave as TBD or placeholders.
    -   Project Structure: Update the file structure listing to reflect current repository state (e.g., `.agent/`, `.git/`, `system_prompt.md`).
    -   Current Task: Clear the initial setup task or update it to "Project Initialized".

3.  Cleanup Source Files:
    -   Delete `some_information_about_project.md` (content has been migrated).

4.  Verification:
    -   Ensure `system_prompt.md` is updated and readable.
    -   Ensure source files are deleted.

# Constraints
-   Do NOT delete `system_prompt.md`.
-   Do NOT use bold or table formatting in `system_prompt.md`.
-   Do NOT fail if source files are missing; simply log/warn and proceed with available info.
-   Preserve existing `system_prompt.md` rules and structure.
