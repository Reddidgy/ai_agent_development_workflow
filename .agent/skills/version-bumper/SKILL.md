---
name: version-bumper
description: Automatically increments the project version by running the version-bumping script. Use when asked to bump the version, prepare a release, or update the version file.
---

# Goal
The goal of this skill is to increment the project's patch version in `version` and stage the change in Git.

# Instructions
1.  **Run Bumping Script**:
    - Execute the command `python scripts/bump_version.py` from the project root.
2.  **Verify Output**:
    - Ensure the script outputs "Bumped version from X.Y.Z to X.Y.Z+1".
3.  **Check Git Status**:
    - Verify that `version` is staged (the script should do this automatically).
4.  **Report Progress**:
    - Inform the user of the new version number.

# Examples
> **User Request**: "Bump the project version."
>
> **Agent Action**:
> 1. Run `python scripts/bump_version.py`.
> 2. Observe output: `Bumped version from 1.0.5 to 1.0.6`.
> 3. Response: "Successfully bumped version to 1.0.6 and staged the change."

# Constraints
- Do not run the script if there are uncommitted changes in `version` that you didn't create.
- Only use the provided `scripts/bump_version.py` script.
- Do not attempt to manually edit the version file unless the script fails.
