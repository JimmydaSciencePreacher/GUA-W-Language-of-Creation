# Investigation 026 — Observation, Measurement, and the Difference Between a Signal and the Thing Signaled

**Primary disciplines:** Metrology, measurement science, experimental physics, observational astronomy, detector physics, radiometry, spectroscopy, calibration science, inverse problems, and philosophy of measurement.

**Investigation status:** Initial evidence-led investigation and Four-Question Study Method review recorded.

**Central question:** When an instrument registers something, what exactly has been witnessed—the physical subject, a signal produced through an interaction, an instrument indication, a calibrated measurement result, or an interpretation of that result?

**Scientific context:** The conversion of physical interactions into instrument indications and measurement results, with particular attention to astronomical observations and indirect measurements.

**Scriptural comparison under examination:** Genesis 1–3 KJV, with particular attention to the distinction between God's originating acts and Word, the created things brought forth, Adam's naming in Genesis 2:19–20, and the human response to testimony and sight in Genesis 3. These passages are examined textually and theologically, not treated as scientific measurement theory.

## 1. Why this investigation follows 025

Investigation 025 examined how a physical phenomenon can remain outside an observational record because of sensitivity, coverage, selection, or interpretation.

Investigation 026 moves one step earlier in the evidentiary chain.

Even when a signal is received and recorded, the record is not automatically identical to the physical property that the investigator wants to know.

A detector may register a voltage, count, displacement, pulse, or pattern. A measurement procedure relates that indication to a defined quantity. A measurement model, calibration, reference, and uncertainty evaluation support the result attributed to the measurand.

The central distinction is:

**The thing investigated, the physical interaction that produces an indication, the indication itself, and the result inferred from it are related—but they are not interchangeable.**

This is not a claim that measurements are unreal or merely subjective. Measurement is an empirical process. The question is what the result is a result *of*, and what chain of evidence justifies attributing it to the intended quantity.

## 2. The vocabulary of measurement: five terms that must not be collapsed

The International Vocabulary of Metrology (VIM, JCGM 200:2012) provides standardized definitions. The following distinctions are essential.

### 2.1 Measurand

The **measurand** is the quantity intended to be measured.

It must be specified sufficiently clearly for the measurement purpose. A statement such as “measure the magnetic field” may be incomplete unless it specifies, for example, location, component or direction, spatial and temporal scale, and relevant physical conditions.

The measurand is not simply whatever number appears on a display.

### 2.2 Effective property and physical interaction

A measuring system interacts with some property or effect of the subject. In an ideal direct measurement, the property that produces the instrument response may coincide with the intended measurand.

In practical measurements, the property that directly affects the instrument can differ from the property the investigator intends to determine. The relationship between them must then be established through a measurement model and supporting evidence.

For example, a thermometer's sensing element responds to a physical effect related to temperature. The displayed temperature is not the same kind of quantity as the element's raw physical response.

### 2.3 Indication

An **indication** is the value provided by a measuring instrument or measuring system.

Examples include:
- a pointer position;
- a digital count;
- an electrical voltage;
- a detector pixel value;
- a spectral line position;
- a time interval recorded by an instrument.

An indication is a result of the instrument's interaction and response. It is not automatically the final value of the intended measurand.

### 2.4 Measurement result

A **measurement result** is the set of quantity values being attributed to a measurand, together with relevant information. A reported result should make its uncertainty and conditions clear.

The result may require corrections, a calibration relation, a mathematical model, and additional input quantities.

### 2.5 Interpretation

Interpretation assigns scientific meaning to a measurement result. It may identify a physical source, infer a mechanism, compare the result with a model, or propose a cause.

A measurement result can be valid while a later interpretation remains uncertain or wrong.

**Key distinction:** An indication belongs to the measuring system; a measurement result is attributed to the measurand; an interpretation explains what that result may mean for the physical subject.

Sources:
- JCGM 200:2012, *International Vocabulary of Metrology — Basic and General Concepts and Associated Terms (VIM)*, especially 2.3, 2.9, 2.10, 2.39, 2.41, 2.48, and 4.1. https://www.bipm.org/documents/20126/2071204/JCGM_200_2012.pdf
- JCGM 100:2008, *Evaluation of Measurement Data — Guide to the Expression of Uncertainty in Measurement (GUM)*. https://www.bipm.org/documents/20126/2071204/JCGM_100_2008_E.pdf

