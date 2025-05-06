# End‑to‑End Audit Data Flow & AI Opportunity Map

## 1. High‑Level Flow Diagram
```
Client            Deloitte            Core Audit Repositories             Analytics Engines                Authoring & Archive
Upload  ───►  Connect  ──►  EMS 4.x / Levia ──►  Omnia  ──►  Reveal → Cortex → Argus ──►  Word / Excel  ──►  Vault & BI
                  ▲                           │                                                  │
                  │                           └─►  Nightly / Realtime Bridge (2025)  ◄────────────┘
                  └─►  Direct Push (future)      
```
*Solid arrows = live today  |  Dashed arrows = future‑state once EMS is retired.*

---


## End‑to‑End Data Flow & AI Opportunities  🚚

| # | Flow Stage    | Systems                        | Pain‑Point         | AI / Automation Fix          |
| - | ------------- | ------------------------------ | ------------------ | ---------------------------- |
| 1 | Client upload | Deloitte Connect               | Manual PBC tagging | NLP auto‑tagger              |
| 2 | Sync          | EMS / Levia                    | Polling, dupes     | Event‑driven dedup           |
| 3 | Bridge        | Omnia                          | Nightly lag        | Direct push                  |
| 4 | Analytics     | Reveal → Cortex → Argus        | Multi‑hop ETL      | Unified GenAI + explanations |
| 5 | Authoring     | Word / Excel + local analytics | Manual refresh     | Auto‑cite & refresh          |
| 6 | Archive       | Vault                          | Manual trigger     | Predictive close             |
| 7 | Reporting     | Power BI / QlikView            | Siloed dashboards  | LLM unified KPI feed         |



# Audit‑Tech & AI Opportunities – Segmented View

Use this version when you need to focus on **one pillar at a time**.  Each category now has its own table – easier to scan, export, or assign owners.

---

## 1. Core Systems  🗄️

| Technology                      | Audit Phase / Use‑Case | Deployed in AU? | RADC Support | AI / Value Opportunity                                                         | Key Notes                                       |
| ------------------------------- | ---------------------- | --------------- | ------------ | ------------------------------------------------------------------------------ | ----------------------------------------------- |
| **Omnia**                       | Fieldwork              | **Yes**         | –            | Conversational GenAI to pre‑populate docs; real‑time anomaly detection (v4.7). | Feature gaps vs EMS; MAT globalisation pending. |
| **Levvia**                      | Fieldwork              | **Yes**         | –            | Predictive planning assistant for small engagements.                           | v3 live Oct 2024; broad rollout June 2025.      |
| **EMS Client**                  | Fieldwork              | **Yes**         | –            | AI summariser of auditor comments & evidence links.                            | EOL May 2027.                                   |
| **Audit Online ⁄ Diagnostics**  | Fieldwork & Review     | **Yes**         | –            | Real‑time risk flags across in‑flight engagements.                             | Web layer on EMS.                               |
| **Quality Assessment Platform** | Quality Mgmt           | **Yes**         | –            | AI‑driven ISQM 1 gap analysis.                                                 | ServiceNow GRC.                                 |
| **InsightBox**                  | Analytics Assist       | **Yes**         | –            | GenAI suggests analytic packages & narratives.                                 | AU analytics platform.                          |
| **Digital Confirmation**        | Substantive – Cash     | **No**          | **Yes**      | API automation; confirmation.com bridge.                                       | Decommissioned in AU; potential FS pilot.       |
| **Document AI (DocAI)**         | Fieldwork              | **No**          | –            | GenAI clause extraction & Omnia integration (June 2025).                       | Kira replaced by GenAI.                         |
| **Asset Count**                 | Inventory Counts       | **No**          | **Yes**      | Mobile vision for count evidence.                                              | BYOD hurdle in AU.                              |
| **Checklist**                   | Throughout             | **Yes**         | –            | Future GenAI auto‑flagging.                                                    | –                                               |
| **Document Generator (Scribe)** | Reporting              | **No**          | –            | GenAI memo drafting & style enforcement.                                       | 1 US memo live.                                 |
| **ACTT**                        | IT Controls            | **Yes**         | –            | AI explanations for control failures.                                          | ERP SOD/GITC/FAC.                               |

---

## 2. Analytics & AI  📊

