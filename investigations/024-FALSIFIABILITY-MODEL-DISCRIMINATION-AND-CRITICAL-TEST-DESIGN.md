# Investigation 024 — Falsifiability, Model Discrimination, and Critical-Test Design

**Primary disciplines:** Philosophy of science, experimental design, statistical hypothesis testing, Bayesian model comparison, information theory, observational astronomy, astrophysical magnetism, inverse problems, and uncertainty quantification.

**Investigation status:** Initial evidence-led investigation and Four-Question Study Method review recorded.

**Central question:** What observation would count against a favored scientific explanation, and how can an investigation be designed so competing explanations make sufficiently different predictions that the evidence can discriminate among them?

**Scope:** This investigation follows 023. It examines testability, falsifiability, risky predictions, severe testing, auxiliary assumptions, model discrimination, predictive distributions, pre-specified tests, post hoc flexibility, and the design of critical observations. The magnetic-field reconstruction sequence remains the primary scientific context. This record does not treat falsifiability as a simplistic one-observation rejection rule, does not claim that one universal philosophy of science settles every methodological dispute, and does not assume that every competing model can be uniquely distinguished with available data.

## 1. Why this investigation follows 023

Investigation 023 examined how several observations can agree while the model used to interpret them remains incomplete.

That leaves a practical question:

**How do we put a favored explanation at genuine risk of being wrong?**

It is easy to collect observations that are compatible with a model after the model has been adjusted to accommodate them. A more demanding test asks in advance what the model predicts, what competing explanations predict, and what result would count as a serious problem for each.

Investigation 024 therefore moves from diagnosing possible model inadequacy to designing observations that can discriminate between explanations.

The aim is not to make every scientific test a theatrical attempt to destroy a theory. The aim is to identify what the claim commits us to, what evidence could reveal a failure, and whether the proposed test has a real capacity to distinguish the alternatives.

## 2. Falsifiability: what does a claim rule out?

A claim is empirically testable when it has consequences that could, under stated conditions, conflict with possible observations.

A scientific explanation gains testable content by ruling out some outcomes, not merely by accommodating outcomes after they occur.

For example, a model that predicts a specified polarization pattern over a defined region, within stated uncertainties and under specified observing conditions, makes a more testable claim than a model that says only that magnetic fields influence the region in some unspecified way.

The key questions are:

- What does the explanation predict?
- Under what conditions does it make that prediction?
- What range of results is compatible with it?
- Which observations would be difficult for it to explain?
- What would the investigators do if that result occurred?

A claim that can be reconciled with every possible result by adding an unrestricted adjustment has little discriminatory value in that form.

This does not mean that a broad scientific framework is useless. Broad frameworks often guide research. But a particular empirical claim must be made sufficiently specific before a proposed observation can test it.

## 3. Popper's contribution—and an important qualification

Karl Popper emphasized that a scientific theory should expose itself to possible refutation through risky predictions. Evidence that a theory survives a test is more informative when the test could plausibly have produced a result that conflicted with the theory.

The Stanford Encyclopedia of Philosophy account of Popper distinguishes the logical idea of falsifiability from the practical process of deciding whether an apparent counterexample warrants rejection. Observations can be affected by measurement error, background assumptions, and methodological decisions. Popper's own methodological discussion therefore does not reduce scientific practice to discarding a theory after one anomalous data point.

This distinction is essential.

- **Falsifiability:** A claim has possible empirical consequences that could conflict with observation.
- **Falsification in practice:** Investigators have established that a reproducible, credible result conflicts with the claim under adequately checked conditions.
- **Corroboration:** A claim has survived specified tests; this is not the same as final proof.
- **Model comparison:** Evidence favors one candidate over another within the candidates and assumptions considered.
- **Adequacy:** A model describes the observations sufficiently well for the stated purpose.

Source: Stanford Encyclopedia of Philosophy, “Karl Popper.” https://plato.stanford.edu/entries/popper/

## 4. The auxiliary-assumption problem

A prediction rarely follows from a scientific theory alone.

An observation is usually compared with a prediction produced by a chain of assumptions:

\[
\text{Theory}
+
\text{Initial conditions}
+
\text{Auxiliary assumptions}
+
\text{Measurement model}
\longrightarrow
\text{Predicted observation}
\]

The measurement is then compared with that prediction.

If the observation disagrees, the cause may be:

