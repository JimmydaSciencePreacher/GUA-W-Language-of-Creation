# Investigation 035 — Transportability, Scope, and the Limits of Generalization Across Populations and Environments

**Primary disciplines:** External validity, causal inference, statistical learning, prediction modeling, ecology, evolutionary biology, measurement science, experimental design, and philosophy of science.

**Investigation status:** Initial evidence-led investigation and Four-Question Study Method review recorded.

**Central question:** When a conclusion succeeds in independent tests, how far may it be carried into new populations, environments, scales, and conditions before its original validation no longer applies?

## 1. Why this investigation follows 034

Investigation 034 examined whether a conclusion can withstand evidence that did not construct it. Investigation 035 examines the scope of the conclusion after it passes such a test.

A result can be reproducible in one setting and fail elsewhere. A prediction model can perform in one hospital but not another. A physical measurement can be reliable within a calibrated range but not outside it. An ecological relationship can hold in one habitat and change under different environmental conditions.

A successful independent test is evidence about the conditions tested. It is not a guarantee about every untested condition.

The sequence is cumulative:
- 028 — Independence of evidence streams.
- 029 — Independence of testing.
- 030 — Distribution shift and changing environments.
- 031 — Uncertainty, calibration, and abstention.
- 032 — Provenance and traceability.
- 033 — Evidence synthesis and dependence.
- 034 — Out-of-sample and prospective confirmation.
- 035 — Scope, transportability, and the limits of generalization.

## 2. Essential terms

### 2.1 External validity

External validity concerns whether inferences from a study apply beyond the specific sample, setting, or conditions in which the study was conducted.

It is not a property established by a single universal score. It is a reasoned judgment about a particular claim and a particular target context.

### 2.2 Generalizability

Generalizability is often used broadly for the applicability of findings to other people, settings, or circumstances. Usage varies across disciplines. State the intended meaning rather than assuming a universal definition.

### 2.3 Transportability

In causal inference, transportability has a more specific meaning: whether causal information learned in a source population or environment can be transferred to a target population or environment, given explicit assumptions and whatever target-population information is available.

Pearl and Bareinboim formalize this problem using selection diagrams and causal inference methods. Their framework makes the assumptions about differences and commonalities between source and target populations explicit. Transfer is not licensed merely because the source study was well conducted.

### 2.4 Reproducibility and transport are different

A result may reproduce in a similar setting yet fail in a substantially different one. Conversely, a result may be transported with a justified model and target-population information even when the target data are not a simple replica of the source data.

The investigator must state whether the question is:
- Does the result recur under similar conditions?
- Does it hold in a different but related setting?
- Can it be transferred to a distinct target population?
- Does it persist under a changed environment or intervention?
- Does it remain valid at a different spatial, temporal, or organizational scale?

These are different tests.

## 3. Define source and target before claiming transfer

A transportability question needs an explicit source and target.

**Source domain:** The population, environment, system, or measurement context from which the original evidence was obtained.

**Target domain:** The population, environment, system, or context to which the conclusion is proposed to apply.

Describe both:
- population or system boundaries;
- inclusion and exclusion conditions;
- time period;
- geography and setting;
- relevant environmental conditions;
- measurement instruments and procedures;
- outcome definitions;
- intervention or exposure conditions;
- and the causal or statistical relationships assumed to remain stable.

A statement such as “the result generalizes” is incomplete without specifying where, to whom, for what outcome, and under which conditions.

## 4. What can change between source and target?

A source and target may differ in several ways.

