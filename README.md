# Environmental Trade-off Calculator

**Project summary:**

- Web calculator for environmental compensation under Resolução SEMIL 02/2024 (São Paulo state, Brazil).
- Product backlog structured as Epics, Features and User Stories in Jira, with DoR and DoD defined.
- Full Lean Inception conducted in Miro, covering all 9 steps of the methodology.
---

## The Problem and Context

The environmental compensation calculation required by Resolução SEMIL 02/2024 is done manually by consultants and engineers, who must consult dozens of pages of regulatory annexes, cross-reference municipal data and perform error-prone calculations. Each calculation can take hours, and any mistake compromises technical reports and licensing processes.

The **Environmental Trade-off Calculator** will be developed as part of the Software Engineering postgraduate programme at PUC-Rio to solve this problem: a web application that automates environmental compensation calculations based on official rules, returning accurate, municipality-specific results in seconds.

---

## 1. The Lean Inception Workshop

We will conduct the full Lean Inception in Miro, covering all 9 steps:

- **Kickoff:** Team alignment and stakeholder presentation.
- **Step 1 — Product Vision:** Value proposition defined for environmental consultants, civil engineers and public agency analysts across SP state.
- **Step 2 — Is / Is Not / Does / Does Not:** Clear scope boundaries — the tool calculates; it does not replace legal opinions or generate official documents.
- **Step 3 — Business Goals:** Save time on compliance, become the reference tool for SEMIL 02/2024 and grow adoption among SP professionals.
- **Step 4 — Personas:** Ana (environmental consultant), Maria (civil engineer) and Mariana (public agency analyst).
- **Step 5 — User Journeys:** 3 journeys mapped — calculate compensation, estimate project cost and verify a submitted calculation.
- **Step 6 — Feature Brainstorming:** Features identified from the user journeys.
- **Step 7 — Technical, UX and Business Review:** Features classified by effort (E$/E$$/E$$$), business value and UX value.
- **Step 8 — Sequencer:** 6 delivery waves defined, with MVP at waves 1 and 2.
- **Step 9 — MVP Canvas:** MVP synthesised with proposal, personas, journeys, features, metrics and cost.

---

## 2. Product Architecture

```
[MVP — Sprint 1]                          [Future increments]
Isolated tree compensation      ══════>   PDF export of results
Forest patch compensation                 CSV batch upload
PPA compensation                          Calculation history
Species conservation status query         Regulation update alerts
REST API (Flask) + Swagger UI             API key authentication
Tabbed HTML/CSS/JS frontend
SQLite DB from official SEMIL CSVs
```

- **Sprint 1 (MVP):** Working API with 4 endpoints, tabbed web interface, database populated from official CSVs and Swagger documentation.
- **Sprint 2 (Increment 1):** Usability improvements — PDF export, municipality autocomplete, responsive layout.
- **Sprint 3 (Increment 2):** Scale — CSV batch upload, local history, URL sharing.

---

## 3. Tech Stack

| Layer | Technology |
|---|---|
| Backend | Python 3 + Flask |
| Database | SQLite |
| API Docs | Swagger / OpenAPI |
| Frontend | HTML, CSS, JavaScript (vanilla) |
| Data | Official SEMIL 02/2024 CSVs |
| Version control | Git + GitHub |

---

## 4. Backlog Structure

The backlog was structured with 5 epics, 9 features and 16 user stories, prioritised according to the Lean Inception sequencer:

- **EP-01 Core Compensation Calculator** 
- **EP-02 Species Conservation Status** 
- **EP-03 API & Documentation** 
- **EP-04 Usability & Frontend** 
- **EP-05 Scale & Future Features** 

Definition of Ready and Definition of Done policies were defined at the end of the backlog and applied to all user stories.

---

## 5. Personas

| Persona | Profile | Main need |
|---|---|---|
| Ana | Environmental consultant, 34 | Fast, accurate compensation values to include in technical reports |
| Marina | Civil engineer, 42 | Compensation cost estimate for project budgeting |
| Mariana | Public agency analyst, 38 | Verify whether a company's submitted calculation is correct |

---

## 6. Repository Structure

```
/
├── canvas-url.txt          # Miro board URL with full Lean Inception and MVP Canvas
├── product-backlog.pdf     # Full backlog: 5 epics, 9 features, 16 stories + DoR and DoD
├── sprint-backlog.pdf      # Sprint 1 backlog: 12 MVP stories + DoR and DoD
├── wireframes/             # UI screens exported from Figma (2 screens, desktop)
│   ├── wireframe-01-example_of_calculator.png
│   ├── wireframe-02-example_of_specie_status.png
└── video-url.txt           # Showcase video URL
```
*Resolução SEMIL 02/2024 — Tool for informational purposes only, not a substitute for official legal review.*
