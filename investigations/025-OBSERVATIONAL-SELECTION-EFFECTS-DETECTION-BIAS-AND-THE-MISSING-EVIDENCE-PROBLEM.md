# Investigation 025 — Observational Selection Effects, Detection Bias, and the Missing-Evidence Problem

**Primary disciplines:** Observational astronomy, astrostatistics, survey design, Bayesian inference, censored and truncated data analysis, measurement theory, astrophysical instrumentation, and philosophy of scientific observation.

**Investigation status:** Initial evidence-led investigation and Four-Question Study Method review recorded.

**Central question:** How do instruments, detection thresholds, survey footprints, sample construction, and interpretation determine which phenomena enter the evidence—and what can legitimately be concluded when something is not detected?

**Scientific context:** Astronomical surveys and the reconstruction of interstellar structure, including magnetic fields, gas, dust, and molecular-cloud populations.

**Scriptural comparison under examination:** Genesis 1–2, with particular attention to Genesis 2:1–5, considered alongside Genesis 3. The biblical text is examined on its own terms. Any comparison with scientific observation is explicitly classified and is not treated as a scientific mechanism or proof of a theological claim.

## 1. Why this investigation follows 024

Investigation 024 asked what observation could count against a favored explanation and how to design tests that distinguish competing models.

That question assumes we have access to the relevant observation.

But what if the phenomenon never enters the dataset?

A source may be too faint for an instrument. A region may not have been surveyed. A signal may fall below a detection threshold. A data-processing pipeline may reject a real source. A sample may be assembled in a way that excludes a class of objects before analysis begins.

The investigator may then examine a dataset that is internally consistent, carefully measured, and honestly reported—but incomplete in a way that affects the conclusion.

This creates a further distinction:

**What is absent from the physical system is not the same as what is absent from the observational record.**

Investigation 025 examines the processes that govern that difference.

## 2. The four conditions: absent, undetected, unrecognized, misinterpreted

The following distinctions are useful, but they are not an exhaustive or necessarily sequential classification.

### 2.1 Not present

The phenomenon or object is genuinely absent from the physical region or system under the stated definition and conditions.

A claim of absence requires evidence appropriate to the question. A non-detection alone does not establish it.

### 2.2 Present but not detected

The phenomenon exists, but the observation does not register it. It may be too faint, too diffuse, obscured, outside the instrument's bandpass, unresolved, or outside the survey footprint.

This is an observational non-detection. It can occur even when the instrument and analysis work as designed.

### 2.3 Detected but not recognized

A signal or feature is present in the recorded data, but the pipeline, classification procedure, or investigator does not identify it as the relevant phenomenon.

Examples include a real source rejected as an artifact, an unusual object assigned to an inappropriate class, or a weak spectral feature overlooked during analysis.

### 2.4 Recognized but incorrectly interpreted

The signal is detected and classified, but its physical meaning is assigned incorrectly or too confidently.

A measured feature may have multiple possible origins. Recognition of a pattern does not uniquely identify its mechanism.

These conditions identify different locations at which an evidentiary account can become incomplete or misleading. They must not be collapsed into one generic category called observational failure.

## 3. The observation chain

A simplified observation chain is:

\[
\text{Physical phenomenon}
\rightarrow
\text{Signal reaching instrument}
\rightarrow
\text{Instrument response}
\rightarrow
\text{Recorded data}
\rightarrow
\text{Detection and selection}
\rightarrow
\text{Classification}
\rightarrow
\text{Interpretation}
\]

Each transition has conditions and limitations.

- The phenomenon may not produce the signal being measured.
- The signal may be absorbed, scattered, diluted, or geometrically inaccessible.
- The instrument may have finite sensitivity, resolution, coverage, or dynamic range.
- Data processing may filter, mask, or reject signals.
- A detection threshold may exclude low-significance events.
- A classification rule may fail for unusual or previously unrecognized cases.
- Interpretation may confuse a proxy or signature with the underlying physical quantity.

A statement about what was observed should identify which portion of this chain supports it.

The instrument does not register all of Creation. It registers signals to which its design and observing conditions make it responsive.

## 4. Detection probability and the selection function

A survey's selection function describes the probability that an object with specified properties is included in the resulting catalogue or sample.

In a simplified form:

\[
S(x)=P(\text{included in sample}\mid x)
\]

Here, \(x\) may include position, brightness, color, size, distance, morphology, spectral properties, observing conditions, or other relevant variables.

