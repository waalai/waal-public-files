
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

## 2. Detailed Stage‑by‑Stage View

| # | Stage                        | Primary Systems                                | Data Assets                        | Pain‑Points / Latencies                    | AI / Automation Opportunity                                |
|---|------------------------------|-----------------------------------------------|------------------------------------|--------------------------------------------|------------------------------------------------------------|
| 1 | **Client Upload**            | Deloitte Connect                               | Source files, PBC metadata         | Manual tagging, inconsistent request names | NLP tagger that auto‑builds PBC requests & metadata.       |
| 2 | **Initial Sync (15‑30 min)** | EMS “PBC” folder, Levia S3, AU Gateway         | Working copy, archive copy         | Duplicate storage; polling‑based sync      | Event‑driven pipeline; dedup & conflict‑detect.            |
| 3 | **Bridge to Omnia**          | Omnia Source Docs (nightly → realtime)         | Consolidated evidence library      | Batch lag; EMS dependency                  | Direct push API; instant analytics trigger.                |
| 4 | **Analytics Chain**          | Reveal → Cortex → Argus                        | Profiling stats, risk flags        | Multiple ETL hops                          | Unified GenAI engine; auto‑explain flags in plain English. |
| 5 | **Authoring Plugins**        | Omnia Word/Excel, Excel Analytics, DataSnipper | Live evidence & analytics extracts | Manual refresh & cache mgmt                | Auto‑refresh; AI‑suggested citations.                      |
| 6 | **Close‑out & Archive**      | Vault (CM‑9)                                   | Sealed engagement package          | Manual trigger delays                      | Predictive “ready‑to‑close” indicator; auto‑archive.       |
| 7 | **Reporting**                | Extended Reporting Data → Power BI, QlikView   | Engagement KPIs                    | Siloed dashboards                          | LLM summariser; proactive SLA alerts.                      |

---

# Consolidated Audit‑Tech & AI Opportunity Matrix  🗂️

A single view that merges **AI Opportunities**, **Deployment Status**, and **Digital Audit Enablers**.  Use the filters (or Ctrl/⌘‑F) to slice by category, audit phase, or deployment readiness.

