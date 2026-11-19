# Evidence Audit Kit

An open workflow and set of agent skills for evidence-led engineering work.

Use an AI coding agent to inspect a codebase, write findings tied to a revision, investigate uncertain claims, help select work, draft scoped fixes, and check delivery evidence. The kit keeps evidence, implementation, verification, deployment, and acceptance distinct so an agent does not report more than the available evidence supports.

It supports engineering reviews for code quality, security, reliability, performance, and operations. The workflow is designed for an agent working with a developer: agents can carry out authorized inspection and implementation, while people retain decisions and authorization that belong to them.

## Use with an agent

1. Put this kit in the repository or workspace where your agent can read it. Keep real audit records and raw evidence in private project storage.
2. Ask the agent to read `AGENTS.md` and `docs/workflow.md` before starting.
3. For a new review, ask it to use `audit-write`. Use `audit-prove` when a claim needs investigation.
4. Use `audit-triage` to recommend dispositions. Use `fix-write` to plan an authorized change and `fix-done` to check its verification, deployment, and acceptance evidence.
5. Ask the agent to update the audit record with what it inspected, what it changed or checked, and what remains unknown.

The skills are in `.agents/skills/`. Codex can discover repository skills there. With another agent, provide the relevant `SKILL.md` as its instructions; exact integration depends on that agent. The workflow can also be followed without skill discovery by asking an agent to read the workflow and templates. This repository does not install or configure an assistant.

## What the kit provides

- Five focused agent skills for audit writing, investigation, triage, fix planning, and delivery review.
- Markdown templates for findings and scoped fixes.
- A fictional example showing how evidence and delivery status can change over time.
- A workflow for preserving revision context, evidence limits, decision authority, and separate implementation, verification, deployment, and acceptance states.

The agent performs the work it is authorized and equipped to do. The kit itself does not run commands, collect evidence, validate records, or connect to external services. The developer and agent still need to agree on access boundaries and which actions are authorized.

## Scope and limits

This is a lightweight workflow, not an audit platform or a guarantee of correctness. It has no automated validator, evidence collector, or external integration. Its usefulness depends on the quality of the agent's inspection and the evidence recorded. Review the agent's work, especially proposed decisions and changes.

Read `examples/synthetic-audit.md` for a fictional worked example. It contains no real trace or measurement.

## Privacy

Keep operational audits, raw evidence, customer data, internal links, and incident details in private project storage. Use synthetic examples when sharing or contributing. Before publishing changes, inspect the complete files and Git history. A secret scan can help find credentials, but cannot establish that business information is safe to disclose.

## License

MIT; see [LICENSE](LICENSE).
