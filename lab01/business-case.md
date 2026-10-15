# Business case: live quizzes for the IT department

## 1. Problem
Instructors in the IT department spend significant time manually grading weekly paper/online quizzes and lack real-time feedback during live lectures. This creates a administrative backlog, delays feedback to students, and reduces classroom engagement.

Assumptions:
- Lecturers running quizzes: 10
- Marking time saved per lecturer per week: 1 h
- Teaching weeks per year: 30
- Total marking hours spent per year: 10 lecturers * 1 h/week * 30 weeks = 300 h/year
- Notional value of one lecturer/student development hour: 10 USD (used for economic valuation)

## 2. Options
| Option | Description | One-off cost | Annual cost | Annual benefit |
|--------|-------------|--------------|-------------|----------------|
| A      | Do nothing  | 0            | 0           | 0              |
| B      | Buy SaaS    | 0 USD        | 1,800 USD   | 3,000 USD      |
| C      | Build       | 4,900 USD    | 300 USD     | 4,800 USD      |

*Note on Option B Pricing:* Based on Kahoot! EDU Standard Higher Education pricing (cited from [Kahoot Pricing Page](https://kahoot.com/upgrade/premiumplus-campus/), accessed October 2026), standard EDU pricing runs at 15 USD per lecturer per month (180 USD/lecturer/year). For 10 lecturers, annual licence cost is 10 * 15 * 12 = 1,800 USD/year.

## 3. Comparison
| Option | Net annual benefit | Payback (years) | Sensitivity (6 lecturers) |
|--------|--------------------|-----------------|---------------------------|
| B      | 3,000 - 1,800 = 1,200 USD | 0.00 (no one-off) | Net Benefit: 1,800 - 1,080 = 720 USD; Payback: 0.00 years |
| C      | 3,000 + 1,800 - 300 = 4,500 USD | 4,900 / 4,500 = 1.09 years | Net Benefit: 1,800 + 1,080 - 300 = 2,580 USD; Payback: 4,900 / 2,580 = 1.90 years |

## 4. Benefits not priced
- **Enhanced Learning Outcomes:** Real-time feedback increases student participation and immediate concept retention.
- **Data Sovereignty & Privacy:** Full on-premise/campus control over student records, performance metrics, and grades without external compliance risks.
- **No Per-Seat Limits:** The custom platform allows scaling to unlimited students and courses without incurring tier upgrades or extra seat charges.
- **Capstone Educational Value:** Students gain practical software engineering, cloud architecture, and project management experience during the development phase.

## 5. Risks per option
### Option A (Do nothing)
- Continued loss of productive instructor time on manual marking.
- Lower student engagement and satisfaction compared to interactive learning standards.

### Option B (Buy SaaS)
- Vendor lock-in and potential subscription price hikes in future billing cycles.
- Privacy and compliance concerns regarding third-party storage of student quiz records.

### Option C (Build Realtime Quiz)
- Schedule delay risking the week 14 pilot deadline.
- Real-time performance and WebSocket latency spikes during high-concurrency live sessions.

## 6. Recommendation and review gate
**Recommendation:** Proceed with **Option C (Build Realtime Quiz)**. Option C provides a net annual benefit of 4,500 USD and achieves full payback within **1.09 years** (and within 1.90 years even under the sensitive scenario of only 6 active lecturers). It secures full data ownership, delivers valuable capstone experience, and avoids recurring per-seat vendor fees.

**Review Gate:** A formal review gate is set at the **week-7 MVP demo**. If the MVP demo in week 7 fails to meet core functional and performance requirements, the department will pivot to **Option B (Buy SaaS)** for the following semester while treating the build project as an extended two-semester initiative.

*(As referenced in `project-charter.md` Section 1).*