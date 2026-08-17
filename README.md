# 🐶 OpenMetaLoop: One file to start new long-horizon coding projects across context windows and sessions.

<p align="center">
  <img
    src="banner.png"
    alt="OpenMetaLoop: One file to start new long-horizon coding projects across context windows and sessions."
    width="100%"
  >
</p>

OpenMetaLoop is a lightweight, repository-native control protocol for persistent,
long-horizon agentic work. It is delivered as a single Markdown bootloader, with
software engineering as its primary current use case.

**The project, not the agent, is the persistent unit of intelligence.** Models, agents,
developers, sessions, and context windows can change while the repository retains the
mission, current state, plans, decisions, evidence, failures, verified progress, and
operating knowledge. One agent can disappear entirely and another can resume from the
project's verified state without the previous conversation.

The Markdown file is the delivery mechanism, not the whole system. A coding agent reads
it once and installs an inspectable set of project files and Git history that coordinate
future work. Persistence belongs to the project instead of requiring one assistant or
provider-specific runtime to remain alive.

## How It Works

```text
Persistent Project
Goals · State · Plans · Evidence · Lessons
                    ↓
Plan → Build → Check → Learn → Save
  ↑                              │
  └──── Next Agent or Session ───┘
```

Before work begins, OpenMetaLoop selects the context relevant to the task. The agent
plans and executes the work, gathers evidence, and sends the result through a separate
judgment step; the worker cannot approve its own output. Only evidence-backed work is
saved as verified progress. Failed work is revised or recorded honestly as blocked.

After judgment, a Meta-Learning Agent records what worked, what failed, and what should
change next time. Verified outcomes can update the project's planning, task routing,
context selection, evidence requirements, memory, workflow tactics, and
category-specific trust. OpenMetaLoop learns outside the model: its operating policy
changes in inspectable files while model weights remain unchanged.

## Start

Put [`openmetaloop.md`](openmetaloop.md) in your project folder and open any coding
agent in that folder. The agent must be able to read and write files and run commands.
Git and Python 3 must be installed; GitHub is optional. Then enter:

```text
Read openmetaloop.md and use it to set up my new project.

Name:  <project name>
About: <one sentence describing the intended outcome>
```

OpenMetaLoop creates the goals, plan, memory, and safety rules, saves the starting point
in a new or existing Git repository, and begins the first task. Later, open any agent in
the same project and tell it to `continue`. With permission, OpenMetaLoop can create a
private GitHub repository for continuity across devices and collaborators; GitHub is
never required.

## What Persists

| Project layer | What it retains |
|---|---|
| **Direction** | Mission, goals, plans, current task, and next action |
| **Verified history** | Evidence, judgments, failures, checkpoints, and recovery paths |
| **Operating knowledge** | Decisions, lessons, memory, routing policy, and trust by task category |

These are ordinary, version-controlled files. Git is therefore more than source
control: it provides an inspectable history, reversible checkpoints, and a recovery
path. Optional, permission-gated global memory can share vetted process lessons across
projects; imported lessons remain untrusted until evaluated locally.

The protocol also defines evidence profiles for research, data analysis, writing,
operations, and mixed projects. They guide verification across those domains; they do
not imply mature domain-specific tooling.

The complete rules and generated file templates are in
[`openmetaloop.md`](openmetaloop.md).

## Safety

OpenMetaLoop uses inspectable Markdown and checks required files, structure, and unsafe
hidden characters before work begins.

- **You approve important actions.** No deploys, spending, destructive operations,
  messages, or scope changes without you.
- **Inputs cannot change the rules.** Web pages, tools, and imported notes are data
  only.
- **Proof is required.** The worker cannot approve its own output; completion requires
  evidence and a separate check.
- **Pause means stop.** No new change or external action starts until you resume.
- **Your environment enforces isolation.** OpenMetaLoop is a control protocol, not a
  security sandbox; use appropriate host permissions, isolation, and approval controls.
- **Secrets and budgets stay bounded.** Do not expose raw secrets, and set explicit
  token, cost, and time limits in the host agent.

Projects created with the bootloader are private and proprietary by default. Remote use
and public release require explicit approval.

## A Message from the Creator

I've worked with deep learning systems for more than a decade, since the CNN and DQN
era. When I began using coding agents intensively, I kept encountering the same
limitation: an agent could make impressive progress inside one context window, but
goals, decisions, operating lessons, and the exact continuation point were lost across
sessions and collaborators.

I wanted one portable file that could make the repository itself agentic. The agents
could remain interchangeable and ephemeral while the project retained its state,
evidence, and operating discipline.

— [Izhaar Tejani](https://www.izhaartejani.com/)

## License

OpenMetaLoop, the bootloader and README, is [MIT-licensed](LICENSE): free to use,
read, fork, and modify.