## 3. The measurement chain

A simplified measurement chain is:

\[
\text{Physical subject}
\rightarrow
\text{Interaction or transduction}
\rightarrow
\text{Instrument response}
\rightarrow
\text{Indication}
\rightarrow
\text{Calibration and measurement model}
\rightarrow
\text{Measurement result}
\rightarrow
\text{Scientific interpretation}
\]

The chain is not always a simple one-way sequence. Instruments may interact with the subject, alter it, or measure only a response that depends on several influence quantities. A measurement model can include many inputs and corrections.

Nevertheless, the chain helps identify what is directly registered and what is inferred.

At each link, ask:

- What physical property or process produces the response?
- What does the sensing element actually interact with?
- What does the instrument output?
- Which reference and calibration relation connect that output to a quantity?
- Which other quantities influence the result?
- What uncertainty remains?
- Which further interpretation is being added?

A statement such as “the instrument measured X” may be acceptable shorthand, but a rigorous investigation should be able to explain the measurement chain behind it.

## 4. Calibration: what it establishes and what it does not

Calibration establishes a relationship, under specified conditions, between reference quantity values and instrument indications, and then uses that relationship to obtain measurement results from indications.

Calibration can reveal systematic deviations and support corrections. It does not mean that an instrument has become perfect.

Calibration does not, by itself, establish:
- that the correct measurand was selected;
- that the measurement model includes every important influence;
- that the instrument was used under the calibration conditions;
- that the measurement uncertainty is adequate for the intended purpose;
- that the final scientific interpretation is correct.

### 4.1 Traceability

Metrological traceability relates a measurement result to a reference through a documented, unbroken chain of calibrations, each contributing to the measurement uncertainty.

Traceability is important for comparability. But traceability alone does not guarantee that the uncertainty is small enough for a particular use, that the model is complete, or that no mistake has occurred.

### 4.2 Calibration is not adjustment

Calibration determines or documents the relationship between indications and reference values. Adjustment changes the measuring system. Verification evaluates whether specified requirements are met. These are related but distinct activities.

A report should not use these terms interchangeably.

Sources:
- JCGM 200:2012, VIM, definitions 2.39–2.45. https://www.bipm.org/documents/20126/2071204/JCGM_200_2012.pdf
- JCGM 104:2009, *An Introduction to the “Guide to the Expression of Uncertainty in Measurement” and Related Documents*. https://www.bipm.org/documents/20126/2071204/JCGM_104_2009.pdf

## 5. Direct and indirect measurement

A direct measurement obtains a value through a procedure in which the intended quantity is closely linked to the instrument indication.

An indirect measurement determines the intended quantity from other measured quantities through a measurement model.

The distinction is not a ranking of good and bad science. Many important physical quantities are determined indirectly.

A measurement model may be written in a general form:

\[
Y=f(X_1,X_2,\ldots,X_n)
\]

Here, \(Y\) is the measurand's estimated value and the \(X_i\) are input quantities. Their uncertainties and correlations contribute to the uncertainty of the result.

A simple model can be adequate for one purpose and inadequate for another. The model must include the quantities known to matter at the required level of accuracy.

The GUM-6 guidance emphasizes that a measurand is often not measured directly but determined from other quantities related to it through a measurement model.

Source: JCGM GUM-6:2020, *Guide to the Expression of Uncertainty in Measurement — Part 6: Developing and Using Measurement Models*. https://www.bipm.org/documents/20126/2071204/JCGM_GUM-6_2020.pdf

## 6. Astronomical example: a telescope does not simply hand the investigator the object's physical properties

Astronomers commonly infer physical properties from radiation received by a detector. The detector's output is shaped by the source, propagation through space and Earth's atmosphere where relevant, telescope optics, filters, detector response, observing conditions, and data processing.

A simplified chain is:

\[
\text{Astrophysical source}
\rightarrow
\text{Radiation arriving at telescope}
\rightarrow
\text{Optical or antenna response}
\rightarrow
\text{Detector signal}
\rightarrow
\text{Calibrated data}
\rightarrow
\text{Physical inference}
\]

