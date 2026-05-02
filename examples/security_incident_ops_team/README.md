# Synthetic Non-Trading Case: Security-Incident Ops Team

This example demonstrates organization-protocol semantics without using private operational records, trading details, or real incident-response instructions. It is not empirical evidence, not security advice, and not an incident-response benchmark.

## Scenario

A company receives a suspicious-account alert. The work is sensitive enough to require institutional control: an AI worker may gather evidence and prepare a packet, but containment, closure, and doctrine mutation require separate authority.

The goal is not to teach security operations tactics. The goal is to show how role families, lanes, messages, verifier gates, no-action, closure, replay, and mutation can make AI labor auditable.

## Role Families And Lanes

| Role family | Example seats | Owns | Does not own |
| --- | --- | --- | --- |
| Management | Incident Manager, Closure Manager | priority, routing, final closure, mutation authority | first-pass evidence collection |
| Triage | Alert Triage Analyst E1, Alert Triage Analyst E2 | alert classification and initial packet draft | containment approval or incident closure |
| Evidence | Evidence Collector, Packet Builder | source gathering, uncertainty notes, packet completeness | final action authorization |
| Verification | Incident Verifier, Containment Verifier | packet acceptance, repair requests, action authorization decision | execution outside the approved envelope |
| Response | Response Executor | bounded response only after authorization | changing doctrine or expanding scope |
| Replay/Doctrine | Replay Analyst, Doctrine Maintainer | outcome review and proposed doctrine patch | live incident execution |

The lanes form a corridor:

```text
manager directive
  -> triage lane
  -> evidence packet lane
  -> verifier lane
  -> response or no-action lane
  -> closure manager
  -> replay / doctrine lane
```

## 1. Broad Intent Becomes Workboard State

The Incident Manager opens a live umbrella:

- Work item: `SEC-001 suspicious-account alert`
- Objective: determine whether the alert justifies containment or monitor-only handling
- Current owner: Incident Manager
- Gate state: triage needed
- Closure rule: manager closure required
- Replay state: pending after outcome window

The live umbrella is compiled into child records:

| Child record | Owner family | Gate |
| --- | --- | --- |
| `SEC-001-A triage packet` | Triage | packet required |
| `SEC-001-B evidence completeness` | Evidence | verifier review required |
| `SEC-001-C containment authorization` | Verification | action gate required |
| `SEC-001-D closure and replay` | Management / Replay | final disposition required |

## 2. Direct Activation Messages

The manager sends focused activation messages instead of broad awareness copies.

```text
Sender: Incident Manager
Recipient: Alert Triage Analyst E1
Work item: SEC-001-A triage packet
Ask: produce an initial triage packet for verifier review
Next action: update the governing work record with evidence basis, uncertainty, and recommended gate state
Reply needed: no if the work record is updated
```

The message activates one bounded work obligation. It does not authorize containment.

## 3. Triage Packet

The triage family updates the governing work record with a packet-shaped artifact:

- alert summary;
- source list;
- evidence freshness;
- affected-scope estimate;
- uncertainty and contradictions;
- recommended next gate;
- no-action triggers;
- downstream owner.

The packet is a reviewable artifact, not an execution order.

## 4. Verifier Gate

The Incident Verifier reviews the packet and makes a state decision:

| Gate field | Decision |
| --- | --- |
| Artifact status | reconstructible |
| Evidence sufficiency | partial |
| Execution authorization | declined |
| Reason | evidence does not justify containment |
| Next owner | Evidence Collector |
| Next action | add missing source context or record monitor-only basis |

This separates two questions:

- Is the artifact reconstructible?
- Is downstream action authorized?

A packet can pass the first gate and fail the second.

## 5. No-Action State

The organization records a valid no-action state:

- Type: monitor-only
- Authority basis: verifier declined containment authorization
- Evidence basis: packet reconstructible but insufficient for action
- Next owner/action: Evidence Collector monitors the outcome window
- Replay requirement: yes

No-action is not inactivity. It is an audited state with authority, evidence, and follow-through.

## 6. Closure Decision

The Closure Manager closes the triage phase only after the governing record is truthful:

- triage packet attached;
- verifier state recorded;
- containment declined;
- monitor-only no-action state recorded;
- no downstream response message needed;
- replay child remains open.

Closure is separate from task completion.

## 7. Replay And Doctrine

After the outcome window, the Replay Analyst records one of two learning paths:

| Replay outcome | Learning destination |
| --- | --- |
| alert remains benign | case-only; no doctrine mutation |
| repeated similar alerts cause repair loops | propose a doctrine patch or role-boundary change |

If repeated evidence supports a reusable change, the Doctrine Maintainer proposes a targeted patch:

```text
Target: triage playbook
Old clause: escalate ambiguous alerts directly to containment review
New clause: route ambiguous alerts to evidence-completeness review before containment review
Authority: manager approval required
Activation: update playbook version and notify affected role families
```

This is a mutation proposal, not automatic self-improvement.

## What This Demonstrates

- Broad owner intent becomes live umbrella and child-path state.
- Role families preserve handoff contracts across multiple seats.
- Messages activate specific work obligations rather than awareness.
- Artifact reconstructibility and action authorization are separate gates.
- No-action can be an audited output.
- Closure requires accepting authority and truthful work state.
- Replay routes learning to case-only, doctrine, role boundary, or another durable layer.
