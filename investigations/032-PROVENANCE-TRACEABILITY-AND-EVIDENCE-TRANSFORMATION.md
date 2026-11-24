# Investigation 032 — Provenance, Traceability, and the Difference Between Received Evidence and a Derived Account

**Primary disciplines:** Data provenance, research reproducibility, information management, digital forensics, AI documentation, data lineage, scientific measurement, and epistemology of evidence.

**Investigation status:** Initial evidence-led investigation and Four-Question Study Method review recorded.

**Central question:** Can a Witness trace a claim back through the transformations to the evidence from which it was derived, and identify where information was added, removed, altered, interpreted, or lost?

## 1. Why this investigation follows 031

Investigation 031 examined uncertainty, calibration, and abstention. Investigation 032 examines the history of the evidence itself. A Witness may honestly report uncertainty and still inherit an error from an earlier summary, copied dataset, altered record, or misinterpreted source.

The sequence is cumulative:
- 028 — Are evidence streams independent, or do they share dependencies?
- 029 — Was evaluation independent of model development?
- 030 — Do changed environments limit prior validation?
- 031 — Is confidence calibrated and is abstention appropriate?
- 032 — What was received, where did it originate, and what transformations occurred?

## 2. Scientific terminology

**Provenance** is information about entities, activities, and agents involved in producing, influencing, or delivering an artifact. The W3C PROV Data Model formalizes these concepts in a domain-agnostic framework. Its core vocabulary includes entities, activities, agents, usage, generation, derivation, attribution, and responsibility.

**Lineage** emphasizes the ordered succession of sources, versions, and processing steps through which data or an artifact developed. Usage varies across fields; this investigation uses lineage for the derivation path and provenance for the broader record of origin and history.

**Traceability** is the practical ability to follow a claim or artifact through identified sources and transformations. It may be partial.

**Metadata** describes an entity. Some metadata records provenance; not all metadata does.

The W3C model is a vocabulary and conceptual structure, not a guarantee that a recorded history is true or complete.

## 3. Why provenance matters

Provenance can help investigators identify:
- the original source and its version;
- the person, organization, instrument, or software associated with an activity;
- the steps that transformed or derived an artifact;
- the dependencies shared by apparently separate sources;
- the location where a discrepancy may have entered;
- the basis needed to reproduce or audit a result;
- and the downstream claims that may need correction.

Provenance does not independently establish truth, completeness, honesty, quality, independence, or scientific validity. A perfectly documented chain can record a flawed experiment or an invalid inference. An authentic source can be mistaken.

## 4. The transformation chain

A conceptual information path is:

\[
\text{Observation}\rightarrow\text{Record}\rightarrow\text{Processing}
\rightarrow\text{Interpretation}\rightarrow\text{Summary}\rightarrow\text{Claim}
\]

This is not a universal sequence. Real workflows branch, merge, revisit earlier steps, and use multiple sources.

At each transition, ask what was preserved, changed, omitted, added, or made uncertain.

### 4.1 Observation to record

Record the measurand, units, instrument or observer, protocol, timestamp, calibration context, sample identity, and relevant uncertainty when available. If context is lost, a later reader may not know what the number represents.

### 4.2 Record to processed data

Filtering, normalization, conversion, cleaning, interpolation, coding, and aggregation can alter the data. Record the operation, criteria, parameters, software, and version. “Cleaned data” alone does not describe what happened.

### 4.3 Processed data to interpretation

Model choice, assumptions, thresholds, causal reasoning, and explanatory language introduce interpretation. Do not present interpretation as raw observation.

### 4.4 Interpretation to summary

Summaries compress. They can omit caveats, disagreements, uncertainty, context, and exceptions. A summary is a derived artifact, not the original source.

### 4.5 Summary to claim

A final claim may be narrower or stronger than its source. Check whether the source actually supports the exact wording, whether it is quotation, paraphrase, inference, or interpretation, and whether qualifications survived.

## 5. Transformations that require a record

| Transformation | Possible change | Useful trace record |
|---|---|---|
| Copying | Version or context detached | Source identifier, version, copy time |
| Format conversion | Precision, fields, encoding, structure | Input/output formats, converter and settings |
| Filtering | Records excluded | Criteria, counts, exclusions |
| Aggregation | Variation compressed | Formula, weighting, grouping |
| Translation | Nuance or ambiguity changed | Source language, translator, version |
| Annotation | Labels or interpretation added | Annotator, scheme, instructions |
| Summarization | Detail and caveats omitted | Source locations and summary scope |
| Model synthesis | Multiple sources and generated text combined | Available inputs, model/version, prompt or procedure, verification |
| Revision | Content changed | Version history and change description |

Transformations are not necessarily errors. The requirement is to disclose material transformations and preserve enough context to assess the resulting claim.

## 6. Example: a laboratory result

