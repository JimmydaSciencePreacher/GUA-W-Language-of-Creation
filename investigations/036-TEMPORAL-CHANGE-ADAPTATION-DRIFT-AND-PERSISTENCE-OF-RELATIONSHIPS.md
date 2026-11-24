# Investigation 036 — Temporal Change, Adaptation, Drift, and the Persistence of Relationships

**Primary disciplines:** Time-series analysis, statistical process control, machine learning, evolutionary biology, ecology, climate science, systems science, measurement science, and dynamical systems.

**Investigation status:** Initial evidence-led investigation and Four-Question Study Method review recorded.

**Central question:** When the conditions of a system change over time, how can a Witness distinguish ordinary variation, adaptation, gradual drift, and a genuine change in the relationship being observed?

## 1. Why this investigation follows 035

Investigation 035 examined whether a result can be carried from one population, environment, or scale into another. Investigation 036 adds time: a system's own conditions may change while it is being observed.

A relationship may persist despite changing inputs. A measured variable may drift because an instrument changes. A population may adapt through evolutionary processes. An ecosystem may reorganize after a threshold is crossed. A machine-learning model may become unreliable because the data-generating process has changed.

These phenomena are not interchangeable. The word *drift* is used differently across disciplines, and *adaptation* has specific meanings that must not be casually transferred from biology to engineering or AI.

The sequence is cumulative:
- 028 — Independence of evidence streams.
- 029 — Independence of testing.
- 030 — Distribution shift and changing environments.
- 031 — Uncertainty, calibration, and abstention.
- 032 — Provenance and traceability.
- 033 — Evidence synthesis and dependence.
- 034 — Out-of-sample and prospective confirmation.
- 035 — Scope, transportability, and generalization.
- 036 — Temporal change, adaptation, drift, and persistence.

## 2. First distinction: variation is not automatically change in the underlying relationship

Every measurement contains some combination of signal, noise, uncertainty, and possible bias. A value that differs from an earlier value does not, by itself, demonstrate a change in the system's governing relationship.

Distinguish:

- **Ordinary variation:** Fluctuation expected within a defined process or model.
- **Measurement variation:** Change attributable to the instrument, procedure, observer, sampling, or data-processing pipeline.
- **Environmental variation:** Change in surrounding conditions that may affect the observed system.
- **Distributional change:** A change in the statistical distribution of observations.
- **Relationship change:** A change in a conditional, causal, or structural relationship of interest.
- **State transition:** A system moves from one identifiable state or regime to another.
- **Adaptation:** A process by which a system changes in response to conditions; its meaning depends on the discipline.
- **Drift:** A term whose technical meaning varies by field. Always define what is drifting: a measurement, a distribution, a parameter, a process, or a relationship.

A single unusual observation may be an outlier, an error, a rare but valid event, or an early indication of change. Classification requires context and repeated or corroborating evidence.

## 3. Time-series and process monitoring

### 3.1 Stationarity

A time series is stationary under a specified definition when relevant statistical properties do not change with time. Strict stationarity concerns invariance of the full joint distribution under time shifts. Weak or covariance stationarity typically concerns a constant mean, constant variance, and autocovariance depending only on lag.

Stationarity is not synonymous with a system being motionless or unchanging in every respect. A system may have changing individual values while its statistical process remains stationary. Conversely, a series may look visually stable while important dependencies or conditional relationships change.

The stationarity claim must identify:
- the variable or multivariate process;
- the time window;
- the statistical properties examined;
- the assumptions and test used;
- and the scale at which stationarity is being considered.

### 3.2 Autocorrelation and dependence

Successive observations may be dependent. Treating time-adjacent observations as independent can underestimate uncertainty and create false confidence in detected changes.

Seasonality, cycles, trends, delayed responses, and feedback must be examined before interpreting apparent drift. A periodic pattern may be recurring variation rather than a new regime.

### 3.3 Change-point detection

Change-point methods look for times at which properties of a sequence appear to change. They may detect changes in mean, variance, distribution, regression relationship, or another specified property.

