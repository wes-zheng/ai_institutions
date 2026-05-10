# Organization Manager - Playbook Writing And Maintenance Standard

Public-safe redacted example. This file preserves the generic operational doctrine and section structure of the source playbook while replacing organization-specific names, private tool names, private issue-tracker references, and domain-specific operating details with neutral terms.

## Purpose

Define the canonical standard for writing, updating, reorganizing, splitting, merging, mirroring, and maintaining playbooks so the playbook stack stays explicit, reusable, auditable, and operationally useful.

This standard exists to make sure playbooks:

- preserve prior learning;
- remain at least as explicit as the doctrine they replace;
- keep reusable workflow doctrine separate from role authority and work-record-specific truth;
- interact correctly with employee role text;
- stay easy to find, read, maintain, and extend;
- do not silently lose live operational detail during cleanup, restructuring, or style passes.

## Scope

Use this playbook for any work that:

- creates a new playbook;
- rewrites an existing playbook;
- renames a playbook;
- merges or splits playbooks;
- reorganizes sections across playbooks;
- creates or refreshes mirror documents for playbooks;
- changes the boundary between overview and specialized playbooks;
- changes the boundary between playbooks, roles, and work records;
- changes whether reusable doctrine belongs in a playbook or employee role text;
- promotes repeated work-record learning into durable doctrine.

This standard governs the playbook system itself. It applies before changing narrower domain playbooks.

## Owner

Organization Manager.

## Trigger / When To Use

Use this playbook when:

- a new reusable workflow or doctrine needs a durable home;
- a current playbook is too vague, too duplicated, too stale, or too hard to use;
- a playbook title or internal structure is being changed;
- a playbook is being split into overview plus specialized documents;
- mirror documents need refresh;
- repeated work-record corrections now deserve promotion into doctrine;
- a role-text audit reveals reusable workflow doctrine trapped in role text;
- a playbook rewrite changes what downstream role text should say;
- a governing work record requires explicit documentation of where doctrine now lives.

Use this playbook before publishing structural playbook changes.

## Do Not Use When

Do not use this playbook as the governing source for:

- role authority;
- employee-specific operating behavior;
- work-record-specific truth;
- temporary one-off exceptions;
- transient item-specific notes that do not yet justify reusable doctrine.

Those belong in:

- roles for authority and role-specific behavior;
- work records for item-specific truth and evidence;
- governing comments or change records for rollout-specific state and validation.

## Canonical Source Rule

The canonical operating instructions live in **Organization Manager - Playbook Writing and Maintenance Standard**.

The playbook system is canonical. Mirror documents are mirrors.

If a mirror exists, it should reflect canonical playbook truth rather than becoming a competing source of doctrine.

## Core Stack-Layer Rule

The stack remains layered:

- playbooks for reusable workflow doctrine;
- roles for authority and role-specific behavior;
- work records for item-specific truth.

Do not collapse these layers together.

Do not put reusable workflow doctrine only on work records when it should live in a playbook.

Do not put role authority or approval ownership into a playbook when it should live in a role.

Do not move work-record-specific truth into a playbook just to make a playbook feel more complete.

Role text is the employee job contract.

Playbooks are reusable operating manuals.

Governing work records are case-specific truth.

## Current High-Signal Canonical Rules

The following rules remain governing and must be preserved:

- Titles are **audience first**: use the role or audience before the dash and the subject after the dash.
- Use **stable role labels, not employee names**, in playbook titles; role labels should normally stay concise.
- Do **not** make the internal H1 depend on the exact playbook title; use a stable content heading instead.
- Mirror titles should match canonical playbook titles exactly unless there is a strong reason not to.
- Refresh mirror headers and first-line canonical-source references when needed so active mirrors do not preserve superseded names.
- During reorganization, merge, or split work, **preserve already-explicit documented learning** unless the content is duplicate or wrong.
- When content moves, record the destination playbook or section on the governing work record so the stack stays auditable.
- Do **not** silently drop still-correct operational tool details; preserve tool-interface facts, parameter requirements, and full-write behavior unless they are verified wrong or obsolete.
- Preserve current administration-tool facts when manager playbooks mention staffing or role maintenance.
- If a still-live operational detail is being moved to a narrower playbook, record the destination explicitly on the governing work record.
- The stack remains layered: playbooks for reusable workflow doctrine, roles for authority and role-specific behavior, work records for item-specific truth.
- Role text should not become the hidden source of reusable workflow doctrine.
- Playbook rewrites that change employee-facing expectations must identify whether downstream role text needs a refresh.
- Use targeted edit only when the current playbook remains materially the same canonical object and the change is local.
- When the majority of a playbook needs rewriting, prefer author-new-plus-retire-old because that path is usually cleaner, faster, and easier to audit.
- Do not keep live staffing rosters inside ordinary workflow playbooks.
- When staffing or role truth is needed, use the organization’s roster/profile/tool administration surfaces rather than copying live roster truth into workflow doctrine.

## No-Loss Doctrine-Update Rule

Any playbook rewrite, cleanup, merge, split, relocation, dedupe pass, style pass, or mirror refresh must follow the no-loss rule.

The no-loss rule means:

- do not lose still-correct doctrine;
- do not lose still-correct operational detail;
- do not lose explicit learned constraints;
- do not lose tool-interface facts, parameter requirements, or full-write behavior;
- do not lose the ability to reconstruct where doctrine moved;
- do not give up live guidance quality for cleaner structure;
- do not lose role-authority clarity when reusable procedure moves into or out of playbooks.

A doctrine update is not successful if the new version is shorter, cleaner, or more elegant but causes a worker to lose usable operating truth.

If content is removed, one of these must be true:

- it is duplicate;
- it is stale;
- it is wrong;
- it belongs in another layer;
- it has been moved to a clearly named destination.

If none of those are true, preserve it.

## Equal-Or-Better Explicitness Rule

Any rewrite, reorganization, merge, split, or style pass must satisfy the equal-or-better explicitness rule.

The equal-or-better explicitness rule means:

- the rewritten playbook must be at least as explicit as the prior governing version;
- any compressed wording must preserve or improve operational clarity;
- any moved doctrine must remain equally discoverable and equally actionable in its new home;
- any role-text impact must preserve or improve authority, ownership, and escalation clarity.

Do not replace explicit instructions with higher-level summaries unless the replacement is clearly equal or better for actual worker execution.

`Cleaner` is not enough.

`More concise` is not enough.

`Less repetitive` is not enough.

The real test is:

- can a worker still do the job at least as correctly as before;
- with at least the same clarity;
- without needing to reconstruct missing steps from memory, work records, chat, prior versions, or stale role text?

If not, the rewrite fails.

## Maintenance-Path Choice Rule

When maintaining a playbook, choose between two default maintenance paths:

- targeted edit;
- author new plus retire old.

### Targeted-Edit Rule

Use targeted edit only when all are true:

- the current playbook remains the same canonical object;
- the title, audience, and core purpose remain materially the same;
- most of the current content still survives;
- the needed change is local or limited to a small number of sections;
- the rewrite can be completed cleanly without a long chain of scattered replacements.

Targeted edit is the preferred path for local repairs, small doctrine additions, title patches, section-level corrections, mirror-reference refreshes, and other bounded updates.

### Author-New-Plus-Retire-Old Rule

Prefer author new plus retire old when the majority or most of the current playbook content needs rewrite.

Use that path when one or more of these are true:

- most sections are going to be rewritten anyway;
- the current section structure is no longer the right shape;
- the rewrite would require many scattered edits across the body;
- the new version will be cleaner and easier to verify as a fresh canonical playbook;
- patching the old document in place would be slower, noisier, or harder to audit than replacing it.

This path is preferred for majority rewrites because it is usually cleaner, faster, and easier to verify than repeatedly editing a document that is about to be mostly replaced.

