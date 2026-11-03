# CareLoop
**The AI operations console for sleep clinics and CPAP providers.**

CareLoop shows clinic staff which CPAP patients need attention today, why, and what to do next — and keeps each follow-up open until it is resolved.

Built at **[SOOMi Health](https://soomihealth.care)** by a non-developer founder working with AI coding agents. This repository is an overview; the source code stays private because the product handles patient health data.

---

## The problem

CPAP therapy for sleep apnea works only if patients keep using it, and many quietly stop. In a Korean national claims study of 102,564 adults, only **12.2%** stayed adherent throughout follow-up (Chang et al., *Sleep Medicine*, 2025).

Clinics and CPAP providers usually see the warning signs, but acting on them is manual work: device reports arrive in different formats from each manufacturer, insurance usage requirements must be checked patient by patient, and follow-up calls depend on staff memory. Most dashboards stop at showing the data.

## What CareLoop does

- **Today's priorities** — a work queue of patients who need attention first, with the reason for each one.
- **Risk signals with reasons** — K-Score, a rule-based score recalculated from recent CPAP usage, classifies adherence-risk signals and shows why a patient was flagged. It is a reference for staff, not a prediction or a diagnosis.
- **Insurance usage tracking** — turns usage reports from different device manufacturers into standard daily records and shows whether each patient meets insurance usage requirements.
- **Tasks and handoffs** — assigns a staff member and a deadline, passes context to the next person, and tracks the task until the issue is confirmed resolved.
- **Ask CareLoop** — staff ask questions in plain language (for example, "Who stopped therapy last month?"). Answers are calculated from the clinic's own records and link back to the source screens.
- **Connected to SOOMi** — SOOMi, the patient-facing channel, talks with patients within clinic-approved guidance. When a concern needs a person, it becomes a CareLoop task, and SOOMi checks back after staff act.

## How a clinic uses it

1. **See** — open CareLoop and check who needs attention today and why.
2. **Act** — assign the right staff member with a deadline, or let SOOMi follow up within approved guidance.
3. **Close the loop** — confirm the issue is resolved and keep the outcome in the patient's record for the next visit or handoff.

## Safety by design

- **Rules decide, AI explains, people approve.** Risk levels come from transparent rules; generative AI writes explanations and drafts.
- **Numbers come from records, not from the AI.** In Ask CareLoop, patient names are not sent to the AI model.
- **Clinicians stay in charge.** CareLoop does not diagnose, prescribe, or change treatment. Messages drafted by AI reach patients only after staff approval.

## How I build it

- Solo, non-developer founder, building with AI coding agents (Claude Code and Codex).
- Since February 2026: **4,300+ commits** and **1,500+ merged pull requests** in the private production repository.
- Every change goes through a pull request with automated tests, code scanning, and AI code review. Production releases go out as a canary with automatic rollback.
- Stack: TypeScript · React · Express · PostgreSQL · Google Cloud Run · Gemini

## Status

- Deployed to production. **Currently running with synthetic (fictional) demo data only** — no real clinic deployments yet.
- Next step: a paid pilot with a partner clinic.
- CareLoop is an operations tool, not a medical device. It does not replace clinical judgment.

---

Contact: [soomihealth.care](https://soomihealth.care)
