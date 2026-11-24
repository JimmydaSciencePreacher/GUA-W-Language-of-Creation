# Investigation 034 — Out-of-Sample Confirmation, Prospective Testing, and the Difference Between Synthesis and Independent Confirmation

**Primary disciplines:** Predictive modeling, statistical learning, experimental design, prospective research, external validation, reproducibility, measurement science, and scientific methodology.

**Investigation status:** Initial evidence-led investigation and Four-Question Study Method review recorded.

**Central question:** How can a conclusion or model assembled from existing evidence face a genuinely new test, rather than merely be reinforced by the same evidence and assumptions from which it was built?

## 1. Why this investigation follows 033

Investigation 033 examined how multiple evidence streams can be synthesized without erasing their dependencies, disagreement, or uncertainty. Investigation 034 asks what happens after a synthesis produces a conclusion.

A conclusion can fit the evidence used to construct it and still fail outside that evidence base. A model can explain its training data, a hypothesis can accommodate known observations, and a composite report can appear coherent—yet each may fail when confronted with observations that were not available during construction.

The sequence is cumulative:
- 028 — Are evidence streams independent?
- 029 — Was evaluation independent of model development?
- 030 — Does changing environment limit generalization?
- 031 — Is uncertainty calibrated and abstention appropriate?
- 032 — Can the source and transformations of evidence be traced?
- 033 — Can multiple sources be synthesized without hiding dependence or disagreement?
- 034 — Can the resulting conclusion withstand a genuinely new test?

## 2. Essential distinctions

### 2.1 Fit is not confirmation

A model's fit to the data used to construct or select it describes how well it accounts for those data under the chosen method. It does not by itself establish performance on new observations.

When a model is repeatedly adjusted in response to a dataset, the dataset becomes part of the development process—even if it is called a test set. Repeated inspection and tuning can gradually adapt the model to the supposed test evidence.

### 2.2 Internal validation

Internal validation estimates performance using the original study sample. Methods include cross-validation and bootstrapping. These methods are valuable for estimating optimism and assessing stability, but they do not provide an entirely new population, time period, or evidence-generation process.

### 2.3 External validation

External validation evaluates a previously developed model in data not used to develop it. Depending on the design, the new data may come from a later period, another institution, another geographic setting, another population, or another measurement environment.

External validation tests transportability to the particular setting represented by the validation data. It does not establish universal validity.

### 2.4 Temporal validation

Temporal validation uses observations from a later time period. It can test whether a result persists as time, practice, equipment, population, or environment changes. The data must be separated so that information from the future does not leak into model development.

### 2.5 Prospective validation

In a prospective design, the protocol is specified before the relevant future outcomes are observed. Predictions or measurements are made and recorded according to that protocol; outcomes are then collected and compared with the pre-specified expectations.

Prospective design can reduce some opportunities for retrospective selection and adaptation. It does not automatically guarantee independence, unbiased measurement, adequate sample size, or generalizability.

### 2.6 Independent replication

Replication is a new attempt to test a result. Independence is a matter of degree and must be described: investigators, data, instruments, materials, analysis, funding, and assumptions may be shared or distinct.

A new analysis of the same data is not a new empirical replication. A new dataset collected by the same group may be a meaningful validation but does not provide the same independence as a separate team using a separate setting. The appropriate description depends on the actual design.

## 3. The validation boundary

A meaningful validation boundary separates information used to construct or select a conclusion from information reserved to test it.

The boundary can be breached by:
- using test observations to select variables or features;
- tuning thresholds after inspecting test outcomes;
- normalizing or imputing data using information from the test set when the deployment setting would not permit it;
- allowing the same subject, site, instrument run, or near-duplicate record to cross development and test partitions;
- selecting the best model after repeatedly comparing many candidates against the same test set;
- using future information to predict an earlier outcome;
- or revising the hypothesis after seeing the purported confirmation.

The relevant question is not simply whether a dataset was labeled “test.” It is whether the information was genuinely unavailable to the development and selection process.

### 3.1 A locked evaluation