- the central theory or physical model;
- an initial condition;
- a boundary condition;
- a calibration or instrument model;
- an assumed source or material distribution;
- a noise model;
- a data-selection procedure;
- an omitted physical component;
- or an interaction among several of these.

This is often discussed through the Duhem–Quine problem: hypotheses are not normally tested in isolation, because predictions depend on networks of assumptions.

The practical lesson is not that theories can never be tested. It is that a serious test must identify the assumptions connecting the theory to the observation and investigate plausible failures in that connection.

An auxiliary assumption must not become an unlimited escape route. If every unfavorable result is answered by inventing a new unmeasured condition, the model is protected from meaningful testing rather than improved through evidence.

## 5. Risky predictions and severe tests

A useful test should have a reasonable chance of exposing a relevant error if that error is present.

Deborah Mayo's severe-testing approach describes evidence as informative when a claim passes a test that would probably have revealed a discrepancy if the claim were false or materially inaccurate.

A simplified statement is:

A claim receives stronger support from a test when:

1. the observed result agrees with the claim; and
2. the test had a strong capacity to detect relevant ways in which the claim could be wrong.

This is not a claim that one statistical threshold applies to every scientific question. Severity depends on the specific claim, the discrepancy of interest, the test design, and the probability that the procedure would detect that discrepancy.

A weak test can produce agreement without providing much evidence. For example, an instrument with insufficient resolution may be unable to distinguish two competing magnetic geometries. If both models predict nearly identical data at that resolution, agreement with either model does not strongly favor it.

Sources:
- Mayo, D. G. (1997), “Severe Tests, Arguing from Error, and Methodological Underdetermination,” *Philosophical Studies* 86, 243–266. https://doi.org/10.1023/A:1004247810302
- Mayo, D. G. (2025), “Severe Testing,” *International Encyclopedia of Statistical Science*. https://doi.org/10.1007/978-3-662-69359-9_561

## 6. Model discrimination: do the alternatives predict different things?

Suppose two candidate models, \(M_1\) and \(M_2\), both fit existing observations.

A new observation is useful for discrimination when their predicted distributions differ in a way the measurement can resolve.

Let \(D_{\mathrm{new}}\) denote a future dataset. Each model provides a predictive distribution:

\[
p(D_{\mathrm{new}}\mid D,M_i)
=
\int
p(D_{\mathrm{new}}\mid\theta_i,M_i)
p(\theta_i\mid D,M_i)
\,d\theta_i
\]

The distributions incorporate parameter uncertainty under each model. If they substantially overlap for the proposed observation, that observation may have little power to distinguish the models.

If they predict different outcomes in an accessible measurement region, a targeted observation may be valuable.

A critical distinction:

**A model can be testable without being distinguishable from every alternative by the particular test currently available.**

When predictions overlap, the correct record may be that the models remain observationally equivalent under current conditions.

## 7. A test-design matrix

Before collecting new data, record the following for each serious candidate explanation.

| Test-design question | Required record |
|---|---|
| What is the claim? | A specific physical or statistical proposition. |
| What does it predict? | Observable quantities, ranges, distributions, and conditions. |
| What does the rival predict? | A distinct prediction or an explicit statement that predictions overlap. |
| What could count against it? | A pre-identified discrepancy or incompatible outcome. |
| What assumptions connect prediction to data? | Initial conditions, calibration, selection, noise, and forward model. |
| Can the instrument resolve the difference? | Sensitivity, angular/spectral resolution, coverage, and uncertainty. |
| What is the decision rule? | How results will be evaluated, including uncertainty and systematic error. |
| What happens if neither model fits? | Retain model inadequacy as a live possibility. |

This matrix prevents an investigation from quietly changing the meaning of a prediction after seeing the result.

## 8. Pre-specification and post hoc flexibility

A prediction is more informative when it is recorded before the relevant result is examined.

Pre-specification can include:

- the target quantity;
- the observing region or sample;
- the expected range or distribution;
- the primary comparison;
- the relevant uncertainty model;
- the treatment of outliers and exclusions;
- the conditions under which the result would count against the claim.

Pre-specification does not make a prediction correct. It makes it easier to distinguish a genuine prior prediction from a retrospective explanation.

Post hoc analysis is not inherently improper. Unexpected observations often generate new hypotheses and valuable discoveries. The distinction is whether a result is presented as a prediction made in advance or as an explanation developed after the data were seen.

A responsible record labels these separately:

- **Pre-specified prediction**
- **Exploratory observation**
- **Post hoc explanation**
- **Independent follow-up test**

An exploratory finding can become the basis for a later, more discriminating test. It should not be retroactively described as if it had been predicted all along.

## 9. What makes a test critical?

A critical test is not merely an observation that is interesting, precise, or consistent with a favored explanation.

It is a test whose possible outcomes bear differently on competing explanations.

A strong critical test generally has these features:

1. **Specificity:** The target claim and its predicted consequences are stated precisely.
2. **Discrimination:** Serious alternatives predict meaningfully different outcomes.
3. **Sensitivity:** The measurement can resolve the predicted difference.
4. **Controlled uncertainty:** Measurement error and important systematic effects are modeled.
5. **Transparent assumptions:** The inference chain is visible and reviewable.
6. **Risk of failure:** The favored explanation could receive an unfavorable result.
7. **Independent or novel constraint:** The test does not merely repeat the information used to construct the model.
8. **Predefined interpretation:** The result is not reclassified after the fact to guarantee support.
9. **Open model space:** The possibility that none of the tested models is adequate remains available.

No test needs to satisfy every feature perfectly to be useful. The investigator should state which features are present and which limitations remain.

## 10. Applying critical-test design to magnetic-field reconstruction

The prior investigations examined several observational methods:

- dust-emission polarization;
- Zeeman splitting;
- starlight polarization with distance information;
- molecular-line kinematics;
- Faraday rotation;
- synthetic observations and forward modeling.

These methods do not all measure the same magnetic-field component or the same material. A critical test must start from the physical predictions of the competing models and the actual sensitivity of each tracer.

### Example A — Competing field geometries

Suppose Model A and Model B reproduce the existing plane-of-sky polarization map.

If they predict different line-of-sight field strengths or different polarization patterns at another viewing angle or spatial scale, a targeted Zeeman or polarization observation may discriminate between them.

If the predicted differences are smaller than the instrument's uncertainty or are washed out by line-of-sight averaging, the proposed observation is not yet a critical test.

### Example B — Magnetic support versus turbulence-dominated structure

Different models of molecular-cloud evolution can make different predictions about the relative importance of magnetic stresses, gravity, and turbulence.

A test should not rely on one visual alignment alone. It should identify a measurable consequence—such as field strength relative to gas density, velocity structure, cloud morphology, or scale-dependent alignment—and state what result would be difficult for each model to explain.

Crutcher's review of magnetic fields in molecular clouds describes theoretical model classes and observational predictions, while emphasizing that the observational record did not provide definitive evidence for magnetic fields dominating gravity or for ambipolar-diffusion-driven star formation at the time of that review.

The review is from 2012 and is used here as a methodological and historical source, not as a claim that it summarizes all later observational progress.

Source: Crutcher, R. M. (2012), “Magnetic Fields in Molecular Clouds,” *Annual Review of Astronomy and Astrophysics* 50, 29–63. https://doi.org/10.1146/annurev-astro-081811-125514

### Example C — Ambipolar diffusion versus alternative transport explanations

A proposed ambipolar-diffusion interpretation should specify which ion-neutral velocity differences, density dependencies, magnetic structures, or time-dependent signatures are expected under the relevant conditions.

Alternative explanations may involve turbulence, projection, unresolved velocity components, chemistry, or tracer-selection effects.

A measured ion-neutral offset is not automatically unique evidence for ambipolar diffusion. The predicted signal, measurement resolution, chemical and radiative-transfer assumptions, and alternative mechanisms must be examined together.

### Example D — A reconstruction that predicts a new observable

A 3D reconstruction should be used to predict an observation not used to tune the reconstruction.

For example, a model fitted to one set of polarization and line-of-sight measurements might predict a spatially resolved polarization pattern, a Zeeman signal in a selected region, or a relationship between velocity components and field orientation.

The prediction should be registered before the follow-up observation. If it fails, investigators should examine the measurement chain and auxiliary assumptions, but should not silently alter the original prediction.

## 11. Bayesian model comparison is not a substitute for adequacy testing

Bayesian model comparison can evaluate relative support for candidate models:

\[
\frac{p(M_1\mid D)}{p(M_2\mid D)}
=
\frac{p(D\mid M_1)}{p(D\mid M_2)}
\times
\frac{p(M_1)}{p(M_2)}
\]