An instrument records readings. A researcher exports them, excludes invalid entries, calculates an average, rounds the result, and writes a report. A second researcher cites one sentence from that report.

The citation alone may not reveal:
- which instrument generated the readings;
- the measurement conditions;
- which entries were excluded and why;
- how the average was calculated;
- how rounding affected the reported value;
- whether the sentence accurately represents the full result.

A useful provenance record links the source readings, processing activity, parameters, derived result, interpretation, and final statement. If the underlying record cannot be inspected, the later researcher should say so.

## 7. Provenance models and recordkeeping

### 7.1 W3C PROV

W3C PROV distinguishes:
- **Entity:** a document, dataset, measurement, report, image, or other artifact;
- **Activity:** collection, measurement, editing, conversion, analysis, or summarization;
- **Agent:** a person, organization, instrument, or software agent associated with an activity.

Relations can describe which entities an activity used or generated, which entity was derived from another, and which agents were associated with the work. PROV also supports bundles, allowing provenance descriptions themselves to have provenance.

### 7.2 Version and integrity

Where useful, record title, author or responsible agent, publication/revision date, retrieval date, DOI or stable identifier, URL, version, source location, and a checksum.

A checksum can help detect whether a file has changed relative to a known value. It does not prove authenticity, accuracy, or suitability.

### 7.3 Reproducibility

Provenance supports reproducibility but does not guarantee it. Reproduction may also require data, code, methods, parameters, software versions, hardware, permissions, and unavailable external dependencies.

### 7.4 Provenance of provenance

A provenance record can itself be copied, edited, generated, or incomplete. When material, record who created or checked it, what evidence was used, and what verification scope was covered. A provenance record is not automatically more authoritative than the artifact it describes.

## 8. AI, retrieval, and derivative reporting

**Retrieval is not verification.** A search result identifies potentially relevant material; it does not establish authenticity, completeness, relevance, independence, or support for a claim.

**A citation is a pointer, not proof.** A citation can be formally correct yet point to a passage that does not support the sentence attached to it.

**Generated summaries are derived artifacts.** They should not be treated as primary sources merely because they are fluent or detailed.

**Source independence can be lost.** Several articles may repeat one press release, dataset, or paper. Their agreement may be a shared dependency, not independent corroboration. This connects directly to Investigation 028.

**Unknown lineage must remain unknown.** An AI system may not have access to the full training provenance or the exact derivation of a generated statement. It must not invent a source chain to fill the gap.

## 9. Practical traceability audit

For a consequential claim, ask:

1. What exact claim is being reviewed?
2. Which immediate source supports it?
3. Where in that source is the support?
4. Which source version was examined?
5. Is the source a measurement, primary study, secondary account, dataset, model output, or interpretation?
6. What transformations occurred?
7. Which agents and activities were involved?
8. Can the source be retrieved and checked?
9. Are there shared upstream dependencies?
10. Which parts are directly supported and which are inferred?
11. What information was added, removed, altered, or omitted?
12. Can another investigator reconstruct the relevant steps?
13. Which links were directly verified and which remain unverified?
14. If an error is found, can downstream claims be located and corrected?

The depth of recordkeeping should be proportionate to the claim's consequence, complexity, and intended reuse.

## 10. Applying the GUA-W descriptive language

| GUA-W term | Bounded application |
|---|---|
| Structure | Sources, records, activities, derived artifacts, and their links |
| Framework | Methods, formats, standards, and recordkeeping procedures |
| Pattern | Repeated provenance relationships or transformation sequences |
| Constraint | Source availability, version limits, integrity checks, missing records |
| Purpose | Audit, attribution, reproduction, correction, or evaluation |
| Manifestation | Trace record, linked artifacts, version history, and final claim |
| Witness | Actual source, instrument, person, software process, analyst, or report |

**Relationship audit**
- **Same mechanism:** Not claimed between provenance standards and the Scriptural source relationship.
- **Comparable relationship:** Provenance distinguishes source entities, derivative artifacts, activities, and agents. GUA-W's descriptive grammar asks what is originating, received, and derivative.
- **Analogy:** A report's lineage can be compared in a limited descriptive sense with distinguishing originating source from derivative Witness. This is not a shared physical or theological mechanism.
- **Unresolved:** Provenance may be incomplete, incorrect, fabricated, or inaccessible. Traceability does not guarantee truth.

## 11. Bounded Scriptural examination — Genesis 1–2 KJV

This section does not claim that Genesis teaches a modern data-provenance standard.

The established GUA-W relationship is **Author → Word → Creation → Witness**. The scientific investigation concerns traceability of derivative records and reports. The Scriptural relationship concerns the Author, Word, Creation, and Witness as established in the project's foundation.

Genesis 2:1–5 records the completed work and a further account of conditions concerning the earth. The later account is not the originating act.

Genesis 3:1–7 distinguishes God's prior Word, competing testimony, human evaluation, and action. A repeated or accepted statement does not thereby acquire the authority of the originating Word.