| Technology                                   | Category                | Audit Phase / Use‑Case | Deployed in AU?         | RADC Support | AI / Value Opportunity                                                               | Key Notes                                       |
| -------------------------------------------- | ----------------------- | ---------------------- | ----------------------- | ------------ | ------------------------------------------------------------------------------------ | ----------------------------------------------- |
| **Omnia**                                    | Core System             | Fieldwork              | **Yes**                 | N/A          | Conversational GenAI to pre‑populate docs; real‑time anomaly detection (v4.7).       | Feature gaps vs EMS; MAT globalisation pending. |
| **Levvia**                                   | Core System             | Fieldwork              | **Yes**                 | N/A          | Predictive planning assistant for small engagements.                                 | v3 live Oct 2024; broad rollout June 2025.      |
| **EMS Client**                               | Core System             | Fieldwork              | **Yes**                 | N/A          | AI summariser of auditor comments & evidence links.                                  | EOL May 2027.                                   |
| **Audit Online / Diagnostics**               | Core System             | Fieldwork & Review     | **Yes**                 | N/A          | Real‑time risk flags across in‑flight engagements.                                   | Web layer on EMS.                               |
| **Quality Assessment Platform (QAP)**        | Core System             | Quality Mgmt           | **Yes**                 | N/A          | AI‑driven ISQM 1 gap analysis.                                                       | ServiceNow GRC.                                 |
| **InsightBox**                               | Core System             | Analytics Assist       | **Yes**                 | N/A          | GenAI recommends analytic packages & narratives.                                     | AU analytics platform.                          |
| **Digital Confirmation**                     | Core System             | Substantive – Cash     | **No**                  | **Yes**      | API integration to automate confirmations (current workaround via confirmation.com). | Tool decommissioned in AU; possible FS use.     |
| **Document AI (DocAI)**                      | Core System / Analytics | Fieldwork              | **No**                  | No           | GenAI clause extraction & Omnia integration (June 2025).                             | Kira replaced by GenAI.                         |
| **Asset Count**                              | Core System             | Inventory Counts       | **No**                  | **Yes**      | Mobile image recognition for count evidence.                                         | BYOD hurdle in AU.                              |
| **Checklist**                                | Core System             | Throughout             | **Yes**                 | N/A          | Digitised checklist validation; future GenAI auto‑flagging.                          | —                                               |
| **Document Generator (Scribe)**              | Core System             | Reporting              | **No (1 memo)**         | No           | GenAI memo drafting & style enforcement.                                             | Limited US memo live; expansion TBD.            |
| **ACTT**                                     | Core System             | IT Controls            | **Yes**                 | N/A          | Extend AI to auto‑explain control failures & suggest remediation.                    | ERP SOD/GITC/FAC testing.                       |
| **Argus / DocAI**                            | Analytics & AI          | Fieldwork              | **No** (Pilot)          | N/A          | Advanced NLP extraction & auto‑risk memos.                                           | Re‑named DocAI; global rollout 2025.            |
| **DataSnipper**                              | Analytics & AI          | Fieldwork              | **Yes**                 | N/A          | GenAI narrative builder around extracted evidence.                                   | Overlaps Tie‑out.                               |
| **Process X‑ray**                            | Analytics & AI          | Planning & Review      | **No**                  | N/A          | GenAI‑suggested targeted tests from process mining.                                  | Hosted NL Azure.                                |
| **Omnia DNAV**                               | Analytics & AI          | Substantive            | **No**                  | N/A          | LLM commentary for investment valuation.                                             | Not yet deployed in AU.                         |
| **Reveal Analytics**                         | Analytics & AI          | Substantive            | **Yes**                 | N/A          | LLM plain‑English translation of regression results.                                 | —                                               |
| **Audit Insights Portal**                    | Analytics & AI          | Planning & Review      | **Yes**                 | N/A          | Forecast emerging risk trends across portfolio.                                      | —                                               |
| **Data Science & Analytics Platform (A\&A)** | Analytics & AI          | Across                 | **Yes**                 | N/A          | Secure GenAI sandbox for practitioners.                                              | Azure foundation.                               |
| **Omnia Data**                               | Analytics & AI          | Reporting              | **No**                  | **Yes**      | GenAI visual narrative over Omnia datasets.                                          | Pilot Apr 2025; go‑live Dec 2025 Y/E.           |
| **Tie‑out**                                  | Not Deployed            | FS Review              | **No**                  | **Yes**      | LLM‑assisted FS tie‑outs (may merge with DataSnipper).                               | Future Omnia integration.                       |
| **DataSnipper FSS**                          | Not Deployed            | FS Review              | **No**                  | N/A          | Same as above; evaluation vs Tie‑out.                                                | —                                               |
| **Smart Review**                             | GenAI                   | Controls Docs Review   | **Planned (May 2025)**  | **Yes**      | Auto‑reviews controls narratives & suggests improvements.                            | Ships with Omnia 4.7.                           |
| **Research Assistant**                       | GenAI                   | Technical Research     | **Pilot (ISA)**         | No           | Chatbot over Research Portal with citation links.                                    | Accuracy improvements in flight.                |
| **Research Portal**                          | Learning & Knowledge    | Planning               | **Yes**                 | N/A          | Semantic search; LLM Q\&A on standards (roadmap).                                    | Replaces Tech Library & DART.                   |
| **Clever Nelly**                             | Learning & Knowledge    | Continuous             | **Yes**                 | N/A          | GenAI to create bespoke learning paths.                                              | Spaced‑learning quizzes.                        |
| **Auditorium**                               | Learning & Knowledge    | Methodology            | **Yes**                 | N/A          | AI template recommender based on engagement context.                                 | To merge into Research Portal (18 mths).        |
| **GAATE**                                    | Learning & Knowledge    | Talent Dev             | **Yes**                 | N/A          | GenAI career coach recommending projects/training.                                   | Usage stats TBD.                                |
| **DART**                                     | Learning & Knowledge    | Planning               | **Legacy (sunsetting)** | N/A          | See Research Portal.                                                                 | Retires Nov 2025.                               |
| **Deloitte Connect**                         | Support & Collab        | Client Collab          | **Yes**                 | N/A          | AI doc‑request bot learns client behaviour.                                          | —                                               |
| **ACMS**                                     | Support & Collab        | Acceptance             | **Yes**                 | N/A          | AI to flag partner rotation issues.                                                  | ServiceNow form replacement.                    |
| **Dayshape**                                 | Support & Collab        | Planning               | **Yes**                 | N/A          | GenAI scenario‑based resourcing optimiser.                                           | Global scheduling.                              |
| **ADC Portal**                               | Support & Collab        | Fieldwork Support      | **Yes**                 | N/A          | Auto‑route tasks to RADC by skill/complexity.                                        | Core on/off‑shore portal.                       |
| **NICE CXone**                               | Support & Collab        | Client Support         | **No**                  | N/A          | Speech‑to‑insight for client calls; auto‑KB tagging.                                 | Cloud CX platform.                              |
| **Confluence / Jira**                        | Support & Collab        | PMO & Dev              | **Yes**                 | N/A          | LLM to summarise project pages & actions.                                            | Atlassian suite.                                |
| **Data Lens**                                | Add‑to‑CMDB             | Reporting              | **No**                  | N/A          | GenAI narrative over Omnia/Levvia KPIs.                                              | Aggregation layer.                              |
| **Corelogic**                                | Add‑to‑CMDB             | Specialist Valuation   | **No**                  | N/A          | AI anomaly detection for property valuations.                                        | —                                               |
| **Controls Advantage**                       | Add‑to‑CMDB             | Controls Testing       | **No**                  | N/A          | AI risk ranking for ERP controls.                                                    | Details TBD.                                    |
| **ExpenseWise**                              | Add‑to‑CMDB             | Advisory Analytics     | **No**                  | N/A          | GenAI expense anomaly classification.                                                | Details TBD.                                    |
| **Quizzed**                                  | Add‑to‑CMDB             | Learning               | **No**                  | N/A          | LLM auto‑generates quiz questions from guidance.                                     | Global learning tool.                           |
| **ADC Portal**                               | Utilities               | On/Off‑shore           | **Yes**                 | N/A          | (See above)                                                                          | Duplicate listed for utility completeness.      |
| **ESG Readiness Tool**                       | ESG                     | Advisory               | **No**                  | TBC          | Compare vs SustainNext; potential GenAI ESG gap analysis.                            | Under evaluation.                               |

> **Legend**
> • *Category* groups by purpose.
> • *RADC Support* indicates whether the Regional Audit Delivery Centre currently assists with the tool/process.
> • Cells in **bold** denote confirmed production use in AU.

Feel free to request a prioritised view (e.g., Quick‑wins quadrant) or cost/ROI overlays.



 
