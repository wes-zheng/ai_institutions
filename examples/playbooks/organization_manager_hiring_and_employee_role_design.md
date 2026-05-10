# Organization Manager - Hiring And Employee Role Design

Public-safe redacted example. This file preserves the generic operational doctrine and section structure of the source playbook while replacing organization-specific names, private tool names, domain maps, staffing assignments, private issue references, and sensitive operational details with neutral terms.

## Purpose

Define the canonical standard for hiring, onboarding, termination, role rewrites, role-family normalization, staffing-map maintenance, and employee tool-access changes.

This playbook exists to make sure role text is a precise employee job contract, while playbooks remain reusable operating manuals for workflow and domain doctrine.

Good role design should make an employee know:

- who they are;
- what they own;
- what they do not own;
- which decisions they can make;
- which outputs they must leave;
- who they normally receive from and hand to;
- when they must escalate;
- which canonical playbooks govern the detailed workflow.

Good role design should not copy large workflow manuals into role text unless the duplication is required for authority, safety, trigger discipline, or interface clarity.

## Scope

Use this playbook for:

- hiring;
- onboarding;
- termination;
- role rewrites;
- role-family normalization;
- staffing rebalances;
- lane or corridor redesigns;
- pod or team-map redesigns;
- downstream interface redesigns;
- employee tool-access changes;
- audits of whether role text is stale or misaligned with canonical playbooks.

## Owner

Organization Manager.

## Authority

Only the Organization Manager, or an explicitly delegated administration role, may:

- hire employees;
- terminate employees;
- change employee role text;
- change employee tool access;
- create playbooks;
- update playbooks;
- retire playbooks;
- approve durable staffing-map changes.

## Trigger / When To Use

Use this playbook before:

- creating a new role;
- rewriting an existing role;
- changing an employee's scope or authority;
- changing a role-family standard;
- adding a new lane, pod, or corridor owner;
- changing the permanent lane map, corridor map, pod map, or staffing map;
- changing employee tools;
- reviewing whether role text has drifted from playbooks;
- promoting a repeated role-confusion failure into durable doctrine.

## Do Not Use When

Do not use this playbook as the governing source for:

- live work-record routing procedure, sprint structure, replay-record structure, or closeout sequencing;
- venue-specific or domain-specific operating doctrine;
- verifier-side or reviewer-side calculation, approval, or gate procedures;
- execution-side workflow procedure;
- domain packet schema, source-stack doctrine, or family-specific method;
- work-record-specific truth that belongs only on the governing work record.

This playbook owns staffing shape, role-family design, role-text standards, role-vs-playbook allocation, tool-parity and tool-write discipline, and the role-design implications of the current organization structure.

## Required Inputs

Before hiring or changing role text, identify:

- real staffing or role-design need;
- governing issue or persistent work record;
- current employee identifier and concise title from the roster tool when discovery is needed;
- current full employee role text from the profile tool if the employee already exists;
- current approved operating model from this playbook when staffing structure is affected;
- live employee roster discovery from the roster tool;
- full employee profile, role truth, and status from the profile tool;
- tool truth from the employee-tool administration surface when staffing or tool access is affected;
- affected role family;
- affected employee or employees;
- canonical playbooks governing the detailed workflow;
- whether the change affects authority, scope, outputs, interface, escalation, tools, staffing map, or all of those;
- current and desired lane, corridor, pod, or staffing map when relevant;
- current and desired tool access when relevant;
- affected downstream employees;
- notification plan.

## Required Outputs

Every substantive hiring or role-design cycle must produce all truthful outputs that apply:

- updated role text when role scope, authority, outputs, or boundaries changed;
- updated operating-model truth when team, lane, seat, or downstream interface design changed;
- exact lane, corridor, pod, or ownership truth when structure changed;
- exact before/after role-state record on the governing work record;
- exact role-vs-playbook allocation decision when reusable doctrine is being moved out of or into role text;
- exact tool-parity comparison when tool access changed;
- exact full intended tool-set write input when tool access changed;
- exact employee notification record;
- exact statement of whether the change alters a shared role-family standard or only one role;
- exact exception record when a role exceeds normal capacity or another structural exception is approved.

Do not leave role ownership, staffing shape, tool-access truth, or notification truth implied.

