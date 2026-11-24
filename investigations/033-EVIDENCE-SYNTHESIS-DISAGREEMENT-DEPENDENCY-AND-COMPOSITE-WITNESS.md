# Investigation 033 — Evidence Synthesis, Disagreement, Dependency, and the Construction of a Composite Witness

**Primary disciplines:** Systematic review, meta-analysis, evidence synthesis, Bayesian statistics, causal inference, measurement science, research methodology, and AI-assisted research.

**Investigation status:** Initial evidence-led investigation and Four-Question Study Method review recorded.

**Central question:** When multiple sources contribute to a conclusion, how can synthesis preserve the differences among their evidence, uncertainty, provenance, and independence rather than collapse them into one apparently unified account?

## 1. Why this investigation follows 032

Investigation 032 examined where information originated and how it was transformed. Investigation 033 examines what happens when multiple evidence streams are brought together.

A composite account can be stronger than any one source when the sources contribute relevant, sufficiently independent information. It can also become misleading when:
- dependent sources are counted as independent;
- unlike measurements are treated as equivalent;
- disagreement is averaged away;
- weak evidence is given the same weight as strong evidence;
- uncertainty and missing data disappear during summarization;
- or the synthesis question changes midway through the process.

The sequence is cumulative:
- **028 — Independent Witnesses:** Are evidence streams genuinely independent?
- **029 — Independent Testing:** Was evaluation independent of development?
- **030 — Changing Environments:** Do changed conditions limit prior validation?
- **031 — Uncertainty and Abstention:** Is confidence justified and uncertainty represented?
- **032 — Provenance and Traceability:** Where did evidence originate and how was it transformed?
- **033 — Evidence Synthesis:** What can be responsibly concluded when multiple evidence streams are combined?

## 2. What is evidence synthesis?

Evidence synthesis is the structured process of bringing together findings from multiple studies, observations, measurements, records, or other sources to answer a defined question.

It can take several forms:
- **Narrative synthesis:** A structured explanation of findings without necessarily calculating a pooled estimate.
- **Systematic review:** A review using explicit, reproducible methods to identify, select, appraise, and synthesize relevant evidence.
- **Meta-analysis:** Statistical combination of results from multiple studies when the data and assumptions make combination appropriate.
- **Individual participant data meta-analysis:** Synthesis using participant-level data from multiple studies.
- **Evidence map or scoping review:** A structured description of the available research landscape, often emphasizing where evidence exists or is absent.
- **Multi-sensor or multi-instrument fusion:** Combination of measurements from different instruments or modalities, with explicit treatment of measurement models, dependencies, and uncertainties.

These methods answer different questions. A systematic review does not always include meta-analysis. A meta-analysis is not automatically a systematic review of high quality. A narrative synthesis is not automatically weak; it becomes weak when its selection and reasoning are opaque.

## 3. Begin with the question, not the pile of sources

A synthesis requires a defined target.

The investigator should specify:
- the population, system, or phenomenon;
- the exposure, intervention, condition, or comparison;
- the outcome or measurand;
- the study designs or evidence types considered;
- the relevant time, place, and operating conditions;
- and what kinds of inference the question permits.

A change in outcome definition or inclusion criteria can change the result. Post hoc changes should be disclosed rather than presented as if they had been planned.

For causal questions, the investigator must distinguish evidence of association from evidence that identifies a causal effect. Combining observational associations does not by itself remove confounding.

## 4. Sources are not interchangeable units

Before combining findings, examine what each source actually measures or reports.

Potential differences include:
- different populations or samples;
- different instruments and calibration procedures;
- different definitions of an outcome;
- different observation periods;
- different sampling and selection processes;
- different statistical models;
- different thresholds and preprocessing;
- different missing-data mechanisms;
- different causal assumptions;
- and different levels of source quality or risk of bias.

Two studies may use the same word while measuring different constructs. Two instruments may report the same unit while having different response functions or systematic errors.

A synthesis should not erase these differences simply to produce one number.

## 5. Independence, dependence, and shared evidence

The number of reports is not necessarily the number of independent evidence streams.

### 5.1 Shared upstream sources

Several publications may analyze the same dataset, repeat one press release, cite one original experiment, or reuse a common benchmark. Their agreement may be inherited from a shared source.