A detected change point is conditional on:
- the chosen data and preprocessing;
- the statistical model;
- the detection threshold;
- the assumed noise process;
- and the method's sensitivity to the type of change.

A change-point alarm does not identify the cause. It indicates that the observations are less compatible with the assumed unchanged process.

### 3.4 Statistical process control

Control charts distinguish common-cause variation within a defined process from signals suggesting special causes. The distinction is operational and model-dependent. Control limits are not automatically specification limits, safety limits, or proof that a process is acceptable.

A process can be statistically stable and still perform badly. A process can be improving or deteriorating while remaining within a broad tolerance band.

## 4. Drift in machine learning and data streams

In machine learning, *concept drift* is often used broadly for temporal change in the data-generating distribution. Some literature distinguishes changes in input distributions from changes in the relationship between inputs and outcomes. Terminology varies, so state the definition used.

Let \(X\) represent inputs and \(Y\) a target.

### 4.1 Covariate or virtual drift

\[
P_t(X)\ne P_{t+1}(X)
\]

The distribution of inputs changes. Under a strict covariate-shift assumption, the conditional relationship \(P(Y\mid X)\) remains stable. That assumption must be checked; it is not guaranteed by observing only input data.

### 4.2 Label or prior shift

\[
P_t(Y)\ne P_{t+1}(Y)
\]

The outcome prevalence changes. Some approaches assume that \(P(X\mid Y)\) remains stable. Again, this is an assumption, not a consequence of a changing class frequency.

### 4.3 Concept or real drift

\[
P_t(Y\mid X)\ne P_{t+1}(Y\mid X)
\]

The relationship between inputs and outcomes changes. A predictor that was useful may become less useful or misleading.

### 4.4 Joint or general distribution change

\[
P_t(X,Y)\ne P_{t+1}(X,Y)
\]

The joint distribution changes. Several kinds of shift may occur together.

### 4.5 Temporal forms of drift

Common descriptions include:
- **Abrupt:** A relatively sudden transition.
- **Incremental:** A relationship or distribution changes progressively.
- **Gradual:** Observations from old and new regimes may coexist during transition.
- **Recurring:** A previously observed distribution or regime returns.

These labels describe the temporal shape of change. They do not identify its cause, whether it is harmful, or whether adaptation is appropriate.

### 4.6 Detection is not explanation

A detector may register a change in input statistics, prediction error, or another monitoring signal. It may not reveal whether the cause is:
- a new population;
- an instrument or software update;
- altered sampling;
- a change in behavior;
- a genuine process change;
- a seasonal cycle;
- or an error in the data pipeline.

Unsupervised monitoring that sees only inputs cannot, in general, establish that the relationship between inputs and unseen outcomes has changed. Outcome labels or another source of relevant evidence may be necessary.

## 5. Adaptation has discipline-specific meanings

### 5.1 Evolutionary adaptation

In evolutionary biology, adaptation commonly refers to a heritable trait shaped by natural selection because it affects reproductive success in a particular environment. The term can also refer to the process of adaptive evolution or, in some contexts, the trait itself.

Natural selection is not the only evolutionary process. Mutation, gene flow, genetic drift, recombination, and population structure also influence evolutionary change.

A trait's present usefulness does not by itself prove that natural selection produced it. Historical evidence, population genetics, comparative evidence, and plausible mechanisms may be needed.

### 5.2 Phenotypic plasticity and acclimation

An organism can change its phenotype in response to environmental conditions without a corresponding genetic change in the population. Phenotypic plasticity describes the capacity of one genotype to produce different phenotypes under different conditions.

Acclimation often refers to physiological adjustment within an individual's lifetime, frequently under controlled or natural environmental change. Usage varies among fields.

These changes must not automatically be called evolutionary adaptation. They operate at different levels and timescales.

### 5.3 Genetic drift

Genetic drift is a change in allele frequencies caused by random sampling effects across generations. It is distinct from natural selection, although both can operate together.

This is especially important for the project's vocabulary: *genetic drift* is not a general synonym for gradual change, system deterioration, or AI concept drift. The shared word does not establish a shared mechanism.

