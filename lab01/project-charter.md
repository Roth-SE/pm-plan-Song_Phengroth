# Project charter: Realtime Quiz platform

| Field    | Value                              |
|----------|------------------------------------|
| Version  | 1.0 (draft for sponsor approval)   |
| Date     | 2026-09-29                         |
| Sponsor  | Head of the IT department          |
| PM       | Tongsreng TAL                     |

## 1. Purpose and justification
Manual marking loads and the absence of instant student feedback create significant grading bottlenecks and reduce classroom engagement. To solve this, the Realtime Quiz platform delivers automated quiz creation, live question broadcasting, and instant grading. As detailed in `business-case.md`, this solution eliminates grading delays, increases student participation through real-time feedback, and reduces instructor administrative workload by 60%.

## 2. Objectives and success criteria
| #  | Objective (what will be true)      | Success criterion (number + week) |
|----|------------------------------------|-----------------------------------|
| O1 | Platform core build and feature implementation | 100% of Must and Should requirements completed by week 6 |
| O2 | Pilot with 50 students in one live session | 50 participants, 0 blocking defects, week 14 |
| O3 | Broadcast latency during the pilot | <= 500 ms at the 95th percentile, measured week 14 |
| O4 | System concurrency and capacity handling | Support 50 concurrent active users without degradation, week 7 |
| O5 | Comprehensive test coverage across all modules | >= 85% automated test coverage achieved by week 11 |

## 3. High-level scope
In scope:
- User authentication and role-based access control
- Quiz creation and question bank management
- Real-time question broadcasting and live timer
- Instant automated scoring and result tabulation
- Student performance dashboard and analytics export

Out of scope:
- Native mobile applications for iOS and Android
- Advanced AI-generated proctoring and facial recognition
- Multi-language localization and translation services
- Integration with third-party enterprise LMS platforms beyond CSV export

## 4. Milestones
| Week | Milestone                          | Ends process group |
|------|------------------------------------|--------------------|
| 1    | Charter approved, team formed      | Initiating         |
| 3    | Requirements and architecture finalized | Planning      |
| 5    | Core backend and database operational | Executing         |
| 7    | MVP demo                           | Executing          |
| 10   | Integration of analytics features  | Executing          |
| 12   | User acceptance testing and bug fixes | Monitoring & Controlling |
| 14   | Pilot with 50 students, closure    | Closing            |

## 5. Budget summary
Effort:  students 4 x 14 x 8 h = 448 h; PM 14 x 3 h = 42 h; total 490 h
Cash:    hosting 4 x 25 USD = 100; domain 15; tools 60; reserve 25 (14 %)
         total 200 USD

## 6. Assumptions
- Participating students will have reliable internet connectivity and modern web browsers during the pilot session in week 14.
- The university IT department will provide necessary server hosting resources and domain registration support on schedule.
- The core project team of four students will consistently dedicate 32 hours per week combined across the 14-week timeline.

## 7. Constraints
- The entire project must be completed within the fixed 14-week semester schedule, concluding with the pilot in week 14.
- Total cash expenditure must not exceed the strict financial cap of 200 USD.
- Development tools and hosting configurations must comply with university open-source and security policies.

## 8. High-level risks
- Network latency spikes during high concurrency live sessions affecting real-time broadcast performance.
- Scope creep or feature bloat delaying MVP delivery beyond week 7.

## 9. Project manager authority
The PM re-plans within the 490 h and 200 USD budget without approval; adding scope, moving the pilot, or spending beyond the reserve needs the sponsor's written approval within 5 working days.

## 10. Approval
Sponsor: ____________________  Date: ________
PM:      ____________________  Date: ________