The selection function can be:

- **Deterministic:** an object either passes or fails a defined cut.
- **Probabilistic:** inclusion varies between zero and one because detection and processing are not perfectly deterministic.

Real survey selection may depend on several interacting properties. A single brightness threshold may not describe completeness if detection also depends on source size, background structure, crowding, position, or observing conditions.

### Completeness and reliability

Two quantities must be distinguished:

- **Completeness:** the fraction or probability of real eligible sources that are detected and included.
- **Reliability:** the fraction or probability of reported detections that correspond to real sources.

A survey can have high reliability but low completeness: most listed sources are genuine, but many real sources were missed.

A survey can have high completeness but lower reliability: most real sources are recovered, but many reported detections are false positives.

These are different properties and require different tests.

A selection function is not merely a correction applied after observation. It is part of the process that determines what evidence is available.

## 5. Detection thresholds do not create a simple boundary between existence and nonexistence

Many observations use a detection criterion based on signal-to-noise ratio or another test statistic.

A threshold can be useful for controlling false detections. But it does not divide the physical world into objects that exist above the threshold and objects that do not exist below it.

A signal below threshold may still contain information. Depending on the measurement and analysis, it may contribute as a weak measurement, an upper limit, a likelihood contribution, or a constraint on a population model.

A source just below a threshold is not physically different merely because the catalogue does not list it. The catalogue boundary is an analytical or operational decision, not necessarily a physical boundary in the system.

Thresholds can also vary across a survey. Background noise, exposure time, detector response, crowding, and observing conditions can make the effective sensitivity spatially nonuniform.

## 6. Non-detections, upper limits, censoring, and truncation

These terms describe different data situations.

### 6.1 Non-detection

A non-detection means that the observation did not meet the adopted criterion for identifying a source or signal.

It does not automatically mean that the true signal is zero.

### 6.2 Upper limit and censored data

In a targeted observation of a known object, the object may be in the sample even when its signal is too weak to measure reliably.

The record may therefore contain an upper limit rather than a precise measured value. This is a form of censored data: the object is known to belong to the sample, but the measurement is only partially constrained.

An upper limit is not a measurement equal to the limit. It represents a statement about the measurement process and uncertainty.

### 6.3 Truncated data

In a blind survey, objects that fail the selection criterion may never enter the catalogue. Their number and properties may not be known from that catalogue alone.

This is truncation: the observed dataset is drawn only from the portion of the population that passed the selection process.

Censoring and truncation are not interchangeable. In censoring, the sample membership may be known while a measurement is limited. In truncation, objects outside the selection region may be absent from the dataset entirely.

### 6.4 Why the distinction matters

If an investigator treats an upper limit as zero, or treats a truncated catalogue as a complete population, estimated distributions and relationships can be biased.

The correct likelihood or statistical model must account for how the observations entered the dataset.

Sources:
- Feigelson, E. D. and Babu, G. J. (2012), “Nondetections: censored and truncated data,” in *Modern Statistical Methods for Astronomy*, Cambridge University Press. https://doi.org/10.1017/CBO9781139015653.011
- Mantz, A. B. (2019), “Coping with selection effects: a Primer on regression with truncated data,” *Monthly Notices of the Royal Astronomical Society* 485, 4863–4872. https://doi.org/10.1093/mnras/stz320

## 7. Selection bias: when the observed sample does not represent the target population

A sample can be accurately measured and still be unrepresentative.

Suppose a survey detects objects more readily when they are bright, compact, nearby, or isolated. The resulting sample may overrepresent those properties.

If investigators estimate the properties of the entire population using only the selected objects, they may infer a distribution that describes the catalogue rather than the underlying population.

Examples include:

- flux-limited galaxy surveys;
- magnitude-limited stellar catalogues;
- exoplanet detection methods that favor certain orbital periods, sizes, or orientations;
- transient surveys whose cadence favors certain event durations;
- molecular-line surveys that preferentially detect particular excitation conditions or chemical abundances;
- polarization observations whose sensitivity varies with intensity, angular scale, and background structure.

Selection effects can influence both the number of detected objects and the relationships inferred among their properties.

### A caution about correction

A statistical correction is only as reliable as the information and assumptions used to construct it. If the selection function is poorly known, or depends on unmeasured properties, a correction can leave residual bias or introduce new uncertainty.