A strong validation design may specify in advance:
- the hypothesis or model version;
- the target population and setting;
- inclusion and exclusion criteria;
- the outcome definition;
- the prediction horizon or observation window;
- the data collection procedure;
- the primary performance measures;
- the analysis plan;
- handling of missing or invalid data;
- subgroup and sensitivity analyses;
- and criteria for interpreting success, failure, or inconclusive results.

The model or hypothesis should be frozen for the primary test. Any changes after outcomes become visible should be recorded as model updating or a new hypothesis, not silently folded into the original validation.

## 4. What counts as genuinely new evidence?

Novelty is not one-dimensional. A validation dataset may be new in one respect and dependent in another.

| Dimension | Possible new evidence | Remaining dependency to examine |
|---|---|---|
| Participants or samples | New individuals or specimens | Shared recruitment or selection process |
| Time | Later observations | Same evolving system or data pipeline |
| Location | New site or region | Shared operators, instruments, or standards |
| Investigator | Separate research team | Shared protocol, sponsor, or analysis code |
| Instrument | Different device or modality | Shared calibration or reference standard |
| Data collection | New measurements | Same source population or sampling bias |
| Analysis | Independent implementation | Same assumptions, model family, or specification |
| Hypothesis | Pre-specified prediction | Flexible interpretation after results are known |

A validation is stronger when its sources of dependence are identified and the new test addresses the uncertainty that matters for the claim.

No single dimension automatically makes a test independent. The relevant question is: independent of what, and for which purpose?

## 5. Prediction must precede the outcome

A prospective test is informative when the prediction is fixed before the outcome is known.

A useful record includes:
1. The claim or model being tested.
2. The exact version and date it was frozen.
3. The target and operating conditions.
4. The predicted outcome or measurable expectation.
5. The allowed uncertainty or decision threshold.
6. The data collection and measurement protocol.
7. The analysis plan and any planned exclusions.
8. The outcome and its measurement source.
9. Deviations from protocol.
10. The result, including negative or inconclusive findings.

Predictions need not always be numerical. A qualitative hypothesis can be prospectively tested if the expected observations and criteria for distinguishing alternatives are stated clearly enough to prevent the result from being redefined after the event.

### 5.1 Preregistration

Preregistration records hypotheses, outcomes, methods, and analysis decisions before data collection or before access to relevant outcomes, depending on the design. It helps distinguish confirmatory analysis from exploratory analysis.

Preregistration is not a guarantee of good science. A poorly designed study can be preregistered. Legitimate protocol amendments may be necessary, but they should be dated, justified, and distinguished from the original plan.

### 5.2 Confirmatory and exploratory analysis

**Confirmatory analysis** tests pre-specified claims using pre-specified methods.

**Exploratory analysis** searches for patterns, generates hypotheses, or investigates unexpected results.

Both are scientifically useful. The problem arises when exploratory findings are presented as if they had been predicted in advance. A discovery made after inspecting data can become a hypothesis for a later independent test.

## 6. A worked example: a prediction model

A research team develops a model to predict an outcome from a set of measurements.

**Stage A — Development:** The team chooses variables, trains the model, selects parameters, and evaluates internal performance using cross-validation.

**Stage B — Freeze:** The team records the final model version, input definitions, preprocessing steps, thresholds, intended population, and primary evaluation metrics.

**Stage C — Prospective test:** At a new site or during a later period, the model receives eligible inputs. Predictions are recorded before the outcomes are known. The model is not altered during the primary evaluation.

**Stage D — Outcome assessment:** Outcomes are measured using the pre-specified definition. Predictions are compared with observed outcomes, including calibration, discrimination, error, and subgroup performance as appropriate to the task.

**Stage E — Interpretation:** The team reports performance, uncertainty, missingness, protocol deviations, and limits on applicability.

If performance is poor, the result is not erased. The team investigates why. If the model is updated using the validation data, that dataset has now contributed to development. The updated model needs a new evaluation on data not used in that update.

## 7. Validation is not one universal test

Different claims require different validation designs.

### 7.1 Predictive claims

A predictive model should be evaluated on data that were not used in its development or selection. Relevant measures depend on the task and may include discrimination, calibration, error, decision utility, and subgroup performance.

### 7.2 Causal claims