### 5.4 Ecological adaptation and acclimation

Ecological systems may respond to changing conditions through species movement, altered abundance, phenotypic plasticity, evolutionary change, altered interactions, or changes in ecosystem processes. These responses may occur at different rates and can have competing consequences.

An ecosystem's persistence does not necessarily mean that its composition or function remains unchanged.

### 5.5 Engineering and AI adaptation

In engineering, adaptive control changes controller behavior in response to estimated system dynamics or operating conditions. In machine learning, adaptation may update model parameters, representations, or decision thresholds as data change.

An adaptive system can improve performance under some conditions while becoming less reliable under others. Updating can also erase useful older behavior, amplify biased feedback, or adapt to noise.

The term *adaptation* in these domains is functional and technical. It does not imply biological evolution, intention, or a common mechanism.

## 6. Persistence, resilience, and regime change

### 6.1 Persistence

Persistence describes continuation over a stated interval or through specified disturbances. It must identify what persists:
- an entity;
- a population;
- a relationship;
- a function;
- a pattern;
- a state;
- or a measured property.

Persistence of one property does not prove persistence of every property or of the mechanism producing it.

### 6.2 Stability

Stability is defined relative to a system, state, perturbation, and criterion. A system may return to an equilibrium after a small perturbation, remain within a bounded range, or maintain a statistical property. These are different meanings of stability.

### 6.3 Resilience

Resilience has multiple technical definitions. In ecology it often concerns the capacity of a system to absorb disturbance and reorganize while retaining key functions, structures, or feedbacks. In engineering it may concern the ability to withstand disruption and recover or continue operating.

Always state the definition and what property is said to be retained.

### 6.4 Resistance and recovery

Resistance concerns how little a system changes during disturbance. Recovery concerns how it returns after disturbance. A system can have low resistance but high recovery, or high resistance but slow recovery.

### 6.5 Regime shifts and tipping points

A regime shift is a substantial reorganization of system dynamics or state. A tipping point is a threshold beyond which a small additional change can lead to a large or self-reinforcing transition.

Not every abrupt observation is a regime shift. Not every threshold is a tipping point. Evidence should address feedback, alternative explanations, and whether the changed state persists.

### 6.6 Hysteresis

Hysteresis occurs when a system's current state depends not only on current conditions but also on its history. The path by which a condition was reached matters. Reversing the external driver may not immediately restore the prior state.

This means that identical present conditions need not produce identical system states when histories differ.

## 7. Distinguishing the possibilities: an investigation protocol

When observations change over time, examine them in this order. This is a research checklist, not a universal causal sequence.

1. **Verify the record.** Check provenance, timestamps, units, calibration, missingness, and processing changes.
2. **Characterize ordinary variation.** Establish expected noise, autocorrelation, cycles, and sampling variability.
3. **Check the observation process.** Ask whether the instrument, observer, protocol, or data pipeline changed.
4. **Identify the changing quantity.** Is it a level, variance, distribution, parameter, conditional relationship, mechanism, or system state?
5. **Locate the time pattern.** Is the change abrupt, incremental, gradual, recurring, transient, or persistent?
6. **Compare candidate explanations.** Consider environmental change, adaptation, selection, feedback, intervention, and confounding.
7. **Seek independent indicators.** Check whether other measurements or evidence streams register the same change and whether they share upstream dependencies.
8. **Test predictions.** Derive what each explanation predicts for observations not used to construct it.
9. **Assess reversibility and history.** Does the system recover, remain changed, or depend on the path taken?
10. **Bound the conclusion.** State the interval, system, conditions, variables, and uncertainties to which the claim applies.

## 8. Worked example: a sensor network over several years

A sensor network reports a gradual rise in measured temperature.

At least five explanations are possible:
- the physical environment is warming;
- sensors are drifting or aging;
- calibration or maintenance practices changed;
- the network's locations or sampling schedule changed;
- the data-processing pipeline introduced a systematic offset.

The rise alone cannot distinguish these explanations.