## Core Doctrine

### 1. Role Text Is The Job Contract

Role text should tell the employee what job they personally hold in the organization.

Role text owns:

- employee-specific mandate;
- assigned scope, lane, corridor, pod, or work surface;
- owned decisions;
- decisions the employee does not own;
- authority boundaries;
- required role outputs;
- normal upstream and downstream collaborators;
- role-specific handoff and escalation triggers;
- role-specific non-goals;
- role-specific safety rails that must be reinforced at the instruction layer.

Role text should be explicit enough that an employee can orient quickly before reading playbooks.

Role text should not become the full operating manual for the reusable workflow.

### 2. Playbooks Are The Reusable Operating Manuals

Playbooks own reusable workflow and domain doctrine.

Playbooks own:

- exact workflow steps;
- artifact schemas;
- required inputs and outputs for recurring work;
- source-stack truth;
- settlement, evidence, or tool mechanics when relevant;
- decision criteria;
- formulas and calculation procedures when relevant;
- implementation methods;
- verifier or reviewer gates;
- execution workflows;
- replay and retro standards;
- repeated failure modes that apply across employees.

If a rule answers "how should this reusable workflow be done?", it belongs in a playbook.

If a rule answers "who owns this decision or boundary?", it belongs in role text.

### 3. Governing Work Records Hold Case-Specific Truth

Governing work records hold only case-specific truth, including:

- work-record-specific evidence;
- latest state;
- exact lane or item;
- blocker;
- next owner;
- next action;
- live decision;
- replay result;
- case-specific exception.

Do not use role text or playbooks to hold one-case facts.

### 4. Role-Text Duplication Rule

Avoid duplicating playbook doctrine in role text unless the duplication is intentional and necessary.

Duplication in role text is allowed when it is needed for one of these reasons:

- authority enforcement;
- trigger discipline;
- irreversible safety boundary;
- high-frequency repeated failure prevention;
- role-family interface clarity;
- assigned scope or named default counterpart;
- manager-only administration boundary.

Duplication in role text is not allowed when it merely copies:

- long artifact schemas;
- source-stack steps;
- domain mechanics;
- implementation details;
- code examples;
- formulas;
- execution procedures;
- replay workflows;
- closeout procedure;
- long failure-mode lists already owned by a canonical playbook.

If role text repeats a playbook rule, keep the role version short and boundary-focused, and name the canonical playbook that owns the detailed procedure.

### 5. Higher-Priority Role-Text Caution

Role text sits above playbooks in the employee instruction stack.

Because of that priority, stale workflow doctrine inside role text can accidentally override newer playbook doctrine.

When rewriting roles:

- keep role text focused on authority, scope, owned outputs, interfaces, and escalation;
- move reusable procedure into the canonical playbook when the playbook is the better home;
- preserve critical boundary reminders only when they are needed for safe execution;
- remove or compress copied workflow detail once the canonical playbook covers it at equal-or-better explicitness.

### 6. Role Text Incompleteness Rule

A role text is incomplete if it does not clearly state:

- who the employee is;
- assigned scope;
- what the employee owns;
- what the employee does not own;
- exact owned decisions;
- required outputs;
- normal collaborator boundaries;
- manager escalation triggers;
- peer messaging triggers;
- which canonical playbooks govern the detailed workflow;
- role-specific failure modes the employee must avoid.

A role text is also incomplete if it contains stale workflow doctrine that conflicts with newer canonical playbooks.

Do not treat a role rewrite as complete while the role text can override, obscure, or duplicate the canonical workflow stack in a way that creates drift.

## Role-Text Structure Standard

Every active role should normally use this shape:

1. Identity and assignment
2. Assigned scope / lane / corridor / pod / work surface
3. You own
4. You do not own
5. Canonical playbooks for detailed workflow
6. Role-specific operating boundaries
7. Normal downstream chain and collaborators
8. Required outputs
9. Messaging and escalation rules
10. Success criteria
11. Failure modes to prevent

Do not force a section if it does not apply, but omissions should be intentional.

### Role Text Skeleton

Use this skeleton when creating a new role or doing a major rewrite:

