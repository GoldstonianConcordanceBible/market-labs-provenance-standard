Market Labs Provenance Standard — Artifact Schema

File: SCHEMA.md
Standard: Market Labs Provenance Standard
Version: 0.1.0
Status: Draft Standard

⸻

Purpose

This document defines the minimum provenance record used across independent Market Labs projects.

The schema is designed to answer five basic questions:

1. What is this artifact?
2. Who or what created it?
3. When did it exist?
4. What evidence status does it carry?
5. What project does it belong to?

The schema should remain simple enough to use consistently.

Projects may extend it locally, but they should not remove required fields without documenting why.

⸻

Core Principle

Every important claim should be traceable to an artifact.

Every important artifact should be traceable to a time, source, project, and evidence class.

⸻

1. REQUIRED CORE FIELDS

Every substantive Market Labs artifact should contain the following fields where technically possible.

Artifact ID:
Canonical Title:
Artifact Type:
Project:
Namespace:
Created Date:
Published Date:
Evidence Class:
Originator:
Source Location:
Status:

⸻

2. ARTIFACT ID

Each artifact receives a stable identifier.

Recommended pattern:

[PROJECT]-[YYYY-MM-DD]-[NNN]

Examples:

DELL-2026-09-03-001
XLABS-2026-09-03-001

For projects requiring additional specificity:

[PROJECT]-[ENTITY]-[YYYY-MM-DD]-[NNN]

Example:

DELL-PREMARKET-2026-09-03-001

Artifact IDs should:

* remain stable,
* avoid spaces,
* avoid dollar signs,
* avoid decorative punctuation,
* avoid changing when a public title changes.

⸻

3. CANONICAL TITLE

The Canonical Title identifies the artifact in the provenance record.

Example:

DELL Premarket Thesis Before the Open — September 3, 2026

The canonical title may differ from:

* a YouTube title,
* a Discord post title,
* a thumbnail,
* a social-media headline.

Public packaging can change.

The canonical artifact identity should remain stable.

⸻

4. ARTIFACT TYPE

Each artifact should have one primary type.

Initial controlled vocabulary:

MARKET THESIS
PRE-EVENT RECORD
POST-EVENT REVIEW
CONTROL TOWER
MODEL ANALYSIS
MULTI-MODEL REVIEW
EXPERIMENT LOG
DATASET
TRANSCRIPT
VIDEO
LIVESTREAM
DOCUMENT
SCREENSHOT
TRADE RECORD
RESEARCH NOTE
DISCLOSURE
GOVERNANCE RECORD

Projects may extend this vocabulary through documented local standards.

Avoid inventing a new Artifact Type when an existing type adequately describes the record.

⸻

5. PROJECT

The Project field identifies the local laboratory or project responsible for the artifact.

Examples:

DELL Market Lab
XLABS

The Project is not necessarily the same thing as the reference asset.

Example:

Project: XLABS
Reference Asset: SPCX

⸻

6. NAMESPACE

The Namespace identifies the broader domain in which the artifact belongs.

For the present standard:

MARKET LABS

Future standards may support additional namespaces, but independent projects should not be automatically merged merely because they use the same provenance framework.

⸻

7. CREATED DATE

The Created Date records when the artifact first existed.

Preferred format:

YYYY-MM-DD

Where time matters:

YYYY-MM-DDTHH:MM:SSZ

or another documented timezone-aware timestamp.

For market records, the timezone should be explicit.

Example:

2026-09-03T08:40:00-04:00

Do not rely on words such as:

today
this morning
before open
yesterday

without preserving an absolute timestamp elsewhere.

⸻

8. PUBLISHED DATE

The Published Date records when the artifact became publicly accessible.

Created Date and Published Date may differ.

Example:

Created Date: 2026-09-03T08:40:00-04:00
Published Date: 2026-09-03T10:12:00-04:00

This distinction matters for pre-event research.

A thesis recorded before an outcome but uploaded afterward should preserve both timestamps.

⸻

9. EVIDENCE CLASS

Use the classifications defined in EVIDENCE.md.

Allowed core values:

VERIFIED
CORROBORATED
AUTHOR-ORIGINATED
PROPOSED
FUTURE EXPERIMENT

Where an artifact contains multiple claims with different evidence classes, classify individual claims where practical rather than assigning one misleading label to the entire document.

⸻

10. ORIGINATOR

The Originator identifies the human or system responsible for producing the artifact.

Examples:

Justin Lee Goldston
ENOCH ONE
Grok
Claude
Gemini
Kimi

If AI materially contributed:

Human Reviewer:
Model:
Model Role:

may also be recorded.

Model output should not automatically be treated as independently verified evidence.

⸻

11. SOURCE LOCATION

The Source Location identifies where the authoritative copy resides.

Examples:

GitHub repository path
YouTube URL
dataset DOI
local archival path
published webpage
platform transaction record

When multiple copies exist, designate one as:

Canonical Source

and list others as mirrors or derivatives.

⸻

12. STATUS

Initial controlled values:

DRAFT
ACTIVE
FROZEN
SUPERSEDED
RETRACTED
ARCHIVED

Definitions:

DRAFT

Still being edited.

ACTIVE

Current operational artifact.

FROZEN

Preserved as a historical record and not altered except for documented corrections.

SUPERSEDED