A stronger investigation would:
- preserve raw readings and metadata;
- inspect calibration and maintenance records;
- compare co-located reference instruments;
- check whether independent measurement systems show a similar trend;
- examine station moves and changes in exposure;
- test for seasonal patterns and autocorrelation;
- document all corrections;
- and report the remaining uncertainty.

If independent instruments show the same physical trend after known measurement changes are accounted for, the environmental explanation gains support. If only one sensor family shifts after a firmware update, an instrument-related explanation becomes more plausible.

Even then, the cause should be stated in proportion to the evidence. Agreement among instruments is not fully independent if they share calibration standards or processing sources.

## 9. When should a system adapt?

Detecting change does not automatically mean that a system should adapt.

Before updating a model or controller, ask:
- Is the change real or a measurement artifact?
- Is it temporary, seasonal, recurring, or persistent?
- Does the change affect the target outcome or only input frequencies?
- Are new observations representative and sufficiently labeled?
- Could adaptation amplify a feedback loop?
- What older capabilities might be lost?
- Can the previous version be restored?
- Is there an independent evaluation after updating?
- Who or what authorizes changes in a safety-critical system?

A cautious approach may monitor, alert, or abstain before adapting. In some applications, a human decision-maker must review the evidence.

Adaptation is an intervention in the system's behavior. It must be evaluated, not treated as inherently beneficial.

## 10. Practical temporal-change audit

1. What exactly is claimed to have changed?
2. Which variable, distribution, relationship, mechanism, or state is being monitored?
3. What is the time interval and sampling frequency?
4. What variation is expected under the unchanged-process model?
5. Are observations autocorrelated or seasonally structured?
6. Did instruments, calibration, operators, or data processing change?
7. Is the change in inputs, outcomes, or their conditional relationship?
8. Is the change abrupt, incremental, gradual, recurring, or transient?
9. Are there independent measurements, and what dependencies do they share?
10. What alternative causes could produce the same observed signal?
11. What evidence would distinguish adaptation from selection, drift, or measurement change?
12. Does the system return after the disturbance is removed?
13. Is there evidence of hysteresis or a persistent regime shift?
14. What property or function is said to persist?
15. What would falsify the proposed explanation?
16. If a model or system is updated, how will the update be independently evaluated?
17. What older performance or behavior could be lost?
18. What remains unknown?

## 11. Applying the GUA-W descriptive language

| GUA-W term | Bounded application |
|---|---|
| **Structure** | The components and relationships of the system at a specified time |
| **Framework** | The physical, ecological, statistical, or operational conditions within which the system is examined |
| **Pattern** | A temporal recurrence, trend, distribution, or relationship supported by observations |
| **Constraint** | Conditions, boundaries, resources, feedbacks, and operating limits that shape observed change |
| **Purpose** | A demonstrated function or explicitly assigned engineering objective; do not infer ultimate purpose from persistence |
| **Manifestation** | The measured or observed expression at a specified time and under specified conditions |
| **Witness** | Sensors, observers, records, samples, and analysis methods that register change |

### Relationship audit

- **Same mechanism:** Only when a discipline's evidence establishes the mechanism in that domain.
- **Comparable relationship:** Different systems can show persistence, response to disturbance, or changing distributions without sharing a mechanism.
- **Analogy:** A temporal record may serve as a limited analogy for examining what a Witness can and cannot register across time.
- **Surface resemblance:** Similar trends or use of the word *drift* do not establish common cause.
- **Unresolved:** Whether a measured change reflects a new mechanism, changed conditions, or changed observation may remain uncertain.

### Critical vocabulary safeguard: Drift

The word *drift* must always be qualified:
- instrument drift;
- parameter drift;
- data or distribution drift;
- concept drift;
- genetic drift;
- or another discipline-specific usage.

These terms are not synonyms. No equation of genetic drift with AI concept drift, physical entropy, theological Fall, mutation, or system failure is established here.

The project's previously recorded state term **Drift** remains unresolved. This investigation does not redefine it, assign it a cause, or convert a scientific use of the word into a GUA-W state definition.

