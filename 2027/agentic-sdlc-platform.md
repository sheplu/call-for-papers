# Beyond Coding Agents: Building the Platform Layer for the Agentic SDLC

## Elevator Pitch

AI coding agents are good at tasks — writing a function, fixing a test, refactoring a module. But software engineering isn't a series of isolated prompts: features span days, decisions outlive sessions, and work crosses pull requests, reviews, and releases. Today, the only durable record of that work is an agent transcript. Transcripts are not state — they're unbounded, untyped, and invisible to every other tool on your team.

What's missing is a platform layer for the agentic SDLC. In this talk I'll show what that layer needs: persistent, queryable state for long-running work; typed task graphs that connect commits to decisions; explicit approval boundaries where humans stay in control; observability across every agent run; and open APIs so agents stay replaceable.

I'll use Shepherd — a local-first platform written in Rust and TypeScript that deliberately does not orchestrate agents — as a running example of building the layer under the agents instead of another agent on top.

This talk isn't about autonomy. It's about the system that makes autonomy observable, replaceable, and controllable.

## Abstract

AI coding agents have crossed the quality threshold: they write working code, fix their own tests, and refactor confidently inside a single session. Yet teams adopting them at scale keep hitting the same wall. Features span days, decisions outlive sessions, and engineering work crosses pull requests, code reviews, releases, and interruptions. The agent's context window has become the de facto project state — and it's a terrible database.

The transcript-as-state model is failing in predictable ways. Context windows are unbounded in cost but bounded in attention: everything important must be re-explained, every session. Transcripts are untyped, so nothing downstream — dashboards, compliance, teammates — can consume them. And they're invisible to every other tool on the team, so each agent, plugin, and IDE lives in its own private bubble of what "the work" is.

The missing piece isn't a smarter agent. It's the platform layer underneath them: persistent, queryable state for long-running engineering work; typed task graphs that connect commits to the decisions behind them; explicit approval and policy boundaries so humans stay in control of consequential actions; observability across every agent run, not per-tool telemetry; and open APIs so the SDLC is shared infrastructure rather than a vendor's walled garden.

I'll ground this in Shepherd, a local-first platform built in Rust and TypeScript that deliberately does not orchestrate agents. Instead of being the agent that runs your SDLC, Shepherd is the substrate that any agent, model, or human can read from and write to — a durable, tool-neutral spine for tasks, decisions, and approvals. You'll see how representing engineering work as a durable graph changes what agents can be trusted with, and how it keeps them replaceable.

You'll leave with a concrete architecture for the agentic SDLC, and a set of platform-engineering ideas — event sourcing, workflow engines, control planes — that we can reuse instead of reinventing.

This talk isn't about autonomy. It's about the system that makes autonomy observable, replaceable, and controllable.

## Full Description

AI coding agents have crossed the quality threshold: they write working code, fix their own tests, and refactor confidently inside a single session. Yet teams adopting them at scale keep hitting the same wall. Features span days. Decisions outlive sessions. Engineering work crosses pull requests, code reviews, releases, handoffs, and interruptions. The agent's context window has become the de facto project state — and it's a terrible database.

### Transcript-as-state is failing

The current model — every agent keeps its own transcript, and "the work" is whatever fits in context — fails in predictable ways:

- **Unbounded and lossy.** Everything important must be re-explained every session. Institutional knowledge evaporates the moment a context window closes.
- **Untyped.** A transcript is prose. Nothing downstream — dashboards, compliance, teammates, other agents — can consume it without an LLM reading it.
- **Invisible.** Each agent, plugin, and IDE lives in its own private bubble of what "the work" is. There is no shared record.

### The missing platform layer

The missing piece isn't a smarter agent. It's the layer underneath them. An agentic SDLC needs platform infrastructure, the same way microservices needed control planes and CI/CD needed pipeline engines:

- **Persistent, queryable state** for long-running engineering work — tasks, decisions, artifacts — that survives sessions and outlives any single agent.
- **Typed task graphs** that connect commits to the decisions behind them, so the project's history is a graph, not a chat log.
- **Approval and policy boundaries** as first-class platform concepts: explicit gates where humans sign off on consequential actions, enforceable regardless of which agent proposed them.
- **Observability** across every agent run — spans, costs, outcomes — instead of per-tool telemetry that never joins up.
- **Open APIs** so the SDLC is shared infrastructure that any tool, model, or human can read from and write to, rather than a vendor's walled garden.

### Shepherd: the layer under the agents

I'll ground all of this in Shepherd, a local-first platform built in Rust and TypeScript that deliberately does not orchestrate agents. That constraint is the point: instead of being the agent that runs your SDLC, Shepherd is the substrate that any agent, model, or human can plug into — a durable, tool-neutral spine for tasks, decisions, and approvals. You'll see how representing engineering work as a durable graph changes what agents can be trusted with, how approval boundaries keep consequential actions human-gated, and how local-first persistence keeps the platform useful even when the network, the vendor, or the model isn't.

### We've built platforms before

The agentic SDLC is not uncharted territory — it's a platform-engineering problem, and we already have the ideas. Event sourcing gives us durable, replayable state. Workflow engines give us long-running tasks with human steps. Control planes give us policy and observability as infrastructure, not features. The talk closes by mapping which existing patterns to reuse, which to adapt, and which genuinely new problems agents introduce.

This talk isn't about autonomy. It's about the system that makes autonomy observable, replaceable, and controllable.

### Takeaways

- Why agent context should not be your project state
- How to represent long-running engineering work as a durable task graph
- Where human approval and policy boundaries belong
- How agents remain replaceable rather than becoming the platform
- How APIs and persistent state let multiple tools and models share one SDLC
- Which platform-engineering patterns to reuse instead of reinvent

## What the Audience Will Gain

- Why agent context should not be your project state
- How to represent long-running engineering work as a durable task graph
- Where human approval and policy boundaries belong
- How agents remain replaceable rather than becoming the platform
- How APIs and persistent state let multiple tools and models share one SDLC
- Which platform-engineering patterns to reuse instead of reinvent

## Target Audience

Platform and DevEx engineers, tech leads, staff engineers, and anyone shipping AI coding agents into real teams.

## Level

Intermediate — no AI/ML background needed.

## Suggested Duration

30–45 minutes (live demo of Shepherd possible)

## Tags

ai-agents, platform-engineering, developer-experience, sdlc, rust, typescript, observability