If using author new plus retire old:

- preserve all still-correct doctrine in the new playbook;
- keep the new canonical title and canonical home explicit;
- record the migration on the governing work record;
- refresh mirrors and references;
- retire the old playbook only after the new canonical version is verified.

## Playbook-Writing Standard

### 1. Write For Operational Use, Not Documentation Aesthetics

A playbook must help someone do real work correctly.

A playbook is not successful because it is short, elegant, or abstract. It is successful when a worker can:

- identify whether it applies;
- follow the workflow;
- produce the required output;
- avoid known failure modes;
- escalate correctly when the playbook does not apply.

Do not compress away operationally useful detail in pursuit of cleanliness.

### 2. Be Explicit Before Being Concise

Prefer:

- explicit conditions;
- explicit triggers;
- explicit required outputs;
- explicit pass/fail gates;
- explicit escalation rules;
- explicit ownership boundaries;
- explicit reroute conditions;
- explicit moved-content destinations.

Do not rely on implication where a concrete rule is possible.

Do not use loose wording when the work depends on exact interpretation.

### 3. Use Positive Instructions, Not Only Prohibitions

A good playbook should tell the worker:

- what this playbook is for;
- when to use it;
- what to do in order;
- what output is required;
- what makes the work complete;
- when to stop, reroute, or escalate.

Failure modes and `do not` rules are required, but they must support a clear positive workflow rather than substitute for one.

### 4. Require Trigger -> Action Clarity

For any rule that depends on a condition, write it in a way that makes the trigger and the required response explicit.

Preferred pattern:

- `If X is true, do Y.`
- `If X is missing, fail and route to Z.`
- `When refresh condition A occurs, rerun sections B and C.`
- `If content moves, record the destination on the governing work record.`
- `If a playbook rewrite changes role-text expectations, record whether the role text must be updated.`

Avoid vague wording like:

- `be mindful of`;
- `consider whether`;
- `keep in mind`;
- `use judgment`;

unless the exact judgment boundary is also made explicit.

### 5. Keep Terminology Stable

Use one stable name for:

- the audience;
- the workflow object;
- the section name;
- the decision type;
- the gate;
- the failure class;
- the migration action;
- the downstream artifact.

Do not alternate between multiple names for the same thing unless the distinction is intentional and explained.

If a term changes, update all still-live mirrors and references.

### 6. Use Stable Section Structures

Every operational playbook should normally include most of these sections when relevant:

- `Purpose`;
- `Scope`;
- `Owner`;
- `Trigger / when to use`;
- `Do not use when`;
- `Required inputs`;
- `Core doctrine`;
- `Exact workflow`;
- `Required outputs`;
- `Definition of done`;
- `Failure modes / escalation`;
- `Update history`.

Not every playbook needs every section, but omissions should be intentional.

Do not use loose narrative structure when the worker needs a predictable operating shape.

## Procedure-Over-Principle Rule

When the organization already knows how a recurring workflow should be performed, the playbook must prefer procedure over principle.

Principles are useful when they clarify intent.

Procedures are required when workers need to execute repeatedly and correctly.

Do not stop at abstract statements like:

- `be explicit`;
- `preserve auditability`;
- `use good judgment`;
- `keep the stack layered`;
- `maintain clarity`;

when the actual operating procedure is known.

A good playbook should convert principle into procedure whenever all are true:

- the task recurs;
- the workflow is known;
- failure modes are known;
- the worker would benefit from explicit step order, pass/fail gates, or required outputs.

Use principle to explain why.

Use procedure to explain how.

If a worker would have to improvise the steps, the playbook is incomplete.

## Doctrine-Promotion Rule

When a rule, pattern, workaround, boundary, work-record-learned constraint, or repeated correction becomes stable and reusable, promote it into doctrine.

Do not leave reusable operating truth buried only in:

- work-record comments;
- one-off repair notes;
- manager messages;
- repeated verbal correction;
- employee memory;
- role text that only one employee sees;
- historical examples.

