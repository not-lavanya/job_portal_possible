# PRD: Job Application Centralization Platform

Team: Group 13 | Date: 2026-10-22 | Status: Living draft

One-liner: We help college students avoid retyping information and get clearer feedback on job applications, so they can focus on tailoring their strongest applications.

## Problem

College students struggle to complete job and internship applications efficiently and accurately because the major application platforms are built around the employer's hiring workflow, not the applicant's experience. Each employer runs its own form, account, and wording, and none of the existing platforms fully solves reuse, clarity, or feedback. Applicants retype the same information, guess at vague instructions and rarely learn their status or why they were rejected, which leads to wasted time, avoidable rejections, uncertainty, and frustration.

## Target user

College students applying to jobs and internships, especially those applying to multiple roles in a short timeframe (e.g., internship season, job hunts) **and small-regional-area recruiters/firm managers lacking HR resources**

## What we learned from research

**Key findings from Monday\'s session:**
- Separate accounts and forms per employer (Workday, Greenhouse, Lever, etc.)
- Resume parsing that doesn\'t remove retyping (Workday/iCIMS scramble fields)
- Reuse tools that stop at employer\'s form (LinkedIn Easy Apply redirects to ATS)
- Vague fields with no explanation (resume format, portfolio links, experience questions)
- No sense of application time (surprise essay questions on final pages)
- Unrealistic or unclear requirements (years of experience, unclear tools)
- Almost no visibility into status or competition (only "Applied" messages)
- Rejections with no reason (generic emails)

**Source:** [research/user-interviews/2026-10-21-interview-notes.md](research/user-interviews/2026-10-21-interview-notes.md)

## Product goals

- Reduce application completion time by 50% for students applying to 3+ roles
- Eliminate retyping of same information across multiple employer applications
- Increase feedback visibility: 80% of applicants should know status within 48 hours
- Reduce rejections caused by vague requirements by 30%
- Achieve company adoption for at least 50% of regional employers in target market

**Source:** [research/2026-10-22-product-goals.md](research/2026-10-22-product-goals.md)

## Solutions we considered

1. **Centralized application profile + autofill** — Students fill once, reuse across all platforms; works on existing forms without company buy-in. Tradeoff: Limited to standard fields, custom questions still require manual entry.

2. **Centralized tracker + calendar + AI agent** — One dashboard tracking status across all employer portals, prevents interview conflicts. Tradeoff: Requires API access to many employer systems; scraping is fragile.

3. **Two-system architecture (applicants vs recruiters)** — Applicants get unified experience; recruiters get standardized templates and feedback. Tradeoff: Complex coordination between two sides; adoption hardest for recruiter side.

**Source:** [research/2026-10-22-solutions-brainstorm.md](research/2026-10-22-solutions-brainstorm.md)

## Proposed solution

Two-sided platform:

**System A — For Applicants:**
- Centralized application tracker showing status across all employer portals
- Single application profile that auto-fills where possible (enhanced resume parsing)
- AI agent assistant that navigates and fills existing forms, estimates completion time
- Interview calendar with conflict detection and automated scheduling

**System B — For Recruiters:**
- Standardized application template system (shared across companies in region)
- Rejection reason dropdown + feedback collection
- Applicant matching and ranking engine

**Regional approach:** Start with one geographic area (e.g., Granville/Columbus, Ohio) focusing on investment firms and local colleges.

## User stories

- As a recruiter in a small regional area, I want a centralized platform to reduce my dependencies and automate work, so that I don't need HR resources to track a lot of applicants.
- As a firm manager in a small regional area, I want the platform to match the best students to my roles, so that I can find top applicants without manual screening.
- As a job applicant, I want the system to be more structural, so that I don't have to re-enter the same information for every employer.
- As a job applicant, I want the process to be less time-consuming and less tedious, so that I can spend my time on tailoring my strongest applications instead of filling forms.
- As a job applicant, I want to be able to track my applications and get the most out of this seasonal probe, so that I know where I stand and can plan interviews without conflicts.

**Source:** [research/2026-10-22-user-stories.md](research/2026-10-22-user-stories.md)

## Potential features

**For Applicants:**
- Centralized application profile (one entry, reused everywhere)
- AI-powered form auto-filling/navigator
- Multi-portal status tracker with real-time updates
- Interview calendar with conflict detection
- Time-to-complete estimator for each application
- Rejection feedback categorization + improvement suggestions
- Regional focus clustering (geographic application groups)

**For Recruiters:**
- Centralized application management dashboard
- Standardized application template system
- Automated applicant matching and ranking
- Rejection reason collection and analysis
- Regional recruiter collaboration tools

## Key assumptions and risks

- **Company adoption will happen** — centralized tracker/template requires employer buy-in
- **Regional clustering works** — students in same geographic area apply to similar firms
- **Manual processes are ripe for automation** — companies that can't afford custom ATS rely on manual work
- **Adoption barrier** — biggest risk; companies use own websites/systems, reluctant to integrate with third-party
- **Seasonal traffic spikes** — internship/job seasons create high-volume tracking burden
- **Apathy** — students/developers may not see value in centralized system
- **API/scraping fragility** — employer portals rarely have public APIs; tracking via scraping breaks often

**Source:** [research/2026-10-22-assumptions-risks.md](research/2026-10-22-assumptions-risks.md)

## Out of scope

- Building custom employer ATS systems for each company
- Full automation of custom essay questions (AI drafting remains against platform policies)
- National scale rollout in initial phase
- Consumer-facing mobile apps (web-first approach)
- Enterprise-grade security compliance beyond basic privacy standards

## Open questions

- How do we fund company adoption for the recruiter side? (paid tiers, college partnerships?)
- What technical approach for tracking status across employer portals (APIs vs scraping vs user reporting)?
- How do we handle the seasonal spikes in application volume without performance degradation?
- What incentives do companies need to adopt the centralized template system?
- How do we validate that the regional approach actually increases adoption?
- What data do we need from companies to build effective matching algorithms?

## Research to do

- Interview 10-15 actual college students applying to internships/jobs to validate pain points
- Interview 5-10 recruiters/HR managers in regional target market to assess template adoption willingness
- Survey current application platforms usage patterns and time costs
- Technical feasibility study: map employer portal integration options for target region

**Source:** [sessions/session-log.md](sessions/session-log.md)