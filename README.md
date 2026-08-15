# 🐶 OpenMetaLoop: One file to start new long-horizon coding projects across context windows and sessions.

<p align="center">
  <img
    src="banner.png"
    alt="OpenMetaLoop: One file to start new long-horizon coding projects across context windows and sessions."
    width="100%"
  >
</p>

Coding agents are highly capable inside a single context window. OpenMetaLoop turns
the repository into the persistent coordination and memory layer for otherwise
ephemeral coding agents.

It is designed to carry long-horizon coding projects across context windows, sessions,
and agents; an approved GitHub remote extends that continuity across devices and
collaborators.

As the repository evolves, any coding agent with the required repository and tool
access can resume from richer recorded context instead of reconstructing the project
from chat history, with the aim of repeating fewer mistakes and working autonomously
for longer stretches as the project's memory, judgment, and discipline accumulate.

OpenMetaLoop is a one-file distribution, not a one-file runtime. When read by a coding
agent, the bootloader installs an inspectable, version-controlled coordination layer
inside the target repository.

## Safety

OpenMetaLoop keeps its rules in readable Markdown files. Before work begins, a
preflight checks that those files are intact, complete, and free of hidden control
characters. The validator also checks the required files, links between them, and
unfinished placeholders.

Four simple rules govern the agent:

- **You approve high-impact actions.** The agent cannot release, deploy, spend money,
  delete data, contact people, or change the project scope without explicit approval.
- **Outside content cannot rewrite the rules.** Web pages, tool results, imported
  notes, and project files may provide information, but they cannot change the goals,
  permissions, or safety settings.
- **The agent must show its work.** A task is not complete because the agent says it
  is complete. It must produce direct evidence and pass a separate check. Important
  or high-stakes work also needs a fresh reviewer or a person.
- **The agent can adapt, but not take control.** It may improve its prompts, routing,
  memory, and evidence requests. It cannot change its core goals, bypass approval,
  or weaken the fixed safety rules.

After a successful check, the project receives a reversible Git checkpoint. `stop`,
`pause`, and `wait` prevent new changes or external actions from starting. A single
operation already in progress may finish or reach its cancellation point. The host
environment still provides the final process isolation and tool permissions.

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
saves the starting point in Git and begins the first task.

When you come back later, open any coding agent in the same project folder and tell it
to `continue`. The agent reads the saved project files instead of relying on the old
chat. With permission, OpenMetaLoop can also create a private GitHub repository so the
project can continue across devices and collaborators. GitHub is never required, and
nothing is made public without explicit approval.

## How It Works

```text
Set Up Once
One File → Project Plan + Memory

Repeat
Plan → Build → Check → Learn → Save
  ↑                              │
  └────── Continue Next Time ─────┘

Git Saves the Project History
GitHub Can Back It Up and Share It
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
operating lessons, and the exact continuation point were easily lost across sessions.

I wanted one portable file that could turn the repository itself into the durable
coordination and memory layer. The agents could remain interchangeable and ephemeral
while the project retained its state, evidence, and operating discipline.

— [Izhaar Tejani](https://izhaartejani.com/)

## License

OpenMetaLoop, the bootloader and README, is [MIT-licensed](LICENSE): free to use,
read, fork, and modify.

Projects created with the bootloader are private and proprietary by default. That is a
separate default for your work, and you can override it for any project.
