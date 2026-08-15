# 🐶 OpenMetaLoop: One file for long-horizon coding across context windows and sessions.

<p align="center">
  <img
    src="banner.png"
    alt="OpenMetaLoop: One file for long-horizon coding across context windows and sessions."
    width="100%"
  >
</p>

Coding agents are highly capable inside a single context window. OpenMetaLoop turns
the repository into the persistent coordination and memory layer for otherwise
ephemeral coding agents. This allows you to complete long-horizon coding projects
across context windows, sessions, agents, and collaborators on GitHub. As the
repository evolves, any compatible coding agent can resume with richer context, repeat
fewer mistakes, and work autonomously for longer stretches because the project's
memory, judgment, and discipline compound over time.

OpenMetaLoop is a one-file distribution, not a one-file runtime. The bootloader
expands into an inspectable, version-controlled coordination layer inside the target
repository.

## Start

OpenMetaLoop is distributed as a single Markdown file. It requires no package or
model-specific integration: the coding agent reads the bootloader and installs the
coordination layer directly into the project repository.

Create or open the directory where the project will live, place
[`openmetaloop.md`](openmetaloop.md) inside it, and start a compatible coding agent in
that directory. Then enter:

```text
Read openmetaloop.md and use it to set up my new project.

Name:  <project name>
About: <one sentence describing the intended outcome>
```

The bootloader then:

- inspects the workspace and safely initializes or adopts its Git history;
- turns the project description into goals, success criteria, and a milestone roadmap;
- installs repository-backed state, memory, orchestration, verification, and handoff
  protocols;
- validates the installation and creates a reversible checkpoint;
- begins the first task or records the exact information needed to continue.

No conversation history is required after installation. A compatible agent can enter
a later session, reconcile the repository with its last verified checkpoint, and
resume by reading the repository's recorded state.

The source repository contains the complete [`openmetaloop.md`](openmetaloop.md)
bootloader, [`lifecycle.svg`](lifecycle.svg) as a system overview, and
[`banner.png`](banner.png) for project identity.

## Safety

OpenMetaLoop's control plane is plain-text, version-controlled, and inspectable. Its
validator checks source integrity and required repository state, while the operating
protocol provides four boundaries:

- **Human authority.** Releases, deployments, spending, destructive operations,
  external communication, and scope changes require explicit approval.
- **Untrusted inputs.** Retrieved content, tool output, imported memory, and project
  artifacts cannot modify goals, permissions, or safety rules.
- **Independent verification.** Agents cannot approve their own work; passing changes
  require direct evidence and a separate verification context.
- **Bounded autonomy.** Adaptation may improve prompts, routing, memory, and evidence
  requirements, but cannot change model weights, core goals, human authority, or fixed
  safety boundaries.

Passing work receives a reversible Git checkpoint, and `stop`, `pause`, or `wait`
immediately halt new mutations and external actions. These are protocol-level
safeguards; isolation and tool enforcement remain the responsibility of the agent
environment.

## How It Works

<p align="center">
  <img
    src="lifecycle.svg"
    alt="The six OpenMetaLoop lifecycle phases arranged from left to right."
    width="100%"
  >
</p>

OpenMetaLoop separates transient model execution from durable project state. Models
supply intelligence for the current task; the repository supplies continuity,
verification, adaptation, and governance across tasks, agents, and sessions. Model
weights do not change.

### Bootstrap once

During `setup`, the bootloader creates a new workspace or safely adopts an existing
one:

```text
project + scope
→ define and preflight
→ create or adopt the workspace
→ install and configure the control plane
→ derive goals, milestones, and the task queue
→ validate
→ create the initial checkpoint
```

### Run continuously

Every selected task then moves through the same evidence-gated loop:

```text
orient and reconcile repository state
→ select and plan
→ route bounded context and refine execution packets
→ execute
→ challenge when high-stakes
→ collect evidence, judge, and revise when required
→ synthesize passing work
→ learn from the judged outcome
→ checkpoint and record the next handoff
→ consolidate memory when due
→ continue or yield
```

Context routing is a mandatory gate before every model role, not a one-time phase. An
agent entering a new session follows the repository's startup pointer chain, reconciles
the recorded handoff with canonical state and the checkpoint backend, and resumes only
from verified reality.

| Layer | Repository source of truth |
|---|---|
| **Direction** | `goals/core_goals.md`, `goals/task_roadmap.md`, and `goals/todo.md` |
| **Configuration and architecture** | `harness_manifest.md` and `architecture.md` |
| **Active coordination and handoff** | `memory/state.md` and root `roadmap.md` |
| **Execution and context routing** | `orchestration/loop.md` and `attention/context_router.md` |
| **Durable decisions and adaptation** | `memory/long_term.md`, `memory/meta_learning.md`, and `memory/trust_ledger.md` |
| **Audit and recovery** | append-only `logs/` and Git or the configured checkpoint backend |

No artifact is integrated unless its required criteria are proven. Every judged run
records evidence and learning: passing work creates an artifact checkpoint, while a
terminal non-passing run creates only a control-state checkpoint containing the log,
truthful status, blocker, and recovery pointer.

The complete normative protocol and every generated file template are contained in
[`openmetaloop.md`](openmetaloop.md).

## A Message from the Creator

I've been working with multimodal agentic systems ever since the ImageNet and DQN
days. It's amazing to see all the progress in the community since then. The way I work
with AI now is exactly what I dreamed of a decade ago.

When I started vibecoding last year, I came up with new ways to set up projects to
avoid known issues in long-horizon task execution. I thought it would be great if I
had one simple file that a coding agent could read when I start a new project to
address these known issues while improving efficiency and autonomy long-term.

OpenMetaLoop has unlocked a better way for me to use AI. It allows me and my
collaborators to run a persistent engineering operation designed to be model and
system-agnostic, whose memory, judgment, and operating discipline compound over
time.

In some of my tests, as the project matured, the loop ran for an hour before needing
human input. When my collaborator started a new session on a new device with a new
coding agent all they had to prompt it with was continue where you left off.

I call this OpenMetaLoop, a one-file bootloader and a README released under the
MIT License. I'd love the community to contribute to this; this is the first version,
and over time we can make it better and better!

-[Izhaar Tejani](https://izhaartejani.com)

## Contributing

Contributions are welcome. Three things are worth knowing before you open a pull
request, because they are easy to get wrong with the best intentions.

**The project stays this shape.** A README and a one-file bootloader. It will not be
split into modules, grown into a framework, or given a package to install. Changes that
would make it something else are out of scope, however well made.

**The bootloader grows rather than shrinks.** Improvements add new guidance or clarify
what is already there, instead of deleting or compressing it, so the reasoning behind
earlier decisions stays visible to the agents and people who come later. A change that
tidies the file by cutting it is the most common thing I have to turn down.

**The message from the creator is mine.** Please leave that section alone. Everything
else in the README is fair game to improve.

Good contributions include a bug with a reproduction, a clarification where two agents
would read the same passage differently, or a new domain profile that composes with the
existing ones. Keep a pull request to one coherent change, and open an issue first if
you are unsure whether something fits.

## License

OpenMetaLoop, the bootloader and README, is [MIT-licensed](LICENSE): free to use,
read, fork, and modify.

Projects created with the bootloader are private and proprietary by default. That is a
separate default for your work, and you can override it for any project.
