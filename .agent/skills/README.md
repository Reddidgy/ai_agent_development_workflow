## ✅ How to Apply a Skill to Your Project

1. **Clone the Skill Repository**
   Place the skill repo (like `ai_devel...`) next to your project, *not inside it*.

2. **Copy `.agent` Folder**
   From the skill repo, copy the entire `.agent` folder into the root of your project:

```
your-project/
└── .agent/
└──── skills/
└────── [any-skill-folder]/
```

3. **Put Skill Inside `.agent/skills/`**
   Inside `.agent/skills/`, place the needed skill folder (e.g. `context-router-initializer`).

4. **Reference the Skill in Your Agent Prompt**
   In your Agent interface, write:

```
Apply adapted skill context-router-initializer to my project

--- specific instructions for the skill application, if needed ---

```