# Your AI Agents Need a Platform Team

## Elevator Pitch

AI agents are no longer just developer tools. They open pull requests, trigger pipelines, provision environments, and increasingly make changes that reach production. They are active participants in software delivery — but the platforms they operate on were designed for humans, and most organizations are letting agents in through the side door.

The common answer is broad access: cloud accounts, repository permissions, over-privileged credentials. That approach recreates the exact problems platform teams spent a decade solving — inconsistent workflows, excessive permissions, fragile automation, and activity nobody can audit.

The fix is not better agents. It's treating agents as first-class platform consumers: instead of raw infrastructure access, give them narrow, deterministic capabilities, and keep identity, policy, credentials, observability, and cost control in the platform where they belong.

This talk walks through the patterns that make it work: dual-audience platform APIs, controlled execution boundaries, agent identity and auditability, where MCP fits alongside traditional APIs and CLIs, and approval gates that don't destroy useful autonomy.

Platform engineering is the foundation of the Agentic SDLC. This talk is about building it that way.

## Abstract

AI agents are becoming active participants in software delivery. They open pull requests, run tests, trigger deployments, and increasingly make changes that reach production. But the platforms they operate on — portals, pipelines, cloud accounts — were designed for human consumers, and most organizations are letting agents in through the side door: shared credentials, broad repository permissions, direct access to cloud infrastructure.

That approach recreates the exact problems platform teams spent a decade solving. Inconsistent workflows reappear as every agent invents its own process. Excessive permissions reappear as over-privileged credentials no one dares to revoke. Fragile automation reappears as scripts that bypass every guardrail. And auditability disappears, because activity happens under identities nobody can attribute.

The fix is not better agents — it's treating agents as first-class platform consumers. Instead of handing agents infrastructure, expose narrow, deterministic capabilities: deploy this service, roll back that release, provision an environment, open a pull request, rotate this credential. Behind those capabilities, the platform keeps doing what platforms do: identity, policy, credentials, observability, and cost control.

The good news is that platform engineers already own most of the answer. Golden paths, internal developer platforms, well-designed APIs, CI/CD, short-lived credentials, policy-as-code, observability, and supply-chain controls all evolve naturally to serve a second kind of consumer. The patterns change less than we expect; the audience changes more.

I'll cover the architectural patterns in practice: designing platform APIs that work equally well for humans and agents, giving agents identities and least-privilege access, treating CI/CD and platform workflows as controlled execution boundaries, making agent activity observable and auditable, understanding where MCP fits alongside traditional APIs and CLIs, applying approval gates without destroying useful autonomy, and building golden paths agents can reliably discover and execute.

The goal is not to build a separate platform for AI. It's to evolve the platform you already have — so it serves human and machine consumers with the same paved roads. Platform engineering is the foundation of the Agentic SDLC, and this talk shows how to lay it.

## Full Description

AI agents are no longer just developer tools. They open pull requests, run tests, trigger pipelines, provision environments, and increasingly make changes that reach production. They are active participants in software delivery — and their numbers are growing.

There's a problem, though. The platforms those agents operate on — portals, pipelines, cloud accounts, repositories — were designed for human consumers. Most organizations are letting agents in through the side door: shared credentials, broad repository permissions, direct access to cloud infrastructure. Nobody sat down and decided agents should have all this access; it accumulated, one integration at a time.

That approach recreates the exact problems platform teams spent a decade solving:

- **Inconsistent workflows** reappear as every agent invents its own process.
- **Excessive permissions** reappear as over-privileged credentials no one dares to revoke.
- **Fragile automation** reappears as scripts that bypass every guardrail.
- **Auditability** disappears, because activity happens under identities nobody can attribute.

### Capabilities, not infrastructure

The fix is not better agents — it's treating agents as first-class platform consumers. Instead of handing agents infrastructure, expose narrow, deterministic capabilities: deploy this service, roll back that release, provision an environment, open a pull request, rotate this credential. Behind those capabilities, the platform keeps doing what platforms do: identity, policy, credentials, observability, and cost control.

In other words, agents get the same treatment we gave humans a decade ago: paved roads instead of raw keys.

### Evolving familiar concepts

The good news is that platform engineers already own most of the answer. Golden paths, internal developer platforms, well-designed APIs, CI/CD, short-lived credentials, policy-as-code, observability, and supply-chain controls all evolve naturally to serve a second kind of consumer. The patterns change less than we expect; the audience changes more.

### Practical architectural patterns

The talk covers eight patterns in practice:

- Design platform APIs that work equally well for humans and agents (dual-audience APIs).
- Prefer narrow, deterministic capabilities over broad cloud or repository permissions.
- Give agents identities with short-lived credentials and least-privilege access.
- Treat CI/CD and platform workflows as controlled execution boundaries.
- Make agent activity observable and auditable.
- Know where MCP fits alongside traditional APIs and CLIs.
- Apply approval gates without destroying useful agent autonomy.
- Build golden paths that agents can reliably discover and execute.

### The goal

The goal is not to build a separate platform for AI. It's to evolve the platform you already have — so it serves human and machine consumers with the same paved roads, the same guardrails, and the same audit trail.

Platform engineering is the foundation of the Agentic SDLC. This talk is about building it that way.

## What the Audience Will Gain

- How to design platform APIs that work equally well for humans and agents
- Why narrow capabilities beat broad cloud or repository permissions
- How to give agents identities with short-lived credentials and least-privilege access
- How to treat CI/CD and platform workflows as controlled execution boundaries
- How to make agent activity observable and auditable
- Where MCP fits alongside traditional APIs and CLIs
- How to apply approval gates without destroying useful agent autonomy
- How to build golden paths that agents can reliably discover and execute

## Target Audience

Platform engineers, DevEx/DevOps engineers, SREs, security engineers, and tech leads building internal developer platforms or shipping AI agents into engineering organizations.

## Level

Intermediate — familiarity with platform engineering concepts is helpful; no AI/ML background needed.

## Suggested Duration

30–45 minutes

## Tags

ai-agents, platform-engineering, developer-experience, idp, mcp, security
