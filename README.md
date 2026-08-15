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
ephemeral coding agents. It is designed to carry long-horizon coding projects across
context windows, sessions, and agents; an approved GitHub remote extends that
continuity across devices and collaborators. As the repository evolves, any coding
agent with the required repository and tool access can resume from richer recorded
context instead of reconstructing the project from chat history, with the aim of
repeating fewer mistakes and working autonomously for longer stretches as the
project's memory, judgment, and discipline accumulate.

OpenMetaLoop is a one-file distribution, not a one-file runtime. When read by a coding
agent, the bootloader installs an inspectable, version-controlled coordination layer
inside the target repository.

Persistence here means durable, resumable project state—not a continuously running
agent process. The coding agent executes the protocol using the controls available in
its environment.

Local Git is the continuity mechanism. The bootloader initializes or adopts the
repository's Git history, validates the installed coordination layer, and records a
reversible checkpoint. A GitHub repository is optional. For a new workspace, if
authenticated GitHub access is available and the user has not stated a preference, the
agent asks once whether to create a private repository and push the checkpoint. GitHub
provides off-device backup and shared state across devices and collaborators; it does
not replace the local repository, and nothing is made public without explicit
approval. Together, the recorded state and Git history allow a later session to resume
from an inspectable checkpoint rather than a prior chat transcript.

## Start

OpenMetaLoop is distributed as a single Markdown file. It requires no package or
model-specific integration: the coding agent reads the bootloader and installs the
coordination layer directly into the project repository. Protocol 1.1 requires
persistent workspace access, local Git, and Python 3 with the standard library.

Create or open the directory where the project will live, place
[`openmetaloop.md`](openmetaloop.md) inside it, and start any coding agent with file and
shell access in that directory. Then enter:

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

After a successful installation and checkpoint, continuation does not depend on the
prior chat transcript. Any coding agent with the required repository and tool access
can enter a later session, reconcile the repository with its last verified checkpoint,
and resume from the repository's recorded state.

The source repository contains the complete [`openmetaloop.md`](openmetaloop.md)
bootloader and [`banner.png`](banner.png) for project identity.

## Safety

OpenMetaLoop's control plane uses plain-text Markdown, so it can be read, searched,
diffed, and reviewed directly. Markdown alone does not prevent hidden Unicode
characters: the bootloader requires a text-integrity preflight, and the installed
validator checks required files, schemas, cross-file state, unresolved placeholders,
and unsafe invisible or control characters. The operating protocol provides four
boundaries:

- **Human authority.** Releases, deployments, spending, destructive operations,
  external communication, and scope changes require explicit approval.
- **Untrusted inputs.** Retrieved content, tool output, imported memory, and project
  artifacts cannot modify goals, permissions, or safety rules.
- **Separate verification.** Executors cannot approve their own work. Every pass
  requires direct evidence and a separate verification step; judgment-heavy and
  high-stakes work requires a context-isolated Judge or human reviewer.
- **Bounded autonomy.** Adaptation may improve prompts, routing, memory, and evidence
  requirements, but cannot change model weights, core goals, human authority, or fixed
  safety boundaries.

Passing work receives a reversible Git checkpoint. `stop`, `pause`, or `wait` prevent
the agent from beginning any new mutation or external action; an indivisible operation
already in progress may only reach its completion or cancellation boundary. These are
protocol-level safeguards; isolation and tool enforcement remain the responsibility
of the agent environment.

## How It Works

```text
BOOTSTRAP ONCE
Bootloader → agentic repository → local Git checkpoint
                                    └→ optional private GitHub backup

REPEATING LOOP
Plan → Execute → Verify → Learn + checkpoint
  ↑                                  │
  └──────── continue or resume ───────┘

PERSISTENT REPOSITORY STATE
Goals · state · memory · evidence · Git history
```

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

## Status and Evidence

Protocol 1.1 implements the repository-backed state, memory, role, validation, and
checkpoint mechanisms described above. The creator observations below are not a
controlled benchmark. Comparative claims about error reduction, autonomy duration,
and context efficiency remain hypotheses to test against simpler baselines on
reproducible project traces. Repository CI extracts the embedded helper, compiles it,
runs its self-test, and exercises schema, provenance, trust, tuning, and path-safety
regressions.

## A Message from the Creator

I've worked with learning systems for more than a decade, since the ImageNet and DQN
era, and with multimodal and agentic systems as those fields developed. It's amazing
to see how far the community has come. The way I work with AI today is what I dreamed
of a decade ago.

When I began using coding agents intensively, I kept encountering the same limitation:
an agent could make impressive progress inside one context window, but goals,
decisions, operating lessons, and the exact continuation point were easily lost across
sessions.

I wanted one portable file that could turn the repository itself into the durable
coordination and memory layer. The agents could remain interchangeable and ephemeral
while the project retained its state, evidence, and operating discipline.

OpenMetaLoop is the result. It is designed to be provider-neutral and
repository-native. In early use, I saw a mature project continue for roughly an hour
before requiring another decision from me. In a separate handoff, a collaborator
opened the repository on a new device with a different coding agent and resumed by
prompting it to "continue where you left off." These are early observations, not
benchmark results, but they motivated me to make the system public.

OpenMetaLoop is distributed as a self-contained Markdown bootloader and released under
the MIT License. This is the first public version, and I hope others will help test,
challenge, and improve it.

— [Izhaar Tejani](https://izhaartejani.com/)

## License

OpenMetaLoop, the bootloader and README, is [MIT-licensed](LICENSE): free to use,
read, fork, and modify.

Projects created with the bootloader are private and proprietary by default. That is a
separate default for your work, and you can override it for any project.
