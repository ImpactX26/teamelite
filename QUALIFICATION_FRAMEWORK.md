# EduGuide AI — Qualification Framework

## Purpose

The qualification stage is an evidence-based pre-screening workflow. It is not a visa, legal, admission, recognition, or hiring decision.

The framework follows the Educaro problem statement requirements to:
- assess the applicant against predefined qualification / eligibility requirements;
- identify missing, incomplete, or inconsistent information;
- provide a clear qualification outcome and outstanding requirements;
- recommend the appropriate next step;
- distinguish verified, applicant-provided, and AI-generated information.

## Applicant evidence model

### Core evidence
- Education: degree / diploma, transcript / mark sheets
- Employment: experience letters and date evidence
- Languages: German / English / other language certificates
- Profile: existing CV
- Media: short introduction video / transcript

### Additional evidence
- Extra courses / further training
- Internships and internship letters
- Professional certifications and certificates
- Academic / personal / client projects and portfolio links
- Awards / hackathons / achievements
- Volunteering / leadership
- Publications / recommendations / other supporting evidence

Extra evidence strengthens profile-to-role alignment and the resume, but cannot override a mandatory pathway requirement.

## Evidence states

- **Verified** — supported by a source that has been reviewed / confirmed.
- **Applicant-provided** — claimed by the applicant but not yet verified against a source.
- **AI-generated** — a summary or inference, never treated as proof.
- **Conflict** — sources disagree; the applicant must clarify.
- **Missing** — required evidence has not been provided.

## Pathway rules used in the prototype

### Study
The prototype expects:
1. Evidence of a university entrance qualification / configured admission route.
2. Programme / subject fit and programme language captured.
3. Required education documents available.

Official German guidance says applicants for study need a university entrance qualification; admission and language requirements depend on the intended programme. Source: Make it in Germany — Requirements for studying.

### Vocational training
The prototype expects:
1. Education / school-leaving evidence.
2. German language evidence at B1 for the configured visa-readiness gate.
3. A defined target vocational training profession / route.
4. Consistent education / employment / internship dates.

Official German guidance states that for third-country vocational training visa purposes, German is usually required at B1; school-based training can additionally require recognition of the school-leaving certificate. Source: Make it in Germany — FAQ / vocational-training guidance.

### Employment
The prototype expects:
1. A primary qualification relevant to the target occupation.
2. Role alignment using education, experience, skills and supporting evidence.
3. The relevant recognition / comparability route to be addressed where applicable.
4. Relevant experience evidence and consistent dates.
5. The language requirement for the target occupation to be checked and documented as required / not required.

Official German guidance states that recognition requirements depend on the profession and purpose of stay. Regulated professions generally require recognition and, where applicable, professional authorisation; non-regulated routes can require proof of comparability depending on the work / visa route. Sources: Make it in Germany — Who needs recognition? / Academic qualifications / Recognition procedure.

## Qualification outcomes

- **PASSED** — all configured hard gates pass with sufficient evidence.
- **CONDITIONALLY READY / NEEDS EVIDENCE** — the applicant is close but one or more gates require evidence or confirmation.
- **BLOCKED** — mandatory evidence or pathway checks are incomplete / unresolved.

The workflow never sends an applicant directly from an unresolved qualification to resume or employer outreach.

## Recovery recommendations

- Missing B1 for vocational training → recommend language preparation / evidence verification.
- Missing programme-fit check for study → complete admission / programme check.
- Missing recognition / comparability route for employment → complete the applicable recognition or comparability assessment.
- Unclear dates → reconcile CV, employment letters and internship letters.

## Resume safety

Only supported facts are placed in the verified resume. Extra courses, internships, projects, certifications and achievements appear in separate evidence sections with source labels.

## Prototype limitation

The supplied website is a front-end prototype. Real PDF OCR, speech-to-text, document classification, recognition lookups, company discovery, email sending, and inbox monitoring require backend services and authenticated integrations. The UI simulates those steps for the hackathon demonstration.