Promote a rule from local learning into playbook doctrine when one or more of these is true:

- the same failure happened more than once;
- the same correction had to be repeated across work records;
- the same workflow step keeps being re-explained;
- the same ambiguity keeps creating worker error;
- the organization now has a settled preferred method.

Doctrine promotion must turn repeated learning into one of:

- an explicit workflow step;
- an explicit required field;
- an explicit gate;
- an explicit definition-of-done item;
- an explicit failure mode;
- an explicit escalation trigger.

Do not promote raw noise.

Do not promote one-off work-record trivia.

Promote stable reusable truth.

## Procedure-Writing Rule

When promoting doctrine, write it in executable form.

Prefer:

- trigger -> action rules;
- numbered workflows;
- required input lists;
- required output lists;
- pass/fail gate language;
- exact reroute conditions;
- explicit escalation rules.

Avoid promoting a lesson only as a principle when the organization already knows the exact operational response.

Weak:

- `be careful not to lose doctrine during cleanup`

Strong:

- `during reorganization, merge, or split work, preserve already-explicit documented learning unless the content is duplicate, stale, wrong, or moved to a named destination recorded on the governing work record`

## High-Performance Playbook Structure Rule

A strong playbook should behave like a reliable operating tool.

That means the core playbook should:

- stay focused on one reusable job;
- provide clear entry conditions;
- provide a clear workflow;
- provide explicit expected outputs;
- separate rules from examples;
- stay small enough to remain readable and maintainable.

### Focus Rule

Each playbook should own one coherent reusable operating problem.

Do not let one playbook become:

- an overview;
- a role document;
- a worked-example bank;
- a work-record log;
- a troubleshooting notebook;

all at the same time.

If a playbook is trying to do too many of those jobs, split it.

### Progressive-Disclosure Rule

The core playbook should contain the governing workflow and decision rules.

Move long supporting material into narrower or linked references when appropriate, including:

- long worked examples;
- large reference tables;
- historical case lists;
- edge-case catalogs;
- detailed tool examples;
- long families of exceptions.

Do not remove useful doctrine. Move supporting detail into a more appropriate home when the core playbook is becoming bloated.

When content is moved:

- preserve the detail;
- name the new destination explicitly;
- record the move on the governing work record.

### One-Level Reference Rule

A playbook should point directly to the next useful reference, not force deep reference-chasing.

Prefer:

- one core playbook;
- one narrower playbook;
- one explicit example document;
- one governing work record.

Avoid chains where the reader must hop through many documents to reconstruct the real rule.

## Naming And Title Standard

### Title Rule

Playbook titles must be audience first:

- `<Audience> - <Subject>`

Examples:

- `Incident Manager - Closure Standard`
- `Research Lead - Method Graduation`
- `Organization Manager - Playbook Writing and Maintenance Standard`

### Stable-Role-Label Rule

Use stable role labels, not employee names, in titles.

Use employee names only when:

- the document is truly person-specific;
- the person-specific ownership is itself part of the doctrine;
- a stable role label would be misleading.

### H1 Rule

Do not make the internal H1 depend on the exact playbook title.

The H1 should be a stable content heading that can survive a title rename without forcing content churn.

### Mirror-Title Rule

Mirror titles should match canonical playbook titles exactly unless there is a very strong reason not to.

If a canonical title changes:

- update the mirror title;
- update the mirror header;
- update the first-line canonical-source reference.

Do not leave superseded names live in active mirrors.

## Required Inputs

Before writing, rewriting, splitting, merging, or moving a playbook, identify:

- the exact reusable operating problem;
- the correct audience;
- the correct stack layer;
- the current canonical source;
- all still-live explicit doctrine in the current version;
- the related role and work-record boundaries;
- any role text that currently duplicates, depends on, or may conflict with the playbook doctrine;
- any mirror documents;
- any governing work records that must preserve the migration record.

## Required Writing Workflow For Playbook Creation Or Rewrite

