# Process groups mapping

## Process groups over the semester

| Process group | Weeks active | Main activities | Outputs | Lab that produces them |
|---------------|--------------|-----------------|---------|------------------------|
| Initiating | Weeks 1–2 | Defining project scope, establishing business justification, identifying initial stakeholders, drafting project charter | Project charter, stakeholder list, business case | Lab 01 |
| Planning | Weeks 1–3 (Initial burst), Weeks 4–14 (Ongoing) | Estimating schedule and cost, risk management planning, architecture design, re-planning after status reviews | PM plan, subsidiary management plans, updated baselines | Labs 02, 03, 04, 07, 08 |
| Executing | Weeks 3–13 | Developing platform core (Must features), implementing Should/Could features, integration testing, system hardening | Working platform software, test reports, MVP release | Labs 05, 06, 10 |
| Monitoring and controlling | Weeks 1–14 | Tracking weekly progress, calculating schedule/cost variance, reviewing risk register, managing change requests | Status reports, issue log, change log, variance reports | Labs 05, 06, 09, 11 |
| Closing | Weeks 13–14 | Executing live pilot with 50 students, conducting post-mortem, gathering lessons learned, administrative project sign-off | Pilot evaluation report, post-mortem, handover document, final repository | Lab 12, Challenge |

## Semester Gantt Chart

```mermaid
gantt
  title Process groups over the 14-week semester (Realtime Quiz)
  dateFormat YYYY-MM-DD
  axisFormat %d %b
  section Initiating
  Charter, stakeholders, business case   :i1, 2026-09-29, 7d
  section Planning
  PM plan and subsidiary plans           :p1, 2026-09-29, 21d
  Re-planning after each status review   :p2, 2026-10-20, 77d
  section Executing
  Build to MVP (Must features)           :e1, 2026-10-13, 35d
  MVP demo                               :milestone, m1, 2026-11-17, 0d
  Should and Could features, hardening   :e2, 2026-11-17, 35d
  section Monitoring and controlling
  Weekly status, variance, change log    :m2, 2026-09-29, 98d
  section Closing
  Pilot with 50 students, lessons learned :c1, 2026-12-29, 7d
  Pilot with 50 students                 :milestone, m2, 2026-12-29, 0d