```markdown
You are <Name>, the <Role Label> at <Organization>.

Assigned scope:
- <scope / lane / corridor / pod / desk surface>

You own:
- <owned decisions and outputs>

You do not own:
- <explicit non-goals and authority boundaries>

Canonical playbooks for detailed workflow:
- <Playbook 1>
- <Playbook 2>

Role-specific operating boundaries:
- <short safety / authority / interface rules only>

Normal downstream chain:
- <upstream owner> -> <this role> -> <downstream owner>

Required outputs:
- <role-owned outputs only>

Messaging and escalation rules:
- <when to message manager>
- <when to message peers>
- <when result stays on-record only>

Success looks like:
- <role-specific success outcomes>

Failure modes to prevent:
- <role-specific failures not already covered better by playbooks>
```

Do not fill the skeleton with copied playbook prose. Use it to write the role's job contract.

## Operating-Model And Role-Template Source Of Truth

This playbook owns the stable operating model, seat map, pod map, downstream interface design, role-family design standards, and role-template blueprints for the example organization.

This playbook does not own live employee roster truth. Use the roster tool for current employee names, identifiers, titles, and active roster visibility. Use the profile tool for full employee profile, role text, and status. Use the tool-access surface for tool-set truth.

### Current Approved Operating Model

The current approved operating model should state:

- number of pods, lanes, or teams;
- number of seats per role family;
- normal capacity per seat;
- one explicit linear downstream chain per lane or pod;
- exception-only overflow or failover;
- full-path reroute rather than split-path handling by default.

### Pod / Lane Map

The live map should use neutral structural labels rather than private staffing details.

Example shape:

- **Pod A:** domain lane A1 and domain lane A2
- **Pod B:** domain lane B1 and domain lane B2
- **Pod C:** domain lane C1 and domain lane C2

Replace the placeholders with public-safe labels only when the map itself is safe to publish.

### Specialist Seat Map

For each specialist family, the map should state:

- which pod or lane the specialist serves;
- which upstream roles hand work to the specialist;
- which downstream role normally receives the specialist's output;
- whether overflow or failover is permitted;
- who approves exceptions.

Do not publish private employee names, private employee identifiers, or sensitive assignment maps in example playbooks.

### Default Downstream Chain

Use a stable default chain:

```text
domain owner -> verifier / reviewer -> executor or implementation owner -> manager review / replay
```

### Role-Template Authority

The role text skeleton and role-family design standards in this playbook are the canonical blueprints for hiring, backfill, expansion, seat activation, and role-family normalization.

When creating or rewriting role text, start from the relevant role-family design standard below, then apply:

- employee name and title;
- seat-specific scope label;
- default pod or lane;
- assigned downstream interfaces;
- canonical detailed workflow playbooks;
- manager-approved seat-specific differences.

Do not copy live employee names, employee identifiers, titles, or active roster tables into this playbook. Those belong in roster, profile, and tool-access surfaces.

### Operating-Model Activation Rule

A staffing, seat, pod, lane, or downstream-interface change is production-ready only after:

- roster discovery exposes the correct live name, employee identifier, title, and active status;
- profile read exposes the correct full role text and status;
- tool-access read exposes the correct tool set when tool access matters;
- this playbook is refreshed if the approved operating model, seat map, pod map, downstream interface design, or role-family template changed;
- affected employees are notified with the governing work record and exact change;
- sprint-opening, grouped-work, and manager-routing surfaces no longer point to superseded staffing truth.

Do not keep a second future-state organization map in this playbook. If a redesign is being considered but is not yet activated, keep that planning on the governing manager work record until the current approved operating model actually changes.

### Steady-State Capacity Rule

Each role seat should have an explicit normal capacity rule unless the manager records a specific exception.

If one role exceeds the normal capacity, the exception must be recorded in the governing work record and reflected in role text or the operating model when durable.

## Role-Family Design Standards

The following public-safe role families are generic placeholders. Replace them with domain-specific names only when the names and responsibilities are safe to publish.

### 1. Domain Owners

Domain-owner role text must explicitly include:

- exact lane, work surface, or domain scope;
- exact default pod or team;
- ownership of domain artifact quality, evidence mapping, source freshness judgment, decision-ready framing, and source-stack recordkeeping;
- non-ownership of final approval, execution handling, manager closure authority, playbook editing, and overflow authorization outside recorded exceptions;
- normal handoff to the assigned verifier or reviewer;
- no direct happy-path message to execution or the manager when verification is the truthful next step;
- boundary that domain owners own artifact substance and decision structure but do not own final authorization or execution state;
- pre-review structure screen: if the selected structure does not survive the governing domain-owner screen, the path should usually not be sent to review unless a named exception is recorded;
- source freshness as a direct confidence input;
- requirement to use canonical domain playbooks for artifact schema, family-specific method, tool mechanics, and required calculation detail;
- success measured by artifact quality, conversion to real decisions, and honest explicit zero or no-send when warranted.

Domain-owner role text should not copy the full source stack, forced artifact schema, implementation procedure, scenario-tree requirements, or code examples. Those belong in canonical domain playbooks.

When one domain-owner role is upgraded for clarity, normalize the full active domain-owner family unless real scope differences require divergence.

### 2. Research Leads

Research Lead role text must explicitly include:

- mandate to improve method quality, calibration, and uncertainty handling for live decisions;
- public-data-first or source-first research expectation where relevant;
- ownership of method research, validation design, benchmark comparison, calibration evidence, error diagnosis, and method-graduation pressure;
- mandatory rerun pressure after research lands;
- promote / hold / drop decision responsibility;
- explicit live-impact and quality-improvement statement requirement;
- no ownership of production artifacts, final approval, execution handling, manager closure authority, playbook editing, or routing overrides outside manager-recorded exceptions;
- requirement to use the relevant method-graduation playbook for detailed workflow;
- requirement to route durable doctrine changes to the Organization Manager rather than editing playbooks directly unless authority is explicitly delegated.

Research Lead role text should not copy full implementation details, validation tables, or code examples. Those belong in method-graduation and domain playbooks.

### 3. Verification / Review Leads

Verification or Review Lead role text must explicitly include:

- assigned pod, lane, or default upstream sources;
- ownership of approve / decline / repair / reroute decisions;
- ownership of artifact-gate enforcement, reviewed judgment, approved structure selection, approved target-state construction when applicable, and authorization-boundary truth;
- non-ownership of upstream domain analysis, upstream artifact rewrite, execution handling after approval, manager closure authority, playbook editing, and free-form cross-pod balancing;
- rule that domain owners do not own final size, cap, target state, or execution authorization when those are verifier-owned in the organization;
- rule that the executor works from the verifier's approved target state and authorization boundary only;
- repair reroute to the relevant domain owner when the artifact gate fails;
- normal downstream handoff to the assigned execution or implementation owner when approval is ready;
- exception-only full-path overflow or failover boundary;
- requirement to use the verification standard for formulas, gates, target-state construction, and review-detail procedures.

Verification Lead role text should not copy the full formula stack or full artifact schema. It may keep short gate reminders when needed for authority enforcement, but the detailed checklist belongs in the relevant verification and domain playbooks.

### 4. Execution / Implementation Leads

Execution or Implementation Lead role text must explicitly include:

- assigned pod, lane, or default upstream sources;
- ownership of execution readiness after approval, target-state alignment, bounded implementation, implementation truth, immediate post-action routing, post-action truth on replay records, and truthful handling for the assigned path;
- non-ownership of upstream domain analysis, artifact rewrite, final approval, manager closure authority, playbook editing, and free-form cross-pod balancing;
- rule that the governing execution envelope comes from the assigned verifier or reviewer;
- rule that execution-side validation is limited to the cited same-source classes and freshness triggers authorized by the governing record;
- normal manager-review handoff after execution-stage work is done;
- replay-record responsibility after any real action;
- prohibition on separate control records as the canonical workflow when replay records are the canonical post-action surface;
- requirement to use the execution standard for detailed execution workflow.

Execution Lead role text should not copy the full action-working procedure or replay workflow when canonical playbooks already cover it at equal-or-better explicitness.

### 5. Organization Manager

The Organization Manager's role text must explicitly include:

- manager-only authority for hiring, termination, role changes, employee tool access, playbook changes, and closure unless explicitly delegated;
- ownership of board truth, manager verification, closure, staffing, role-text truth, playbook maintenance, sprint or work-target truth, structure truth, stalled-work recovery, assignment activation, canonical operating-model truth, overflow or failover authorization, live downstream truth, and role-boundary truth;
- explicit assignment activation by direct message;
- ownership and maintenance of this playbook as the canonical operating-model, seat-map, pod-map, downstream-interface, and role-template source;
- overflow or failover authorization;
- explicit current staffing-state discipline;
- paired live-work and retro or replay surfaces when the workflow requires both;
- manager-created child work records when broad intent must be compiled into owned work;
- strict one activation message for one created child record rule;
- role-text maintenance rule: role text changes should follow this playbook and keep reusable workflow doctrine in canonical playbooks.

The manager role text may contain more structural staffing truth than other roles, but this playbook should own the canonical operating model, seat map, pod map, downstream interface design, and role-template blueprints. Live named roster truth should be discovered through roster/profile/tool surfaces, not duplicated across manager surfaces.

## Style-Diversity Rule

Role texts should share explicitness, boundary clarity, and operating quality without collapsing into one generic copy-paste voice.

That means:

- keep the same structural explicitness across a role family;
- keep interface terminology stable where the interface is shared;
- keep shared authority boundaries stable;
- allow real differences in emphasis, examples, workflow nuance, and failure modes when jobs are genuinely different;
- do not flatten specialist roles into generic domain-owner language when the role is substantively different.

Style diversity is acceptable only when ownership, outputs, interfaces, escalation rules, and canonical playbook references remain equally explicit.

## Employee Tool Usage Rule

Use the organization administration tools according to their current contract:

- use the roster-listing tool for roster discovery, employee identifiers, names, and concise titles only; do not treat it as a full role-text source;
- use the profile-read tool when the manager needs the full employee profile, full role text, current title, or status;
- use the tool-read surface when the manager needs current tool access;
- use the hire action with both the concise title and full role text when creating a new employee;
- use the title-change action for title-only corrections;
- use the role-edit action for role-text changes by replacing a precise matching old string with a new string; do not treat it as a blind full replacement unless the old string is the verified full current role text;
- use the tool-replacement action for full tool-set replacement;
- use the inbox-read surface when inbox state or employee response truth matters;
- use the direct-message action for direct employee notifications;
- use the terminate action only when the governing staffing decision is a real termination.

Because roster-listing output is title-level roster output, any role audit, role rewrite, or role-family normalization must read each affected employee profile before changing role text. Any tool-parity check must read each affected employee's tool set before changing tools.

## Tool-Access Parity And Write Rule

When hiring into an existing live role family or adding another pod lead:

1. compare the new hire's tool access against the comparable already-live role in the same family;
2. do not leave the new hire in a structurally weaker operating state without a deliberate recorded reason;
3. record the exact before/after tool-access comparison on the governing work record.

Manager write method for tool updates:

- read the target employee's current tool-access list;
- when using full tool replacement, pass the employee identifier and the full intended final tool list in the same write;
- treat tool replacement as a full replacement, not a partial patch;
- when restoring parity, the safest method is usually to start from the comparable live role's tool list and write the full intended final list;
- do not omit tools you intend to preserve, because the write should reflect the entire target tool set.

## Activation / Notification Rule

A role-change or staffing action is not complete until:

1. the role text is updated;
2. the related governing work record records the new state;
3. affected employees are notified directly with the governing work record and exact change;
4. this playbook is updated if the permanent operating model, seat map, pod map, downstream interface design, or role-family template changed.

## Exact Workflow

When handling a hire, termination, staffing rebalance, role rewrite, role-family refresh, or tool-access change, follow this order:

1. Identify the real staffing or role-design need and the governing work record.
2. Determine whether the change affects one role, one role family, one lane map, one pod map, one tool set, or the full organization shape.
3. Read the current full role text, title, and status for each affected existing employee; read tool sets when tool access matters; then read the canonical playbooks that govern the detailed workflow for that role.
4. Classify each piece of proposed role content as role-specific, reusable workflow, or case-specific truth.
5. Keep role-specific authority, ownership, scope, required outputs, interfaces, and escalation in the role text.
6. Move or point reusable workflow doctrine to the canonical playbook instead of copying it into role text, unless a duplication exception is required by the role-text duplication rule.
7. Preserve safety-critical role reminders that prevent authority or trigger mistakes.
8. Remove or compress stale copied workflow details when the canonical playbook already owns the detail at equal-or-better explicitness.
9. If the role belongs to an active role family, normalize the relevant family standard unless a real scope difference justifies divergence.
10. If tool access changes, run the parity comparison, construct the full intended final tool-set input, and record the before/after comparison on the governing work record.
11. Update this playbook when the permanent operating model, seat map, pod map, downstream interface design, or role-family template changed.
12. Notify affected employees directly with the governing work record and exact change.
13. Verify that roster truth, profile truth, tool truth, role text, operating-model truth, canonical playbooks, and notification truth all match before calling the action complete.

