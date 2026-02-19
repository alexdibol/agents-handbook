# Agents Handbook — Agentic Architectures in Finance (LangGraph-Only)

Governance-first · auditable · reproducible · human-accountable  
Built for **MBA / Master of Finance cohorts** and **professional finance / trading / research practitioners** who need mechanism clarity under constraint.

---

## What this repository is

This repository is the governed home of **Agents Handbook**: a modular, Colab-first suite that teaches **agentic architectures in finance** using **LangGraph only**.

The objective is not “prompting tricks.”  
The objective is **systems engineering**: explicit state, routing logic, bounded loops, termination rules, and control-grade artifacts that let a reviewer answer:

- what happened  
- why it happened  
- what the system believed at each gate  
- where the system stopped  
- what remains unknown

This handbook is intentionally explicit about its limits:

- it does **not** promise correctness of external facts  
- it does **not** claim deployability or production readiness by default  
- it does **not** treat generated outputs as verified evidence  

It is a mechanism-first, governance-first teaching and research environment designed to be:

- deterministic under seed  
- reviewable via mandatory artifacts  
- constrained by explicit gates and early-termination rules  
- transparent about facts vs assumptions vs open items

**Core premise:**  
**Capability ↑ ⇒ Risk ↑ ⇒ Controls ↑**

---

## Repository structure

- **/handbook/**  
  Written material: architecture notes, patterns, governance framing, and how to read the graphs.

- **/notebooks/**  
  The 10 Colab notebooks (N1–N10). Each notebook is intentionally constrained and designed to run end-to-end with reproducible artifacts.

---

## Canonical links

### Repository
- https://github.com/alexdibol/agents-handbook

### Handbook
- Folder: https://github.com/alexdibol/agents-handbook/tree/main/handbook

### Notebooks
- Folder: https://github.com/alexdibol/agents-handbook/tree/main/notebooks

---

## Architecture roadmap (10 governed notebooks)

Each notebook is a finance objective mapped to a reusable agentic pattern.

1) **N1 — Personal finance triage & missing-info discovery**  
   Conditional retry loop for missing inputs; bounded attempts; stops when sufficient information exists or escalation is required.

2) **N2 — Advice suitability boundary & refuse/redirect paths**  
   Hard branching + early termination. The workflow enforces scope boundaries and refusal posture where required.

3) **N3 — Credit memo drafting with evidence gaps**  
   Structured critique loop. Produces a memo draft while explicitly tracking evidence gaps and open items.

4) **N4 — Trading hypothesis + backtest wrapper**  
   Tool-augmented node. Hypothesis formation + test harness + diagnostics + decision gate (promote/revise/reject).

5) **N5 — Execution/tactics under liquidity conditions**  
   Stateful regime machine. Execution tactics respond to liquidity/volatility regimes under bounded iteration.

6) **N6 — Portfolio rebalancing with risk/cost perspectives**  
   Parallel committee + aggregation. Multiple perspectives evaluate actions; an aggregator reconciles outputs and records disagreements.

7) **N7 — IB pitchbook sections (comps/rationale/risks)**  
   Hub-and-spoke constellation. Section agents produce components; a hub assembles, validates completeness, and flags gaps.

8) **N8 — M&A diligence Q&A over documents**  
   Router + retrieval. Classify question → retrieve evidence → answer with provenance and explicit uncertainty handling.

9) **N9 — Treasury liquidity/covenant monitoring**  
   Event-driven workflow. Monitor metrics; detect breach signals; escalate; generate reviewable control outputs.

10) **N10 — Multi-desk research synthesis + red-team**  
   Supervised multi-agent system. Synthesis plus adversarial review; promotion gate for publishable output.

---

## What every notebook enforces (non-negotiable)

This repository follows a strict “laboratory contract.” Every notebook:

- uses **LangGraph only** (architecture-first)
- defines explicit **TypedDict state**
- uses an **AgentNode** abstraction
- implements **conditional routing**
- implements **bounded loops** (no unbounded retries)
- renders a **Mermaid graph** (programmatic render in Colab)
- reads the model API key via:
  - `from google.colab import userdata`
  - `userdata.get("ANTHROPIC_API_KEY")`
- exports run artifacts every execution:
  - `run_manifest.json`
  - `graph_spec.json`
  - `final_state.json`

This is not “extra process.”  
This is what makes agentic work reviewable.

---

## How to use this repository

Recommended learning posture:

1) Read the relevant note in **/handbook/** (mental model + failure modes).  
2) Run the notebook as-is (no edits).  
3) Inspect the artifacts and trace outputs.  
4) Stress the system structurally (increase ambiguity, reduce evidence, tighten gates).  
5) Document failure modes and termination reasons.  
6) Only then modify one mechanism at a time.

**Operating rule:** if the workflow “works” only when you ignore gates, loops, or termination logic, then it does not work.

---

## Shared governance spine (applies across this repo)

- **Generation ≠ verification**  
  Model output is always **Not verified** until qualified humans validate it.

- **Facts vs assumptions discipline**  
  Facts provided, assumptions made, and open questions are explicitly separated (in state and in outputs).

- **Scope and boundary control**  
  Clear task definitions, stop-if rules, and refusal posture where applicable.

- **Auditability by design**  
  Artifacts enable reconstruction, supervision, and review.

- **Human accountability**  
  Responsibility never leaves the human professional.

---

## Who this is for

Designed for:

- MBA and Master of Finance students  
- finance practitioners building governed workflows  
- systematic trading / research teams building agentic research pipelines  
- risk, compliance, and model governance teams  
- instructors teaching agent systems responsibly  

This is not a “magic AI” repository.  
The objective is **mechanism literacy** and **governed implementation**.

---

## Use of generative AI tools (transparency statement)

Generative AI tools may have been used to assist drafting, editing, formatting, or code scaffolding.

However:

- conceptual design  
- pedagogical structure  
- governance logic and control definitions  
- integration decisions  
- final editorial judgment and acceptance  

were **human-led, human-supervised, and human-approved** at all times.

The author assumes **full responsibility** for the content, structure, interpretation, and conclusions presented in this work.

---

## IMPORTANT DISCLAIMERS (read before use)

### Educational / Non-Reliance
All materials are provided **for educational and research purposes only**.  
Nothing in this repository constitutes:

- investment advice  
- trading advice  
- legal advice  
- tax advice  
- accounting or audit advice  
- compliance determinations  
- operational recommendations  

Qualified human professionals must review, verify, and approve any real-world use.

### Not verified
Unless explicitly stated otherwise in a particular artifact, treat all outputs, claims, calculations, citations, and conclusions as **Not verified**.

### Confidentiality and data hygiene
Do not paste confidential, proprietary, regulated, or personally identifying information into external systems.  
Use anonymization/redaction and **minimum-necessary** inputs by default.  
You are responsible for compliance with privacy, confidentiality, recordkeeping, and information security obligations.

### No fabricated sources or claims
Zero tolerance for invented citations, performance claims, fees, terms, or consequences.  
When evidence is missing, the correct output is a **verification task list**, not persuasive narrative.

---


## License (MIT)

This project is released under the **MIT License**.

**Copyright (c) 2026 Alejandro Reynoso**

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the “Software”), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED “AS IS”, WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

---

## Contact

Alejandro Reynoso  
Email: areynoso@yahoo.com  
GitHub: https://github.com/alexdibol