Predictive accuracy does not establish causality. A model can predict an outcome using proxies or confounded associations without identifying the effect of an intervention.

Causal claims require designs and assumptions appropriate to causal identification, such as randomized experiments or well-justified observational designs. External prediction performance cannot substitute for causal identification.

### 7.3 Measurement claims

A measurement method may need comparison with reference methods, calibration standards, inter-laboratory comparisons, repeatability and reproducibility studies, and tests across relevant operating ranges.

Agreement between two instruments is not sufficient if both share the same systematic error or reference bias.

### 7.4 Mechanistic claims

A proposed mechanism may require interventions, perturbations, measurements of intermediate processes, and predictions that distinguish it from competing mechanisms. Reproducing a correlation alone does not confirm the mechanism.

### 7.5 Practical impact claims

A model can predict accurately without improving decisions or outcomes when used. Claims that a tool improves behavior, safety, health, or cost-effectiveness require impact evaluation, often comparing its use with an appropriate alternative.

Validation of technical performance and validation of real-world impact are distinct.

## 8. Success, failure, and inconclusive results

A validation plan should not define success only after the results are visible.

### Success

A result meets the pre-specified criteria within the tested population, setting, measurement system, and uncertainty. The conclusion should remain limited to that scope.

### Failure

The result contradicts the prediction or fails the pre-specified performance criteria. This is evidence against the tested claim in the tested conditions. It may identify a model limitation, a failed assumption, or a boundary condition.

### Inconclusive

The data are insufficient to distinguish the alternatives or estimate performance with useful precision. Inconclusive is not the same as confirmation or disproof.

### Partial success

A model may perform well overall but fail for particular subgroups, sites, time periods, or conditions. Aggregate performance must not hide consequential failures.

A failed test is not a reason to silently redefine the original prediction. A revised claim may be worth investigating, but it is a new claim with its own evidential history.

## 9. Updating after validation

Validation can reveal that a model requires recalibration, refitting, new variables, changed thresholds, or a different model family.

Updating is legitimate when disclosed. But after validation data are used to change the model, they are no longer an untouched independent test of the updated version.

A disciplined cycle is:

\[
\text{Develop}\rightarrow\text{Freeze}\rightarrow\text{Validate}
\rightarrow\text{Learn}\rightarrow\text{Update}\rightarrow\text{New validation}
\]

This is a descriptive research cycle, not a proposed GUA-W runtime or architectural sequence.

The updated version should carry its own version identifier and validation record. Results for different versions should not be blended as though they came from one unchanged model.

## 10. Common failure modes

| Failure mode | Why it misleads | Safeguard |
|---|---|---|
| Test-set tuning | Test data become development data | Freeze model and analysis before evaluation |
| Temporal leakage | Future information enters past prediction | Enforce time-respecting data separation |
| Duplicate leakage | Near-identical records cross partitions | Group by subject, source, site, or event |
| Repeated test reuse | Repeated decisions adapt to the test set | Reserve new data or account for adaptive use |
| Outcome redefinition | Success criteria change after results | Pre-specify outcomes and disclose amendments |
| Selective reporting | Only favorable metrics or subgroups appear | Report planned and relevant unplanned analyses |
| Shared systematic error | Different sources repeat the same bias | Map calibration and upstream dependencies |
| Overgeneralization | One setting is treated as universal | State tested population and conditions |
| Post hoc explanation | A new story is presented as the original prediction | Separate exploratory findings from confirmation |
| Model updating without new test | Updated model is evaluated on data used to update it | Obtain new independent evaluation data |

## 11. Practical independent-validation audit

For a consequential conclusion, ask:

1. What exact claim, model, or hypothesis is being tested?
2. What version was fixed before the test?
3. Which data were used to construct, tune, select, or interpret it?
4. Were the validation observations genuinely unavailable during those steps?
5. Are there duplicate subjects, events, samples, or records across partitions?
6. Does the validation use new time periods, sites, populations, instruments, or investigators?
7. Which dependencies remain shared?
8. Was the prediction or primary expectation recorded before the outcome?
9. Were outcomes and exclusions defined in advance?
10. Were primary metrics and decision thresholds specified?
11. Were all relevant results, including negative and subgroup results, reported?
12. Were deviations or protocol amendments disclosed?
13. Does the validation test prediction, causation, mechanism, measurement, or practical impact?
14. Does the conclusion stay within the population and conditions actually tested?
15. Was the model changed after seeing validation results?
16. If changed, is there a new untouched dataset for testing the updated version?
17. Can another investigator reconstruct the test from its records?
18. What observation would count against the claim?

