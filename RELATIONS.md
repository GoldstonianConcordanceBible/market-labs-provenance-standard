Market Labs Provenance Standard — Relationships

File: RELATIONS.md
Standard: Market Labs Provenance Standard
Version: 0.1.0
Status: Draft Standard

⸻

Purpose

This document defines how Market Labs projects and artifacts may be related to one another.

The goal is to preserve useful provenance without automatically merging independent laboratories, audiences, brands, repositories, or communities into one universal semantic graph.

⸻

Core Principle

Shared infrastructure does not create a relationship.

Two projects may use the same provenance standard without being:

* affiliated,
* operationally connected,
* commercially related,
* part of the same experiment,
* part of the same audience,
* or part of the same public knowledge graph.

A relationship must be intentionally created and supported.

⸻

1. RELATIONSHIPS ARE EXPLICIT

Do not infer a relationship merely because two artifacts:

* share an author,
* share a GitHub organization,
* use the same schema,
* use the same evidence classes,
* use the same AI system,
* appear on the same YouTube channel,
* or were created during the same period.

A relationship exists in the provenance layer only when it is explicitly recorded.

⸻

2. ARTIFACT RELATIONSHIPS

The following relationship types are approved for artifacts.

part_of

Use when an artifact is formally part of a defined project, series, study, or experiment.

Example:

Artifact:
XLABS-SPCX-2026-09-03-001
part_of:
XLABS

⸻

references

Use when one artifact cites or discusses another artifact without being derived from it.

Example:

DELL-POSTEVENT-2026-09-03-002
references:
DELL-PREMARKET-2026-09-03-001

⸻

derived_from

Use when an artifact was materially produced from another artifact.

Examples:

* transcript derived from video,
* summary derived from research note,
* chart derived from dataset.

Example:

Artifact:
DELL-2026-09-03-001-TRANSCRIPT
derived_from:
DELL-2026-09-03-001-VIDEO

⸻

continues

Use when an artifact intentionally continues a prior record.

Example:

Artifact:
XLABS-SPCX-2026-09-04-001
continues:
XLABS-SPCX-2026-09-03-001

⸻

reviews

Use when a later artifact evaluates an earlier artifact after additional information becomes available.

Example:

DELL-POSTEVENT-2026-09-03-002
reviews:
DELL-PREMARKET-2026-09-03-001

⸻

supersedes

Use when a newer artifact formally replaces an older operational artifact.

Example:

Standard-v0.2
supersedes:
Standard-v0.1

Superseded artifacts should remain preserved.

⸻

same_experiment_as

Use only when two artifacts genuinely belong to the same defined experiment.

Do not use this relationship merely because they use similar methods.

⸻

supports

Use when an artifact provides evidence supporting a claim or another artifact.

This relationship should identify the supporting evidence rather than imply certainty beyond that evidence.

⸻

contradicts

Use when an artifact materially conflicts with an earlier claim or record.

Preserve contradictions rather than silently resolving them.

⸻

corrects

Use when a later artifact formally corrects a factual or provenance error in an earlier artifact.

⸻

3. PROJECT-LEVEL RELATIONSHIPS

Projects may also have explicit relationships.

Approved initial project relationships:

uses_standard
references_project
replicates_method
shares_methodology
derived_project
independent_of

⸻

4. uses_standard

This is the default relationship between a Market Lab and this repository.

Example:

Project:
XLABS
uses_standard:
Market Labs Provenance Standard

This relationship does NOT imply that XLABS is affiliated with every other project using the standard.

⸻

5. replicates_method

Use when one Market Lab intentionally applies a methodology previously used by another lab.

Example:

Project:
NVDA Market Lab
replicates_method:
DELL Market Lab

This means the methodology was replicated.

It does not mean the projects share:

* assets,
* governance,
* finances,
* audiences,
* Discord servers,
* or token structures.

⸻

6. shares_methodology

Use when two independent projects use the same method without one being a direct replication of the other.

Example:

DELL Market Lab
shares_methodology:
XLABS

Use this sparingly.

Often uses_standard is sufficient.

⸻

7. references_project

Use when one project discusses another project but is not structurally dependent on it.

⸻

8. independent_of

Use when explicit separation is important.

Example:

XLABS
independent_of:
SpaceX

or in human-readable form:

XLABS is an independent research laboratory and is not represented as an official SpaceX project.

This relationship may also be expressed through disclosure rather than machine-style relationship fields.

⸻

9. RELATIONSHIPS THAT MUST NOT BE INFERRED

The following relationships must never be inferred without documented evidence:

partner_of
sponsored_by
endorsed_by
owned_by
operated_by
official_project_of
authorized_by
affiliated_with
invested_in
funded_by
controlled_by

These require actual supporting records.

⸻

10. REFERENCE-ASSET RELATIONSHIP

Market Labs must distinguish:

project relationship

from:

research subject relationship

Example:

Project:
XLABS
studies:
SPCX

This does not mean:

XLABS affiliated_with SpaceX

Likewise:

Project:
DELL Market Lab
studies:
DELL

does not imply official affiliation with Dell Technologies.

⸻

11. APPROVED studies RELATIONSHIP

Use:

studies

when a laboratory systematically analyzes a reference asset, market, company, sector, or phenomenon.

Examples:

DELL Market Lab
studies:
DELL
XLABS
studies:
SPCX

