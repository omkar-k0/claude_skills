# Verified facts (single source of truth for all career claims)

Rules for this file:
- Only facts Omkar has confirmed belong here. Items marked [CONFIRM] were seeded from conversation history or his notes and must be confirmed by him before use in any application deliverable. Never fill a [CONFIRM] by guessing.
- Every claim in a CV bullet, STAR story, LinkedIn section, or cover message must trace to a line in this file.
- When a fact changes (new grade, finished course, new project milestone), update the line, do not duplicate it.
- Project result numbers may only be claimed when an eval table in the project repo backs them (ship-with-eval). Projects marked "eval pending" are described by what they do, not by results.

## Career target
- Applied AI and data Werkstudent and junior roles in Germany. SAP is out of scope as a target.

## Education
- M.Sc. Big Data & Business Analytics, FOM University of Applied Sciences, Essen, Germany. [CONFIRM: start date, expected graduation, current grade average]
- Coursework includes quantitative data analysis / research methods, NLP, data analytics. [CONFIRM exact module names for CV use]
- [CONFIRM: Bachelor's degree, institution, country, year]

## Projects
### ESG rating changes and corporate bond spreads (solo research project)
- Panel regression study, German DAX firms, 2019-2024.
- Stack: Python (linearmodels, statsmodels), data via Refinitiv Workspace.
- Repository: github.com/krakmo1/esg-bond-spreads
- Supervised by Dr. Lars Klingenberger. [CONFIRM: final grade/status, headline finding in one sentence]

### FinBERT NLP project (SEC EDGAR filings)
- Fine-tuned FinBERT comparing sentiment/language in Oil & Gas vs Enterprise Software firms' filings.
- Environment: conda on Apple Silicon with MPS support. Presented May 2026. [CONFIRM: outcome, grade, dataset size]

### Guidance Reconciliation Engine (SEC EDGAR guidance vs outcome)
- Live on Vercel since 24 Oct 2026. Architecture: rule layer, confidence gate, LLM adjudicator with quote checks, blind labelling sheet.
- Status: eval labels pending. No result numbers may be claimed until an eval table exists.

### ContractTracker (MSA obligation extraction)
- Plan: eval set of at least 20 hand-labelled MSAs, scheduled after V1.1 ships.
- Status: no eval yet. No result numbers may be claimed. [CONFIRM: is V1.1 shipped, is it public]

### Werkbank (furniture order routing)
- reports/eval.md: 40% auto-routed at 96% accuracy on hand-written requests; 83% at 99.7% after 100 simulated corrections. These numbers may be claimed, citing that file. [CONFIRM: repo public, client or personal project]

### XAUUSD backtesting package (personal quant project)
- Event-driven backtesting engine for a sweep-reversal strategy; config-driven YAML architecture; Dukascopy data handling; DST-aware session level building; multi-target TP ladder; instrument-agnostic via config switching.
- Demonstrates: Python packaging, data engineering, financial data handling. Demo accounts only, no real money. [CONFIRM: repo public? line count/scale claim allowed?]

### Claude Agent Skills library (personal)
- Designed and built reusable AI agent skills (structured SKILL.md workflows) for study, research, career, and daily-planning workflows. Demonstrates: LLM orchestration, prompt/workflow engineering, confidence-gated design.

## Technical skills (demonstrable in interview)
- Python: pandas, statsmodels, linearmodels, transformers/FinBERT fine-tuning.
- Econometrics: panel data (FE/RE, clustered SEs, Hausman), hypothesis testing.
- NLP: transformer fine-tuning, SEC EDGAR data acquisition.
- Confidence-gated LLM systems: rule layer plus LLM adjudication with confidence scores and citations (Guidance Reconciliation Engine, Werkbank).
- Agent frameworks (self-studied, project-applied where noted): CrewAI, LangGraph, AutoGen, LlamaIndex. [CONFIRM which have actual project artifacts vs study-only]
- SAP: SAP Learning Hub Student Edition access; foundational S/4HANA and BW/4HANA study. Not a career target; list only if a posting asks. [CONFIRM completed courses/badges, list individually]
- Git/GitHub.

## Languages
- English: fluent (working/academic language).
- German: FOM Deutsch exam on 13 Nov 2026, level A1 to A2. Working level is low. Goals: solid A2 by 22 Jan 2027, B1 exam in summer 2027. Do not claim A2 before the exam result, and never B1+ until certified. [CONFIRM: exam result once known]
- [CONFIRM: native language(s)]

## Work experience
- [CONFIRM: any prior work experience, internships, roles in India or Germany. Currently no entries; do not invent any]

## Constraints (for compliance mode)
- International student in Germany; standard student work-hour limits apply. [CONFIRM: residence permit type / §16b status]
- Based in Essen; Deutschland-Ticket holder; realistic commute range is the NRW regional network. [CONFIRM: district still Rüttenscheid]