| Dimension | Example of change | Potential consequence |
|---|---|---|
| Population composition | Age, health, experience, genetic or demographic composition | Different baseline risks or effect modifiers |
| Selection process | Different recruitment or inclusion criteria | Selection bias or different sampled relationships |
| Geography | Climate, altitude, soil, infrastructure, location | Changed operating conditions |
| Time | New technology, policy, behavior, or disease prevalence | Temporal drift |
| Environment | Temperature, pressure, resources, habitat | Changed physical or biological response |
| Measurement | New sensor, calibration, assay, or observer | Measurement non-equivalence |
| Practice | Different procedures or operator behavior | Changed implementation |
| Intervention | Different dose, version, timing, or delivery | Changed causal effect |
| Scale | Individual to population, local to global, micro to macro | Emergent behavior or aggregation effects |
| Institutional setting | Primary versus specialist care, laboratory versus field | Different processes and case mix |
| Data process | New coding, missingness, sampling, or preprocessing | Distribution and measurement shift |

A difference does not automatically invalidate transfer. It identifies a question that must be assessed.

## 5. Mechanisms, effect modifiers, and stable relationships

A central task is to determine which relationships are expected to remain stable and which may vary.

### 5.1 Effect modifiers

An effect modifier is a variable across whose levels the effect of an exposure or intervention differs, under the chosen scale and estimand.

If an intervention works differently in different populations, the target population's distribution of effect modifiers matters.

### 5.2 Confounding and selection

A source study's associations may depend on confounding structures or selection processes that differ in the target domain. A causal effect cannot be transported by simply carrying over an observed association.

### 5.3 Mechanism stability

A proposed mechanism may be stable across settings while the observed result changes because the surrounding conditions differ. Alternatively, a mechanism itself may change or cease to operate under target conditions.

Mechanism stability must be supported, not assumed. A plausible story about why a relationship should persist is not a substitute for evidence or a clearly stated causal model.

### 5.4 Invariance

Some scientific relationships remain stable under specified transformations or across specified environments. Invariance is always relative to the variables, transformations, and domain being considered.

Do not call a relationship universal merely because it remained stable across a small set of tested environments.

## 6. Formal view: transporting causal information

Pearl and Bareinboim's transportability framework distinguishes a source domain from a target domain and represents differences using selection diagrams.

The basic question is not “Are the populations identical?” They need not be. The question is whether the causal quantity of interest can be identified in the target using source information, target observations, and defensible assumptions about which causal relations differ.

A schematic expression is:

\[
P_T(Y\mid do(X=x))
\]

where the subscript \(T\) denotes the target population. The goal is to determine whether this target causal effect can be derived from available source experimental evidence and target-domain information.

The expression does not itself supply the answer. Identification depends on the causal structure and assumptions.

### 6.1 Selection diagrams

Selection diagrams use special nodes or edges to represent differences between domains in relevant mechanisms or distributions. These diagrams help make explicit where source and target may differ.

The diagram is a model of assumptions, not direct proof that the assumptions are true. Its conclusions are conditional on its adequacy.

### 6.2 Data-driven approaches

Methods may use target-population data to reweight source observations, adjust for differences in covariate distributions, or combine heterogeneous datasets.

Examples include:
- importance weighting or density-ratio weighting;
- standardization and outcome modeling;
- calibration or recalibration;
- hierarchical or multi-site models;
- data augmentation;
- and internal-external cross-validation across sites.

Each method has assumptions. Reweighting, for example, requires adequate overlap: target cases must not require extrapolation into regions unsupported by the source data. Extreme weights can make estimates unstable.

### 6.3 Knowledge-driven approaches

Causal knowledge can help identify which relationships are expected to remain stable and which may change. This can reduce the need to treat every variable as freely transferable.

But causal assumptions must be justified. A diagram or expert judgment does not become evidence merely because it is formalized.

## 7. Distribution shift is not one phenomenon

A target domain may differ from the source in several statistical ways.

### 7.1 Covariate shift

The distribution of predictors changes while the conditional relationship between predictors and outcome is assumed stable:

\[
P_T(X)\ne P_S(X),\qquad P_T(Y\mid X)=P_S(Y\mid X)
\]

This assumption may support reweighting approaches when overlap and other conditions are adequate.

### 7.2 Label shift

The outcome prevalence or class distribution changes while the conditional distribution of predictors given the outcome is assumed stable:

\[
P_T(Y)\ne P_S(Y),\qquad P_T(X\mid Y)=P_S(X\mid Y)
\]

This also requires assumptions and reliable estimates.

### 7.3 Concept shift

The relationship between predictors and outcome changes:

\[
P_T(Y\mid X)\ne P_S(Y\mid X)
\]

A model that relies on the old relationship may become miscalibrated or inaccurate. Reweighting predictor frequencies alone does not solve a changed conditional relationship.

### 7.4 Measurement shift

The target system may record variables differently because of a changed instrument, coding system, protocol, or observer. Apparent distribution shift can therefore arise from changed measurement rather than changed underlying phenomenon.

These categories are useful diagnostics, not exhaustive or mutually exclusive descriptions of every real-world change.

## 8. Scale matters

A relationship at one scale may not hold at another.

### 8.1 Spatial scale

A pattern observed locally may not persist regionally or globally. Local conditions, boundaries, and interactions can matter.

### 8.2 Temporal scale

A short-term response may differ from a long-term response. Feedback, adaptation, cumulative effects, and changing conditions can alter the observed pattern.

### 8.3 Organizational scale

Individual behavior does not automatically predict group behavior. Aggregation can create or conceal relationships. This is one reason ecological inference and the ecological fallacy require care.

### 8.4 Physical and biological scale

A mechanism at molecular scale may contribute to a cellular process, but the higher-level behavior can depend on additional interactions and constraints. A lower-level account does not automatically exhaust the higher-level phenomenon.

Scale transitions require evidence and an explicit account of what is preserved, what changes, and what new interactions appear.

## 9. Worked example: a model moved to a new environment

A predictive model is developed in a group of hospitals and externally validated in another hospital. It performs well in that validation.

The organization then proposes using it across a national network, including rural clinics and specialist centers.

The original validation is relevant, but it does not establish performance in every new site.

The transport assessment should ask:
- Do the new sites serve similar populations?
- Are referral patterns and disease prevalence different?
- Are measurements collected using the same instruments and protocols?
- Are predictors coded consistently?
- Are missing data generated in the same way?
- Are treatment practices and outcome definitions comparable?
- Does the model depend on variables that behave differently in the target sites?
- Is there adequate overlap between source and target cases?
- Which sites can be used for prospective validation?
- What monitoring will identify performance deterioration after deployment?

A defensible plan might include site-specific external validation, recalibration where justified, prospective evaluation, subgroup reporting, and continued monitoring. If the model is updated using target data, the updated version requires an appropriately independent evaluation.

The conclusion should be limited to the sites and conditions for which supporting evidence exists.

## 10. A transferability audit

For a claim proposed for a new domain, ask:

1. What exact result or relationship is being transferred?
2. What was the source population, environment, or scale?
3. What is the target population, environment, or scale?
4. Which differences between source and target are known?
5. Which differences are unknown or unmeasured?
6. Which variables may modify the relationship or effect?
7. Which causal or statistical relationships are assumed invariant?
8. What evidence supports those invariance assumptions?
9. Are measurement procedures comparable?
10. Is the target represented in the source data, or is extrapolation required?
11. Is there adequate overlap or positivity for the intended method?
12. Could selection, confounding, or missingness differ?
13. Are spatial, temporal, or organizational scale changes involved?
14. What target-domain data are available?
15. What external or prospective validation is needed?
16. What would indicate that the relationship no longer transports?
17. Does the claim distinguish evidence-supported transfer from theoretical possibility?
18. Is the conclusion limited to the tested target domain?

## 11. What a successful transfer claim should report

A responsible transfer report identifies:
- the source and target domains;
- the result or causal quantity of interest;
- the differences considered;
- the assumptions required;
- the data used from each domain;
- the method used to adjust or transport;
- the overlap and extrapolation limits;
- uncertainty and sensitivity analyses;
- external or prospective validation results;
- and the target settings to which the conclusion may reasonably apply.

A statement of transferability without these details is difficult to evaluate.

## 12. Applying the GUA-W descriptive language

