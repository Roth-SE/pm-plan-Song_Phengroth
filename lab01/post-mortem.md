# Post-mortem: CampusPay Wallet Case Study (Fictional)

## 1. Timeline and sources

| # | When | Event | Source |
|---|------|-------|--------|
| 1 | Month 1 | Head of Finance sponsors CampusPay wallet via informal email to build a cashless canteen/library app in one semester without issuing a signed charter. | Fictional case from Lab-01 |
| 2 | Month 2 | Lead developer assumes dual roles of Project Manager and primary programmer; initial development begins without a formal PMO or governance oversight. | Fictional case from Lab-01 |
| 3 | Month 3 | Following an unconstrained user survey, project scope creeps significantly to include bus ticket booking and campus parking payments. | Fictional case from Lab-01 |
| 4 | Month 4 | System build finishes with progress reported as "on schedule," but no end-to-end load testing or real card terminal integration tests are conducted. | Fictional case from Lab-01 |
| 5 | Month 5 (Day 1) | Official go-live occurs; campus card terminals reject 40% of payment transactions, leading to doubled canteen queue lengths. | Fictional case from Lab-01 |
| 6 | Month 5 (Day 3) | Severe operational disruption forces complete withdrawal and shutdown of the application after three days in production. | Fictional case from Lab-01 |
| 7 | Month 10 | Application is relaunched five months later with a drastically reduced scope, serving canteen payments only. | Fictional case from Lab-01 |

## 2. Classification and organisation

- **Project / Programme:** Started as a standalone project, but rapidly turned into an uncoordinated pseudo-programme when additional distinct domain projects (bus ticketing, parking management) were added without structural realignment or separate governance.
- **Structure and PM authority:** Operates in a **Functional Organisation**. The PM was a lead developer with dual roles, holding zero formal authority to manage budget, reject scope creep, or enforce cross-departmental testing.
- **Sponsor, charter, PMO:** **No formal sponsor** (the Head of Finance only sent an informal email and never attended reviews), **no project charter** to baseline constraints, and **no PMO** to enforce quality assurance or delivery standards.

## 3. Success criteria

- **Stated:** Arbitrary schedule target ("Launch in September") without functional baseline or quality constraints.
- **Missing measurable criteria:** Transaction failure rate (< 1%), system latency under peak load (< 500 ms), terminal interface compatibility (100% card terminal handshake success), and user queue throughput time.
- **Ignored dimensions:** 
  - *Benefits:* Real economic savings and canteen queue reduction were completely lost due to system failure.
  - *Users:* Student and staff satisfaction severely damaged by 40% payment failure rate.
  - *Operations:* IT operational readiness, staff training, and terminal hardware integration were ignored prior to go-live.
  - *Team:* Developer burnout and reputation loss caused by working under unmanaged scope and dual roles.

## 4. Process groups and knowledge areas

| Process group | What went wrong or was skipped |
|---------------|--------------------------------|
| **Initiating** | Skipped entirely; no formal charter was signed and the sponsor never formally accepted responsibility, leaving scope boundaries undefined. |
| **Planning** | Inadequate and unbaselined; schedule was fixed to an arbitrary date while requirements were allowed to expand continuously without risk or cost planning. |
| **Executing** | Team focused strictly on coding features while skipping essential integration work, hardware validation, and pre-deployment trial runs. |
| **Monitoring and controlling** | Progress was falsely reported as "on schedule" without real evidence or quality metrics, falling into the invisibility trap. |
| **Closing** | No formal post-launch review or operational handover occurred; the application was abruptly pulled after total operational breakdown on day 3. |

**Knowledge areas most responsible:**
1. **Scope Management:** Scope creep was uncontrolled; adding bus ticketing and parking features without evaluating impact, schedule baseline changes, or sponsor approval.
2. **Quality Management:** Integration testing with physical card terminals was completely omitted before launch day, directly causing the 40% failure rate.
3. **Stakeholder / Governance Management:** The sponsor was non-engaged and absent from reviews, leaving no executive backing or steering authority to make critical project decisions.

## 5. Ethics

- **Decision examined:** Launching the CampusPay wallet to the entire campus population without conducting end-to-end hardware testing or verifying transaction stability with physical card terminals.
- **Ethical Analysis (PMI Code of Ethics):**
  - **Responsibility:** Failed to protect the institution and students from operational chaos by deploying unverified software into a critical daily function (canteen queues).
  - **Respect:** Disregarded student and canteen staff time by exposing them to doubled queue times and rejected transactions without warning.
  - **Fairness:** Unfairly shifted risk onto end users and front-line canteen workers without providing fallback payment procedures.
  - **Honesty:** Misrepresented project readiness by declaring "on schedule" delivery while hiding the complete absence of integration test results.

## 6. What our project will do differently

| # | Commitment (We will ...) | Measured by | By week | Charter line |
|---|--------------------------|-------------|---------|--------------|
| 1 | Hold a signed project charter with an active sponsor who formally approves Phase Gates at Week 1, Week 7, and Week 13 | Signed charter document and recorded gate meeting minutes | 1 | Charter Section 10 (Approval) & Section 9 (Authority) |
| 2 | Enforce strict scope control by rejecting any non-goal or out-of-scope feature request without a written change order approved by the sponsor | Change log with 0 unapproved scope additions | 14 | Charter Section 3 (High-level scope: Out of scope list) |
| 3 | Execute automated unit, integration, and load testing simulating 50 concurrent active users before conducting any live demonstration | Test execution report showing >= 85% code coverage and 0 blocking bugs | 11 | Charter Section 2 (Objective O4 & O5) |
| 4 | Validate real-time WebSocket communication latency under 500 ms on campus infrastructure prior to pilot deployment | Performance testing log with 95th percentile latency <= 500 ms | 12 | Charter Section 2 (Objective O3) & Section 8 (Risks) |
| 5 | Complete a pre-pilot operational readiness assessment with IT operations before handing over production artifacts | Signed operational runbook (`docker-compose.prod.yml`) and deployment checklist | 13 | Charter Section 4 (Milestones) & Section 9 (PM Authority) |