When writing or rewriting a playbook, do the following in order:

1. Identify the exact reusable operating problem the playbook should solve.
2. Identify the correct stack layer: playbook, role, or work record.
3. Identify whether the content is shared doctrine, family-specific implementation, role authority, item-specific truth, historical example, or rollout evidence.
4. Identify the current canonical source and all still-live mirrors.
5. Identify any role text that currently duplicates, depends on, or may conflict with the playbook doctrine.
6. Preserve all still-correct existing explicit doctrine.
7. Choose the maintenance path explicitly: use targeted edit when the current playbook remains materially the same and the needed change is local; prefer author-new-plus-retire-old when the majority or most of the playbook content needs rewrite.
8. Mark content as removable only if it is duplicate, stale, wrong, in the wrong layer, or being moved to a named destination.
9. Rewrite the core workflow so it is explicit and operational.
10. State the required outputs and definition of done.
11. State the failure modes and escalation triggers.
12. If detail is too long for the core playbook, move it to a narrower or reference document rather than silently deleting it.
13. If reusable workflow doctrine is removed from role text or moved into a playbook, preserve the role's authority and safety boundaries explicitly in the correct role-design surface.
14. Record all moved doctrine on the governing work record with exact destination references.
15. Record whether downstream role text needs no change, refresh, or immediate update.
16. Verify the rewritten version satisfies the no-loss doctrine-update rule.
17. Verify the rewritten version satisfies the equal-or-better explicitness rule.

## Shared-Vs-Specialized Allocation Rule

When a stack has both an overview playbook and a narrower specialized playbook:

- the overview playbook should own shared method and shared workflow doctrine;
- the narrower playbook should own specialized implementation, traps, and examples;
- the narrower playbook should not become a stale partial copy of the overview;
- the overview should not absorb specialized detail that makes it noisy for other audiences.

Use this allocation pattern:

- `Overview` owns the shared standard.
- `Specialized playbooks` own only implementation details unique to that work family.
- `Worked examples / references` hold long example content.
- `Roles` hold authority and role-specific behavior.
- `Work records` hold rollout truth, evidence, and item-specific state.

## Duplication Rule

Duplication is allowed only when it makes the system materially easier to use and maintain.

Duplication is bad when it creates:

- stale copies;
- conflicting rules;
- unclear canonical ownership;
- silent divergence;
- higher-priority role text that accidentally overrides newer playbook doctrine.

Before duplicating a rule, ask:

- Is this genuinely needed in two places?
- Is one location clearly canonical?
- Will both copies realistically stay synced?
- Would a short pointer be better?
- If one copy is in role text, is the duplication needed for authority, safety, trigger discipline, or interface clarity?

If the answer is no, do not duplicate.

Role-text duplication is allowed only when needed for:

- authority enforcement;
- trigger discipline;
- irreversible safety boundary;
- high-frequency repeated failure prevention;
- role-family interface clarity;
- assigned scope or named default counterpart;
- manager-only administration boundary.

Role text should not copy long artifact schemas, source-stack steps, domain mechanics, implementation details, code examples, formula stacks, execution procedures, replay workflows, closeout procedures, or long failure-mode lists already owned by canonical playbooks.

## Preservation Rule

During reorganization, merge, or split work, preserve already-explicit documented learning unless the content is duplicate or wrong.

This includes:

- workflow details;
- boundary rules;
- naming conventions;
- tool-interface facts;
- parameter requirements;
- full-write behavior;
- operational caveats;
- previously earned doctrine from prior work records.

Do not remove a rule just because it feels too detailed.

Do not remove a rule just because the new document should be cleaner.

Do not remove a rule unless one of these is true:

- the rule is duplicate;
- the rule is stale;
- the rule is wrong;
- the rule belongs in another layer;
- the rule is being moved to a clearly named destination.

## Operational-Detail Preservation Rule

Do **not** silently drop still-correct operational tool details.

Preserve:

