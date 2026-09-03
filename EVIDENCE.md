Market Labs Provenance Standard — Evidence Classification

File: EVIDENCE.md
Standard: Market Labs Provenance Standard
Version: 0.1.0
Status: Draft Standard

⸻

Purpose

This document defines the evidence classifications used by independent Market Labs projects.

The purpose of these classifications is to distinguish:

* what has been directly verified,
* what is supported by multiple sources,
* what originates with the researcher,
* what is currently a proposal,
* and what has not yet occurred.

These labels describe the status of evidence.

They do not indicate whether an asset, company, market thesis, creator, model, or project is good or bad.

⸻

Core Rule

Every material research claim should be distinguishable from interpretation, proposal, and future expectation.

The standard evidence classes are:

1. VERIFIED
2. CORROBORATED
3. AUTHOR-ORIGINATED
4. PROPOSED
5. FUTURE EXPERIMENT

⸻

1. VERIFIED

Use VERIFIED when the stated fact can be directly supported by a primary source, original record, or directly observable artifact.

Examples may include:

* an official filing,
* an official company publication,
* an authenticated transaction,
* an original timestamped recording,
* an original screenshot with preserved provenance,
* a published repository commit,
* a directly observed market price at a documented time,
* a platform record,
* an official government record,
* an original dataset.

Example

DELL closed at a specified price on a specified date.

If supported by an appropriate market-data source:

Evidence Class: VERIFIED

⸻

2. CORROBORATED

Use CORROBORATED when a claim is supported by multiple credible sources or when a secondary source independently supports a primary observation.

Corroboration strengthens a claim but should not be confused with direct verification.

Examples:

* multiple reputable reports describing the same event,
* historical claims supported by several archival sources,
* independent reporting consistent with an original observation,
* several datasets pointing toward the same factual conclusion.

Example

Multiple historical records independently support the identification of a location or event.

Evidence Class: CORROBORATED

⸻

3. AUTHOR-ORIGINATED

Use AUTHOR-ORIGINATED when the material represents an original interpretation, thesis, framework, hypothesis, terminology, commentary, or conclusion produced by the researcher.

Examples:

* a market thesis,
* an interpretation of price action,
* the Market Labs architecture,
* a newly defined analytical framework,
* an original term,
* an interpretation of historical evidence,
* a qualitative judgment.

Example

The researcher believes DELL is exhibiting a particular market structure before the opening bell.

Evidence Class: AUTHOR-ORIGINATED

This label does not mean the claim is false.

It means the interpretation originates with the author and should not be presented as externally verified fact.

⸻

4. PROPOSED

Use PROPOSED for something that has been designed, recommended, planned, or suggested but has not yet been implemented or established.

Examples:

* proposed Discord architecture,
* proposed token design,
* proposed research methodology,
* proposed partnership,
* proposed product functionality,
* proposed experiment,
* proposed governance mechanism.

Example

XLABS may use a particular future governance structure.

Until implemented:

Evidence Class: PROPOSED

A proposal must never be described as an operational capability merely because it appears in a planning document.

⸻

5. FUTURE EXPERIMENT

Use FUTURE EXPERIMENT when the statement describes an experiment, observation, comparison, or intervention that has not yet occurred.

Examples:

* an upcoming market test,
* a future metadata audit,
* a planned model comparison,
* a scheduled replication,
* a proposed prospective observation.

Example

A future study will compare retrieval performance across alternative metadata architectures.

Before execution:

Evidence Class: FUTURE EXPERIMENT

Once the experiment begins or concludes, its resulting artifacts receive their own evidence classifications.

⸻

Predictions Are Not Outcomes

Market Labs must preserve the distinction between:

what was known before an outcome

and

what became known afterward.

A pre-event thesis remains an AUTHOR-ORIGINATED thesis even if the eventual market movement agrees with it.

The later outcome should be recorded separately as VERIFIED when appropriate evidence exists.

Do not rewrite the earlier record to make a prediction appear more certain after the result is known.

⸻

Models Are Sources of Analysis, Not Automatic Evidence

Outputs from GPT, Claude, Gemini, Grok, Kimi, ENOCH ONE, or another AI system do not automatically become VERIFIED or CORROBORATED because multiple models agree.

Model outputs may be classified as:

AUTHOR-ORIGINATED / MODEL-GENERATED ANALYSIS

or another project-defined subtype.

Agreement among models may be documented as:

MODEL AGREEMENT

but model agreement is not equivalent to independent factual verification.

External claims produced by models should be independently sourced before being labeled VERIFIED.

⸻

Evidence Can Change

Evidence classifications may change when new information becomes available.

Example:

PROPOSED

↓

implementation occurs

↓

VERIFIED

Another example:

AUTHOR-ORIGINATED

↓

independent sources later support the claim

↓

the original interpretation remains AUTHOR-ORIGINATED, while the new supporting evidence may separately be classified as CORROBORATED or VERIFIED.

Do not silently overwrite the historical classification.

Preserve the evolution of the record.

⸻

Minimum Artifact Requirement

Where practical, each substantive Market Labs research artifact should contain:

Evidence Class: [classification]

Evidence Date: [YYYY-MM-DD]

Evidence Source: [source or artifact reference]

Researcher/Node: [originating human or system]

⸻

Governing Principle

Observation is not interpretation.

Interpretation is not verification.

Agreement is not proof.

Proposal is not implementation.

Prediction is not outcome.

Preserve what was known before the outcome.