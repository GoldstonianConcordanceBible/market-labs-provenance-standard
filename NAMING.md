Market Labs Provenance Standard — Naming & Entity Resolution

File: NAMING.md
Standard: Market Labs Provenance Standard
Version: 0.1.0
Status: Draft Standard

⸻

Purpose

This document defines how names, aliases, symbols, repositories, research projects, and public-facing identities are represented across independent Market Labs projects.

The goal is consistent entity resolution without forcing every project into one universal public identity.

⸻

Core Principle

One canonical name per entity.

Aliases may exist.

Stylized branding may exist.

Ticker symbols may exist.

But every entity must have one authoritative canonical form for research and provenance purposes.

⸻

1. CANONICAL NAME

Every project or entity must define a:

Canonical Name

This is the authoritative name used in research records, provenance files, registries, and relationship data.

Examples:

DELL Market Lab

XLABS

Market Labs

The canonical name should remain stable unless a documented rename occurs.

⸻

2. DISPLAY NAME

An entity may also have a public-facing display form.

Example:

Canonical Name:

Goldstonian Civil War

Stylized Display Name:

The Goldstonian Civil $War

The display form may contain:

* stylization,
* punctuation,
* symbols,
* capitalization,
* creative branding.

The canonical name should prioritize interoperability and clarity.

⸻

3. SYMBOL OR TICKER

Ticker symbols must be stored separately from entity names.

Example:

Reference Asset: DELL

Laboratory: DELL Market Lab

Companion Symbol: $DLAB

Do not treat:

$DLAB

and:

DELL Market Lab

as interchangeable entities.

A ticker identifies an asset or symbol.

A laboratory identifies a research project.

⸻

4. REFERENCE ASSET VS. LABORATORY

Market Labs must preserve the distinction between the object being studied and the laboratory studying it.

Example:

Reference Asset: SPCX

Laboratory: XLABS

Canonical explanatory language:

SPCX is the reference asset. XLABS is the laboratory.

Likewise:

Reference Asset: DELL

Laboratory: DELL Market Lab

Companion Symbol: $DLAB

These relationships should be explicit rather than inferred from naming similarity.

⸻

5. ALIASES

Aliases exist for legitimate alternate references.

Examples:

Canonical:

ENOCH ONE

Possible alias:

Enoch One

Canonical:

XLABS

Possible explanatory alias:

SpaceX Market Labs

Aliases should be stored in the local project registry.

They should not replace the canonical name unless a formal rename occurs.

⸻

6. DEPRECATED NAMES

When a name is retired, preserve it as:

Deprecated Alias

Do not silently remove the old name from provenance records.

Example:

Canonical Name: [new name]

Deprecated Alias: [old name]

Deprecated Date: [YYYY-MM-DD]

Reason: [documented reason]

This preserves continuity across older videos, commits, posts, and research artifacts.

⸻

7. PROJECT-LOCAL CANON

Each independent Market Lab maintains its own local canonical registry.

Examples:

DELL-CANON.md

XLABS-CANON.md

Future labs should maintain equivalent files.

There is no requirement for one universal registry containing every project, token, book, historical artifact, or community.

⸻

8. FEDERATED NAMING

Shared infrastructure does not create shared public identity.

Two projects may use the same Market Labs Provenance Standard while remaining independently named and independently governed.

Therefore:

shared schema ≠ shared brand

shared evidence standard ≠ shared audience

shared provenance grammar ≠ automatic semantic relationship

Cross-project relationships must be intentionally recorded.

⸻

9. GITHUB REPOSITORY NAMING

Repository names should be descriptive and stable.

Preferred patterns:

DELL-Market-Lab

XLABS-Market-Labs

market-labs-provenance-standard

Avoid repository names that require insider knowledge to understand what the repository contains.

Repository names should not change merely for promotional campaigns.

⸻

10. DISCORD SERVER NAMING

Each Market Lab should maintain its own community identity.

Preferred:

DELL Market Lab

XLABS — SPCX Market Lab

Avoid one universal Discord server that automatically combines unrelated research, theological, historical, educational, market, and tokenized projects.

Cross-community bridges may exist where appropriate.

⸻

11. YOUTUBE AND PUBLIC TITLE RULE

Public-facing titles should normally begin with the subject a new viewer can understand.

Preferred:

DELL Premarket Thesis Before the Open | DELL Market Lab

Rather than:

DLAB-001 PRE-EVENT CONTROL TOWER

Internal identifiers belong in provenance records unless they are themselves useful to the audience.

⸻

12. KNOWN BEFORE UNKNOWN

The default public naming rule is:

Known entity first. Internal ontology second.

Examples:

SPCX Market Analysis | XLABS

DELL Earnings Review | DELL Market Lab

This improves comprehension without abandoning the project identity.

⸻

13. DO NOT FORCE TICKER SYMBOLS INTO EVERY SURFACE

Ticker symbols may be useful for:

* market-specific posts,
* asset references,
* exchange contexts,
* provenance records,
* aliases,
* tags.

They do not need to appear in every:

* repository name,
* title,
* Discord channel,
* educational artifact,
* public description.

Use them where they clarify rather than where they merely decorate.

⸻

14. NO IMPLIED AFFILIATION

Naming must not imply sponsorship, endorsement, partnership, ownership, or official authorization where none exists.

For example, a laboratory studying a company or reference asset must remain distinguishable from the company itself.

Preferred:

DELL Market Lab — Independent Research

Avoid naming that could reasonably be interpreted as an official DELL organization.

The same principle applies to SPCX, SpaceX, NVIDIA, educational institutions, platforms, government agencies, and other third parties.

⸻

15. LOCAL ENTITY RECORD

Each canonical entity should eventually include:

Canonical Name:
Entity Type:
Display Name:
Symbol/Ticker:
Aliases:
Deprecated Aliases:
Parent Namespace:
Reference Asset:
Affiliation Status:
Date Introduced:
Status: ACTIVE / DORMANT / DEPRECATED
Notes:

Not every field applies to every entity.

⸻

16. EXAMPLE — DELL MARKET LAB

Canonical Name: DELL Market Lab

Entity Type: Independent Market Lab

Display Name: DELL Market Lab

Reference Asset: DELL

Companion Symbol: $DLAB

Parent Namespace: Market Labs

Affiliation Status: Independent; no implied official affiliation with Dell Technologies

Status: ACTIVE

⸻

17. EXAMPLE — XLABS

Canonical Name: XLABS

Entity Type: Independent Market Lab

Display Name: XLABS

Reference Asset: SPCX

Explanatory Language: SpaceX Market Labs / SPCX Market Lab, where context requires explanation

Parent Namespace: Market Labs

Affiliation Status: Independent; no implied affiliation with SpaceX or related entities

Status: ACTIVE

⸻

18. NAMING CHANGE CONTROL

A canonical name should change only when there is a documented reason.

Every rename should record:

Old Name

New Name

Effective Date

Reason

Affected Repositories

Affected Communities

Affected Public Records

Migration Notes

Old artifacts should not be rewritten solely to make history appear cleaner.

Preserve what the project was called at the time.

⸻

19. GOVERNING PRINCIPLES

One canonical name per entity.

Ticker is not project.

Reference asset is not laboratory.

Stylized branding is not necessarily canonical naming.

Shared infrastructure does not imply shared identity.

Aliases assist retrieval; they do not replace provenance.

Do not imply affiliation that does not exist.

Preserve historical names when names change.