Investigators should report the assumptions used to estimate completeness and should test the sensitivity of conclusions to plausible alternatives.

## 8. The selection function must be investigated, not merely assumed

The Gaia DR3 selection-function study illustrates why catalogue construction matters. Comparing model predictions with an astronomical catalogue requires knowledge of the processes that determined which objects were included. Those processes can involve detection efficiency, apparent magnitude, data quality, and processing decisions.

The study describes a catalogue selection function as a probability of inclusion and emphasizes that knowing what could not be observed can be essential to interpreting what was observed.

A complete sample may sometimes be obtained by restricting analysis to a region where inclusion probability is near one. But this can discard much of the population and narrow the scientific question.

An alternative is to model the selection process explicitly, while acknowledging that reconstructing every detail of catalogue construction can be difficult.

Source: *An empirical model of the Gaia DR3 selection function* (2023), *Astronomy & Astrophysics*. https://doi.org/10.1051/0004-6361/202244784

## 9. A deeper limitation: the missing population may not resemble the detected population

It is tempting to assume that objects just below a detection threshold are like the objects just above it, only weaker.

That assumption may be wrong.

The properties of the population can change near or beyond the detection boundary. Faint galaxies may differ in size, morphology, environment, or other properties from brighter galaxies. Objects at greater distances may represent different epochs or conditions. A detection threshold can therefore exclude not just weaker examples of the same class, but a population with a different distribution of properties.

Gallagher and Smeenk discuss this challenge in observational astronomy and also identify a subtler issue: computational limitations can restrict which alternative scenarios are simulated and considered.

They call attention to the problem of “uncomputed alternatives.” If a simulation program only explores a restricted set of possible histories, a real system arising from an unmodeled alternative may not be considered in the interpretation.

This links Investigation 025 to Investigation 023: an incomplete observational sample and an incomplete model space can reinforce one another.

Source: Gallagher, S. C. and Smeenk, C. (2023), “What’s in a Survey? Simulation-Induced Selection Effects in Astronomy,” in *Philosophy of Astrophysics*, Synthese Library. https://doi.org/10.1007/978-3-031-26618-8_12

## 10. The missing-evidence problem in interstellar and magnetic-field research

The previous investigations used complementary astronomical tracers to reconstruct gas and magnetic structure. Selection effects can affect each tracer differently.

### 10.1 Dust emission polarization

Polarized dust emission depends on dust properties, temperature, grain alignment, optical depth, magnetic-field orientation, and line-of-sight integration.

A weak or absent polarized signal does not necessarily mean that dust or magnetic field is absent. The polarization fraction can be reduced by geometric cancellation, unresolved field structure, optical-depth effects, or changes in grain alignment.

A polarization non-detection must be interpreted through the emission and measurement model.

### 10.2 Zeeman measurements

Zeeman splitting can constrain the line-of-sight magnetic field in suitable spectral transitions.

But detectability depends on line strength, spectral resolution, signal-to-noise, excitation, optical depth, and the material sampled by the transition.

A non-detection does not establish that the line-of-sight field is zero. It may constrain the field only within the sensitivity and tracer conditions of that observation.

### 10.3 Molecular-line tracers

Different molecules and transitions trace different density, temperature, chemistry, and excitation conditions.

A molecule not detected in a region may be chemically depleted, poorly excited, optically affected, or below sensitivity. It does not automatically follow that the gas itself is absent.

A tracer is not identical to the full physical material it helps reveal.

### 10.4 Faraday rotation

Faraday rotation requires a suitable polarized background or emitting source and depends on the line-of-sight integral of electron density and magnetic field.

The absence of a usable rotation measurement may reflect a lack of suitable background sources, depolarization, source confusion, or survey coverage rather than the absence of magnetized plasma.

### 10.5 Starlight polarization and distance sampling

Starlight polarization depends on background stars being available, measurable, and sufficiently characterized. The spatial distribution of stars and their distances affects which portions of a cloud can be sampled.

An unsampled region is not thereby an empty region.

### 10.6 Combined interpretation

Different tracers have different selection functions and physical sensitivities. Combining them can reduce some blind spots, but only if their selection processes and shared dependencies are understood.

A multi-tracer reconstruction should therefore record not only what each method measures, but also which parts of the physical system each method could not constrain.

## 11. Non-detection as evidence: what can legitimately be inferred?

A non-detection can be informative when the probability of detection under a specified hypothesis is known or credibly modeled.