This should be one of the most common Market Labs relationships.

⸻

12. TOKEN RELATIONSHIPS

Tokenized assets require precise relationship language.

Approved examples:

companion_asset_of
created_for_experiment
referenced_by
used_in_experiment

Avoid vague relationships such as:

powers
backs
represents
owns

unless those claims are factually and legally accurate.

⸻

13. COMPANION ASSET

For the DELL structure:

$DLAB
companion_asset_of:
DELL Market Lab

This should not imply ownership of DELL or economic rights in Dell Technologies.

The exact meaning of companion_asset_of should be described in the local project documentation.

⸻

14. XLABS / SPCX RELATIONSHIP

The preferred semantic relationship is:

XLABS
studies:
SPCX

Public explanatory language:

SPCX is the reference asset. XLABS is the laboratory.

Do not use:

XLABS owned_by SpaceX
XLABS official_project_of SpaceX
XLABS affiliated_with SpaceX

unless such a relationship actually exists.

⸻

15. CROSS-LAB BRIDGES

A bridge between two Market Labs must have a defined reason.

Acceptable bridge reasons include:

* methodology replication,
* shared provenance standard,
* comparative research,
* explicit multi-lab experiment,
* shared educational module.

A bridge should not exist simply to create network density.

⸻

16. DISCORD RELATIONSHIPS

Discord servers should remain independently scoped.

Example:

XLABS Discord
represents_community_for:
XLABS
DELL Discord
represents_community_for:
DELL Market Lab

Cross-server channels or announcements may reference another laboratory where relevant.

That does not make the communities one organization.

⸻

17. GITHUB RELATIONSHIPS

Repositories should relate through explicit documentation rather than automatic universal linking.

Example:

XLABS-Market-Labs
uses_standard:
market-labs-provenance-standard

Optional:

replicates_method:
DELL-Market-Lab

Only add that second relationship if the XLABS implementation genuinely replicates the DELL methodology.

⸻

18. YOUTUBE RELATIONSHIPS

YouTube videos may belong to more than one playlist where the relationship is genuine.

However:

* one shared creator,
* one shared YouTube channel,
* or one shared production system

does not automatically make the videos part of one canonical research series.

Use playlists intentionally.

⸻

19. FEDERATED NAMESPACE RULE

The standard adopts a federated architecture.

Each project may maintain:

* its own CANON,
* its own repository,
* its own Discord,
* its own artifact registry,
* its own disclosures.

Projects share a provenance grammar without surrendering local identity.

⸻

20. PUBLIC GRAPH VS. PRIVATE RECORD

A relationship may exist in internal provenance without needing to become a prominent public cross-link.

For each relationship, consider:

Public Visibility:
PUBLIC / INTERNAL / RESTRICTED

Example:

A methodological relationship between two projects may be useful in GitHub provenance but unnecessary in a public YouTube description.

⸻

21. RELATIONSHIP RECORD TEMPLATE

Use:

Source Entity:
Relationship:
Target Entity:
Evidence Class:
Source:
Date Recorded:
Public Visibility:
Notes:

⸻

22. EXAMPLE — DELL TO STANDARD

Source Entity:
DELL Market Lab
Relationship:
uses_standard
Target Entity:
Market Labs Provenance Standard
Evidence Class:
VERIFIED
Source:
DELL Market Lab repository
Public Visibility:
PUBLIC

⸻

23. EXAMPLE — XLABS TO SPCX

Source Entity:
XLABS
Relationship:
studies
Target Entity:
SPCX
Evidence Class:
AUTHOR-ORIGINATED
Source:
XLABS project documentation
Public Visibility:
PUBLIC
Notes:
SPCX is the reference asset. XLABS is the independent laboratory.

⸻

24. EXAMPLE — XLABS TO DELL MARKET LAB

Only if methodology is intentionally replicated:

Source Entity:
XLABS
Relationship:
replicates_method
Target Entity:
DELL Market Lab
Evidence Class:
VERIFIED
Source:
Market Labs implementation record
Public Visibility:
PUBLIC

If no replication has occurred yet:

Do not create the relationship.

⸻

25. DO NOT BUILD RELATIONSHIPS FOR SEO

The provenance graph is not a keyword-linking strategy.

Do not create relationships merely to:

* increase search visibility,
* make projects appear larger,
* manufacture authority,
* imply ecosystem scale,
* or associate a project with a better-known company.

The graph should describe reality.

⸻

26. RELATIONSHIPS MAY CHANGE

Relationships may:

* become active,
* expire,
* be corrected,
* be superseded,
* or be reclassified.

Preserve historical relationship records where they materially affect interpretation.

⸻

27. MINIMUM GOVERNANCE RULE

Before creating a cross-project relationship, ask:

1. Is the relationship real?
2. Can it be described precisely?
3. Is there supporting evidence?
4. Does the relationship need to be public?
5. Could the wording imply more than actually exists?

If any answer is uncertain, do not create the public relationship yet.

⸻

28. GOVERNING PRINCIPLES

Relationships are explicit, not assumed.

Shared standard does not mean shared identity.

Studying an asset does not create affiliation with its issuer.

One author does not make every project one ecosystem.

Replicated methodology is not shared ownership.

Public links should be intentional.

Do not manufacture authority through graph density.

The graph describes reality; it does not create reality.