Do not treat a staffing or role-text change as complete while role text, playbook truth, tool truth, or staffing truth still disagree.

## Role-Text Review Checklist

Before publishing a role rewrite, verify:

- the role states exact identity and assigned scope;
- owned decisions are explicit;
- non-owned decisions are explicit;
- authority boundaries are explicit;
- normal downstream chain is explicit;
- peer and manager messaging triggers are explicit;
- required outputs are explicit;
- role-specific escalation triggers are explicit;
- canonical playbooks for detailed workflow are named;
- duplicated playbook doctrine is limited to intentional authority, safety, trigger, or interface reinforcement;
- copied formulas, schemas, methods, and long workflows have been removed or replaced by canonical playbook references;
- the role does not conflict with newer canonical playbooks;
- related roles in the same family remain aligned unless a real scope difference is recorded;
- employee tools are still sufficient for the role.

## Definition Of Done

Done means:

1. every active role meets the role-text structure standard;
2. every active lane, surface, or queue has a named owner when ownership is required;
3. no role seat exceeds its normal capacity without an explicit exception;
4. lane-to-pod or work-surface truth is explicit where structurally relevant;
5. specialist roles have explicit owned decisions, outputs, and messaging boundaries;
6. downstream role families use role / pod interfaces rather than stale single-person structural routing;
7. the normal happy-path chain is explicit and linear through the assigned downstream role sequence;
8. role text names canonical playbooks for detailed workflow when needed;
9. reusable workflow doctrine stays in playbooks rather than being copied into role text without a valid duplication reason;
10. roster truth, profile truth, tool truth, operating-model truth, and role text match;
11. tool-access changes preserve parity or record the deliberate exception explicitly;
12. employee notifications are complete;
13. shared live workflow procedure stays in the workflow playbook while this playbook keeps staffing and role-design doctrine.

## Failure Modes / Escalation

Escalate or reject the role-design change if any of these occur:

- a role omits owned decisions, required outputs, authority boundaries, or message boundaries;
- a role omits canonical playbooks needed for detailed workflow;
- a role copies full workflow doctrine that belongs in playbooks;
- a role hard-codes formulas, artifact schemas, source-stack doctrine, implementation details, code examples, replay procedure, closeout procedure, or execution workflows already owned by canonical playbooks;
- a role contains stale copied workflow doctrine that conflicts with newer playbooks;
- a domain-owner role omits default pod, freshness, normalized decision-structure ownership, current-context boundary, approve-ready handoff doctrine, explicit no-size / no-cap / no-target-state boundary, pre-review screen, linear next-owner routing, or exception-only overflow/failover doctrine;
- a Research Lead role omits quality improvement, calibration, live impact, validation, benchmark, rerun, or promote / hold / drop requirements;
- a Verification Lead role omits artifact-gate authority, approved target-state ownership, approved delta truth, authorization-boundary truth, or no-upstream-domain-analysis boundary;
- an Execution Lead role omits approved target-state boundary, authorization-boundary truth, packet-defined freshness boundary, execution-time blocker boundary, replay-record responsibility, or no-upstream-domain-analysis boundary;
- the Organization Manager role omits ownership of this playbook's operating-model / role-template source of truth, current staffing and structure truth, overflow/failover authorization, role-boundary truth, strict one-message-per-child-record activation, or role-text maintenance doctrine;
- a hiring or staffing update relies on roster listing as if it contained full role text instead of reading the full employee profile and role truth;
- a hiring or staffing update changes tool truth without recording the full intended final tool set, parity check, or governing work-record result;
- role text, roster truth, profile truth, tool truth, and this playbook's operating-model truth disagree;
- this playbook drifts back into owning live workflow procedure that has a clearer canonical home in the workflow playbook.
