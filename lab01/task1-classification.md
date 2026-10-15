# Task 1: project, operation or programme?

| #  | Initiative | Temporary? | Unique? | Coordinated? | Class | Justification |
|----|------------|------------|---------|--------------|-------|---------------|
| 1  | Build the Realtime Quiz platform and pilot it with 50 students in week 14 | yes | yes | no | Project | Has a clear deadline (week 14) and builds a platform that did not exist before. |
| 2  | Run the nightly backup of the gicitc.com PostgreSQL database | no | no | no | Operation | Repeats every night with the same output and no end date; it is part of keeping the service running. |
| 3  | Move the department's three web servers to a new Linode region before 15 December | yes | yes | no | Project | Has a strict deadline (15 December) and results in a one-time relocation configuration. |
| 4  | Answer helpdesk tickets within the 4-hour service level | no | no | no | Operation | Ongoing support activity without a fixed end date, maintaining continuous service levels. |
| 5  | "Digital classroom": Realtime Quiz, LMS upgrade and lecture capture sharing one login and one grade export | yes | yes | yes | Programme | Three related projects; the shared login and grade export are a benefit that none of them delivers alone, so they are coordinated. |
| 6  | Apply the monthly security patches to the VPS | no | no | no | Operation | Recurring monthly maintenance routine performed continuously to keep systems updated. |
| 7  | Add multi-node scaling (RabbitMQ relay, Redis registry) to Realtime Quiz next semester | yes | yes | no | Project | Features a fixed timeframe (next semester) to introduce new architecture features to the system. |
| 8  | Operate the Realtime Quiz platform after go-live: password resets, restarts, monitoring | no | no | no | Operation | Continuous post-launch operational support aimed at maintaining platform availability. |
| 9  | Write and publish the department's annual IT report for the dean by 31 January | yes | yes | no | Project | Has a defined deadline (31 January) and yields a unique report document for that specific year. |
| 10 | Replace 40 wireless access points in two buildings during the summer break | yes | yes | no | Project | Time-bound to the summer break and creates a newly updated infrastructure setup across two buildings. |

## Grey zones
1. **Initiative 7 (Add multi-node scaling next semester):** It could be classified either as an operational maintenance release or as a distinct project. Extra information regarding whether the sponsor funds it as a separate endeavour with its own target end date and budget would settle its classification.
2. **Initiative 9 (Write and publish annual IT report by 31 January):** It is repetitive annually like an operation, yet each report covers unique content and has a strict deadline. Knowing who authorised it, whether a dedicated project budget exists, and how "done" is defined by leadership would clarify if it is managed as a standalone mini-project or standard routine operational duty.

## What our project hands over
At go-live in week 14, the project team hands over day-to-day maintenance to the IT department's operational support staff who will run and monitor the platform. To ensure smooth operation, the support staff need comprehensive deployment documentation, system access privileges, and clear escalation procedures from the project team. Finally, training sessions and user guides for handling common issues like password resets and service restarts must be delivered to the operational team before final sign-off.