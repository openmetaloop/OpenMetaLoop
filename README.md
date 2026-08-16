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

Before work begins, OpenMetaLoop checks that its files are complete and unchanged.

- **You approve important actions.** No deploys, spending, deletion, messages, or scope changes without you.
- **Inputs cannot change the rules.** Web pages, tools, and imported notes are data only.
- **Proof is required.** The agent must show evidence and pass a separate check.
- **Pause means stop.** No new change or external action starts until you resume.

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

Projects created with the bootloader are private and proprietary by default. That is a
separate default for your work, and you can override it for any project.