## 12. Applying the GUA-W descriptive language

| GUA-W term | Bounded application |
|---|---|
| **Structure** | The arrangement separating development evidence from validation evidence |
| **Framework** | Protocol, model specification, measurement method, and evaluation design |
| **Pattern** | Repeated performance or failure across new observations and settings |
| **Constraint** | Population, time, environment, instrument, protocol, and data-access boundaries |
| **Purpose** | The precise claim or intended use being tested |
| **Manifestation** | Observed outcomes and measured validation results |
| **Witness** | Instruments, investigators, records, datasets, and reports that register the test |

### Relationship audit

- **Same mechanism:** Not asserted across scientific validation and Scriptural testimony.
- **Comparable relationship:** A claim is evaluated against evidence beyond the evidence used to construct it. This is a relationship between a proposed account and an external test.
- **Analogy:** The distinction between an originating source and derivative reports can be compared descriptively with the distinction between a hypothesis and a test of that hypothesis. This does not make the scientific test a theological witness or establish a shared mechanism.
- **Unresolved:** No finite validation program establishes universal performance across all possible populations, times, conditions, or future environments.

## 13. Bounded Scriptural examination — Genesis 1–2 KJV

This investigation does not claim that Genesis teaches preregistration, model validation, experimental design, or statistical testing.

The project's established Scriptural foundation remains the literal KJV account of Genesis 1–2 and the relationship **Author → Word → Creation → Witness**.

The scientific question concerns whether a derivative conclusion can be tested against new observations without allowing the construction process to determine the test result. That is a methodological question about scientific claims. It does not authorize a scientific method to judge, revise, or become the source of the biblical account.

Genesis 2:1–5 remains within its textual context as the account of completed Creation and the conditions described there. The scientific validation concepts in this investigation are not imported into the passage as hidden technical meanings.

The bounded correspondence is only this: a derivative report must not be confused with the source or reality about which it reports. No identity of mechanism is claimed.

## 14. Four-Question Study Method

### 1. What must AI ask to understand GUA-W?

AI must ask whether a conclusion is being repeated from the evidence that created it or tested against evidence that was genuinely outside its construction. It must identify the model or claim version, the validation boundary, shared dependencies, pre-specified expectations, and the limits of the tested setting.

### 2. What is GUA-W revealing that helps AI understand?

The established relationship remains **Author → Word → Creation → Witness**. This investigation does not add a GUA-W stage or reinterpret Genesis as a scientific validation protocol. It uses the established distinction between originating source and derivative account as a bounded descriptive safeguard.

### 3. What am I learning about what I am witnessing?

A model's apparent fit is not independent confirmation. Internal validation, external validation, prospective testing, replication, causal identification, measurement validation, and real-world impact evaluation answer different questions.

A valid test requires a meaningful boundary between construction and evaluation. New data can still share important dependencies. Negative and inconclusive results must remain visible. Updating a model with validation data creates the need for a new test of the updated version.

### 4. What am I learning about the Witness through what I am witnessing?

The investigator can unintentionally protect a favored conclusion by repeatedly changing the model, test, threshold, or interpretation after seeing results. The Witness must be willing to record failure, distinguish prediction from post hoc explanation, and state exactly what the test did and did not establish.

A Witness does not gain independence merely by describing a test as independent. The dependencies and procedures must be examined.

## 15. Triple Constraint examination

### Biblical compliance

Genesis 1–2 KJV remains the foundational Scriptural context. The Author, Word, Creation, and Witness relationship is preserved. No modern validation method is attributed to Scripture.

**Assessment:** Admissible as a bounded descriptive examination.

### Scientific coherence

The investigation distinguishes internal validation, external validation, temporal validation, prospective testing, replication, causal identification, measurement validation, and impact evaluation. It recognizes leakage, adaptive test reuse, shared dependencies, and the limited scope of any finite validation.

