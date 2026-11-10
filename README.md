# Hire FIRST prototype

A working prototype of a skills-based hiring engine, built for IDFC FIRST Bank FAME 6.0 Open Innovation Challenge, Problem Statement 2 (Reimagining Hiring at Scale).

**Live demo:** https://kirtikbiswas.github.io/hire-first-prototype/

## What it shows

- **Candidate view:** a phone-style app beside a live engine trace. A candidate describes her work in Hindi, Hinglish or English. Matching roles re-rank as she types. She applies with a Hindi CV, gets one clarifying question instead of a rejection, and is shortlisted after answering.
- **Recruiter view:** the same application with the evidence line behind each skill score, a comparison with a keyword filter, a four-bucket triage board, and a talent pool of people who applied for other roles.

- **Guided demo:** Play demo runs Asha's whole story on its own, with captions.
- **Presenter mode:** Present runs the same story one step at a time. Press the right arrow, Space, Enter or a clicker to move on; Esc stops.

## How it works

A small skills dictionary in Hindi, Hinglish and English maps phrases to competencies. Each role lists the competencies it needs, with weights. The score is the share of weighted competencies the engine finds evidence for. Candidates are sorted into four buckets: strong match (80% or more), potential match (50 to 79%), uncertain (under 50%), and fails a mandatory criterion. No borderline candidate is rejected without a question.

In production the dictionary would be replaced by a language model trained on the bank's own role competencies. The triage rules stay the same.

## Notes

Student concept by Kirtik Biswas, Sabhya Arora and Abhik Pramanik (IIM Tiruchirappalli). Not an IDFC FIRST Bank system. All people, CVs and roles are samples.

Single static HTML file with no build step. Open `index.html` in a browser, or view the GitHub Pages link above.
