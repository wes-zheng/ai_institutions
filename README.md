# From Agents to Institutions

[![DOI](https://zenodo.org/badge/1227585368.svg)](https://doi.org/10.5281/zenodo.20033468)

**I started with agents. I ended up needing an institution.**

This repo is a public technical report and reference package about a simple idea:

> If AI is going to do real work, the interesting question is not only whether an agent can act. It is whether the work can be owned, authorized, reviewed, stopped, closed, replayed, and improved.

Current agent stacks are getting good at tools, memory, handoffs, traces, workflows, and multi-agent collaboration. Those are important. But after running a human-owned, AI-staffed operational desk, I kept seeing failures that did not look like model failures anymore.

They looked like organizational failures.

A task had no owner. A plausible answer had no verifier decision. A tool-using worker could see data but was not authorized to act. A message was stale but still triggered work. A workflow finished but the governing record stayed open. A lesson was written in chat but never changed the playbook.

So the core claim of this project is:

> **AI labor needs institutions, not just agents.**

Not institutions in the legal or bureaucratic sense. I mean the small, durable control surfaces that make work accountable: owners, roles, records, review gates, stop states, closure, replay, and doctrine updates.

---

## The 2-minute version

Most agent demos ask:

> Did the agent complete the task?

Real work asks more annoying questions:

| Agent question | Work question |
| --- | --- |
| Can it act? | Who owns this now? |
| Can it use tools? | What is it authorized to do? |
| Can it hand off? | Did accountability actually transfer? |
| Can it remember? | Did the lesson become durable doctrine? |
| Can it finish? | Who accepted closure? |
| Can it produce output? | Was no-action the right output? |

The last row is underrated. In real operations, the correct answer is often:

- do not send;
- decline;
- wait for evidence;
- reroute;
- keep open;
- close with no downstream action;
- replay later after ground truth arrives.

If your AI system has no first-class way to represent those states, it will tend to create motion instead of accountable work.

---

## The bug I kept hitting

The system did not fail only because an AI worker was dumb.

It failed because the worker was operating inside a weak institution.

Examples:

1. **Broad intent did not become owned work.**  
   A manager-level request sounded clear in chat, but no child record had a precise owner, next action, and closure condition.

2. **Tool access looked like authority.**  
   A worker could inspect data, but seeing data is not the same thing as being allowed to act on it.

3. **Review was not a state.**  
   A verifier could write comments, but unless the output became `accept`, `repair`, `reroute`, `decline`, `block`, or `approve`, no one knew what had actually happened.

4. **Completion was not closure.**  
   Agents love saying they are done. Work is only closed when the right owner or manager accepts the final state.

5. **Memory was not doctrine.**  
   A lesson in chat helped the current conversation. It did not reliably change what the next worker would do.

6. **Reflection was not learning.**  
   A postmortem is not learning unless it lands somewhere durable: a role contract, playbook, tool rule, workboard rule, message rule, staffing change, topology change, or an explicit `case-only` note.

This project is my attempt to name that missing layer and make it testable.

---

## What I mean by an AI institution

An **AI organization** is not just many agents.

It is a control system around agents.

```text
model
  -> agent
  -> workflow / team
  -> organization

unit of control:
generation -> tool action -> routed steps -> institutional labor
```

The institutional layer asks whether work is:

```text
owned
  -> authorized
  -> evidence-backed
  -> reviewed
  -> stoppable
  -> closed
  -> replayed
  -> improved
```

In the report, I call this **institutional control**.

The basic primitives are:

| Primitive | Plain-English meaning |
| --- | --- |
| `EmployeePrincipal` | a persistent AI worker identity with a role, inbox, tools, and history |
| `RoleContract` | what the worker owns, what it is forbidden to do, and when it must escalate |
| `WorkRecord` | the source of truth for a work item |
| `WorkMessage` | an auditable trigger or handoff, not just a chat message |
| `VerifierDecision` | stateful review: accept, repair, reroute, decline, block, or approve |
| `NoActionState` | a valid stop, no-send, decline, stand-down, already-done, or explicit zero |
| `ClosureDecision` | accepted final state, not self-declared completion |
| `ReplayRecord` | delayed outcome truth and what should be learned from it |
| `MutationRecord` | a governed change to roles, playbooks, tools, messages, topology, staffing, or workboard rules |

The model call is one worker cycle inside this larger structure.

---

## Why a prediction-market desk?

The field setting was a human-owned, AI-staffed prediction-market desk.

That sounds niche. It is deliberately stressful.

Prediction-market work forces the system to deal with:

- uncertain evidence;
- changing external state;
- role boundaries;
- risk review;
- execution authority;
- valid no-action;
- delayed settlement;
- post-outcome replay.

That makes it a good stress test for institutional control.

But this is **not** a trading-strategy repo. It is not financial advice. It does not claim trading performance. The point is not that AI systems should trade. The point is that high-skill AI work needs explicit ownership, authority, evidence, review, stopping, closure, replay, and learning.

The same pattern shows up in security operations, software release review, compliance workflows, research operations, support escalations, data analysis, and any team where an AI system can create work faster than humans can govern it.

---

## What changed after adding the institutional layer?

The report is careful about evidence. This was not a randomized benchmark and not a deployment-wide causal proof.

Still, the audits found useful bounded signals.

| Finding | Evidence in the report | Safe interpretation |
| --- | --- | --- |
| Manager closure became visible. | A pre/pressure sample showed **12/43** closure-state failures or complete/open pressures. A post-gate sample showed **0/36** such failures. | In the coded samples, the closure gate made final state auditable. |
| Mature work paths exposed final state. | **20/20** final live dispositions reached manager verification, with **0/20** unresolved review gaps after final closeout. | The selected mature closeout window was auditable. |
| No-action became first-class. | In one mature window, **6/6** applicable no-execution paths had explicit no-action or no-replay treatment. | The system could represent “do nothing” as a real outcome. |
| Replay became separable from live work. | **14/14** ordered/replay paths were replay-closed in the selected mature window. | Outcome reconciliation became a separate state, not a chat afterthought. |
| Message discipline became inspectable. | A post-window inbox audit sampled **220** rows across **11** AI employees, with **218** eligible work-trigger opportunities and no stale/superseded action observed. | Strong post-window auditability, without a matched historical denominator. |
| The broader corpus reduced cherry-pick concern. | A private expanded audit covered **237** Linear-traceable issue IDs across several strata. | Better than selected-window-only evidence, but still not a random full-corpus estimate. |

The conservative takeaway:

> Institutional controls did not prove that the AI was “better” in every sense. They made the work more inspectable, more stoppable, and more governable.

For real AI work, that matters.

---

## A tiny example

Imagine you ask an AI worker:

> “Review this customer-impact incident and send the update.”

A normal agent stack might produce a polished message.

An institutional stack asks:

```text
Who owns the incident record?
What evidence is attached?
Is this worker authorized to send externally?
Did a verifier accept, repair, reroute, decline, or block?
Is the message stale because the incident state changed?
Is no-send the correct action?
Who can close the work?
After the incident resolves, does replay change the playbook?
```

That can sound bureaucratic. But it is exactly the difference between “an AI wrote something” and “the work survived contact with operations.”

---

## Try the idea in your own workflow

You do not need my system to try the core idea.

Pick one recurring workflow where you already use AI. For example:

- code review;
- security triage;
- customer escalation;
- sales research;
- research synthesis;
- incident review;
- compliance checklist;
- data-analysis request.

Then create a minimal `WorkRecord` before asking the AI to act.

```yaml
work_record:
  id: WR-001
  owner: ai_research_assistant
  human_owner: you
  status: open
  exact_ask: "Analyze these customer complaints and propose next action."
  accepted_evidence:
    - support_ticket_export
    - product_release_notes
  forbidden_actions:
    - email_customer_directly
    - change_account_status
  verifier_required: true
  no_action_allowed: true
  next_action: "prepare evidence-backed recommendation"
  closure_rule: "human accepts, keeps open, or reroutes"
  replay_rule: "after outcome, classify lesson as playbook change or case-only"
```

Now force every AI output to end with this:

```yaml
institutional_state:
  owner: ...
  next_action: ...
  evidence_used: ...
  verifier_decision_needed: yes/no
  action_authorized: yes/no
  no_action_state: none/no-send/decline/blocked/stand-down/already-done/explicit-zero
  closure_state: open/closed/kept-open/rerouted
  replay_needed: yes/no
  doctrine_mutation_candidate: role/playbook/tool/message/workboard/topology/staffing/case-only/none
```

This one change catches a surprising amount of fake progress.

---

## The five checks I now use before trusting AI work

### 1. Ownership

Can I point to the current owner of the work item?

If not, I do not have a work system. I have a transcript.

### 2. Authority

Can this worker do the thing it is proposing to do?

Tool access is not authority. Seeing a database, inbox, repo, ticket, or market does not mean the worker is allowed to mutate it.

### 3. Evidence

Can a verifier reconstruct the output from attached evidence?

If not, it is plausible prose.

### 4. Closure

Who accepted that this is done?

A workflow can finish while the work remains open. An agent can say “complete” while a manager would say “blocked,” “reroute,” or “keep open.”

### 5. Replay

After the real-world outcome arrives, what changes?

If the answer is “the AI remembers,” that is not enough. Memory is private continuity. Doctrine is shared institutional state.

---

## What is in this repo

| Path | What it is for |
| --- | --- |
| [`technical_report/paper.pdf`](technical_report/paper.pdf) | formatted technical report |
| [`technical_report/paper.md`](technical_report/paper.md) | manuscript source |
| [`technical_report/paper.tex`](technical_report/paper.tex) | generated LaTeX artifact |
| [`technical_report/references.bib`](technical_report/references.bib) | bibliography |
| [`examples/`](examples/) | synthetic, non-trading examples for trying the idea safely |
| [`examples/security_incident_ops_team/`](examples/security_incident_ops_team/) | example of institutional-control semantics in a security-incident workflow |
| [`api/`](api/) | minimal public setup notes for the reference implementation |
| [`CITATION.cff`](CITATION.cff) | citation metadata |
| [`LICENSE`](LICENSE) | CC BY 4.0 license for the public paper, docs, and examples |

Start with the report if you want the research argument. Start with the security-incident example if you want the fastest non-trading way to test the mental model.

---

## What this is not

This repo does **not** claim:

- financial performance;
- forecasting accuracy;
- a trading strategy;
- autonomous trading safety;
- deployment-wide causal improvement;
- model-independent superiority;
- that the public synthetic example proves the field-study results;
- that every institutional primitive is novel by itself.

The claim is narrower and, I think, more useful:

> Some failures we blame on agents are really failures of the institution around the agents.

---

## Why I think this matters for human work

The optimistic version of AI at work is not “replace the whole team with a swarm of agents.”

The useful version is more boring and more powerful:

- fewer orphaned tasks;
- fewer stale handoffs;
- fewer unreviewed plausible answers;
- fewer actions without authority;
- more valid no-action;
- clearer human ownership;
- better post-outcome learning;
- less time spelunking through chat transcripts trying to figure out what happened.

The goal is not to make AI systems more autonomous for its own sake.

The goal is to make AI labor accountable enough that humans can safely delegate more low-leverage coordination work and spend more time on judgment, taste, strategy, and responsibility.

---

## FAQ

### Is this just “multi-agent systems”?

No. Multi-agent systems ask how agents coordinate. This project asks whether work has durable institutional state: owner, authority, evidence, verifier decision, no-action, closure, replay, and mutation.

A multi-agent team can still lose accountability in chat.

### Is this just project management?

Partly, and that is the point.

Human organizations already learned that work needs ownership, review, escalation, closure, and postmortems. AI agents do not make those needs disappear. They make them more urgent because they can produce convincing work very quickly.

### Is this just bureaucracy?

Bad institutional control is bureaucracy.

Good institutional control is the smallest set of durable fields needed to prevent fake progress, unauthorized action, stale work, and forgotten learning.

### Why use the word “employee”?

Only as an operational term. An AI employee here means a persistent institutional principal with a role, inbox, tools, authority limits, and history. It is not a legal, moral, or anthropomorphic claim.

### Can I use this without building a whole platform?

Yes. Start with a work-record template and force every AI output to declare owner, evidence, authority, no-action, closure, and replay state.

You can do this in a spreadsheet, issue tracker, Markdown file, or ticket system.

### What would make this stronger research?

Public-safe row-level audit packets, independent coding, stronger pre/post denominators, recurrence checks after doctrine changes, and synthetic benchmark tasks for institutional control.

I am interested in those next.

---

## Open questions

I would love feedback on these:

1. What is the minimal institutional schema that catches most AI-work failures without creating too much overhead?
2. Can no-action be benchmarked well?
3. How should verifier decisions be represented across different domains?
4. When should a replay result mutate doctrine versus stay case-only?
5. Can agent benchmarks include ownership, authority, closure, and replay, not only task success?
6. What does a good “AI organization protocol” look like above MCP, A2A, workflows, and agent SDKs?

---

## Suggested reading path

For a quick read:

1. Read this README.
2. Skim the abstract in [`technical_report/paper.pdf`](technical_report/paper.pdf).
3. Open [`examples/security_incident_ops_team/`](examples/security_incident_ops_team/) and map the primitives to your own workflow.

For the full argument:

1. Read [`technical_report/paper.md`](technical_report/paper.md).
2. Look at the evidence tables and limitations.
3. Try rewriting one of your AI workflows with `WorkRecord`, `VerifierDecision`, `NoActionState`, `ClosureDecision`, and `ReplayRecord`.

---

## Citation

```text
Zheng, Wes. From Agents to Institutions: A Field Study of Institutional Control in an AI-Staffed Prediction-Market Desk. Technical report, 2026.
```

For structured metadata, see [`CITATION.cff`](CITATION.cff).

---

## License

The public paper, documentation, and examples are released under the license in [`LICENSE`](LICENSE).

---

## The shortest possible summary

Agents produce actions.

Institutions make work accountable.

If we want AI to help humans with real work, we should build the institution around the agent as carefully as we build the agent itself.