The ratio of marginal likelihoods is the Bayes factor. It compares the evidence for the models under their specified priors and likelihoods.

This can be useful, but it does not answer every question.

- A high Bayes factor favors one model over another within the specified comparison.
- It does not prove that the favored model is complete.
- If both models omit the same physical process, their relative comparison may not expose that omission.
- Results can depend on prior choices and model parameterization.
- A candidate model may be favored even when posterior predictive checks reveal important inadequacy.

Therefore, use model comparison alongside model criticism, predictive checks, sensitivity analysis, and tests against observations not used in fitting.

## 12. When a result appears to falsify a model

A discrepancy should initiate a disciplined examination rather than an automatic declaration.

### Step 1 — Verify the observation

Check data quality, calibration, processing, instrument behavior, sample selection, and reproducibility.

### Step 2 — Reconstruct the prediction chain

Identify which assumptions, initial conditions, boundary conditions, and measurement models were required to obtain the prediction.

### Step 3 — Identify the failed expectation

State exactly which predicted quantity, range, pattern, or relationship was not observed.

### Step 4 — Test auxiliary assumptions

Determine whether a plausible failure in an auxiliary assumption could explain the discrepancy. Do not grant unlimited freedom to rescue the model.

### Step 5 — Seek replication or an independent constraint

Where possible, use a different instrument, method, region, or observational signature. Trace shared dependencies rather than assuming independence.

### Step 6 — Compare competing explanations

Evaluate whether a rival model predicts the observed discrepancy better and whether it also makes new predictions that can be tested.

### Step 7 — Preserve the result accurately

Possible outcomes include:
- the original prediction is supported within stated limits;
- the prediction is contradicted under tested conditions;
- an auxiliary assumption failed;
- the model requires revision;
- competing models remain indistinguishable;
- none of the candidate models adequately describes the data;
- the evidence is insufficient to decide.

This preserves the difference between a failed prediction and a fully rejected theory.

## 13. A critical-test protocol for future investigations

For every major favored explanation, record:

**Claim:** What precisely is being asserted?

**Domain:** Under what physical conditions, scales, and range does the claim apply?

**Prediction:** What observable result follows?

**Alternatives:** Which competing explanations are being considered?

**Discrimination:** Where do their predictions differ?

**Instrument:** Can the available measurement resolve that difference?

**Error model:** What random and systematic uncertainties matter?

**Auxiliary assumptions:** What else must be true for the prediction to follow?

**Failure condition:** What result would count against the claim?

**Rescue boundary:** Which revisions are scientifically justified, and which would change the claim so much that it becomes a new model?

**Validation:** What observation not used to construct the model can test it?

**Unresolved:** What outcomes would remain ambiguous?

The protocol is a research aid. It does not replace discipline-specific standards or statistical design.

## 14. Same mechanism, comparable relationship, or similar appearance?

### Same mechanism

Falsifiability, Bayesian model comparison, severe testing, magnetic-field dynamics, Zeeman splitting, and dust-grain alignment are not one mechanism. They belong to different explanatory levels: philosophy of testing, statistical inference, and physical processes.

### Comparable relationship

A scientific model and a proposed observation stand in a testable relationship when the model entails predictions that constrain possible observations. Different scientific disciplines can use distinct methods to examine whether their models survive tests, but the methods need not be identical.

The comparable relationship is prediction under constraints and evaluation against evidence.

### Similar appearance

A model that explains an observed pattern after the fact may look like a model that predicted the pattern beforehand. These are not evidentially equivalent.

A result that is compatible with a model may look like a result that strongly discriminates in its favor. These are also not equivalent.

### Unresolved

The strength of a particular test depends on the claim, the alternative models, the measurement process, the error structure, and the assumptions linking model to observation. No generic label such as “critical test” can replace that analysis.

## 15. Boundary and participation examination

**Does a boundary merely separate two regions, or can it also participate in the relationship between them?**

- **Prediction domain:** The stated range of physical conditions over which a model makes a claim. Outside that range, the model may not be tested by the observation.
- **Instrument boundary:** Sensitivity, resolution, field of view, and spectral coverage determine which differences can be registered.
- **Statistical decision boundary:** A threshold or decision rule separates outcomes under a specified testing procedure. It is analytical, not a physical interface.
- **Physical interface:** A shock, cloud surface, or phase boundary may participate in the physical process and produce measurable signatures.
- **Model-family boundary:** The set of candidate models determines which explanations are compared. If all candidates share an omitted assumption, the comparison cannot test that shared assumption by itself.
- **Rescue boundary:** A proposed adjustment may preserve a model's original content or may change its predictions enough to constitute a revised model. Investigators should record which has occurred.