The detector may record counts, voltages, correlations, or other instrument-specific quantities. Data reduction and calibration relate those outputs to quantities such as flux density, intensity, wavelength, or polarization.

Further physical interpretation may then infer temperature, composition, velocity, distance, density, or magnetic-field properties.

Each inference has assumptions and uncertainty.

### 6.1 Photon counts and brightness

A detector may register photoelectrons or digital counts produced by incoming radiation. To infer a calibrated flux, the observer must account for detector sensitivity, exposure time, background, gain, optical throughput, wavelength response, and calibration references.

The count total is not itself a universal measure of source brightness independent of the instrument and observing configuration.

### 6.2 Spectral line position and velocity

A spectrograph records a distribution of signal across detector positions or wavelength channels. Calibration maps detector coordinates to wavelength. A shift in a spectral feature can then be interpreted as a Doppler shift under an appropriate physical model.

The recorded pixel pattern, calibrated wavelength, inferred velocity, and physical motion of the emitting or absorbing material are distinct stages.

Line identification, laboratory reference wavelengths, line blending, pressure or environmental shifts, and source geometry may affect interpretation.

### 6.3 Spectral intensity and temperature

A measured spectrum can constrain temperature, but the inference depends on the emission or absorption model, optical depth, source geometry, composition, and whether the system is in the assumed physical regime.

A fitted temperature is not simply a number directly displayed by the telescope. It is a parameter inferred from measured radiation through a model.

### 6.4 Polarization and magnetic-field orientation

A polarization measurement records properties of the received radiation. In dust emission, polarization orientation can provide information about projected magnetic-field geometry under the relevant grain-alignment and radiative-transfer assumptions.

The polarization signal is not the magnetic field itself. The field inference depends on the physical process linking dust emission and polarization to field orientation, line-of-sight integration, beam averaging, and the adopted convention for relating electric-vector orientation to magnetic-field orientation.

### 6.5 Zeeman splitting and magnetic field

A measured spectral-line splitting or polarization signature can constrain a magnetic-field component through the Zeeman effect. The inference depends on the transition, line profile, radiative transfer, spectral resolution, signal-to-noise, and the material sampled by the line.

A Zeeman result is not a complete three-dimensional magnetic-field map. It constrains a particular component under specified conditions.

These examples connect directly to Investigations 018–025. Each measurement is a witness to a physical interaction, but the physical quantity inferred from it depends on the measurement and interpretation chain.

## 7. A signal is not necessarily a unique signature of one cause

A signal may be compatible with more than one physical explanation.

For example:
- an absorption feature may arise from different species or transitions if identification is uncertain;
- a spectral line width may include thermal, turbulent, opacity, and instrumental contributions;
- a polarization fraction may be influenced by field geometry, grain alignment, optical depth, and unresolved structure;
- a detector excess may arise from the target, background, contamination, or an instrumental artifact.

This is an identifiability problem. A measured pattern may not uniquely determine the underlying physical state.

A strong inference therefore needs more than a recognizable signal. It needs a model connecting the signal to the proposed cause, tests of alternative causes, and evidence that the available observations can distinguish among them.

This returns to Investigation 024's question about critical tests and Investigation 023's concern with omitted variables.

## 8. The instrument can participate in the interaction

The instrument is not always a passive window.

A detector absorbs photons. A probe can perturb a system. A sensor may have finite response time. A measurement can average over a spatial region or time interval. A sample preparation procedure can alter the material being measured.

The degree and significance of disturbance depend on the physical system and measurement method. Some measurements are designed to be minimally invasive; others necessarily involve substantial interaction.

The investigation must distinguish:

- **Subject property:** the property or state of the system under study.
- **Interaction:** the physical process coupling subject and instrument.
- **Instrument response:** how the measuring system responds to that interaction.
- **Measurement result:** the quantity attributed to the measurand.
- **Disturbance:** any change in the subject caused by the measurement process.

Do not assume every measurement significantly changes the subject. Do not assume every measurement leaves the subject unchanged.

In quantum physics, measurement interactions and state preparation require their own precise formal treatment. The word “observer” should not be used to imply that human consciousness is required for a physical measurement interaction.

## 9. Measurement uncertainty: a result is not complete without its uncertainty