- tool-interface facts;
- parameter requirements;
- full-write behavior;
- trigger specifics;
- output format expectations;
- other still-live implementation details;

unless they are verified wrong or obsolete.

If an operational detail is being moved to a narrower playbook:

- record the destination explicitly;
- record that move on the governing work record.

## Required Output Contract Rule

Every operational playbook should say what the worker must produce.

Required outputs may include:

- a decision;
- an artifact packet;
- a reroute;
- a verification result;
- a recorded state change;
- a failure classification;
- a closeout summary;
- a migration record;
- an escalation message.

Do not assume the worker will infer the required output from the body text.

Use explicit wording such as:

- `Required outputs`;
- `Exact required output`;
- `Definition of done`.

## Example And Counterexample Rule

Use examples when they materially improve execution quality.

A strong playbook should include examples when:

- the rule is easy to misread;
- the distinction between pass and fail is subtle;
- the worker needs a model of a good output;
- the worker needs to distinguish a real migration from a fake cleanup.

When examples are long, move them to reference documents and point to them explicitly.

Prefer including both:

- a good example;
- a fail example or failure pattern;

when the distinction is operationally important.

## Auditability Rule

Playbook maintenance must stay auditable.

When doctrine moves, record on the governing work record:

- what changed;
- why it changed;
- where it moved;
- which playbook is now canonical;
- whether any mirror changed;
- whether any downstream role text also changed;
- if downstream role text did not change, why no role-text update was needed.

Do not perform silent doctrine migration.

Do not let a cleanup pass erase the ability to reconstruct where a rule went.

## Mirror-Maintenance Workflow

When a canonical playbook changes and a mirror exists:

1. Check whether the mirror title still matches the canonical title.
2. Refresh the mirror header if the canonical title or scope changed.
3. Refresh the first-line canonical-source reference if needed.
4. Remove superseded names from still-live mirrors.
5. Verify the mirror does not preserve stale doctrine after the update.

If a mirror is intentionally different, record the reason explicitly.

## Reorganization / Merge / Split Workflow

When reorganizing playbooks:

1. Identify the exact current canonical source.
2. Identify what content is shared, specialized, role-specific, work-record-specific, duplicate, stale, wrong, or reference material.
3. Identify any role text that duplicates or depends on the doctrine being moved.
4. Preserve all still-correct explicit doctrine.
5. Move content only when the new destination is clearer and still discoverable.
6. Record the destination playbook or section on the governing work record.
7. Refresh mirrors and references.
8. Verify the new stack is easier to use and no less explicit than before.
9. Verify no still-live operational detail was silently lost.
10. Verify any repeated work-record learning that triggered the reorganization has been promoted into explicit doctrine where appropriate.
11. Record whether downstream role text needs no change, refresh, or immediate update.

## Role-Text Interaction Rule

Role text is the employee job contract.

Role text should own:

- employee-specific mandate;
- assigned scope;
- owned decisions;
- non-owned decisions;
- authority boundaries;
- required role outputs;
- normal collaborator boundaries;
- role-specific handoff and escalation triggers;
- role-specific non-goals;
- role-specific safety rails needed at the instruction layer.

Playbooks should own:

- reusable workflow steps;
- artifact schemas;
- required inputs and outputs for recurring work;
- source-stack truth;
- tool mechanics;
- decision criteria;
- calculation procedures;
- implementation details;
- verification gates;
- execution workflows;
- replay and retro standards;
- repeated failure modes that apply across employees.

Because role text has higher instruction priority than playbooks, stale workflow doctrine inside role text can override newer playbook doctrine.

When a playbook rewrite changes role-facing expectations:

1. identify the affected role family;
2. determine whether role text needs no change, a later refresh, or an immediate update;
3. preserve role authority and safety boundaries in role text;
4. avoid copying full reusable workflow back into role text;
5. record the role-text impact decision on the governing work record.