**Assessment:** Scientifically coherent. Independent confirmation is a design property that must be demonstrated, not a label assigned to a dataset.

### GUA-W consistency

The established descriptive vocabulary is used without adding a GUA-W stage, runtime, or state. The comparison remains relational and bounded; no scientific validation mechanism is equated with a theological mechanism.

**Assessment:** Consistent as a bounded descriptive application.

## 16. Established, inferred, and unresolved

### Established
- Apparent performance on development data can be optimistic.
- Internal validation uses the original study sample and does not replace external validation.
- External validation tests performance in data not used for model development.
- Validation may be temporal, geographic, institutional, or population-based.
- Prospective protocols can make expectations and evaluation procedures explicit before outcomes are observed.
- Test-set reuse and tuning can compromise independence.
- A model's predictive performance does not establish causal validity or real-world impact.
- Updating a model with validation data means those data are no longer an untouched independent test of the updated version.
- Performance in one validation setting does not establish universal generalizability.

### Supported inference
A conclusion is more credibly tested when the claim and evaluation procedure are fixed before relevant outcomes are observed, the validation evidence is not used to construct the claim, dependencies are disclosed, and the reported conclusion remains within the tested scope.

### Unresolved
- What degree of investigator, instrument, or institutional independence is sufficient for different scientific claims?
- How can independence be assessed when data provenance is incomplete?
- How should prospective validation be designed when the environment changes during data collection?
- What is the best balance between realistic deployment conditions and controlled testing?
- How should multiple external validations be synthesized when their populations and measurement systems differ?
- How can adaptive test-set use be detected in long-running model development?
- What evidence is sufficient to support transfer to a new population or environment?
- How can validation of technical accuracy be connected to evidence of real-world benefit without conflating them?
- How should negative and inconclusive tests alter confidence in a claim?
- What remains untested even after repeated successful validation?

## 17. Sources

1. Collins, G. S., Reitsma, J. B., Altman, D. G., and Moons, K. G. M. (2015). “Transparent Reporting of a multivariable prediction model for Individual Prognosis Or Diagnosis (TRIPOD): The TRIPOD Statement.” *BMJ* 350, g7594. https://doi.org/10.1136/bmj.g7594. The statement distinguishes internal validation from evaluation in other participant data and describes temporal, geographic, and setting-based external validation.
2. Moons, K. G. M., et al. (2015). “The TRIPOD Statement: Explanation and Elaboration.” *Annals of Internal Medicine* 162(1), W1–W73. https://doi.org/10.7326/M14-0698. Discusses model development, validation, transportability, and the distinction between validation and impact studies.
3. Kapoor, S., and Narayanan, A. (2023). “Leakage and the reproducibility crisis in machine-learning-based science.” *Patterns* 4(9), 100804. https://doi.org/10.1016/j.patter.2023.100804. Examines data leakage and the relationship between evaluation data and the distribution to which scientific claims are intended to apply.
4. U.S. Food and Drug Administration. *Clinical Decision Support Software: Guidance for Industry and Food and Drug Administration Staff*. https://www.fda.gov/regulatory-information/search-fda-guidance-documents/clinical-decision-support-software. Discusses transparency about data, validation, and limitations for clinical decision support.
5. Steyerberg, E. W. (2019). *Clinical Prediction Models*, 2nd ed. Springer. https://doi.org/10.1007/978-3-030-16399-0. Provides methodological treatment of prediction model development, validation, and updating.

**Scriptural sources:** King James Version, Genesis 1–2. Scientific sources are not offered as authorities for Scriptural meaning.

## 18. Next question emerging

Investigation 034 examines how a conclusion can face evidence that did not construct it. A further question now emerges:

**When a conclusion succeeds in independent tests, how far may it be carried into new populations, environments, scales, and conditions before its original validation no longer applies?**

Possible next investigation:

**Investigation 035 — Transportability, Scope, and the Limits of Generalization Across Populations and Environments.**

This is a proposed lead, not a predetermined assignment.

---

**A conclusion that survives a new test has passed that test—not every test that could ever be asked of it.**