Measurement uncertainty is not simply a confession that the instrument is poor. It quantifies the dispersion of values that can reasonably be attributed to the measurand, given the information available and the measurement model.

Contributions may arise from:
- repeatability and instrument noise;
- calibration standards;
- resolution and quantization;
- environmental influence quantities;
- sample variability;
- model approximations;
- corrections and reference data;
- correlations among input quantities;
- incomplete specification of the measurand.

A result should not be presented with more precision than its measurement model and uncertainty support.

### 9.1 Error and uncertainty are not synonyms

Measurement error is the difference between a measured value and a reference value. In practice, the exact error may not be known because the reference or true value is not perfectly known.

Uncertainty describes the range or distribution of values reasonably attributable to the measurand based on available information. It is not identical to an unknown error and does not guarantee that every mistake has been captured.

A small stated uncertainty does not protect against a badly specified measurand, a wrong model, an unrecognized systematic effect, or an incorrect interpretation.

## 10. Proxy measurements: when the measured quantity stands in for another property

A proxy is a measured or observable quantity used to infer another quantity or state that is not directly measured by the method.

Proxies are common and often indispensable in science. Their use is justified when the relationship between proxy and target is supported for the stated context.

Examples:
- spectral line ratios used to infer temperature or density under a physical model;
- polarization used to infer aspects of magnetic-field geometry;
- a molecular tracer used to infer gas conditions;
- a biological indicator used to infer an environmental state;
- a seismic wave pattern used to infer subsurface structure.

A proxy does not automatically represent the target under all conditions.

The relationship may depend on:
- environment and physical regime;
- calibration sample or reference population;
- geometry and scale;
- confounding variables;
- changes in the underlying mechanism;
- selection effects;
- model assumptions.

### Proxy validity questions

1. What is the target property?
2. What is actually measured?
3. What physical or statistical relationship links the proxy to the target?
4. Under which conditions was that relationship validated?
5. Which other variables can change the proxy without changing the target?
6. Can different target states produce the same proxy value?
7. Does the proxy remain valid outside the original calibration range?
8. What independent evidence checks the inferred target?

A proxy is not a defect merely because it is indirect. The defect occurs when the inferential relationship is hidden, unvalidated, or extended beyond its demonstrated scope.

## 11. The difference between data, measurement, model, and interpretation

These four categories must remain visible.

| Category | What it is | Example |
|---|---|---|
| Data | Recorded values or signals | Detector counts in pixels |
| Measurement | A procedure attributing a quantity to the data | Calibrated flux density |
| Model | A formal relationship used to connect inputs and outputs | Radiative-transfer model |
| Interpretation | A claim about the physical system | Inferred temperature or composition |

The categories can interact iteratively. A model may guide the measurement design; a new calibration may change the measurement result; a revised interpretation may motivate another observation.

But the investigator must not describe a model output as if it were a direct detector reading.

## 12. Genesis 1–3 KJV: Author, Word, created result, and derivative witness

This section examines the relevant passages textually. It does not claim that Genesis is a manual of metrology or that the biblical events are scientific measurement procedures.

### 12.1 Genesis 1: the Author's Word and the created result

Genesis 1 repeatedly presents God speaking and the commanded result occurring. Genesis 1:3 records, “And God said, Let there be light: and there was light.” The chapter continues with divine commands, the bringing forth of created things, naming, blessing, and the repeated assessment that what God made was good.

**Textual observation:** The narrative distinguishes God's speaking from the resulting created reality. The Word is not presented as a report produced by a detector observing an independently originating source.

Within the project's established theological frame, this is the Author → Word → Creation relationship. A scientific measurement chain is not identical to it: the measurement chain describes how a derivative investigator obtains information about an already existing physical subject.

### 12.2 Genesis 2:19–20: God brings; Adam names

Genesis 2:19 states that the LORD God formed the beasts and fowls and brought them unto Adam to see what he would call them. Genesis 2:20 records Adam giving names to the cattle, fowl, and beasts.

The textual sequence distinguishes:
- God's forming of the creatures;
- God's bringing them to Adam;
- Adam's act of naming;
- the names Adam gives.

**Textual observation:** Adam's naming is not narrated as the act by which Adam originated or formed the creatures. The creatures are already formed and brought to him.