Suppose a hypothesis predicts a signal with a distribution of possible measured outcomes. An observation that does not cross the detection threshold can then be compared with that predicted distribution.

The evidential value depends on:

- the predicted signal strength and variability;
- instrument sensitivity and noise;
- background and foreground contributions;
- detection efficiency;
- false-positive and false-negative rates;
- observing coverage and duration;
- the model connecting the physical hypothesis to the measured signal.

A non-detection can disfavor a hypothesis if that hypothesis strongly predicted a detectable signal under the actual observing conditions.

But if the signal could readily have fallen below threshold, the non-detection may provide little constraint.

The relevant question is not simply “Was it detected?” but:

**If the proposed phenomenon were present as specified, how likely is it that this observation would have detected it?**

This is the detection-probability counterpart to Investigation 024's critical-test question.

## 12. Designing an observation that can reveal what is missing

A disciplined investigation of observational absence should proceed as follows.

### Step 1 — Define the target

Specify the physical phenomenon, property, population, or signal being investigated.

### Step 2 — Define the observation domain

Record the sky area, distance range, time interval, wavelength or frequency coverage, angular and spectral resolution, and relevant physical conditions.

### Step 3 — Characterize sensitivity

Estimate detection probability as a function of the properties that affect detection. Avoid assuming one universal threshold if sensitivity varies across the survey.

### Step 4 — Test completeness and reliability

Use injection-and-recovery tests, suitable reference catalogues, repeated observations, or other validated procedures where applicable. Record both missed real sources and false detections.

### Step 5 — Preserve sub-threshold information

Where the data permit, retain flux measurements, likelihoods, upper limits, and low-significance signals rather than reducing everything to detected/not detected.

### Step 6 — Model selection

Include the selection process in population inference or explicitly restrict the inference to a justified complete region.

### Step 7 — Examine unobserved alternatives

Ask which physical populations, geometries, signal forms, or histories are absent from the simulation and analysis space. Distinguish computational convenience from physical exclusion.

### Step 8 — Seek complementary witnesses

Use different wavelengths, tracers, instruments, or methods where they respond differently to the phenomenon. Trace common selection effects and model assumptions.

### Step 9 — State the inference boundary

Report what the observation constrains, what it cannot constrain, and what remains unknown.

## 13. Genesis 1–2 (especially Genesis 2:1–5) and Genesis 3: a careful textual examination

This section is included because the user has identified these passages as a particularly important scriptural context for examining presence, preparation, manifestation, and the Witness. The passages must be read on their own terms before any comparison is proposed.

### 13.1 Genesis 2:1–5 — completion, host, and conditions preceding growth

The KJV text of Genesis 2:1 states that the heavens and earth were finished, “and all the host of them.” Genesis 2:2–3 describes the completion of God's work, the seventh day, and its blessing and sanctification.

Genesis 2:4 begins the account of the generations of the heavens and the earth. Genesis 2:5 then describes a condition in which the plant of the field was not yet in the earth and the herb of the field had not yet grown. The verse gives two stated conditions: the LORD God had not caused it to rain upon the earth, and there was not a man to till the ground.

The text therefore places these statements together:

- the heavens, earth, and their host are described as finished;
- the account then describes plants not yet grown in the stated conditions;
- rain and a man to till the ground are named in the explanation of that condition.

This requires care. Genesis 2:5 does not say that every later plant was already visibly manifested, nor does it explicitly state that God was holding every seed in His hand. Genesis 1:11 has already recorded God's command concerning the earth bringing forth grass, herb yielding seed, and fruit tree yielding fruit after its kind, whose seed is in itself.

A disciplined reading preserves the wording and sequence of both chapters rather than supplying an unstated mechanism.

**Textual observation:** Genesis 2:1–5 distinguishes the completed work and its host from a subsequent description of particular plant growth under stated conditions.

**Textual observation:** The passage identifies rain and a man to till the ground as conditions relevant to the described state.

**Unresolved textual question:** How should the relationship between Genesis 1:11–13 and Genesis 2:5 be understood in the wider literary and theological structure of Genesis 1–2? The wording, chronology, and relation between the accounts deserve direct examination rather than a premature harmonization.

### 13.2 Genesis 3 — a changed human relation to the command and to what is seen

Genesis 3 records the serpent's conversation with the woman, the questioning and alteration of God's command, the woman's assessment of the tree, the taking and eating, the giving to her husband, and the subsequent recognition of their nakedness and hiding.

