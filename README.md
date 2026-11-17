# Manual QA Portfolio — MindBridge Education Platform

End-to-end manual testing documentation and defect management deliverables for **MindBridge Education**, an e-learning platform covering course discovery, cart management, checkout, and learner enrollment.

## Deliverables

| Document | Scope & Focus |
| :--- | :--- |
| **[01-Test-Coverage-Document.pdf](01-Test-Coverage-Document.pdf)** | Test coverage plan for the multi-step course & tutor registration flow across QA (`localhost:8081`) and Staging (`localhost:8082`) environments (Functional, Negative, Regression, Usability, Responsive). |
| **[02-Compatibility-Matrix.pdf](02-Compatibility-Matrix.pdf)** | Risk-based browser/OS test matrix targeting 90% of active user traffic (iOS/iPadOS Safari and Windows 11 Chrome/Edge) with exclusion rationale for legacy browsers. |
| **[03-Exploratory-Testing-and-Defect-Reports.pdf](03-Exploratory-Testing-and-Defect-Reports.pdf)** | Time-boxed exploratory testing charter on the checkout flow using heuristics (unexpected characters, rapid clicks, boundary values, browser navigation interruption), Jira bug reports (`MIN-7`, `MIN-8`), and defect recovery analysis. |
| **[04-Bug-Triage-Report.pdf](04-Bug-Triage-Report.pdf)** | Severity vs. Priority evaluation and triage decisions for five release defects (`MB-201` through `MB-205`), separating technical impact from business urgency. |
| **[05-Root-Cause-Analysis-MB-141.pdf](05-Root-Cause-Analysis-MB-141.pdf)** | Post-mortem RCA on a reporting defect with a 14-day MTTR and two "Cannot Reproduce" reopens, introducing a pre-submission Definition of Ready checklist. |

## Key Testing Highlights

* **Exploratory & Negative Testing:** Identified an unhandled `HTTP 500` server error caused by `<` and `>` characters in payment input fields, duplicate order submission risks on rapid button clicks, and state loss on browser back-navigation.
* **Defect Lifecycle & Recovery:** Reworked a rejected/non-reproducible ticket (`MIN-8`) by adding exact preconditions, Chrome DevTools Network logs, deterministic inputs, and environment details.
* **Triage & Process Improvement:** Applied structured Severity vs. Priority classification across UI, functional, and legacy-browser defects, and defined concrete defect-reporting standards to reduce developer bounce rates.

## Tools Used

* **Test & Defect Management:** Jira Cloud
* **Debugging & Inspection:** Chrome DevTools (Network & Console tabs, Mobile Viewport Emulation)
* **Documentation:** Test Plans, Compatibility Matrices, Exploratory Charters, Triage & RCA Reports