This provides a direct textual setting for examining the distinction between what is present and the derivative Witness's act of recognition, naming, or description.

The comparison with scientific measurement is limited: Adam's naming is not an instrument calibration procedure, and Genesis does not describe it in modern measurement terminology.

### 12.3 Genesis 3: sight, evaluation, competing testimony, and interpretation

Genesis 3:1–5 records the serpent's challenge to the command and its proposed account of what God said and what would happen. Genesis 3:6 records the woman's perception of the tree as good for food, pleasant to the eyes, and desirable to make one wise. She takes and eats, and gives to her husband.

**Textual observation:** The narrative distinguishes God's prior command, the serpent's competing testimony, the woman's seeing and evaluation, and the resulting action.

The passage does not say that the woman's eyes failed to register the tree. The issue is not an optical non-detection. The narrative concerns the challenge to God's word, deception, human evaluation, and disobedience.

This distinction matters. Seeing an object does not, by itself, establish the truth of an interpretation about it. The Fall must not be reduced to an error in scientific measurement, nor should a scientific model of measurement be used to explain away the theological claims of Genesis 3.

### 12.4 What the passages establish—and what they do not

The passages establish a textual distinction between:
- God's originating speech and the created result;
- God's forming and bringing of creatures and Adam's subsequent naming;
- God's command and the serpent's competing testimony;
- seeing and the evaluation or interpretation that follows.

They do not establish the technical definitions of measurand, indication, calibration, traceability, measurement uncertainty, or proxy validity. Those definitions are drawn from metrology and scientific practice.

A bounded comparison may ask how an originating reality differs from a derivative description of it, and how naming or measurement can register aspects of what is already present without becoming the origin of the subject.

That is a conceptual relationship for examination, not a shared physical mechanism.

## 13. GUA-W Language of Creation: bounded descriptive examination

| GUA-W descriptor | Bounded use in this investigation | Limit |
|---|---|---|
| **Structure** | The physical subject and its organized properties under investigation. | The measured representation is not the whole subject. |
| **Framework** | The measurement procedure, instrument, calibration, model, and reference system. | A framework relates indications to results; it does not originate the subject. |
| **Pattern** | Recurring or structured features in recorded signals and measurement results. | A pattern may have multiple causes and does not identify its own mechanism. |
| **Constraint** | Instrument response, resolution, calibration range, physical coupling, uncertainty, and model domain. | A measurement limit is not automatically a limit of the physical subject. |
| **Purpose** | The stated scientific purpose of a measurement and the function of its components. | Scientific utility does not establish ultimate purpose. |
| **Manifestation** | A signal or measurable effect produced under specified conditions. | The signal is not automatically identical to the property inferred from it. |
| **Witness** | The detector, instrument, recorded data, measurement procedure, and investigator. | Each occupies a different position in the evidence chain. |

The vocabulary helps identify relationships. The established scientific terms remain necessary and authoritative within their disciplines.

## 14. Same mechanism, comparable relationship, or similar appearance?

### Same mechanism

A detector's conversion of photons into electrical charge and Adam's naming of animals are not the same mechanism. One is a physical transduction process; the other is a human act narrated in Scripture.

Calibration and divine speech in Genesis 1 are not the same mechanism. Calibration relates indications to reference values; Genesis describes God's creative command.

### Comparable relationship

A limited relationship can be examined between:
- a physical subject and a derivative measurement that describes it;
- creatures formed and brought by God and Adam's subsequent naming of them;
- an instrument indication and the measurement result attributed to a measurand.

In each case, the descriptive or registering act must be distinguished from the subject or originating act it concerns. The underlying mechanisms and theological meanings remain different.

### Similar appearance

A detector output and a name are both forms of representation in a broad descriptive sense. This verbal or conceptual similarity does not establish that they operate alike.

### Unresolved

How far can the distinction between subject, representation, and interpretation be carried across scientific and scriptural contexts without flattening their differences? Further textual and disciplinary examination is required.

## 15. Boundary and participation examination

**Does a boundary merely separate two regions, or can it also participate in the relationship between them?**