Genesis 3:6 records the woman's perception of the tree as good for food, pleasant to the eyes, and desirable to make one wise. The narrative then records the eating and the opening of the eyes in Genesis 3:7.

The passage concerns disobedience, deception, human judgment, and the consequences of the Fall. It should not be reduced to a scientific example of detection bias.

For this investigation, a limited textual question is relevant:

**What changes when the human Witness no longer receives and responds to God's command in the same way?**

The narrative presents a change in how the command is handled and how the tree is evaluated. The woman considers the tree through the stated attractions; the serpent has already challenged the meaning and consequence of God's word.

This is a theological and textual examination of the human response to God's command. It is not a claim that Genesis 3 describes an instrument's detection threshold, an astronomical selection function, or a scientific mechanism of missing data.

### 13.3 What these passages do—and do not—establish for this investigation

They establish the scriptural foundation from which the project's language is drawn and provide a textually important distinction between God's completed work, the conditions described in Genesis 2:5, and the human response to God's command in Genesis 3.

They do not, by themselves, establish the technical concepts of observational completeness, selection bias, censored data, false negatives, or detection probability. Those concepts belong to scientific disciplines and must be established through scientific evidence.

A possible comparison may be investigated between:

- what exists and what is presently manifest under stated conditions;
- what is available in a system and what a particular witness registers;
- the limits of a witness and the limits of its means of reception;
- a change in the conditions of observation and a change in the interpretation of what is observed.

These are proposed comparative questions, not established identities.

**The critical safeguard:** Do not equate the Fall with an astronomical detection failure. Do not equate Genesis 2:5's agricultural conditions with an instrument's selection function. Preserve the theological meaning of the text and the scientific meaning of the method.

## 14. GUA-W Language of Creation: bounded descriptive examination

| GUA-W descriptor | Bounded use in this investigation | Limit |
|---|---|---|
| **Structure** | The physical system or population that an observational program seeks to examine. | The catalogue is not the complete physical system. |
| **Framework** | The instrument, survey, processing pipeline, selection model, and inferential assumptions. | The framework shapes what is registered; it does not create the physical population. |
| **Pattern** | The distribution and relationships among detected, undetected, and partially measured signals. | A pattern in a selected sample may not represent the full population. |
| **Constraint** | Sensitivity, resolution, coverage, thresholds, physical conditions, and selection criteria. | Analytical limits must not be mistaken for physical absence. |
| **Purpose** | The stated scientific objective or demonstrated function of a measurement or survey. | The investigator's objective does not establish ultimate purpose. |
| **Manifestation** | The signal or physical effect that becomes measurable under specified conditions. | A non-detection does not establish that the underlying phenomenon is absent. |
| **Witness** | The instrument, data record, detection procedure, classifier, and investigator. | Each has distinct reception, recording, and interpretation limits. |

The vocabulary describes the relationship between the physical subject, observational framework, constraints, manifestation, and witness. It does not replace the scientific account or imply that every unobserved feature is physically present.

## 15. Same mechanism, comparable relationship, or similar appearance?

### Same mechanism

A telescope's sensitivity limit, a molecular transition's excitation requirements, dust-grain alignment, and the theological account of the Fall are not the same mechanism. They belong to different explanatory domains.

### Comparable relationship

Different observational systems can exhibit a comparable relationship: the conditions and capabilities of a witness influence which aspects of a subject are registered. The underlying physical and technical mechanisms can remain different.

The Genesis 2:1–5 textual examination and the scientific distinction between physical presence and observed manifestation may invite a limited comparison concerning conditions and manifestation. That comparison requires further textual and scientific work and is not a demonstrated common mechanism.

### Similar appearance

A scientific non-detection and a biblical description of something not yet grown may both use language of absence or non-manifestation. That verbal resemblance does not establish that the conditions, causes, or meanings are identical.

### Unresolved

Whether a more precise correspondence can be developed between the Genesis 1–2 textual sequence and the scientific distinction between physical existence, manifestation, and observation remains open. The comparison must be tested against the actual wording and context of Scripture and the actual definitions and evidence of the scientific disciplines.

## 16. Boundary and participation examination

**Does a boundary merely separate two regions, or can it also participate in the relationship between them?**