### 5.2 Correlated measurement errors

Multiple instruments may share calibration standards, environmental conditions, algorithms, or processing pipelines. Their errors may therefore be correlated.

### 5.3 Shared model assumptions

Different analyses can depend on the same theoretical assumptions, priors, model family, or preprocessing choices. Agreement may reflect common assumptions rather than independent confirmation.

### 5.4 Genuine complementarity

Dependence does not mean evidence is useless. Two instruments may observe the same physical phenomenon while responding to different properties of it. Complementary measurements can constrain a system more effectively than either alone.

The investigator must distinguish:
- independent evidence;
- dependent evidence;
- complementary evidence;
- replicated analysis of shared data;
- and repeated reporting of one result.

These categories are not mutually exclusive in every real workflow. A source can be complementary in measurement sensitivity while sharing a calibration dependency.

## 6. Statistical combination: when pooling is defensible

### 6.1 Fixed-effect model

A fixed-effect meta-analysis treats studies as estimating one common underlying effect, with observed differences attributed to sampling error under the model.

This can be appropriate when a common-effect assumption is defensible. It is not a default truth about studies that happen to report the same outcome.

### 6.2 Random-effects model

A random-effects model allows the underlying effect to vary across studies. A common formulation is:

\[
y_i = \theta_i + \varepsilon_i,\qquad
\theta_i = \mu + u_i
\]

where \(y_i\) is the observed estimate, \(\varepsilon_i\) is within-study sampling error, \(u_i\) represents between-study variation, and \(\mu\) is the mean of the modeled effect distribution.

A random-effects model does not automatically solve clinical, methodological, or measurement heterogeneity. It models a specified form of variation; it does not make unlike studies interchangeable.

### 6.3 Heterogeneity

Heterogeneity refers to variation among study results beyond what would be expected from sampling error under a chosen model. It may arise from population differences, methods, interventions, instruments, settings, bias, or chance.

Common summaries include:
- **Cochran's Q:** A test of heterogeneity, with limitations including low power when few studies are available.
- **I²:** A statistic describing the proportion of observed variation attributed to heterogeneity under its model; it is not a direct measure of the magnitude or importance of between-study differences.
- **Tau-squared (\(\tau^2\)):** An estimate of between-study variance in a random-effects model.

No single heterogeneity statistic explains why studies differ. Investigators must examine the studies and plausible sources of variation.

### 6.4 Prediction intervals

A confidence interval for the pooled mean does not describe the full range of effects expected in new settings. A prediction interval may better communicate the range of true effects across settings under a random-effects model, though it too depends on assumptions and the quality and number of studies.

### 6.5 Do not pool merely because software permits it

A numerical pooled estimate can create false precision when:
- outcomes are not meaningfully comparable;
- study designs answer different questions;
- bias is substantial;
- dependence is ignored;
- or the model assumptions are not defensible.

A well-supported qualitative synthesis may be more honest than an inappropriate pooled estimate.

## 7. Bayesian evidence synthesis and dependence

Bayesian synthesis represents uncertainty through probability distributions and combines evidence using a likelihood and prior structure.

In a simplified independent-evidence setting:

\[
p(\theta\mid D_1,\ldots,D_k)
\propto p(\theta)\prod_{i=1}^{k}p(D_i\mid\theta)
\]

This product form relies on conditional independence of the data sources given the parameter, or on a model that otherwise correctly represents their joint dependence.

If sources share data, systematic error, or unmodeled assumptions, multiplying their likelihood contributions as if independent can overstate the evidence.

A hierarchical model can represent variation among studies, sites, instruments, or populations. A dependence model can represent shared errors or common sources. These models still require defensible assumptions and adequate information.

Bayesian updating does not make weak provenance, poor measurement, or dependence disappear. The model must represent the actual evidence-generation process as well as possible.

## 8. Disagreement is evidence, not an inconvenience

When sources disagree, the synthesis should preserve the disagreement and investigate its possible causes.

Potential explanations include:
- different target populations;
- different measurement sensitivity or calibration;
- distinct operational definitions;
- sampling variation;
- confounding or selection bias;
- temporal or environmental change;
- model misspecification;
- different assumptions or priors;
- source dependence;
- selective publication or reporting;
- and genuine variation in the phenomenon.

