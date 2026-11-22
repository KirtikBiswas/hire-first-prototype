# Hire FIRST prototype

An interactive student concept for IDFC FIRST Bank FAME 6.0, Problem Statement 2: **Reimagining Hiring at Scale**.

**Live demo:** https://kirtikbiswas.github.io/hire-first-prototype/

## What the prototype demonstrates

### Candidate experience
- Describe work experience in Hindi, Hinglish or English and see a rule-based skill trace.
- Discover sample roles through transferable competency signals rather than exact job-title phrases.
- Apply with a pasted CV or upload a plain-text `.txt` CV (up to 500 KB).
- Use browser/device speech recognition for dictation where supported. Available language choices include Hindi, English (India), Bengali, Tamil and Marathi; actual availability depends on the browser and device.
- Explicitly opt in or out of future-opportunity matching. Candidates can withdraw consent later.
- Track clarification requests, recruiter decisions, interview scheduling, sample offer acceptance and preboarding.

### Recruiter experience
- Review candidates across four buckets: Strong, Potential, Uncertain and Fails mandatory criterion.
- Inspect supporting evidence, negative statements and contradictory statements for each competency.
- Shortlist, request clarification, reject with a reason, schedule an illustrative interview, issue a sample offer, start preboarding and confirm joining.
- See candidate status updates reflected in the candidate tracker during the same browser session.
- Rediscover only profiles that have explicitly opted in and match the current role.
- Explore sample source mix, triage counts and offer-to-joining counts.
- View a role-relevant six-archetype sourcing playbook.
- Ask the rule-based recruiter copilot questions about the loaded sample records.

### Simulation Lab
- Test transferable insurance/FMCG sales experience.
- Test negative and contradictory statements.
- Test missing and failed mandatory qualification cases.
- Inspect score, bucket, evidence and the reason for the result.
- Load a selected scenario into the candidate journey.

### Guided presentation
- **Present** runs the nine-step Asha story one step at a time, from her Hindi description to the recruiter's shortlist and her updated tracker. Press the right arrow, Space, Enter or a clicker to advance; Esc stops.
- **Play demo** runs the same story automatically with captions in about a minute.
- During either mode the page hides the intro banner, scrolls to each step and highlights what to look at, so it works on a laptop screen shared over a video call.

## How the screening logic works

A small phrase dictionary in Hindi, Hinglish and English maps candidate statements to nine sample competencies. Each role has weighted competencies. The score is the share of weighted competencies with unambiguous positive evidence.

- Strong match: 80% or more, subject to mandatory criteria.
- Potential match: 50-79%.
- Uncertain: below 50%, mandatory information not stated, or contradictory competency evidence.
- Fails mandatory criterion: a sample mandatory criterion is explicitly not met.

Negative statements do not earn competency credit. When the prototype detects both positive and negative statements for the same competency, it flags a conflict and routes the profile to Uncertain. Clarification answers are checked for evidence relevant to the question before they are added to the sample profile.

**The percentage is a weighted evidence score, not a probability of job success. Strong match is a recommendation for recruiter review, not an automatic shortlist. Recruiters remain responsible for hiring decisions.**

## Important prototype limitations

- This is a front-end prototype using in-memory sample data. A page refresh resets interactions. It does not connect to IDFC FIRST Bank systems or any ATS.
- The screening mechanism is a deterministic phrase dictionary and rule-based negation/conflict heuristic, not a trained AI/LLM. It can miss context, sarcasm, complex negation and language variations. Human review is required.
- Only plain-text `.txt` CV upload is parsed in this version. PDF/DOC/DOCX extraction needs a document-processing service.
- Speech recognition is provided by the browser/device and may use an external speech service according to its privacy settings. Hire FIRST does not store audio or send it to a Hire FIRST backend.
- Consent, application status, sourcing, analytics and copilot outputs are local demo interactions, not persisted production records.
- Analytics are calculated from sample candidates. They are not bank performance data or validated business outcomes.
- Interview dates, offers and preboarding are illustrative workflow simulations, not real appointments or employment offers.
- Any production use would require ATS integration, secure backend storage, DPDP and legal review, role validation, bias/adverse-impact testing, security controls and a monitored pilot.

## Run locally

Open `index.html` in a modern browser. There is no build step or package manager.

## Team

Student concept by Kirtik Biswas, Sabhya Arora and Abhik Pramanik, IIM Tiruchirappalli. Not an IDFC FIRST Bank system. All people, CVs, roles and workflow events are sample data.
