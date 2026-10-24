# Solutions Brainstorm (2026-10-22)

## Architecture Decision: Two Systems

The team decided on a two-sided architecture:

### System A — For Applicants
Centralized tracker + calendar + AI agent assistant + enhanced autofill from resume/profile

### System B — For Recruiters
Centralized template system + rejection feedback (future events eliminated)

## Why This Architecture
The core problem is structural: how portals are designed and how the process is facilitated online. Splitting into two systems addresses this at both ends — applicants get a unified experience, recruiters get a standardized template.

## Hard Parts Identified by Team
1. Designing the centralized system
2. Getting the top companies on board
3. Actively tracking so many companies correctly
4. Anomaly detection
5. Handling the responsibilities of so many applications and the emotions involved in the process