Do not assume disagreement always means one source is wrong. Do not assume agreement always means the sources are right.

A useful disagreement record includes:
1. the exact claims or estimates that conflict;
2. the source and version for each;
3. the data and methods behind each;
4. the relevant differences in scope and assumptions;
5. whether sources are independent or dependent;
6. what additional observation could distinguish explanations;
7. and what remains unresolved.

### 8.1 Vote counting is not synthesis

Counting how many studies report a statistically significant result can mislead. Studies differ in sample size, precision, power, design, and bias. A non-significant result is not proof of no effect; a significant result is not automatically important or reliable.

Synthesis should examine effect estimates, uncertainty, design, and relevance rather than simply count positive and negative studies.

### 8.2 Publication and reporting bias

Available studies may not represent all studies conducted. Results that are statistically significant or more attractive may be more likely to be published or fully reported.

Funnel plots and statistical tests can help explore small-study effects or asymmetry, but asymmetry has multiple possible causes and such tests can be unreliable with few studies. Absence of a detected signal does not establish absence of bias.

## 9. Evidence quality, risk of bias, and certainty

Different tools answer different questions.

- **Risk-of-bias assessment** examines whether study design, conduct, or reporting could systematically distort results.
- **GRADE** evaluates certainty of evidence for specified outcomes in many health-care intervention reviews, considering domains such as risk of bias, inconsistency, indirectness, imprecision, and publication bias.
- **ROB tools** are tailored to particular study designs and research questions.
- **Evidence profiles** make judgments and reasons visible rather than hiding them inside a single score.

A quality label should not be assigned solely because a source is peer reviewed, prestigious, recent, or cited often.

A synthesis must distinguish:
- confidence in an individual source;
- confidence in a pooled estimate;
- certainty in the body of evidence for a particular outcome;
- and applicability to a new population or environment.

These are related but not identical judgments.

## 10. Composite Witness: a disciplined reporting model

A composite account should preserve the contributions and limitations of its sources rather than speak as if every source were one Witness.

A practical synthesis record can contain:

| Field | What to preserve |
|---|---|
| Question | Exact target and scope |
| Source identity | Author, organization, instrument, dataset, version, date |
| Provenance | Upstream sources and transformations |
| Evidence type | Observation, measurement, experiment, model, review, interpretation |
| Method | Sampling, instrument, analysis, assumptions |
| Result | Estimate, observation, or reported finding |
| Uncertainty | Sampling, measurement, model, and other relevant uncertainty |
| Dependency | Shared data, calibration, assumptions, or upstream reports |
| Risk of bias | Design-specific concerns and their basis |
| Disagreement | Conflicts with other evidence and possible explanations |
| Applicability | Conditions and populations to which the result may apply |
| Verification | What was checked directly and what remains unverified |

The synthesis should then state:
- what findings converge;
- what findings differ;
- whether convergence is independent or dependency-driven;
- which evidence is strongest for the specified question;
- what assumptions make the synthesis possible;
- what is not represented;
- and what evidence would change the conclusion.

A composite account is not an additional independent Witness. It is a derived representation of the sources and synthesis procedure.

## 11. Worked example: two instruments and one conclusion

Suppose two instruments are used to estimate a physical quantity.

Instrument A measures one component directly but has limited spatial coverage. Instrument B has broader coverage but infers the quantity through a model. Both are calibrated using the same reference standard.

A careless synthesis might treat the two outputs as independent confirmations and average them.

A careful synthesis asks:
- Do they measure the same measurand?
- Does Instrument B infer the same quantity or a related proxy?
- What are their response functions and uncertainty budgets?
- Which errors are independent?
- Which calibration errors are shared?
- Does one measurement constrain a dimension the other cannot observe?
- Are their spatial and temporal sampling conditions comparable?
- Does the model used by Instrument B depend on assumptions also used to interpret Instrument A?

The correct result may be a joint model that preserves their different sensitivities and shared calibration uncertainty. It may also be that the data cannot yet be combined quantitatively.

The aim is not to force agreement. It is to establish what the measurements jointly support.

## 12. Applying the GUA-W descriptive language