These are bounded textual observations and comparisons, not claims that the passages describe provenance software, databases, or information-processing mechanisms.

## 12. Four-Question Study Method

### 1. What must AI ask to understand GUA-W?

AI must distinguish the originating source, directly received evidence, derived artifacts, and the report being produced. It must ask what the immediate source is, whether it was examined, which transformations occurred, and whether a traceable chain is actually available. It must not invent lineage where records are missing.

### 2. What is GUA-W revealing that helps AI understand?

The established relationship remains **Author → Word → Creation → Witness**. This research examines traceability in scientific and informational workflows without equating provenance standards with Scriptural mechanisms or modifying the established architecture.

### 3. What am I learning about what I am witnessing?

Provenance records origins, activities, agents, and derivations. Traceability depends on recorded and recoverable links. Transformations can alter or omit information without necessarily being improper. Summaries are derived artifacts. Citations require support-checking. Sources can share dependencies. Provenance of provenance matters. A documented chain does not guarantee truth or scientific quality.

### 4. What am I learning about the Witness through what I am witnessing?

A Witness can inherit limitations or distortions from the chain through which evidence is received. An investigator who sees only a final summary may be unable to distinguish direct observation from a conclusion several steps removed. The Witness should report what source it examined, what it did not examine, what derivation is known, and what remains uncertain or unverified.

## 13. Triple Constraint examination

**Biblical compliance:** Genesis 1–2 KJV remains the foundational Scriptural context. The Author, Word, Creation, and Witness relationship is preserved. Provenance standards are not attributed to Scripture. **Assessment:** Admissible as a bounded descriptive examination.

**Scientific coherence:** Established provenance concepts and W3C PROV are used to examine transformations, versioning, traceability, and reproducibility, with limitations stated. **Assessment:** Scientifically coherent; provenance supports evaluation but does not establish truth.

**GUA-W consistency:** Existing descriptive vocabulary is used without adding a GUA-W stage, runtime, or state. No identity of mechanisms is asserted. **Assessment:** Consistent as a bounded descriptive application.

## 14. Established, inferred, and unresolved

### Established
- Provenance describes origins, entities, activities, agents, and derivations.
- W3C PROV provides a domain-agnostic conceptual model.
- Provenance can support auditing, attribution, evaluation, and reuse.
- Processing, filtering, translation, annotation, and summarization can change or omit information.
- Several publications can share an upstream source.
- AI summaries are derived artifacts.
- A documented chain does not itself establish authenticity, accuracy, independence, or truth.

### Supported inference
A derivative claim can be evaluated more responsibly when its source, transformations, version, and verification scope are visible. The Witness should distinguish direct examination from inherited summaries, known lineage from missing lineage, and evidence from interpretation.

### Unresolved
- How much provenance detail is sufficient for different claim types and consequences?
- How can lineage be captured across distributed systems?
- How can provenance be audited when sources disappear or access is restricted?
- How can faithful transformations be distinguished from subtle distortions?
- How can provenance be captured when model internals or training sources are inaccessible?
- How should uncertainty be represented at each stage of a long derivation chain?
- How can provenance metadata be checked against actual activities?
- How can evidence lineage and source independence be assessed together?
- What methods best preserve source passages, context, caveats, and version information in AI-assisted research?

## 15. Sources

1. W3C (2013), [PROV-DM: The PROV Data Model](https://www.w3.org/TR/prov-dm/).
2. W3C (2013), [PROV Model Primer](https://www.w3.org/TR/prov-primer/).
3. W3C (2013), [PROV-Overview](https://www.w3.org/TR/prov-overview/).
4. W3C (2013), [Constraints of the PROV Data Model](https://www.w3.org/TR/prov-constraints/).
5. Paulus and Biskup (2023), “Towards more reproducible and FAIRer research data: documenting provenance during data acquisition using the Infofile format,” *Digital Discovery* 2, 234–244. [DOI](https://doi.org/10.1039/D2DD00131D).
6. Wittner et al. (2024), “Toward a common standard for data and specimen provenance in life sciences,” *Learning Health Systems* 8(1), e10365. [DOI](https://doi.org/10.1002/lrh2.10365).

**Scriptural sources:** King James Version, Genesis 1–2 and Genesis 3:1–7. Scientific sources are not offered as authorities for Scriptural meaning.

## 16. Next question emerging

Investigation 032 raises the next question:

**When evidence from different Witnesses is combined, how can the resulting account preserve disagreement, dependency, and differing levels of support rather than collapse them into one apparently unified conclusion?**

Possible next investigation: **Investigation 033 — Evidence Synthesis, Disagreement, Dependency, and the Construction of a Composite Witness.**

---

**A traceable report does not guarantee a true report. It makes the report's history more visible, so the evidence and transformations can be examined rather than trusted solely on assertion.**