| GUA-W term | Bounded application |
|---|---|
| **Structure** | The organization of source and target systems, their components, and their relationships |
| **Framework** | The scientific model, measurement method, causal diagram, or transfer procedure |
| **Pattern** | A relationship observed across specified populations, environments, or scales |
| **Constraint** | Conditions, boundaries, mechanisms, and domain differences that limit transfer |
| **Purpose** | The defined scientific question or intended use; do not infer ultimate purpose from predictive usefulness |
| **Manifestation** | The observed or measured result in a specified target context |
| **Witness** | Instruments, samples, observers, datasets, and reports that register the source and target phenomena |

### Relationship audit

- **Same mechanism:** Must be demonstrated within the particular scientific domain; it is not inferred from similar results alone.
- **Comparable relationship:** A relationship may remain similar across domains even when the underlying mechanisms or surrounding conditions differ.
- **Analogy:** A source-to-target comparison may be used as a limited analogy for examining scope, but analogy does not establish common mechanism.
- **Unresolved:** Whether a relationship remains invariant outside tested conditions may remain unknown.

The shared descriptive vocabulary must earn its usefulness in each domain. If a term does not clarify the evidence, do not force it into the account.

## 13. Bounded Scriptural examination — Genesis 1–2 KJV

This investigation does not claim that Genesis teaches external validity, causal transportability, distribution shift, or scale invariance.

The project's foundational Scriptural relationship remains **Author → Word → Creation → Witness**. The scientific investigation asks whether findings obtained in one specified domain may be applied to another domain. That is a question about the scope of scientific evidence and the assumptions needed for transfer.

Genesis 1–2 KJV remains the foundation from which the project's descriptive language is investigated. The scientific terms in this document are not inserted into the text as hidden technical meanings, nor do scientific transfer methods authorize changes to the Scriptural source.

The bounded comparison is that a derivative scientific account must state the conditions and scope of what it reports. The scope of a scientific model is not the scope or authority of the Author.

## 14. Four-Question Study Method

### 1. What must AI ask to understand GUA-W?

AI must ask what the source domain is, what target domain is proposed, which relationships are claimed to persist, what conditions differ, and what evidence or assumptions support transfer. It must identify when it is extrapolating beyond observations and distinguish a demonstrated transfer from a plausible hypothesis.

### 2. What is GUA-W revealing that helps AI understand?

The established foundation remains **Author → Word → Creation → Witness**. The investigative grammar provides questions about structure, framework, pattern, constraint, purpose, manifestation, and Witness. It does not guarantee that every scientific relationship will transfer across every domain, nor does it replace the scientific explanation.

### 3. What am I learning about what I am witnessing?

External validity and transportability are specific to a claim and target domain. Population composition, environment, measurement, time, scale, selection, and causal mechanisms can affect transfer. Some differences can be adjusted for under explicit assumptions; others may require new data or make transfer unsupported.

A successful validation in one setting is a bounded result. It is not a universal certificate.

### 4. What am I learning about the Witness through what I am witnessing?

The Witness can overextend a result by carrying a conclusion beyond the conditions in which it was observed. Familiarity, successful replication, and mathematical formalism do not eliminate the need to examine target-domain differences.

The Witness must state the reach of the evidence, identify extrapolation, preserve unknowns, and remain willing to narrow a claim when its scope is not supported.

## 15. Triple Constraint examination

### Biblical compliance

Genesis 1–2 KJV remains the foundational Scriptural context. The Author, Word, Creation, and Witness relationship is preserved. Modern scientific concepts are not attributed to the biblical text.

**Assessment:** Admissible as a bounded descriptive examination.

### Scientific coherence

The investigation distinguishes external validity, generalizability, transportability, distribution shift, effect modification, causal assumptions, measurement differences, and scale. It recognizes that transfer methods rely on explicit assumptions and target-domain evidence.

**Assessment:** Scientifically coherent. No result is treated as universal merely because it passed a finite set of validation tests.

### GUA-W consistency