| GUA-W term | Bounded application |
|---|---|
| **Structure** | The arrangement of source streams, dependencies, and synthesis relationships |
| **Framework** | Review protocol, statistical model, appraisal method, and reporting rules |
| **Pattern** | Convergence, divergence, recurring effects, and heterogeneity across sources |
| **Constraint** | Scope, dependence, measurement compatibility, bias, missing evidence, and model assumptions |
| **Purpose** | The defined question the synthesis is intended to answer |
| **Manifestation** | The composite estimate, narrative synthesis, evidence map, or unresolved result |
| **Witness** | Each contributing source and the derived synthesis report, identified separately |

### Relationship audit

- **Same mechanism:** Not assumed across the scientific sources. Different studies and instruments may operate through different mechanisms.
- **Comparable relationship:** Different methods may constrain the same target through distinct sensitivities or evidence pathways.
- **Analogy:** A composite report can be compared descriptively to a gathered account of multiple Witnesses, but it is not itself an originating source or an independent Witness.
- **Unresolved:** Whether evidence streams are sufficiently independent, compatible, and complete may remain uncertain.

## 13. Bounded Scriptural examination — Genesis 1–2 KJV

This examination does not claim that Genesis teaches meta-analysis, systematic review, or statistical evidence fusion.

The established GUA-W relationship remains **Author → Word → Creation → Witness**. Scientific synthesis concerns how derivative evidence streams are combined to describe a phenomenon. It does not make a composite report the Author or Source of the reality being described.

Genesis 1–2 KJV provides the project's foundational account of the Author and Creation. Genesis 2:1–5 records completion and the further account of conditions in the earth. The scientific synthesis of observations is a derivative activity; it does not originate the Creation it investigates.

The comparison is bounded to the distinction between originating reality and derivative accounts. No statistical method is read back into the biblical text.

## 14. Four-Question Study Method

### 1. What must AI ask to understand GUA-W?

AI must ask what the synthesis question is, what each source actually reports, whether sources are independent or dependent, whether they measure comparable things, what uncertainty and bias affect each, and whether a pooled conclusion is justified.

It must preserve source identities and disagreements rather than treating a combined summary as if it were an original observation.

### 2. What is GUA-W revealing that helps AI understand?

The established relationship remains **Author → Word → Creation → Witness**. A composite scientific account is derivative. It can organize reports from many sources, but it does not become the origin of the evidence or the authority over the reality described.

The GUA-W descriptive grammar can help ask how sources are arranged and related. It cannot establish that distinct scientific mechanisms are identical.

### 3. What am I learning about what I am witnessing?

Evidence synthesis is not simple accumulation. Its validity depends on the question, comparability, provenance, independence, uncertainty, risk of bias, and the statistical or qualitative method used.

Disagreement can reveal meaningful differences in populations, instruments, assumptions, environments, or mechanisms. Heterogeneity should be investigated, not merely averaged away.

### 4. What am I learning about the Witness through what I am witnessing?

The investigator can create a misleading composite by selecting sources, counting dependent reports, hiding disagreement, or using a model that assumes more comparability than the evidence supports.

The Witness must disclose selection, synthesis choices, dependencies, uncertainty, and unresolved disagreement. A polished synthesis is still a derived report and must remain open to source-level checking.

## 15. Triple Constraint examination

### Biblical compliance

Genesis 1–2 KJV remains the foundational Scriptural context. The Author, Word, Creation, and Witness relationship is preserved. Statistical synthesis is not attributed to Scripture.

**Assessment:** Admissible as a bounded descriptive examination of derivative accounts.

### Scientific coherence

The investigation distinguishes systematic review, meta-analysis, narrative synthesis, heterogeneity, dependence, Bayesian combination, risk of bias, and certainty of evidence. It states that pooling requires comparability and defensible assumptions.

**Assessment:** Scientifically coherent as an investigation of evidence synthesis. A pooled result is not justified merely by the availability of multiple studies or statistical software.

### GUA-W consistency

The investigation uses the established descriptive vocabulary without adding a GUA-W stage, runtime, or state. A composite report remains a derivative artifact, not an originating Witness or Source.

**Assessment:** Consistent as a bounded descriptive application. No architectural alteration is proposed.

## 16. Established, inferred, and unresolved