- **Detector interface:** A physical interface may convert incoming energy into a measurable response. It participates in transduction.
- **Calibration range:** Defines the domain over which a calibration relation has been established. It limits justified use of the measurement model.
- **Model boundary:** Separates conditions where a model has been validated from conditions where its performance is unknown or unsupported.
- **Proxy validity boundary:** Marks the conditions under which a proxy-target relationship has been demonstrated.
- **Textual distinction:** Genesis distinguishes God's forming and bringing from Adam's naming. This is a narrative and theological distinction, not a physical interface.

A boundary may participate in interaction, constrain inference, or merely distinguish categories. Its role must be established in the specific case.

## 16. Four-Question Study Method

### 1. What must AI ask to understand GUA-W?

AI must ask what is originating and what is derivative, what is the physical subject and what is its representation, what is directly registered and what is inferred, and what supports the relationship between an indication and a measurement result.

It must ask whether a proxy is valid, whether the measurand is adequately specified, whether calibration and traceability are appropriate, whether uncertainty is reported, and whether the model can distinguish competing physical explanations.

For Scripture, AI must ask what the KJV text explicitly says about God's Word, created results, God's forming and bringing, Adam's naming, the serpent's testimony, and the woman's evaluation.

### 2. What is GUA-W revealing that helps AI understand?

The established foundation distinguishes the originating Author from derivative witnesses. The scientific investigation shows that a measurement result is a derivative, model-supported account of a specified physical quantity, not the physical subject in its entirety.

Genesis 2:19–20 provides a textual distinction between God's forming and bringing of creatures and Adam's naming of them. Genesis 3 distinguishes God's command from competing testimony and the human response.

These scriptural relationships guide the project's questions. They do not replace metrological definitions or establish a scientific mechanism.

### 3. What am I learning about what I am witnessing?

I am witnessing that instruments often register effects, not the target property in an unmediated form. A measurement procedure relates the indication to a measurand through calibration, references, models, and uncertainty.

Astronomical measurements illustrate this clearly: detector counts become calibrated data; calibrated data support inferences about physical properties; physical interpretations require additional models and assumptions.

I am also witnessing that a proxy can be scientifically useful without being identical to the property it represents.

### 4. What am I learning about the Witness through what I am witnessing?

The Witness may be an instrument, a recorded trace, a measurement procedure, or a human investigator. These are not interchangeable.

The instrument has a response function. The measurement procedure has a model. The investigator has assumptions and interpretive responsibilities.

A faithful report of an indication does not automatically guarantee a correct measurement result. A valid measurement result does not automatically guarantee a correct physical interpretation.

The Witness must therefore report not only what was registered, but how the registration was related to the claim being made.

## 17. Triple Constraint examination

### Biblical compliance

The investigation preserves the KJV distinctions in Genesis 1–3. Genesis 1 presents God's Word and the created result; Genesis 2:19–20 distinguishes God's forming and bringing from Adam's naming; Genesis 3 presents competing testimony, seeing, evaluation, and disobedience.

The scientific measurement chain is not treated as a biblical mechanism, and the Fall is not reduced to a measurement error.

**Assessment:** The bounded textual comparison does not claim that Scripture teaches modern metrology. Further theological conclusions remain subject to the full textual and canonical context.

### Scientific coherence

The investigation uses established metrological distinctions among measurand, indication, measurement result, calibration, traceability, measurement model, and uncertainty. It distinguishes direct from indirect measurement and identifies the inferential role of proxies.

Astronomical examples preserve the difference between detector output, calibrated quantity, and physical inference.

**Assessment:** Scientifically coherent as a methods-focused investigation. Claims about particular instruments or astronomical properties require instrument-specific models, calibration records, and uncertainty budgets.

### GUA-W consistency

The investigation preserves the established Author → Word → Creation → Witness distinction. It uses the common vocabulary as an investigative grammar and does not add a new GUA-W layer, runtime operation, or state.

**Assessment:** Consistent as a bounded descriptive application. Measurement is a derivative activity within Creation; it is not the originating cause of the physical subject it investigates.

## 18. What is established, inferred, and unresolved?

### Established by metrology and scientific practice