| Technology                | Audit Phase / Use‑Case | Deployed in AU?  | AI Opportunity                              | Notes               |
| ------------------------- | ---------------------- | ---------------- | ------------------------------------------- | ------------------- |
| **Argus / DocAI**         | Fieldwork              | Pilot            | Advanced NLP extraction; auto‑risk memos.   | Global rollout ’25. |
| **DataSnipper**           | Fieldwork              | **Yes**          | GenAI narrative on extracted evidence.      | Overlaps Tie‑out.   |
| **Process X‑ray**         | Planning & Review      | No               | GenAI targeted testing from process mining. | Hosted NL Azure.    |
| **Omnia DNAV**            | Substantive            | No               | LLM commentary for investment valuation.    | –                   |
| **Reveal Analytics**      | Substantive            | **Yes**          | Plain‑English regression output via LLM.    | –                   |
| **Audit Insights Portal** | Planning & Review      | **Yes**          | Forecast emerging risk trends.              | –                   |
| **Data Science Platform** | Across                 | **Yes**          | Secure GenAI sandbox.                       | Azure foundation.   |
| **Omnia Data**            | Reporting              | Pilot (Dec 2025) | GenAI visual narrative over datasets.       | –                   |

---

## 3. GenAI Roadmap  🤖

| Technology             | Use‑Case            | Deploy Status      | RADC Support | Value                                           |
| ---------------------- | ------------------- | ------------------ | ------------ | ----------------------------------------------- |
| **Smart Review**       | Controls Doc Review | Planned (May 2025) | **Yes**      | Auto‑suggest improvements.                      |
| **Research Assistant** | Technical Research  | Pilot (ISA)        | –            | Chatbot with citations; accuracy work underway. |

---

## 4. Learning & Knowledge  📚

| Technology          | Primary Use                | Deployed?  | AI Opportunity            | Notes                         |
| ------------------- | -------------------------- | ---------- | ------------------------- | ----------------------------- |
| **Research Portal** | Standards & manuals search | **Yes**    | Semantic/LLM Q\&A.        | Replaces Tech Library & DART. |
| **Clever Nelly**    | Continuous learning        | **Yes**    | GenAI personalised paths. | –                             |
| **Auditorium**      | Methodology templates      | **Yes**    | AI template recommender.  | Rolling into Research Portal. |
| **GAATE**           | Talent development         | **Yes**    | GenAI career coach.       | Usage stats TBD.              |
| **DART**            | Legacy research            | Sunsetting | –                         | Retires Nov 2025.             |

---

## 5. Support & Collaboration  🤝

| Technology            | Use‑Case                  | Deployed? | AI Opportunity                            |
| --------------------- | ------------------------- | --------- | ----------------------------------------- |
| **Deloitte Connect**  | Client collaboration      | **Yes**   | Smart doc‑request bot; event‑driven sync. |
| **ACMS**              | Engagement acceptance     | **Yes**   | AI partner‑rotation checker.              |
| **Dayshape**          | Resource planning         | **Yes**   | GenAI scenario optimiser.                 |
| **ADC Portal**        | On/Off‑shore coordination | **Yes**   | Auto‑route tasks to RADC.                 |
| **NICE CXone**        | Client support calls      | No        | Speech‑to‑insights; KB tagging.           |
| **Confluence / Jira** | PMO & dev                 | **Yes**   | LLM page/action summariser.               |

---

## 6. Pipeline / Not‑Yet‑Deployed  🛠️

| Tech                | Planned Phase | RADC Support | Opportunity            | Status                    |
| ------------------- | ------------- | ------------ | ---------------------- | ------------------------- |
| **Tie‑out**         | FS Review     | **Yes**      | LLM‑assisted tie‑outs. | Future Omnia integration. |
| **DataSnipper FSS** | FS Review     | –            | Alt to Tie‑out.        | Evaluation stage.         |

---

## 7. Add‑to‑CMDB & Utilities  📝

| Technology             | Area               | AI Opportunity                                  | Note         |
| ---------------------- | ------------------ | ----------------------------------------------- | ------------ |
| **Data Lens**          | Reporting          | GenAI narrative over KPIs.                      | –            |
| **Corelogic**          | Valuation support  | AI detect valuation anomalies.                  | –            |
| **Controls Advantage** | Controls testing   | AI risk ranking.                                | Details TBD. |
| **ExpenseWise**        | Advisory analytics | GenAI classify anomalies.                       | TBD.         |
| **Quizzed**            | Learning polls     | Auto‑generate quiz questions.                   | Global tool. |
| **ESG Readiness Tool** | ESG advisory       | Compare vs SustainNext; GenAI ESG gap analysis. | Under eval.  |

---

> **How to use** → Filter one table at a time or copy just the relevant segment into your deck or backlog.  If you’d like cost columns, ownership, or ROI scoring added, let me know!

---

*The End‑to‑End Data Flow Map remains unchanged below for reference.*

---


