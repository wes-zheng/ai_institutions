# From Agents to Institutions
[![DOI](https://zenodo.org/badge/1227585368.svg)](https://doi.org/10.5281/zenodo.20033468)

Public V1.0 package for a technical report on institutional control for AI labor.

The paper studies a human-owned, AI-staffed prediction-market desk as an empirical stress test for a broader systems claim: AI labor can be made more auditable, controllable, and better structured for governed improvement through institutional design, not only through agent autonomy.

**Author:** Wes Zheng

## Repository Contents

- `technical_report/paper.pdf` - readable public technical report.
- `technical_report/paper.md` - manuscript source of truth.
- `technical_report/paper.tex` - generated LaTeX artifact.
- `technical_report/references.bib` - BibTeX bibliography for the LaTeX artifact.
- `api/` - minimal public setup notes for trying the reference implementation.
- `examples/` - synthetic non-trading examples for trying the ideas without private operational details.
- `CITATION.cff` - citation metadata.
- `LICENSE` - CC BY 4.0 license for the public paper, docs, and examples.

## Paper Frame

Title:

> From Agents to Institutions: A Field Study of Institutional Control in an AI-Staffed Prediction-Market Desk

Core thesis:

> High-skill AI labor takes more than agent capability: it needs institutional-control mechanisms that make ownership, authority, evidence, verification, no-action, closure, replay, and governed adaptation auditable and controllable.

The prediction-market desk is the empirical setting, not the paper's product identity or a trading-strategy claim. The intended contribution is a portable institutional layer above models, agents, workflows, and teams.

## Claim Boundaries

The report argues for institutional auditability and controllability. It does not claim:

- global decision-quality improvement;
- trading performance or forecasting accuracy;
- recurrence reduction without extracted recurrence evidence;
- model-independent causal proof;
- fully autonomous or human-free operation;
- financial advice or a trading strategy.

## How To Read

Start with `technical_report/paper.pdf` for the formatted report or `technical_report/paper.md` for the source text. The report is structured as:

1. problem and thesis;
2. related-work positioning;
3. institutional-control framework;
4. field setting and study design;
5. method/system stack;
6. evaluation framework;
7. bounded results;
8. anchor mechanism cases;
9. discussion;
10. ethics, risk, and compliance;
11. limitations;
13. appendices.

## Try The Idea

1. Read `technical_report/paper.pdf` or `technical_report/paper.md` for the institutional-control framework.
2. Use the report appendices for paper-safe artifact field sets covering roles, work records, messages, verifier decisions, and replay records.
3. Walk through `examples/security_incident_ops_team/` before adapting the ideas to your own non-sensitive workflow.
4. Use `api/README.md` and `api/quickstart.md` only if you want to configure the public reference implementation.

Use synthetic, non-sensitive work examples when experimenting with roles, work records, messages, verifier decisions, no-action states, and replay.