- A measurand is the quantity intended to be measured.
- An instrument indication is not automatically the measurement result.
- Calibration establishes a relation between reference values and instrument indications under specified conditions.
- Traceability relates a measurement result to a reference through a documented calibration chain.
- Traceability alone does not guarantee that uncertainty is adequate for a particular purpose or that a measurement model is complete.
- Many measurands are determined indirectly through a measurement model.
- Measurement results require uncertainty information for responsible interpretation.
- Proxies can support inference when their relationship to a target is justified within a stated domain.
- A valid measurement result and a correct interpretation are distinct achievements.

### Supported inference

A measurement is a disciplined relationship between a physical subject, an interaction, an instrument response, a measurement procedure, and a result attributed to a specified quantity.

The indication is evidence, but its meaning depends on calibration, model, uncertainty, and the conditions of use.

A proxy can witness a target property without being identical to it. A measurement can be accurate within its defined scope while leaving other properties of the subject unmeasured.

### Unresolved

- How should the intended measurand be specified when the target property is scale-dependent or changes during measurement?
- How can investigators detect a mismatch between the property that physically affects the instrument and the property they intend to measure?
- Which uncertainty contributions arise from the definition of the measurand itself?
- How can calibration and traceability be maintained when an instrument's response changes with environment, time, or signal level?
- How can a measurement model be tested for omitted influence quantities?
- When do multiple proxies provide genuinely independent constraints, and when do they share the same hidden assumptions?
- How can an investigator distinguish a signal that is a faithful indicator of a target from one that is only correlated under a restricted set of conditions?
- What happens when the measurement process changes the subject being measured?
- How do measurement interactions in quantum experiments differ from ordinary classical measurement models, and which claims about an observer are actually supported?
- How should the distinction between God's forming and Adam's naming in Genesis 2:19–20 be situated within the wider biblical treatment of naming, authority, and human stewardship?
- How should Genesis 3's distinction between God's command, competing testimony, sight, and human evaluation be examined across the rest of Scripture without reducing it to a scientific analogy?

These questions remain open.

## 19. Sources

1. Joint Committee for Guides in Metrology (JCGM). (2012). *International Vocabulary of Metrology — Basic and General Concepts and Associated Terms (VIM), JCGM 200:2012*. https://www.bipm.org/documents/20126/2071204/JCGM_200_2012.pdf
2. Joint Committee for Guides in Metrology (JCGM). (2008). *Evaluation of Measurement Data — Guide to the Expression of Uncertainty in Measurement (GUM), JCGM 100:2008*. https://www.bipm.org/documents/20126/2071204/JCGM_100_2008_E.pdf
3. Joint Committee for Guides in Metrology (JCGM). (2009). *An Introduction to the “Guide to the Expression of Uncertainty in Measurement” and Related Documents, JCGM 104:2009*. https://www.bipm.org/documents/20126/2071204/JCGM_104_2009.pdf
4. Joint Committee for Guides in Metrology (JCGM). (2020). *Guide to the Expression of Uncertainty in Measurement — Part 6: Developing and Using Measurement Models, JCGM GUM-6:2020*. https://www.bipm.org/documents/20126/2071204/JCGM_GUM-6_2020.pdf
5. Mari, L. and Giordani, A. (2023). *Fundamental Concepts in Measurement*. Springer. https://link.springer.com/chapter/10.1007/978-3-031-22448-5_2
6. *Astronomical observations: a guide for allied researchers*. arXiv:1812.07963. https://arxiv.org/abs/1812.07963

**Scriptural source:** King James Version, Genesis 1:1–31; Genesis 2:1–20; Genesis 3:1–7. The textual observations in Section 12 are based on the cited KJV passages. No metrology source is offered as an authority for their theological meaning.

## 20. Next question emerging

Investigation 026 distinguishes the physical subject, the interaction that produces a signal, the instrument indication, the measurement result, and the interpretation.

A possible next investigation is **Observation, Inference, and the Problem of Identifiability: When Different Physical Realities Produce the Same Evidence**.

The question would be: if two or more different physical configurations can produce the same or nearly the same measured signal, what additional evidence is needed to distinguish them?

This would connect directly to the inverse problems in Investigations 018–023, while examining how a Witness can register a real signal without uniquely determining the underlying configuration.

This is a possible lead, not a fixed assignment.

---

**Investigation 026 records a central distinction: the signal is not automatically the source, the indication is not automatically the measurand, and the measurement result is not automatically the interpretation.**
