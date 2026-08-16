# 🐶 OpenMetaLoop: One file to start new long-horizon coding projects across context windows and sessions.

<p align="center">
  <img
    src="banner.png"
    alt="OpenMetaLoop: One file to start new long-horizon coding projects across context windows and sessions."
    width="100%"
  >
</p>

Coding agents have become highly capable in single sessions but fail when operating across multiple context windows and collaborators.
OpenMetaLoop turns the repository into the persistent coordination and memory layer for otherwise ephemeral coding agent projects.

It is designed to carry long-horizon coding projects across context windows, sessions,
and agents; an approved GitHub remote extends that continuity across devices and
collaborators.

## Safety

OpenMetaLoop serves as a starter prompt to lay the foundation for your next coding agent project. Projects created with the bootloader are private and proprietary by default. OpenMetaLoop itself is not software and therefore does not execute code. However, because it drives autonomous LLM behavior, users must be aware of the following AI safety boundaries:

**Features**
* **Local-First Isolation:** Because OpenMetaLoop relies on local file management and Git repositories, code execution and changes stay isolated to your local environment unless you explicitly push them to a remote repository.
* **Version-Controlled Audit Trails:** Every decision, plan update, and progress milestone is recorded as a local Git commit history, ensuring every modification made by ephemeral coding sessions remains fully traceable, auditable, and reversible.
* **Deterministic Verification Guardrails:** Agents are explicitly forbidden from self-certifying their own work. The loop requires agents to validate code against objective, mechanical evidence (such as test suites or schema checks) before committing a state checkpoint, mitigating the risk of hallucinated success.
* **Private and Proprietary Defaults:** Projects initialized via the bootloader enforce private and proprietary boundary rules by default, preventing accidental exposure of sensitive business logic when cooperating with external agents.

**Risks**
* **Host Execution Constraints (Bring Your Own Sandbox):** OpenMetaLoop is a control protocol, not a security sandbox. It instructs your coding agent to run shell commands and modify files. You must ensure your coding agent is running in a secure, isolated environment (like a DevContainer or Docker) or configure it to require human approval before executing terminal commands.
* **Secret Persistence Risk:** Because OpenMetaLoop persists project memory, decisions, and history in plain-text Markdown files, agents may accidentally write API keys or passwords into the repository history if exposed to them. Never paste raw secrets into the chat or allow the agent to read `.env` files. 
* **Resource & Budget Bounding:** If an agent encounters persistent errors, the `Plan → Build → Check` loop can run continuously. Always set strict token limits or cost boundaries in your host coding agent to prevent budget exhaustion.



## Start

Put [`openmetaloop.md`](openmetaloop.md) in your project folder and open any coding
agent in that folder. The agent must be able to read and write files and run commands.
Git and Python 3 must be installed; GitHub is optional. Then enter:

```text
Read openmetaloop.md and use it to set up my new project.

Name:  <project name>
About: <one sentence describing the intended outcome>
```

That's it. OpenMetaLoop creates the project's goals, plan, memory, and safety rules. It
saves the starting point in a new or existing Git repository and begins the first task.

When you come back later, open any coding agent in the same project folder and tell it
to `continue`. The agent reads the saved project files instead of relying on the old
chat.

## How It Works

```text
Set Up Once
One File → Project Plan + Memory

Repeat
Plan → Build → Check → Learn → Save
  ↑                              │
  └────── Continue Next Time ─────┘

Git Saves the Project History
```

OpenMetaLoop writes the project's goals, plan, progress, decisions, and lessons into
the repository. That gives each coding agent a shared source of truth outside the chat.

For every task, the agent plans the work, builds it, checks the result, records what it
learned, and saves a checkpoint in Git. Work that does not pass its checks is revised
or recorded honestly as blocked.

When a session ends, the next agent reads the same repository, verifies the last saved
state, and can continue. Local Git keeps the history; an approved private GitHub
repository makes it available across devices and collaborators. OpenMetaLoop stores
its memory in the repository; it does not change model weights.

The complete rules and generated file templates are in
[`openmetaloop.md`](openmetaloop.md).

## A Message from the Creator

I've worked with deep learning systems for more than a decade, since the CNN and DQN era.
When I began using coding agents intensively, I kept encountering the same limitation:
an agent could make impressive progress inside one context window, but goals, decisions,
operating lessons, and the exact continuation point were lost across sessions and collaborators.

I wanted one portable file that could make the repository itself agentic. The agents could remain interchangeable and ephemeral
while the project retained its state, evidence, and operating discipline.

— [Izhaar Tejani](https://www.izhaartejani.com/)

## License

OpenMetaLoop, the bootloader and README, is [MIT-licensed](LICENSE): free to use,
read, fork, and modify.