If role text contains full reusable workflow doctrine that now belongs in a playbook, move or point that doctrine to the canonical playbook and leave only the short role-specific authority, safety, or interface reminder in role text.

Use **Organization Manager - Hiring and Employee Role Design** as the canonical standard for writing or rewriting role text.

## Role-Vs-Playbook Boundary Rule

Playbooks should say how reusable work is done.

Roles should say:

- who owns what;
- what authority they have;
- what they do not own;
- what outputs they must leave;
- when they must escalate.

Do not let a playbook become the hidden source of role authority.

Do not let a role become the hidden source of reusable workflow doctrine.

If a rule answers `who owns this?`, it likely belongs in a role.

If a rule answers `how should this reusable workflow be done?`, it likely belongs in a playbook.

If a rule is duplicated in role text only to reinforce authority, safety, trigger discipline, or interface clarity, keep the role-text version short and point to the canonical playbook for detailed procedure.

## Work-Record-Vs-Playbook Boundary Rule

Work records should hold:

- item-specific state;
- evidence;
- rollout progress;
- moved-content destinations;
- validation results;
- one-off truth.

Playbooks should hold:

- reusable doctrine;
- stable workflow;
- stable decision rules;
- stable failure modes;
- stable promoted learning.

Do not leave durable doctrine only on a work record.

Do not pollute playbooks with item-specific transient state.

## Definition Of Done

A playbook-writing or playbook-maintenance task is done only when:

1. the correct canonical home is explicit;
2. the title follows the audience-first naming rule;
3. stable role labels are used unless a true person-specific document is required;
4. the internal H1 is stable and not brittle to future title changes;
5. still-correct prior doctrine has been preserved;
6. duplicate, stale, or wrong content has been removed or moved explicitly;
7. moved doctrine has an explicit destination;
8. the core workflow is explicit and operational;
9. required outputs are explicit;
10. stack-layer boundaries are explicit;
11. role-text interaction has been checked when the rewrite changes employee-facing expectations;
12. downstream role-text impact is recorded as no change, later refresh, or immediate update when applicable;
13. mirrors are refreshed when needed;
14. active mirrors do not preserve superseded names;
15. still-live operational details have not been silently dropped;
16. the new structure is at least as explicit as the prior one;
17. the chosen maintenance path matches the scale of change: targeted edit for local change, author-new-plus-retire-old for majority rewrite;
18. the rewrite satisfies the no-loss doctrine-update rule;
19. the rewrite satisfies the equal-or-better explicitness rule;
20. known recurring work has been written as procedure rather than left at principle-only level;
21. stable repeated work-record learning has been promoted into explicit doctrine where appropriate;
22. the governing work record records what moved, why, and where when reorganization occurred.

## Failure Modes / Escalation

Escalate or reject the rewrite if any of these occur:

- the rewrite compresses away prior explicit learning;
- the maintainer tries to patch through a majority rewrite with scattered edits when author-new-plus-retire-old would be cleaner and easier to audit;
- the rewrite becomes less explicit than the prior playbook;
- still-correct operational detail is silently dropped;
- tool-interface facts or parameter requirements disappear without justification;
- a specialized playbook becomes a stale partial duplicate of an overview playbook;
- canonical ownership becomes ambiguous;
- mirror titles drift from canonical titles without reason;
- active mirrors preserve superseded names;
- internal headings are brittle to future title renames;
- role authority is hidden in playbooks;
- reusable workflow doctrine is hidden only in roles or work records;
- role text copies full reusable workflow doctrine without a valid authority, safety, trigger, or interface reason;
- stale role text could override newer playbook doctrine;
- a playbook rewrite changes role-facing expectations but does not record downstream role-text impact;
- work-record-specific truth is promoted into playbook doctrine;
- long supporting detail is deleted instead of moved to a suitable reference;
- content is moved without recording its destination;
- principle-only wording is left in place where the organization already has a known reusable procedure;
- repeated work-record learning is not promoted into doctrine;
- the new playbook is cleaner-looking but less operationally useful.
