# Main Development AI Prompt

This directory contains the primary system prompt template used to initialize AI development agents for software engineering tasks.

## What is it?

The `system_prompt.md` is a foundational persona and rule-set designed for AI agents. It establishes:
- **Role**: Senior Full-Stack Developer and Solution Architect.
- **Mission**: Architecting and building clean, scalable, and maintainable software.
- **Strict Guidelines**: Mandatory confirmation sentences, OS-specific command awareness, and non-negotiable quality priorities.
- **Standardized Output**: A structured response format to ensure consistency across all agent interactions.

## How to use it first time?

1. **Copy the Template**: file `system_prompt.md` to your repository (to the root for example).
2. **Replace Placeholders**: Fill in the following placeholders:
    - `___OS_TYPE___`: The operating system you are working on (e.g., MacOs, Linux, Windows).
    - `___APPLICATION_NAME___`: The name of the application being developed.
3. **Replace More**: Replace anything generic to your project related
4. **Set Your First Task**:
    - `___YOUR_FIRST_TASK_TO_AI_AGENT___`: The initial objective for the AI agent.
5. **Initialize your Agent**: And provide him the only sentence `You MUST Read updated system_prompt.md file and achieve the goal!`

## How to use it iteratively?

1. **Set Your Task In The Goal Section**:
2. **Initialize your Agent**: And provide him the only sentence `You MUST Read updated system_prompt.md file and achieve the goal!`  
(I'm using shortcut just for this sentence)

## Placeholders

- `___OS_TYPE___`: Operating system context for command execution.
- `___APPLICATION_NAME___`: Subject of the development work.
- `___YOUR_FIRST_TASK_TO_AI_AGENT___`: The goal to be achieved by the AI agent.

## Tips
1. You can ask update your app specification by the agent after the implementation  
...