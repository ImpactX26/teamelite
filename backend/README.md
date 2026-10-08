# Production integration contract

The current demo is intentionally runnable as a static HTML prototype. The following server-side services are required to turn the workflow into real automation:

1. **Document agent** — OCR/PDF/DOCX extraction, evidence classification, source citations, consistency checks.
2. **Video agent** — object storage + speech-to-text + transcript analysis for background, motivation and career goals.
3. **Qualification agent** — deterministic eligibility rules plus an agent that requests missing evidence.
4. **Resume agent** — generates a PDF/DOCX resume using only verified/applicant-approved facts.
5. **Company/job discovery** — search approved job/company sources for the applicant's target domain and Germany pathway.
6. **Mail agent** — connected mailbox provider sends approved applications and records message IDs.
7. **Reply agent** — monitors replies, detects interview invitations, extracts date/time/time zone, stores the event, and triggers notifications.
8. **PostgreSQL** — applicant profile, evidence records, verification status, resume versions, outreach records, interview events and audit trail.

Recommended API surface:

- `POST /api/applicants/:id/documents`
- `POST /api/applicants/:id/video`
- `POST /api/applicants/:id/analyze`
- `GET /api/applicants/:id/qualification`
- `POST /api/applicants/:id/resume/generate`
- `GET /api/applicants/:id/companies?domain=...&country=Germany`
- `POST /api/applicants/:id/outreach/approve`
- `GET /api/applicants/:id/interviews`
- `POST /api/webhooks/mail/reply`

Important safety rule: external email sending must require an explicit applicant approval step, and every generated resume fact should retain its source and verification state.