- **Instrument sensitivity boundary:** Determines the range of signals that can be reliably detected. It is an operational boundary, not a physical edge of the object.
- **Survey footprint:** Separates observed from unobserved regions of the sky. It defines the survey's spatial coverage, not the extent of the underlying population.
- **Detection threshold:** Separates reported detections from non-detections under a decision rule. It participates in catalogue construction but does not divide existence from nonexistence.
- **Physical interface:** A cloud boundary, shock, or phase interface may participate in physical transport, emission, absorption, or interaction.
- **Textual boundary:** A passage or narrative transition can organize the reader's attention and distinguish conditions or events in the text. Its literary role must be established through textual analysis, not assumed to be a physical mechanism.

A boundary may affect what can be observed or how a system behaves. The investigation must identify which type of boundary is present and what evidence establishes its role.

## 17. Four-Question Study Method

### 1. What must AI ask to understand GUA-W?

AI must ask what is physically present, what signal it produces, what the instrument can receive, what the processing pipeline retains, and what the investigator can infer. What is the selection function? How are completeness and reliability measured? Is the dataset censored or truncated? What could remain outside the observational record? What does a non-detection actually constrain?

For the scriptural examination, AI must ask what Genesis 2:1–5 explicitly states about completion, host, plant growth, rain, and man's tilling, and what Genesis 3 explicitly records about the serpent's challenge, the woman's evaluation, and the act of eating. AI must not substitute a scientific analogy for textual interpretation.

### 2. What is GUA-W revealing that helps AI understand?

The established foundation identifies the originating Source, Creation, and derivative Witness. The scientific investigation examines the limits through which derivative instruments and investigators register aspects of Creation.

Genesis 2:1–5 and Genesis 3 remain scriptural sources with their own textual and theological meaning. They prompt careful questions about completion, stated conditions, manifestation, reception, and human response. Any relationship to scientific observation remains a proposed comparison until the source and evidence establish its scope.

### 3. What am I learning about what I am witnessing?

I am witnessing that observational data are shaped by the physical signal, the instrument, the observing conditions, selection rules, processing, classification, and interpretation. A non-detection can be informative, but its meaning depends on the probability that the phenomenon would have been detected if present as specified.

I am also witnessing that an observed sample may not represent the full population. The unobserved population may differ from the detected population, and computational limits can restrict which alternatives are even considered.

### 4. What am I learning about the Witness through what I am witnessing?

The Witness is not identical to the means by which it receives information. An instrument has a response range; a survey has a footprint; a classifier has categories; an investigator has assumptions and interpretive limits.

A faithful report of recorded data can still be incomplete as an account of the physical system. The Witness must report both what was registered and the conditions under which registration was possible.

The investigator must also resist treating what is outside the chosen method as though it were outside reality.

## 18. Triple Constraint examination

### Biblical compliance

The investigation retains Genesis 1–2 KJV as the scriptural foundation and examines Genesis 2:1–5 and Genesis 3 without claiming that they explicitly teach modern observational statistics. The comparison is bounded and does not equate the Fall with scientific measurement failure.

**Assessment:** No direct contradiction is introduced by the bounded comparison. The precise theological meaning of the passages remains governed by textual and contextual examination, not by astronomical analogy.

### Scientific coherence

The investigation distinguishes detection probability, completeness, reliability, non-detection, upper limits, censoring, truncation, selection bias, and interpretation. It recognizes that a non-detection can constrain a hypothesis only in relation to the expected signal and the actual observing process.

**Assessment:** Scientifically coherent as a methods-focused investigation. A claim about a particular undetected population requires a characterized selection function, justified assumptions, and appropriate uncertainty analysis.

### GUA-W consistency

The established architecture remains unchanged. The investigation uses the common vocabulary to describe the physical subject, observational framework, constraints, manifestation, and derivative witnesses. It does not elevate a survey, instrument, or scientific model into the originating Source.

**Assessment:** Consistent as a bounded descriptive application. No new GUA-W layer or operation is proposed.

## 19. What is established, inferred, and unresolved?

### Established by the cited literature

- Astronomical catalogues are shaped by selection processes, and those processes must be understood when comparing observations with population models.
- Completeness and reliability describe different properties of a detection catalogue.
- Censored and truncated datasets are different statistical situations and require different treatment.
- Non-detections and upper limits can contain information and should not automatically be replaced by zero.
- Selection effects can make an observed sample unrepresentative of the population under study.
- Simulations can help characterize survey selection, but computational limits can also restrict which alternatives are considered.
- The detection probability of an object can depend on multiple intrinsic and observational properties, not simply one universal brightness threshold.