The established descriptive vocabulary is applied as an investigative grammar, not as a forced taxonomy or replacement for scientific mechanisms. No GUA-W stage, runtime, or state is added or altered.

**Assessment:** Consistent as a bounded descriptive application.

## 16. Established, inferred, and unresolved

### Established
- External validity concerns application beyond the original study sample and conditions.
- Transportability can be formalized for causal effects across source and target populations.
- Transfer depends on assumptions about differences and commonalities between domains.
- Distribution shift can involve changes in predictors, outcomes, or predictor-outcome relationships.
- Measurement changes can create apparent differences between source and target data.
- Reweighting and other data-driven approaches require assumptions such as adequate overlap.
- Relationships can vary across spatial, temporal, and organizational scales.
- External validation in one target dataset does not establish performance in all possible targets.
- A conclusion should state the domain and conditions to which its evidence applies.

### Supported inference
A transfer claim is more defensible when the source and target are explicitly described, the relationships assumed to remain stable are identified, target-domain differences are measured or bounded, and the transferred result is evaluated in the intended target context.

### Unresolved
- How can relevant domain differences be identified when important variables are unmeasured?
- How should a transfer claim be bounded when target environments change continuously?
- What evidence is sufficient to justify invariance of a mechanism or causal relationship?
- How can scale-dependent effects be distinguished from genuine failures of transfer?
- How should multiple target domains be synthesized when each requires different adjustments?
- How can transferability be assessed when source and target populations have little or no overlap?
- When does recalibration suffice, and when is a new model or theory required?
- How can an AI system reliably detect when a user asks it to extrapolate beyond its evidence?
- How should monitoring identify gradual loss of transportability after deployment?
- What would justify a claim of broad generality, and what would remain outside its scope?

## 17. Sources

1. Pearl, J., and Bareinboim, E. (2014). “External Validity: From Do-Calculus to Transportability Across Populations.” *Statistical Science* 29(4), 579–595. https://doi.org/10.1214/14-STS486.
2. Bareinboim, E., and Pearl, J. (2013). “A General Algorithm for Deciding Transportability of Experimental Results.” *Journal of Causal Inference* 1(1), 107–134. https://doi.org/10.1515/jci-2012-0004.
3. Ploddi, K., Martin, G. P., O’Connell, M., et al. (2026). “Scoping review of methodology for aiding generalisability and transportability of clinical prediction models.” *Diagnostic and Prognostic Research* 10, 25. https://doi.org/10.1186/s41512-026-00237-8.
4. Van Calster, B., McLernon, D. J., van Smeden, M., Wynants, L., and Steyerberg, E. W. (2020). “Calibration: the Achilles heel of predictive analytics.” *BMC Medicine* 18, 230. https://doi.org/10.1186/s12916-020-01655-5.
5. Debray, T. P. A., Riley, R. D., Rovers, M. M., Reitsma, J. B., and Moons, K. G. M. (2013). “Individual participant data meta-analysis for a binary outcome: one-stage or two-stage?” *PLoS ONE* 8(4), e60650. https://doi.org/10.1371/journal.pone.0060650.
6. “External validation of prognostic models: what, why, how, when and where?” (2021). *BMJ* / open-access review. https://pmc.ncbi.nlm.nih.gov/articles/PMC7857818/.

**Scriptural sources:** King James Version, Genesis 1–2. Scientific sources are not offered as authorities for Scriptural meaning.

## 18. Next question emerging

Investigation 035 examines how far findings may be transferred across populations, environments, and scales. A further question emerges:

**When the conditions of a system change over time, how can a Witness distinguish ordinary variation, adaptation, gradual drift, and a genuine change in the relationship being observed?**

Possible next investigation:

**Investigation 036 — Temporal Change, Adaptation, Drift, and the Persistence of Relationships.**

This is a proposed lead, not a predetermined assignment.

---

**A conclusion may travel only as far as its evidence and assumptions permit. A successful result in one domain is not a universal passport into every other domain.**
