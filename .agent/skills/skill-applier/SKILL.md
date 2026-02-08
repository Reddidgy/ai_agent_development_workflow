---
name: skill-applier
description: Use this skill to apply and adapt a specific Antigravity skill to the current project context. It ensures that skill instructions are mapped to project-specific paths and configurations.
---

# Goal
The goal of this skill is to intelligently apply an existing skill to the project by analyzing the project structure and adapting the skill's generic instructions to the local environment.

# Instructions
1.  Locate Target Skill:
    - Identify the skill to be applied (e.g., from `.agent/skills/`).
    - Read the `SKILL.md` of the target skill to understand its requirements and steps.
2.  Context Analysis:
    - Analyze the current project's directory structure (e.g., check for `src/`, `frontend/`, `backend/`, `api/`).
    - Identify configuration files (e.g., `package.json`, `requirements.txt`, `.env`).
3.  Instruction Mapping:
    - Map the generic paths in the target skill to the actual paths in the project.
    - If the skill requires specific technologies (e.g., React vs. Vue), ensure the implementation matches the project's stack.
4.  Sequential Execution:
    - Execute the adapted instructions one by one.
    - Use `run_command` for installations or scripts if specified and safe.
    - Use `write_to_file` or `replace_file_content` for code modifications.
5.  Verification:
    - Run tests or manual checks as defined in the target skill or as appropriate for the adaptation.
    - Document the changes made in a `walkthrough.md` if performing a complex task.

# Examples
> User Request: "Apply the `branding-themes-toggle` skill to this project."
>
> Agent Action:
> 1. Read `.agent/skills/branding-themes-toggle/SKILL.md`.
> 2. Identify that the project uses Vite and React in `frontend/`.
> 3. Adapt the CSS variable definitions to `frontend/src/index.css`.
> 4. Create the `ThemeToggle` component in `frontend/src/components/`.
> 5. Integrate the toggle into `MainLayout.tsx`.
> 6. Verify by running the dev server.

# Constraints
- Safety First: Never execute destructive commands without confirming they are adapted correctly.
- Consistency: Maintain the existing coding style and project architecture.
- No Overwriting: Do not overwrite critical project files unless specifically instructed or required by the skill.
- Portability: Ensure all resources from the target skill are correctly referenced or copied if necessary.
- Structure: Always follow the Goal -> Instructions -> Examples -> Constraints structure.