### Supported inference

A Witness may report all registered signals faithfully while still providing an incomplete account of the physical system because the means of observation did not register every relevant feature.

A non-detection is not equivalent to proof of absence. Its evidential strength depends on how likely the observation was to detect the phenomenon under the hypothesis being examined.

Different witnesses can provide complementary evidence when their sensitivities and selection processes differ, but combining them does not automatically remove shared blind spots.

### Unresolved

- How can the selection function be estimated when catalogue construction includes undocumented or changing decisions?
- How should investigators model a population whose properties change near and beyond the detection boundary?
- How can a survey reveal a population that is absent from its own catalogue?
- How should the uncertainty in a selection function be propagated into physical conclusions?
- How can researchers distinguish a truly absent component from one that is below sensitivity, obscured, unresolved, or chemically untraced?
- How do selection effects interact with the missing-variable problem from Investigation 023?
- How can simulations expose alternatives that were not included in the simulation design?
- What combination of dust polarization, Zeeman measurements, molecular tracers, and other observations best constrains regions that any one tracer cannot see?
- What is the precise textual and theological relationship between Genesis 1:11–13 and Genesis 2:1–5?
- How should the completion and host described in Genesis 2:1–2 be related to the plant-growth conditions described in Genesis 2:5?
- What does Genesis 3 establish about the human response to God's command, and which proposed comparisons with reception, recognition, or interpretation remain only analogical?
- Can a careful textual comparison clarify the distinction between what is given, what is manifest under stated conditions, and what a derivative Witness registers without turning that comparison into an asserted scientific mechanism?

These questions remain open.

## 20. Sources

1. *An empirical model of the Gaia DR3 selection function* (2023). *Astronomy & Astrophysics*. https://doi.org/10.1051/0004-6361/202244784
2. Mantz, A. B. (2019). “Coping with selection effects: a Primer on regression with truncated data.” *Monthly Notices of the Royal Astronomical Society* 485, 4863–4872. https://doi.org/10.1093/mnras/stz320
3. Feigelson, E. D. and Babu, G. J. (2012). “Nondetections: censored and truncated data.” In *Modern Statistical Methods for Astronomy*. Cambridge University Press. https://doi.org/10.1017/CBO9781139015653.011
4. Andreon, S. and Hurn, M. (2013). “Measurement errors and scaling relations in astrophysics: a review.” *Statistical Analysis and Data Mining* 6, 15–33. https://doi.org/10.1002/sam.11173
5. Boubert, D. et al. (2022). “A selection function toolbox for subsets of astronomical catalogues.” *Monthly Notices of the Royal Astronomical Society* 510, 4626–4645. https://academic.oup.com/mnras/article/510/3/4626/6479135
6. Gallagher, S. C. and Smeenk, C. (2023). “What’s in a Survey? Simulation-Induced Selection Effects in Astronomy.” In *Philosophy of Astrophysics*, Synthese Library. https://doi.org/10.1007/978-3-031-26618-8_12
7. Koen, C. (2026). “Statistical Issues Often Overlooked when Analyzing Astronomical Data.” *The Astrophysical Journal Supplement Series* 282, 31. https://doi.org/10.3847/1538-4365/ae25eb

**Scriptural source:** King James Version, Genesis 1:11–13; Genesis 2:1–5; Genesis 3. The textual observations in Section 13 are based on the cited KJV passages; no scientific source is offered as an authority for their theological meaning.

## 21. Next question emerging

Investigation 025 shows that the evidence available to an investigator is shaped by the selection process that admits observations into a dataset. The unobserved population may differ from the observed population, and a non-detection only constrains a hypothesis when the probability of detection is understood.

A possible next investigation is **Observation, Measurement, and the Difference Between a Signal and the Thing Signaled**: what exactly does an instrument measure, how does a physical interaction become a recorded value, and under what conditions can a proxy or signal be mistaken for the underlying property?

This would continue the examination of the Witness while connecting the scientific measurement chain to the distinctions already raised in Genesis 1–2 and Genesis 3. The scriptural comparison would remain a separate textual inquiry, not a presumed scientific mechanism.

This is a possible lead, not a fixed assignment.

---

**Investigation 025 records the distinction between physical absence and observational absence. It also records that a Witness's report must be read together with the conditions and limits of reception.**