## 12. Bounded Scriptural examination — Genesis 1–2 KJV

This investigation does not claim that Genesis teaches stationarity, evolutionary adaptation, concept drift, resilience, change-point detection, or dynamical-systems theory.

The project's foundational Scriptural relationship remains **Author → Word → Creation → Witness**. Genesis 1–2 KJV remains the source context for the established GUA-W foundation. Scientific descriptions of temporal change are examined within their own disciplines and are not inserted into the biblical text as hidden technical meanings.

The distinction relevant to this investigation is one of source and report: a scientific Witness records phenomena over a defined interval and under defined conditions. Its temporal record may be incomplete, its measurement may be limited, and its interpretation may require revision. Those limitations concern the derivative scientific account; they do not authorize alteration of the Scriptural source.

No scientific theory of biological or physical change is offered as a replacement for the biblical account, and no theological conclusion is inferred from a statistical trend alone.

## 13. Four-Question Study Method

### 1. What must AI ask to understand GUA-W?

AI must ask what is changing, what is persisting, what is merely varying, and what evidence distinguishes these possibilities. It must identify the discipline-specific meaning of drift or adaptation, the time scale, measurement process, causal assumptions, and the boundaries of any conclusion. It must not import one discipline's definition into another.

### 2. What is GUA-W revealing that helps AI understand?

The established source relationship remains **Author → Word → Creation → Witness**. The shared investigative vocabulary asks what structure and pattern are observable, what constraints and conditions apply, what manifestation is registered, and what the Witness can actually detect. It does not predetermine a scientific mechanism or alter the established architecture.

### 3. What am I learning about what I am witnessing?

Temporal change can occur in measurements, distributions, relationships, mechanisms, and system states. These are different objects of investigation. Adaptation has distinct biological, ecological, engineering, and machine-learning meanings. Persistence and resilience must identify what property is retained and under which disturbance. A change detector can identify a statistical signal without explaining its cause.

### 4. What am I learning about the Witness through what I am witnessing?

The Witness may mistake a changed record for a changed reality, a recurring pattern for a permanent law, or a familiar word for a shared mechanism. The Witness may also protect a favored model by adapting it too quickly or by dismissing observations that do not fit.

A disciplined Witness preserves the earlier record, tracks changes in instruments and assumptions, seeks independent indicators, distinguishes detection from explanation, and reports when the cause remains unknown.

## 14. Triple Constraint examination

### Biblical compliance

Genesis 1–2 KJV remains the foundational Scriptural context. The Author, Word, Creation, and Witness relationship is preserved. Modern scientific categories are not attributed to the text.

**Assessment:** Admissible as a bounded descriptive examination.

### Scientific coherence

The investigation distinguishes variation, measurement change, distribution shift, relationship change, adaptation, genetic drift, resilience, stability, and regime shifts. It recognizes that temporal detection is not causal explanation and that terminology varies across disciplines.

**Assessment:** Scientifically coherent, provided each use of *drift*, *adaptation*, *persistence*, and *stability* is explicitly defined.

### GUA-W consistency

The established vocabulary is used as an investigative grammar. The unresolved GUA-W term Drift is not redefined, and no stage, runtime, or state is added or altered.

**Assessment:** Consistent as a bounded descriptive application.

## 15. Established, inferred, and unresolved

### Established
- Time-dependent data may violate assumptions of a time-invariant distribution.
- Stationarity has specific statistical definitions and is not equivalent to an absence of change in every system property.
- Change-point detection can identify statistical changes but does not by itself establish their causes.
- Concept drift terminology varies; changes in input distributions and changes in input-outcome relationships must be distinguished.
- Unsupervised input monitoring cannot, by itself, establish a change in an unobserved outcome relationship.
- Biological adaptation, phenotypic plasticity, acclimation, and genetic drift refer to distinct concepts.
- Persistence, stability, resistance, recovery, and resilience describe different properties.
- Hysteresis means system behavior can depend on its history.
- Adaptation of a model or controller must be evaluated because updating can introduce new errors or remove previous capabilities.