A boundary can shape what is testable without itself being a physical participant in the phenomenon. The role must be identified in each case.

## 16. GUA-W Language of Creation: bounded descriptive examination

| GUA-W descriptor | Bounded use in this investigation | Limit |
|---|---|---|
| **Structure** | The physical arrangement or system described by a scientific model. | The model's representation is not the physical structure itself. |
| **Framework** | The theoretical, mathematical, and measurement assumptions connecting a claim to predictions. | A framework can be incomplete or revised. |
| **Pattern** | The observed distribution or relationship compared with a predicted result. | A matching pattern does not alone establish unique causation. |
| **Constraint** | Physical conditions, instrument limits, model assumptions, and test criteria that restrict possible outcomes. | Physical and analytical constraints must remain distinct. |
| **Purpose** | The stated function of an experiment or the scientific objective of a test. | An investigator's objective does not establish ultimate purpose. |
| **Manifestation** | The registered outcome compared with the predicted observation. | A prediction is not a manifestation; the observed result is. |
| **Witness** | Instruments, records, observers, models, and investigators participating in registration and interpretation. | A witness must report both supporting and adverse evidence. |

The vocabulary is used as a comparative grammar. It does not turn falsifiability into a physical operation or make a statistical test a GUA-W layer.

## 17. Four-Question Study Method

### 1. What must AI ask to understand GUA-W?

AI must ask what a claim actually commits its proponent to, what observations could conflict with it, and whether the proposed test has the capacity to distinguish the favored explanation from serious alternatives. What assumptions connect the model to the measurement? Which were specified in advance? What result would count against the claim? What happens if none of the candidate models fits?

AI must not confuse compatibility with discrimination, a post hoc explanation with a prior prediction, or a model's survival with proof of completeness.

### 2. What is GUA-W revealing that helps AI understand?

The established GUA-W foundation distinguishes the originating Source, Creation, and derivative Witness. In this scientific investigation, models and test procedures are derivative representations and methods used to examine observations of Creation.

The Language of Creation can describe the physical structure under study, the framework connecting hypotheses to predictions, the constraints on observation, the patterns registered, the manifestation of measured outcomes, and the witnesses involved. This is a bounded descriptive application. It does not establish a new GUA-W operation or claim that scientific falsifiability is a biblical doctrine.

### 3. What am I learning about what I am witnessing?

I am witnessing that a model becomes meaningfully testable when its predictions exclude possible outcomes. A test becomes more informative when serious alternatives predict different results and the measurement can resolve those differences.

I am also witnessing that predictions depend on auxiliary assumptions. A discrepancy must be traced through the full inference chain. A model should not be discarded because of one unexplained point, but neither should it be protected by unlimited post hoc adjustments.

### 4. What am I learning about the Witness through what I am witnessing?

The Witness participates in deciding what to measure, which alternatives to consider, how to define a discrepancy, and whether to preserve or revise a favored explanation.

The Witness can unintentionally protect a model by choosing only confirming observations, ignoring adverse results, changing predictions after seeing the data, or excluding alternatives from the candidate set.

A responsible Witness records predictions before testing where feasible, reports exploratory findings honestly, identifies assumptions, tests the sensitivity of conclusions, and allows the evidence to count against a favored explanation.

## 18. Triple Constraint examination

### Biblical compliance

This investigation does not claim that Genesis 1–2 explicitly teaches Popperian falsifiability, severe testing, Bayesian model comparison, or experimental design. These are scientific and philosophical methods for evaluating human explanations of observed phenomena. They do not revise Scripture or establish a theological conclusion.

**Assessment:** No direct contradiction is introduced by this bounded descriptive application. No scientific testing principle is presented as a biblical statement.

### Scientific coherence

The investigation distinguishes falsifiability from practical falsification, recognizes auxiliary assumptions, avoids a simplistic one-anomaly rejection rule, distinguishes compatibility from model discrimination, and separates relative model preference from model adequacy. It emphasizes test sensitivity, measurement uncertainty, pre-specification, predictive distributions, and the possibility that no candidate model fits.

