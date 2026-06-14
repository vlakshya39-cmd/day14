# day14
# Day 14 — AI Red Flag Detector for Job Seekers 🚩

> Part of my **#Claude60DaysChallenge** — building one small AI-powered project every day using
> Claude.

## 📌 Overview

Today's project is an **AI Red Flag Detector** — a Claude prompt/workflow that analyzes a job
description + company information and produces a structured **risk assessment report** to help
job seekers spot red flags *before* applying or accepting an offer.

The detector checks for:

- ⚠️ Unrealistic requirements (excessive experience, contradictory expectations)
- 🔥 Toxic workplace signals ("wear many hats", "hustle culture", burnout indicators)
- 🏠 Remote job authenticity (hidden office/relocation requirements)
- 📋 Hiring risks (missing salary info, vague responsibilities, suspicious practices)
- 🏢 Company risks (reputation, stability, layoffs/growth signals)

It then outputs an **Overall Risk Score**, a **Top Red Flags** list with severity ratings, a
**Risk Breakdown table**, a **Final Verdict** (✅ / ⚠️ / ❌), and **5 Smart Interview Questions**
tailored to validate the flagged risks.

## 🧪 Test Case

For this run, the detector was tested on a **real job posting** — Infosys' entry-level
*Associate / Software Engineer* role — combined with publicly available company information
about Infosys.

Claude also performed live **web research** to verify recent, time-sensitive company signals
(fresher onboarding timelines, recent layoffs/assessment policies, recognitions/awards) rather
than relying purely on the prompt text.

**Result:** Overall Risk Score **52/100** → **⚠️ Apply with Caution**

## 📂 Repository Structure

```
Day-14-AI-Job-RedFlag-Detector/
├── README.md                     # This file
├── prompts/
│   └── prompt.md                 # The exact prompts used (system + follow-up)
├── analysis/
│   └── job_red_flag_report.md    # Full text/markdown version of the report
├── output/
│   └── Infosys_Associate_SDE_RedFlag_Report.pdf   # Final designed PDF report
└── screenshots/
    ├── 01_overall_risk_score.png
    ├── 02_top_red_flags.png
    ├── 03_positive_signals.png
    ├── 04_risk_breakdown.png
    ├── 05_final_verdict.png
    └── 06_interview_questions.png
```

## 🖼️ Screenshots

**Overall Risk Score**
![Overall Risk Score](./screenshots/01_overall_risk_score.png)

**Top Red Flags**
![Top Red Flags](./screenshots/02_top_red_flags.png)

**Positive Signals**
![Positive Signals](./screenshots/03_positive_signals.png)

**Risk Breakdown**
![Risk Breakdown](./screenshots/04_risk_breakdown.png)

**Final Verdict**
![Final Verdict](./screenshots/05_final_verdict.png)

**5 Smart Interview Questions**
![Interview Questions](./screenshots/06_interview_questions.png)

## 📄 Final PDF Report

A polished, chart-based PDF version of the full report (gauge chart for overall risk score, a
severity bar chart for red flags, and a category risk-breakdown chart) is available here:

➡️ [`output/Infosys_Associate_SDE_RedFlag_Report.pdf`](./output/Infosys_Associate_SDE_RedFlag_Report.pdf)

## 🛠️ Tools Used

- **Claude (Sonnet 4.6)** — analysis, risk scoring, and report writing
- **Web search** — to verify current company-specific facts (recent layoffs, onboarding delays,
  awards/recognitions)
- **Python (matplotlib + reportlab)** — to generate the charts and assemble the final PDF report

## 💡 Key Takeaways

- A job description that looks "clean" on paper can still hide systemic risks that only show up
  when you cross-reference real-world company behavior (e.g., onboarding delays, conditional
  termination after training).
- Structuring the analysis with a numeric score + severity ratings + a risk-breakdown table makes
  it much easier to compare multiple job offers side by side.
- The "Smart Interview Questions" section turns the analysis into something *actionable* —
  candidates can directly probe the exact risks identified during the interview process.

---

⬅️ [Back to main #Claude60DaysChallenge repo](../)