Replaced by a newer artifact.

RETRACTED

Withdrawn because of a material error, compliance problem, or other documented reason.

ARCHIVED

Retained primarily for historical reference.

⸻

13. RECOMMENDED MARKET FIELDS

Market-related artifacts should additionally include:

Reference Asset:
Market:
Stage:
Position Status:
Instrument:
Time Horizon:
Thesis:
Invalidation:
Risk Statement:
Outcome Known At Creation:

⸻

14. STAGE

Recommended values:

PRE-EVENT
LIVE
POST-EVENT
RETROSPECTIVE

These stages describe chronology.

They do not indicate certainty or performance.

⸻

15. OUTCOME KNOWN AT CREATION

This is a critical provenance field.

Allowed values:

YES
NO
PARTIAL

Example:

Outcome Known At Creation: NO

This helps distinguish:

* genuine pre-outcome analysis,
* live observation,
* retrospective commentary.

Do not revise this field after the fact.

⸻

16. THESIS

Where applicable, summarize the analytical proposition as it existed at creation.

Example:

Thesis:
DELL is being monitored for a potential long setup based on the documented premarket conditions.

Avoid rewriting the thesis after the outcome becomes known.

⸻

17. INVALIDATION

Where appropriate, document what would have caused the thesis to be reconsidered.

Example:

Invalidation:
Breakdown below the predefined technical level or emergence of contradictory market evidence.

The purpose is provenance, not trading instruction.

⸻

18. RESULT / OUTCOME

A later result should be added as a linked artifact where possible rather than silently rewriting the original pre-event artifact.

Example:

Original:
DELL-PREMARKET-2026-09-03-001
Reviewed By:
DELL-POSTEVENT-2026-09-03-002

This preserves chronology.

⸻

19. OPTIONAL RELATIONSHIP FIELDS

Artifacts may include:

Part Of:
References:
Derived From:
Continues:
Reviewed By:
Supersedes:
Related Artifact:
Same Experiment As:

Relationship definitions are governed by RELATIONS.md.

Do not create a relationship merely because two artifacts share an author.

⸻

20. DISCLOSURE FIELDS

Where applicable:

Independent Research:
Affiliation Disclosure:
Creator Position:
Creator Economic Interest:
Affiliate Economic Interest:
Sponsorship:
Referral Relationship:
Acquisition Link Present:
Educational / Research Purpose:

Detailed disclosure requirements are governed by DISCLOSURES.md.

⸻

21. FILE NAMING

Where practical, use the Artifact ID as the filename base.

Example:

DELL-2026-09-03-001.md
DELL-2026-09-03-001.pdf
DELL-2026-09-03-001.vtt
DELL-2026-09-03-001.png

This allows related files to remain grouped even when their public titles differ.

⸻

22. MINIMUM RECORD TEMPLATE

Projects may copy this template:

Artifact ID:
Canonical Title:
Artifact Type:
Project:
Namespace:
Created Date:
Published Date:
Evidence Class:
Originator:
Canonical Source:
Status:
Reference Asset:
Stage:
Outcome Known At Creation:
Summary:
Sources:
Relationships:
Disclosures:
Revision History:

⸻

23. REVISION HISTORY

Every material correction should preserve:

Revision Date:
Changed By:
Change:
Reason:

Do not silently edit historical records when the correction affects interpretation or chronology.

For trivial formatting changes, a full revision record is optional.

⸻

24. EXAMPLE — DELL PRE-EVENT ARTIFACT

Artifact ID:
DELL-PREMARKET-2026-09-03-001
Canonical Title:
DELL Premarket Thesis Before the Open — September 3, 2026
Artifact Type:
PRE-EVENT RECORD
Project:
DELL Market Lab
Namespace:
MARKET LABS
Created Date:
2026-09-03T08:40:00-04:00
Evidence Class:
AUTHOR-ORIGINATED
Originator:
Justin Lee Goldston
Reference Asset:
DELL
Stage:
PRE-EVENT
Outcome Known At Creation:
NO
Status:
FROZEN

The eventual market result belongs in a separate post-event artifact.

⸻

25. EXAMPLE — XLABS ARTIFACT

Artifact ID:
XLABS-SPCX-2026-09-03-001
Canonical Title:
SPCX Market Observation — September 3, 2026
Artifact Type:
MARKET THESIS
Project:
XLABS
Namespace:
MARKET LABS
Reference Asset:
SPCX
Evidence Class:
AUTHOR-ORIGINATED
Originator:
Justin Lee Goldston
Outcome Known At Creation:
NO
Status:
FROZEN
Affiliation Disclosure:
Independent research. No implied affiliation with SpaceX or related entities.

⸻

26. WHAT THIS SCHEMA DOES NOT DO

This schema does not:

* certify that a claim is true,
* establish regulatory status,
* prove model independence,
* prove predictive skill,
* establish affiliation,
* combine independent laboratories,
* turn GitHub records into financial advice,
* make every artifact part of one public knowledge graph.

It establishes provenance and recordkeeping.

⸻

27. GOVERNING PRINCIPLES

Stable ID.

Absolute timestamp.

Evidence class.

Known-before-outcome preserved.

Public packaging may change; provenance should not.

Do not rewrite predictions after results are known.

Link the later outcome to the earlier record.

Shared schema does not create shared identity.