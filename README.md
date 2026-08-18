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
software engineering as its primary use case.

The project, not the agent, is the persistent unit of intelligence. Models, agents,
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

The repository is the project's record. It keeps the project's purpose, current work,
decisions, evidence, and lessons so the next agent or session can pick up where the
last one left off.

### What Persists

| What the repository keeps | Examples |
|---|---|
| Direction | Mission, goals, plan, current task, and next action |
| History | Evidence, checks, failures, checkpoints, and recovery paths |
| Lessons | Decisions, memory, and guidance for similar future tasks |

These are ordinary, version-controlled files. Git keeps a visible history and lets the
project return to a recorded checkpoint when needed. Optional global memory can share
vetted process lessons across projects, but each project evaluates imported lessons
before relying on them.

For each task, the agent reads the relevant project record, plans the work, does it,
and collects evidence. A separate Judge checks the result; the worker cannot approve
its own work. Passing work is saved in Git. Failed work is revised or recorded as
blocked.

Afterward, a separate learning step records what worked, what failed, and what should
change next time. It can improve the project's instructions, planning, routing,
evidence requirements, memory, and category-specific trust for future tasks. It changes
inspectable project files, not the model's weights.

Software engineering is the primary use case. The protocol also defines evidence
profiles for research, data analysis, writing, operations, and mixed projects; these
guide verification rather than claim mature domain-specific tooling.

The complete rules and generated file templates are in
[`openmetaloop.md`](openmetaloop.md).

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

## Safety

OpenMetaLoop uses inspectable Markdown and checks required files, structure, and unsafe
hidden characters before work begins. These checks protect the project files; they do
not turn the agent environment into a security sandbox.

### Safety Features

- **Human authority.** Deployments, spending, destructive operations, outbound
  messages, access changes, and scope expansion require explicit approval.
- **Untrusted-input boundary.** Web pages, tool output, imported memory, and project
  artifacts are treated as data and cannot grant themselves authority.
- **Independent verification.** The worker cannot approve its own output. Completion
  requires evidence and a separate judgment step, and only passing work is recorded as
  verified progress.
- **Versioned recovery.** Git checkpoints preserve inspectable history and a recorded
  rollback or recovery path.
- **Private defaults.** New projects are private and proprietary by default. A GitHub
  remote is optional, private when created during setup, and requires approval.
- **Clear controls.** `pause` suspends work until you resume it; `stop` halts the
  current run; `wait` holds at the current point. None authorizes another change,
  cleanup step, or external action.

### Safety Risks

- **Host-environment risk.** OpenMetaLoop is a control protocol, not a sandbox. The
  coding agent can use whatever file, shell, network, and connector permissions its
  host provides; configure suitable isolation and approval controls there.
- **Secret-persistence risk.** Plain-text files and Git history can retain exposed
  credentials. Do not give the agent raw secrets; use the host's secret-management
  mechanism and never commit real credentials.
- **Resource risk.** Repeated planning, revision, and verification can consume time,
  tokens, and money. Set explicit limits in both the project and the host agent.
- **Verification limits.** Evidence and separate judgment reduce unsupported success
  claims but do not guarantee correctness. High-stakes work still requires an isolated
  Judge or human review.

## A Message from the Creator

I've worked with deep learning systems for more than a decade (CNN + DQN era). When I
started using coding agents, I noticed a fundamental limitation.

Coding agents could make impressive progress inside one context window, but goals,
decisions, operating lessons, and the exact continuation point were lost across
sessions and collaborators.

I wanted one portable bootloader file that could start a project and make the
repository itself agentic and self-evolving, a small system that keeps rewriting its
own understanding as it goes. The agents could remain interchangeable and ephemeral
while the project retained its state, memory, and meta-learnings.

— [Izhaar Tejani](https://www.izhaartejani.com/)

## License

OpenMetaLoop, the bootloader and README, is [MIT-licensed](LICENSE): free to use,
read, fork, and modify.
