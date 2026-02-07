---
name: skill-creator
description: Use this skill to create new Antigravity skills. It ensures that new skills follow best practices for directory structure, YAML metadata, goal definition, instructions, examples, and safety constraints.
---

# Goal
The goal of this skill is to architect and create a new Antigravity skill that is modular, reusable, and safe, following the "Anti-gravity" best practices.

# Instructions
1.  **Define Scope and Name**:
    - Determine if the skill is Workspace-scoped (`.agent/skills/<skill-name>/`) or Global-scoped (`~/.gemini/antigravity/skills/<skill-name>/`).
    - Use a short, descriptive `kebab-case` name for the skill directory.
2.  **Create Directory**: 
    - Create the skill directory if it doesn't exist.
3.  **Draft SKILL.md**:
    - Create the `SKILL.md` file within the directory.
4.  **Write YAML Frontmatter**:
    - `name`: Use the `kebab-case` identifier.
    - `description`: Write a clear, action-oriented summary. (Critical: The agent uses ONLY this to decide whether to trigger the skill).
5.  **Define Goal**:
    - State the skill's objective in a single, clear sentence under the `# Goal` heading.
6.  **Write Instructions**:
    - Provide a numbered list of step-by-step instructions under the `# Instructions` heading.
    - Be explicit and reference specific tools or commands.
7.  **Provide Examples**:
    - Include a few-shot example under the `# Examples` heading to guide behavior and output format.
8.  **Set Constraints**:
    - Define negative constraints (what NOT to do) under the `# Constraints` heading.
    - Include safety rules and output format requirements.

# Examples
> **User Request**: "Create a skill to format JSON files."
>
> **Agent Action**:
> 1. Create directory `.agent/skills/json-formatter`.
> 2. Create `.agent/skills/json-formatter/SKILL.md`.
> 3. Populate `SKILL.md` with:
>    ```markdown
>    ---
>    name: json-formatter
>    description: Automatically formats and validates JSON files using standard indentation. Use when the user asks to "prettify" or "fix" JSON.
>    ---
>    # Goal
>    Format and validate JSON files to ensure they are readable and syntactically correct.
>    ...
>    ```

# Constraints
- Do not overwrite existing skills without explicit user confirmation.
- Always include the `# Constraints` section in the new skill.
- Ensure the `description` in YAML is action-oriented and mentions the trigger conditions.
- Every skill created MUST follow the structure: YAML -> Goal -> Instructions -> Examples -> Constraints.