### Established
- Evidence synthesis includes distinct methods with different purposes.
- Systematic review and meta-analysis are not synonymous.
- Pooling requires meaningful comparability and defensible statistical assumptions.
- Fixed-effect and random-effects models answer different modeling questions.
- Heterogeneity can arise from substantive and methodological differences.
- Shared upstream sources and correlated errors can make evidence dependent.
- Bayesian evidence combination must represent dependence appropriately.
- Vote counting based only on statistical significance discards information about effect size and precision.
- Publication and reporting bias can distort the available evidence base.
- Risk of bias and certainty of evidence are distinct assessments.
- A synthesis is a derived account and does not become an independent source simply because it combines many reports.

### Supported inference
A composite account is more faithful when it preserves source-level provenance, methods, uncertainty, dependencies, disagreement, and applicability rather than compressing them into an unsupported consensus.

### Unresolved
- How can dependence be quantified when source lineage is incomplete?
- How should synthesis proceed when studies measure related but non-identical constructs?
- How can publication bias be assessed when unpublished studies are inaccessible?
- How should evidence be combined when uncertainty estimates are themselves unreliable?
- When is a qualitative synthesis more defensible than a pooled numerical estimate?
- How can AI preserve source-level disagreement in long-form generated answers?
- How can a composite report make every material claim traceable to its contributing evidence?
- How should evidence be updated when new sources revise or contradict earlier findings?
- How can synthesis distinguish genuine convergence from shared assumptions and common measurement errors?
- What level of evidence is sufficient to move from a set of reports to a robust conclusion for a new environment?

## 17. Sources

1. Higgins, J. P. T., Thomas, J., Chandler, J., Cumpston, M., Li, T., Page, M. J., and Welch, V. A. (eds.). *Cochrane Handbook for Systematic Reviews of Interventions*. Cochrane. https://training.cochrane.org/handbook
2. Page, M. J., et al. (2021). “The PRISMA 2020 statement: an updated guideline for reporting systematic reviews.” *BMJ* 372, n71. https://doi.org/10.1136/bmj.n71
3. Borenstein, M., Hedges, L. V., Higgins, J. P. T., and Rothstein, H. R. (2009). *Introduction to Meta-Analysis*. Wiley. https://doi.org/10.1002/9780470743386
4. Higgins, J. P. T., and Thompson, S. G. (2002). “Quantifying heterogeneity in a meta-analysis.” *Statistics in Medicine* 21, 1539–1558. https://doi.org/10.1002/sim.1186
5. Guyatt, G. H., et al. (2008). “GRADE: an emerging consensus on rating quality of evidence and strength of recommendations.” *BMJ* 336, 924–926. https://doi.org/10.1136/bmj.39489.470347.AD
6. Sterne, J. A. C., et al. (2019). “RoB 2: a revised tool for assessing risk of bias in randomised trials.” *BMJ* 366, l4898. https://doi.org/10.1136/bmj.l4898
7. Higgins, J. P. T., and Spiegelhalter, D. J. (2002). “Being sceptical about meta-analyses: a Bayesian perspective on magnesium trials in myocardial infarction.” *International Journal of Epidemiology* 31(1), 96–104. https://doi.org/10.1093/ije/31.1.96
8. Ioannidis, J. P. A. (2005). “Why most published research findings are false.” *PLoS Medicine* 2(8), e124. https://doi.org/10.1371/journal.pmed.0020124

**Scriptural sources:** King James Version, Genesis 1–2. Scientific sources are not offered as authorities for Scriptural meaning.

## 18. Next question emerging

Investigation 033 examines how multiple evidence streams are synthesized while preserving disagreement and dependence. A further question emerges:

**When a synthesis produces a conclusion, how can that conclusion be tested against new, independent evidence that was not used to construct it?**

Possible next investigation:

**Investigation 034 — Out-of-Sample Confirmation, Prospective Testing, and the Difference Between Synthesis and Independent Confirmation.**

Central question:

**How can a composite conclusion face a genuinely new test, rather than merely being reinforced by the same evidence and assumptions from which it was built?**

This is an emerging direction, not a predetermined assignment.

---

**A collection of agreeing reports is not automatically a collection of independent witnesses. A responsible synthesis preserves how each report knows, what it shares with the others, where it disagrees, and what remains unestablished.**