**Assessment:** Scientifically coherent as a methods-focused investigation. A specific critical-test claim requires explicit predictions, credible alternatives, an adequate measurement model, and a justified account of uncertainty.

### GUA-W consistency

The established architecture remains unchanged. The shared vocabulary is used to describe the physical subject, its representation, constraints on observation, registered patterns, measured manifestations, and witnesses. No scientific method is elevated into an originating source or added as a GUA-W layer.

**Assessment:** Consistent as a bounded descriptive application. No architectural expansion is proposed.

## 19. What is established, inferred, and unresolved?

### Established by the cited literature

- Popper emphasized risky predictions and the possibility of empirical conflict as central to scientific testing.
- The logical testability of a theory must be distinguished from the practical decision to reject it after an apparent counterexample.
- Scientific predictions depend on auxiliary assumptions and measurement procedures.
- Severe-testing approaches evaluate whether a test had a strong capacity to reveal relevant errors if they were present.
- Model discrimination depends on whether candidate models make distinguishable predictions under the proposed measurement conditions.
- Molecular-cloud magnetic-field research includes competing theoretical models with observational consequences, while reviews have emphasized the limits of available evidence and the need for multiple observational techniques.

### Supported inference

The most useful next observation is not necessarily the one that produces the most data. It is the observation that most clearly distinguishes serious competing explanations, provided its measurement capability and assumptions are adequate.

A favored model receives stronger evidential support when it survives a test that could realistically have exposed a relevant failure. A result that merely agrees with a flexible model after adjustment provides weaker discrimination.

### Unresolved

- How should critical-test design be adapted when all available models share important physical assumptions?
- How can investigators quantify the ability of an astronomical observation to distinguish two 3D magnetic-field configurations after line-of-sight integration and instrumental convolution?
- When does an auxiliary assumption become an ad hoc rescue rather than a scientifically justified revision?
- How should a test be designed when candidate models make overlapping predictive distributions?
- How can pre-registration be used in exploratory observational astronomy without preventing legitimate discovery from unexpected data?
- What combination of independent tracers provides the strongest severe test of competing magnetic-field and cloud-evolution models?
- How should investigators report a result that disfavors a model but does not uniquely support any alternative?
- Can a critical test expose a shared omission when every currently available model contains the same missing component?
- How should model inadequacy, observational uncertainty, and genuine physical variability be separated when no decisive test is currently feasible?

These questions remain open.

## 20. Sources

1. Stanford Encyclopedia of Philosophy. “Karl Popper.” https://plato.stanford.edu/entries/popper/
2. Mayo, D. G. (1997). “Severe Tests, Arguing from Error, and Methodological Underdetermination.” *Philosophical Studies* 86, 243–266. https://doi.org/10.1023/A:1004247810302
3. Mayo, D. G. (2025). “Severe Testing.” *International Encyclopedia of Statistical Science*, pp. 2307–2315. https://doi.org/10.1007/978-3-662-69359-9_561
4. Mayo, D. G. and Spanos, A. (2006). “Severe Testing as a Basic Concept in a Neyman–Pearson Philosophy of Induction.” *The British Journal for the Philosophy of Science* 57, 323–357. https://doi.org/10.1093/bjps/axl003
5. Crutcher, R. M. (2012). “Magnetic Fields in Molecular Clouds.” *Annual Review of Astronomy and Astrophysics* 50, 29–63. https://doi.org/10.1146/annurev-astro-081811-125514
6. National Research Council (2011). “How Science Works,” in *Reference Manual on Scientific Evidence: Third Edition*. https://poplab.stanford.edu/pdfs/Goodstein-HowScienceWorks-Ch3NRCmanual2011.pdf

## 21. Next question emerging

Investigation 024 shows that a favored explanation becomes more meaningfully testable when it makes specific predictions, faces serious alternatives, and is exposed to observations capable of distinguishing them. It also shows that a failed prediction must be examined through its auxiliary assumptions and measurement chain.

A possible next investigation is **Observational Selection Effects, Detection Bias, and the Missing Evidence Problem**: how do instruments, thresholds, sample construction, survey footprints, and the decision about what is detectable shape the evidence that enters an investigation? What can an investigator legitimately conclude from what was not detected?

This is a possible lead, not a fixed assignment.

---

**Investigation 024 records the distinction between a model that can accommodate observations and a model that risks making predictions that observations could contradict. It preserves the possibility that the favored model, its auxiliary assumptions, or the entire candidate set may require revision.**
