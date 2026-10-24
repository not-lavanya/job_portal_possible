# Assumptions, Risks & Unknowns (2026-10-22)

## Key Assumptions
1. **Company adoption will happen** — centralized tracker/template requires employer buy-in
2. **Regional clustering works** — students in same geographic area apply to similar firms (e.g., investment banking in Granville/Columbus)
3. **Manual processes are ripe for automation** — companies that can't afford custom ATS rely on manual work

## Risks
1. **Adoption barrier** — biggest risk; companies use own websites/systems, reluctant to integrate with third-party
2. **Seasonal traffic spikes** — internship/job seasons create high-volume tracking burden
3. **Apathy / "not my problem" mindset** — students/developers may not see value in centralized system
4. **API/scraping fragility** — employer portals rarely have public APIs; tracking via scraping breaks often

## Edge-Case Probe Results
- **What if tracker works but AI autofill fails on a custom form?** → Student still wastes time re-entering info; value drops significantly
- **What if tracker is live but recruiters never adopt template?** → Applicant has tracking but no benefit from standardized fields; fragmented experience continues
- **Regional approach** — easier to get initial traction; companies can't afford custom careers pages; students at local schools already have network effects

## Mitigation Ideas
- Start regional: one city/college cluster first
- Build for companies that already use shared ATS (Workday, etc.) as low-hanging fruit
- Offer manual-entry fallback if AI autofill fails