### Supported inference
A temporal-change claim is more defensible when the investigator defines the property being monitored, verifies the measurement process, accounts for expected variation and dependence, distinguishes distributional from relationship change, tests competing explanations, and bounds the conclusion to the observed time interval and conditions.

### Unresolved
- How can an investigator distinguish a very slow drift from a long-period cycle when the observation window is limited?
- What evidence is sufficient to identify a genuine change in mechanism rather than a change in conditions?
- How should monitoring thresholds be selected when false alarms and missed changes have unequal costs?
- When does adaptation improve a system, and when does it destabilize or degrade it?
- How can interacting forms of change be separated when multiple drivers evolve together?
- How can a system's history be measured well enough to test hysteresis?
- What does persistence mean when components change but function remains?
- How can a Witness distinguish a recurring regime from a genuinely new state?
- Which forms of drift, if any, might be relevant to the still-unresolved GUA-W state term—and what evidence and source constraints would be required before making any comparison?
- What is the proper boundary between a scientific description of change and a theological claim about the source or meaning of Creation?

## 16. Sources

1. Hinder, F., Vaquet, V., and Hammer, B. (2024). “One or two things we know about concept drift—a survey on monitoring in evolving environments. Part A: detecting concept drift.” *Frontiers in Artificial Intelligence* 7. https://doi.org/10.3389/frai.2024.1330257. Reviews definitions and monitoring of drift, including temporal forms and the distinction between changes in marginal and conditional distributions.
2. Hinder, F., Vaquet, V., and Hammer, B. (2024). “One or two things we know about concept drift—a survey on monitoring in evolving environments. Part B: locating and explaining concept drift.” *Frontiers in Artificial Intelligence* 7. https://doi.org/10.3389/frai.2024.1330258. Examines causes, localization, and explanation of drift.
3. Lukats, D., Zielinski, O., Hahn, A., and Stahl, F. (2024; published in *International Journal of Data Science and Analytics*, 2025). “A benchmark and survey of fully unsupervised concept drift detectors on real-world data streams.” https://doi.org/10.1007/s41060-024-00620-y. Reviews unsupervised detection and its limits when outcome labels are unavailable.
4. Gama, J., Žliobaitė, I., Bifet, A., Pechenizkiy, M., and Bouchachia, A. (2014). “A survey on concept drift adaptation.” *ACM Computing Surveys* 46(4), Article 44. https://doi.org/10.1145/2523813.2523815. Reviews concept drift and adaptation in learning systems.
5. Holling, C. S. (1973). “Resilience and Stability of Ecological Systems.” *Annual Review of Ecology and Systematics* 4, 1–23. https://doi.org/10.1146/annurev.es.04.110173.000245. Foundational discussion distinguishing resilience and stability in ecological systems.
6. Scheffer, M., et al. (2001). “Catastrophic shifts in ecosystems.” *Nature* 413, 591–596. https://doi.org/10.1038/35098000. Reviews abrupt regime shifts and mechanisms that can produce them.
7. Pigliucci, M. (2001). *Phenotypic Plasticity: Beyond Nature and Nurture*. Johns Hopkins University Press. Examines phenotypic plasticity and its relationship to evolutionary biology.
8. Futuyma, D. J., and Kirkpatrick, M. (2017). *Evolution*, 4th ed. Sinauer Associates. Provides standard evolutionary definitions and distinctions among natural selection, mutation, gene flow, and genetic drift.

**Scriptural sources:** King James Version, Genesis 1–2. Scientific sources are not offered as authorities for Scriptural meaning.

## 17. Next question emerging

Investigation 036 examines temporal change and the persistence of relationships. A further question now emerges:

**When several interacting processes change together, how can a Witness distinguish the contribution of each process from the behavior of the whole system?**

Possible next investigation:

**Investigation 037 — Interacting Processes, Feedback, Emergence, and the Limits of Single-Cause Explanation.**

This is a proposed lead, not a predetermined assignment.

---

**A changing observation does not tell us, by itself, what changed. The Witness must distinguish the change in the record, the change in the conditions, and the change in the relationship being reported.**
