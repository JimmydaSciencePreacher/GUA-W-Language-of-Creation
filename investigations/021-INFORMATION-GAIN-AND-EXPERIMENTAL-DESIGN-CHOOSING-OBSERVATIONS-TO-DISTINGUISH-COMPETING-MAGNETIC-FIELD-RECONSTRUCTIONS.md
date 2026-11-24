# Investigation 021 — Information Gain and Experimental Design: Choosing Observations to Distinguish Competing Magnetic-Field Reconstructions

**Primary disciplines:** Bayesian experimental design, information theory, astrophysical magnetic-field reconstruction, observational astronomy, polarimetry, radio astronomy, spectroscopy, statistical decision theory, and inverse-problem theory.

**Investigation status:** Initial evidence-led investigation and Four-Question Study Method review recorded.

**Central question:** Given multiple physically distinct magnetic-field reconstructions that remain compatible with current observations, which additional observation, observing configuration, or combination of measurements would most effectively distinguish them?

**Scope:** This investigation follows 020. It examines expected information gain, utility functions, experimental design, adaptive observation, model discrimination, complementary measurements, and the limits of information-based optimization. It does not assume that maximum information gain is always the best practical observing choice, that all new data are independent, or that a mathematically optimal design guarantees a correct physical model.

## 1. Why this investigation follows 020

Investigation 019 examined whether reconstructed magnetic structures can be recovered and independently validated. Investigation 020 examined how priors, regularization, and model restrictions influence which reconstruction is selected when the inverse problem is underdetermined.

A natural next question is:

**If several reconstructions remain plausible, what should we observe next to tell them apart?**

This changes the investigative question from merely analyzing available data to planning a measurement that could resolve a specific uncertainty.

An observing program has finite resources: telescope time, detector sensitivity, wavelength coverage, angular resolution, spectral resolution, sky coverage, calibration effort, and available targets. Repeating a measurement can improve precision, but a different kind of measurement may be more informative if it responds differently to the competing physical explanations.

The next observation should therefore be selected in relation to the unresolved question—not merely because the instrument can collect more data.

## 2. Experimental design: observation is not always passive

In ordinary analysis, the data have already been collected and the investigator asks what they imply.

In experimental design, the investigator can choose some features of the measurement before collecting it. Depending on the observing program, these may include:

- target selection;
- wavelength or frequency bands;
- spectral resolution;
- angular resolution and spatial sampling;
- integration time and sensitivity;
- observing epoch or cadence;
- polarization sensitivity and calibration strategy;
- field of view and sky coverage;
- complementary tracers or instruments;
- the sequence in which observations are made.

Let the chosen observing configuration be represented by \(\boldsymbol{\xi}\). The predicted data distribution depends on that design:

\[
p(\mathbf{d}\mid\boldsymbol{\theta},\boldsymbol{\xi},M)
\]

where \(\boldsymbol{\theta}\) represents unknown physical parameters and \(M\) is the model or candidate explanation.

The design changes which information the experiment can register. It does not change the underlying physical reality being investigated merely because the investigator changes the instrument settings.

## 3. Expected information gain

One widely used Bayesian design criterion is expected information gain (EIG). It quantifies the expected change from a current prior distribution to a posterior distribution after a proposed observation.

For a candidate design \(\boldsymbol{\xi}\):

\[
\operatorname{EIG}(\boldsymbol{\xi})
=
\mathbb{E}_{\mathbf{d}\sim p(\mathbf{d}\mid\boldsymbol{\xi})}
\left[
D_{\mathrm{KL}}
\left(
p(\boldsymbol{\theta}\mid\mathbf{d},\boldsymbol{\xi})
\,\Vert\,
p(\boldsymbol{\theta})
\right)
\right]
\]

Here:

- \(D_{\mathrm{KL}}\) is the Kullback–Leibler divergence;
- the posterior describes the updated distribution after a possible result;
- the prior describes the current distribution before that observation;
- the expectation averages over possible data outcomes predicted for the proposed design.

In plain language:

**EIG asks how much we expect a proposed observation to change what we know, averaged over the possible results of that observation.**

The expected value is calculated before the new data are collected. It is not a claim that the actual observation will necessarily be informative. A particular outcome may provide less information than expected, or may reveal that the model family was inadequate.

EIG depends on the current prior, likelihood, forward model, and chosen quantity of interest. It is not an assumption-free measure of absolute truth.

## 4. Information gain is not the same as scientific importance

A design can maximize expected information gain about parameters that are not the main scientific concern.

For example, a proposed observation might sharply constrain a nuisance parameter such as calibration offset while doing little to distinguish two competing magnetic topologies. Another design might provide less total information but strongly discriminate the physical alternatives that matter to the investigation.

Therefore the investigator must first specify the target of learning.

Possible targets include:

- field inclination;
- field strength;
- plane-of-sky orientation;
- line-of-sight field component;
- field curvature or topology;
- the number and distance distribution of dust layers;
- coupling between field and gas;
- the relative contribution of multiple emitting or absorbing regions;
- discrimination between two or more candidate physical models.

A useful design criterion should be aligned with the scientific question. Total parameter uncertainty, uncertainty in one derived quantity, and probability of distinguishing candidate models are different objectives.

## 5. Model discrimination: choose observations that make alternatives predict different things

Suppose two candidate models, \(M_1\) and \(M_2\), both reproduce current observations.

A proposed measurement is valuable for model discrimination when the models predict meaningfully different distributions for its possible outcomes.

The relevant question is not merely:

“Will this measurement be precise?”

It is:

“Do the competing explanations predict different results for this measurement, at a level the instrument can distinguish?”

A highly precise observation may be unhelpful if both models predict almost the same signal. A less precise observation may be decisive if the predictions are sufficiently different.

Possible design objectives include expected information gain about model identity, expected change in posterior model probabilities, expected Bayes-factor separation, or a decision-theoretic utility tied to the scientific consequence of choosing incorrectly.

Model-discrimination criteria require explicit candidate models. An alternative excluded from the model set cannot be selected by the design procedure.

## 6. Complementary observations and independent information

Investigation 018 examined complementary observational witnesses of magnetic-field and gas structure, including dust polarization, Zeeman splitting, stellar polarization with distance information, molecular-line kinematics, and Faraday rotation.

Investigation 021 asks a more specific question: which of these observations adds information that the current set does not already contain?

Examples of different observational sensitivities include:

- **Dust polarization:** constrains projected magnetic-field orientation, subject to grain alignment, line-of-sight integration, and emission weighting.
- **Zeeman splitting:** provides information about the line-of-sight magnetic-field component in suitable spectral lines and physical conditions.
- **Starlight polarization with distance estimates:** can help separate cumulative dust-polarization contributions along a sightline.
- **Molecular-line spectroscopy:** constrains gas velocity structure, excitation, and tracer-dependent components; it does not directly measure every magnetic-field property.
- **Faraday rotation:** probes magnetized plasma along the line of sight, with sensitivity to electron density and magnetic-field orientation and strength in combination.
- **Multifrequency polarized synchrotron emission:** can constrain magnetized emitting volumes, subject to cosmic-ray electron distributions, Faraday effects, and model assumptions.

These methods do not measure the same quantity. Their value may come from complementary sensitivity to different components of a coupled physical system.

However, combining measurements does not automatically make the evidence independent. Instruments may share calibration errors, models may share assumptions, and multiple tracers may sample overlapping material. Correlated errors and shared model dependencies must be represented in the joint analysis.

**Complementarity is a property to demonstrate through the measurement model, not to assume from the fact that two instruments are different.**

## 7. A practical design comparison

Consider two candidate reconstructions that both fit the available dust-polarization map.

- Model A attributes the observed polarization pattern mainly to a coherent projected field with relatively simple depth structure.
- Model B attributes much of the same projected pattern to several dust layers with different orientations along the line of sight.

The next observation should be chosen by comparing what each model predicts for candidate measurements.

Possible candidates:

1. Obtain stellar polarization measurements for stars with reliable distance estimates along the same sightline.
2. Obtain a suitable Zeeman measurement in a tracer of the relevant gas component.
3. Obtain molecular-line velocity-resolved data to test whether distinct components are present.
4. Obtain higher angular-resolution dust polarization data.
5. Extend wavelength or frequency coverage to test assumptions about emission, opacity, or polarized components.

The design process would:

- generate predictions from both models for each candidate observation;
- include realistic noise, calibration, sensitivity, and selection effects;
- estimate the expected ability of each candidate to separate the models;
- account for telescope time, feasibility, and cost;
- select a design based on the stated scientific objective;
- collect the observation;
- update the inference and test predictive performance.

No one candidate is universally best. The best choice depends on the physical models, source properties, available instrumentation, and the specific degeneracy.

## 8. Information gain under practical constraints

Pure information maximization may select an observation that is impractical, prohibitively expensive, or scientifically misaligned.

A practical design may optimize expected utility subject to constraints:

\[
\boldsymbol{\xi}^{*}
=
\underset{\boldsymbol{\xi}\in\mathcal{D}}{\operatorname{argmax}}
\;
\mathbb{E}[U(\boldsymbol{\xi},\mathbf{d})]
\]

where:

- \(U\) is the chosen utility;
- \(\mathcal{D}\) is the set of feasible observing designs;
- the expectation is over possible outcomes.

The utility may include information gain, model discrimination, expected parameter precision, or scientific decision value, while accounting for costs and operational constraints.

Examples of constraints include:

- telescope availability;
- exposure time;
- weather and observing conditions;
- detector noise and systematic calibration;
- angular and spectral resolution;
- target visibility;
- data volume and analysis capacity;
- the need for simultaneous or coordinated observations.

A design is optimal only relative to the objective, candidate designs, assumptions, and constraints that were specified.

## 9. Adaptive observation: an observation–inference–design cycle

Some investigations can update their observing strategy as data arrive.

A simplified adaptive cycle is:

1. **Observation:** collect the currently planned data.
2. **Inference:** update parameter and model distributions.
3. **Diagnosis:** identify which uncertainties or model distinctions remain important.
4. **Design:** evaluate candidate next observations.
5. **Selection:** choose a feasible observation with high expected utility for the stated question.
6. **Repeat:** use the new data to update the inference and decide whether another observation is warranted.

This is sometimes described as an observation–inference–design cycle.

It can improve efficiency when the forward model is reliable enough to predict the consequences of candidate observations and when the costs of adapting the plan are manageable.

It can also fail if the model omits the true physical explanation, if systematic errors are underestimated, or if the design criterion rewards the wrong target. Adaptive observation does not remove the need for model checking and independent validation.

## 10. Information gain and the Witness

A measurement is a witness to particular properties of a system, under particular conditions, through a particular instrument and method.

A new observation may add information because it:

- samples a different component;
- measures a different projection;
- resolves a previously blended contribution;
- extends the distance range;
- provides a different spectral or temporal response;
- reduces a particular degeneracy;
- tests a prediction on which candidate models disagree.

The new measurement does not automatically provide a complete view. It adds a constrained evidentiary record.

The investigator must state what the instrument can register, what it cannot register, what physical conditions affect the signal, and how the result is combined with existing observations.

A larger dataset is not necessarily a more informative dataset. The value of additional evidence depends on what uncertainty it addresses and how reliably the measurement model represents the observation process.

## 11. Published methodological evidence

### 11.1 Adaptive Bayesian exploration in astronomy

Loredo describes an adaptive scientific-exploration framework organized around an Observation–Inference–Design cycle. Bayesian inference quantifies what has been learned from current data, while Bayesian decision theory can select new observations expected to be most informative.

The work illustrates the logic with simulated examples, including an extrasolar-planet orbit problem. It is a methodological framework, not a demonstration that every astronomical observing program should use one universal EIG criterion.

Source: Loredo, T. J. (2003), “Bayesian Adaptive Exploration in a Nutshell,” PHYSTAT2003. https://www.slac.stanford.edu/econf/C030908/papers/TUHT004.pdf

### 11.2 Bayesian design for astronomical sky surveys

A study of sparse sky sampling applies Bayesian experimental-design ideas to galaxy-survey strategy. It compares observing a larger area sparsely with observing a smaller area more densely and shows that the preferred design depends on the parameters and scientific figure of merit being targeted.

This is an important caution: the best survey strategy depends on the question. More observations concentrated in one place are not automatically more useful than a different distribution of observing effort.

Source: “Sparsely sampling the sky: a Bayesian experimental design approach” (2013), *Monthly Notices of the Royal Astronomical Society* 433, 3523. https://academic.oup.com/mnras/article/433/4/3523/1750741

### 11.3 Bayesian inference for solar and stellar magnetic fields

A Bayesian treatment of magnetic-field inference under the weak-field approximation discusses prior information and presents a hierarchical procedure intended to make results less sensitive to the precise prior choice. It also analyzes how noise degrades information in Stokes profiles and demonstrates the framework using IMaX data.

This is relevant to magnetic-field inference and shows that instrument information content and prior sensitivity are part of the same measurement problem. It concerns solar/stellar atmospheric measurements, not direct three-dimensional molecular-cloud reconstruction.

Source: “Bayesian inference of solar and stellar magnetic fields in the weak-field approximation” (2011), *The Astrophysical Journal* 731, 27. https://doi.org/10.1088/0004-637X/731/1/27

### 11.4 Information gain and experimental design in inverse problems

A 2026 preprint develops bounds on expected information gain for Bayesian optimal experimental design, including nonlinear forward models and non-Gaussian priors. It aims to reduce the computational burden of estimating EIG and discusses signal-to-noise and Fisher-information-based approximations.

This is recent methodological work, not a magnetic-field observation study. It supports the broader point that calculating the value of a proposed observation can itself be computationally difficult and approximate.

Source: Doumbouya, M., Vidard, A., and Zahm, O. (2026), “Certified Bayesian optimal experimental design: from Expected Information Gain to Signal-to-Noise Ratio,” arXiv:2609.32282. https://arxiv.org/abs/2609.32282

### 11.5 Optimal design for model discrimination

Research on optimal experimental design with adjoint-accelerated Bayesian inference examines designs that maximize information about unknown parameters, sensor placement, and discrimination between candidate models. It demonstrates that the best observation can depend on whether the goal is parameter precision or model discrimination.

The study is a general physics-based experimental-design example, not a direct astrophysical magnetic-field survey.

Source: “Optimal experiment design with adjoint-accelerated Bayesian inference,” *Data-Centric Engineering*. https://www.cambridge.org/core/journals/data-centric-engineering/article/optimal-experiment-design-with-adjointaccelerated-bayesian-inference/DBF73676F5B13E2CB6F6DCC6D101ECF1

## 12. Same mechanism, comparable relationship, or similar appearance?

### Same mechanism

Bayesian updating, information-theoretic scoring, telescope measurement, radiative transfer, Zeeman splitting, and magnetic-field evolution are distinct mechanisms or processes. An information-gain calculation does not physically alter a magnetic field.

### Comparable relationship

A candidate observing design changes which aspects of a system can be distinguished by the resulting evidence. Different instruments and methods can provide complementary constraints on different properties.

The comparable relationship is selective access to evidence, not a common physical mechanism among the instruments or the astronomical processes they measure.

### Similar appearance

Two datasets may both be described as “more information,” yet one may add independent sensitivity to a previously unconstrained parameter while another merely repeats an already well-constrained measurement. Their numerical size or visual richness does not establish equal informational value.

### Unresolved

For any specific magnetic cloud, which new observation has the greatest expected value must be calculated from the candidate models, their predicted signals, instrument characteristics, noise, systematics, and the scientific quantity of interest.

## 13. Boundary and participation examination

**Does a boundary merely separate two regions, or can it also participate in the relationship between them?**

- **Instrument sensitivity boundary:** A detection threshold separates detectable from undetectable signals under specified conditions. It shapes which evidence enters the dataset, but does not establish that undetected structure is absent.
- **Wavelength or frequency coverage:** A bandpass limits the signal components sampled. Extending coverage may expose different physical contributions.
- **Angular-resolution boundary:** The beam and sampling determine which spatial structures are resolved or blended. A resolution limit can conceal distinctions without physically removing them.
- **Distance boundary:** A finite set of background stars or sources limits how far along a sightline a layer decomposition can be constrained.
- **Physical interface:** A cloud boundary or plasma interface may participate in transport, field coupling, or emission processes. This is a physical role requiring evidence, not merely an observational selection.
- **Model boundary:** A candidate model family defines which configurations the inference can represent. It participates in the analysis by excluding alternatives, but it is not a physical boundary in the astronomical object.

The investigation distinguishes observational limits, mathematical selection boundaries, and physical interfaces. Their roles must not be conflated.

## 14. GUA-W Language of Creation: bounded descriptive examination

| GUA-W descriptor | Bounded use in this investigation | Limit |
|---|---|---|
| **Structure** | The physical magnetic-field and gas configuration being investigated. | The reconstruction may remain non-unique. |
| **Framework** | The observing design, forward model, instrument model, and inferential procedure. | These are human methods of inquiry, not the physical source of the observed system. |
| **Pattern** | The features or relationships different candidate observations are designed to distinguish. | A pattern in a measured signal may have multiple physical explanations. |
| **Constraint** | Instrument limits, observing resources, physical conditions, and model restrictions. | Observational constraints differ from physical constraints and analytical assumptions. |
| **Purpose** | The stated scientific objective of a measurement or observing program. | An investigator's objective does not establish ultimate purpose in Creation. |
| **Manifestation** | The signal registered under a chosen observing configuration. | The signal is a measurement mediated by the instrument and physical conditions. |
| **Witness** | The telescope, detector, calibration record, data product, analysis method, and investigator. | Each witness registers only a bounded aspect of the system. |

The common descriptive grammar helps compare the physical subject, observing framework, conditions, measurable signals, and witnesses. It does not equate information theory with a physical law or a telescope with the system it observes.

## 15. Four-Question Study Method

### 1. What must AI ask to understand GUA-W?

AI must ask what uncertainty remains after Investigation 020, which candidate physical explanations remain compatible with the current evidence, and what observation would make their predictions differ. What is the target of information gain? Which instrument can measure it? Are the expected signals distinguishable after realistic noise and systematic effects? Is the new information independent of existing data?

AI must not assume that more data, higher precision, or a larger dataset necessarily resolves the most important uncertainty.

### 2. What is GUA-W revealing that helps AI understand?

The established GUA-W foundation distinguishes the originating Source, Creation, and derivative Witness. In this investigation, the observing system and analytical framework are derivative means of registering and interpreting properties of the physical system.

The Language of Creation can describe the structure being investigated, the framework of observation, the constraints on measurement, the pattern sought, the signal manifested, and the witnesses that register it. This is a bounded descriptive application, not a new GUA-W architectural layer.

### 3. What am I learning about what I am witnessing?

I am witnessing that the design of an observation can influence what becomes distinguishable in the resulting evidence. Experimental design makes the choice of the next measurement an explicit part of the scientific process.

Expected information gain can compare candidate observations before they are made, but its result depends on the current models, priors, likelihoods, utility, and feasible designs. A design optimized for one parameter or model distinction may not be optimal for another.

Complementary instruments can add different constraints, but their information is not automatically independent. Their joint value must be demonstrated through the measurement model and validation.

### 4. What am I learning about the Witness through what I am witnessing?

The investigator does not merely receive data passively when designing an observation. The investigator chooses where, when, how, and what to measure, often under finite resources.

Those choices influence which questions can be answered. A responsible Witness states the objective, candidate alternatives, expected limitations, selection criteria, and the assumptions used to calculate expected value. After collecting data, the investigator must compare the actual result with the prediction and preserve outcomes that contradict the preferred model.

## 16. Triple Constraint examination

### Biblical compliance

This investigation does not claim that Genesis 1–2 explicitly describes information theory, Bayesian experimental design, telescope selection, or expected information gain. These are scientific and mathematical methods used to investigate created phenomena. They do not revise Scripture or establish a theological conclusion.

**Assessment:** No direct contradiction is introduced by this bounded descriptive application. No scientific result is presented as a biblical statement.

### Scientific coherence

The investigation distinguishes expected information gain from realized information, total parameter precision from model discrimination, and complementary measurements from statistically independent evidence. It identifies the dependence of design criteria on priors, likelihoods, candidate models, utility functions, and practical constraints. The cited astronomy examples are separated from general methodological studies and are not misrepresented as direct molecular-cloud demonstrations.

**Assessment:** Scientifically coherent as a methods-focused investigation. A concrete observing recommendation requires a defined target, candidate models, forward predictions, and realistic instrument characterization.

### GUA-W consistency

The established architecture remains unchanged. The common vocabulary describes the physical structure, observation framework, constraints, manifestations, and witnesses without treating the instrument or method as the originating source.

**Assessment:** Consistent as a bounded descriptive application. No architectural expansion is proposed.

## 17. What is established, inferred, and unresolved?

### Established by the cited literature

- Bayesian experimental design can evaluate candidate observations by their expected information gain.
- Adaptive observation can cycle between collecting data, updating inference, and selecting a subsequent measurement.
- The scientific objective matters: survey designs can differ in value depending on which parameters or models are to be constrained.
- Bayesian methods have been applied to solar and stellar magnetic-field inference, including explicit examination of prior sensitivity and noise.
- Information-gain calculations can be computationally demanding, especially for nonlinear models and non-Gaussian priors.
- Experimental design can target discrimination between candidate models as well as parameter precision.

### Supported inference

A useful next observation should be chosen because it is predicted to reduce a specified uncertainty or distinguish specified alternatives, after accounting for realistic noise, systematic effects, feasibility, and dependence on existing data.

The most informative observation is not necessarily the one with the highest raw sensitivity, greatest data volume, or most visually detailed result.

### Unresolved

- Which candidate measurements most effectively distinguish competing 3D magnetic-field topologies in realistic molecular-cloud conditions?
- How should expected information gain be modified when the main objective is model discrimination rather than parameter precision?
- How can correlated calibration errors and shared model assumptions be included in the information value of multiple instruments?
- When does a new tracer add genuinely independent information rather than another measurement of a coupled or overlapping component?
- How should observation design account for the possibility that all current candidate models are incomplete?
- How robust are optimal observing choices to prior sensitivity and uncertainty in the forward model?
- What is the best way to balance information gain, observing time, feasibility, and scientific consequence?
- Can a staged observing strategy identify an unexpected physical component that was absent from the initial model set?

These questions remain open.

## 18. Sources

1. Loredo, T. J. (2003). “Bayesian Adaptive Exploration in a Nutshell.” PHYSTAT2003. https://www.slac.stanford.edu/econf/C030908/papers/TUHT004.pdf
2. “Sparsely sampling the sky: a Bayesian experimental design approach” (2013). *Monthly Notices of the Royal Astronomical Society* 433, 3523. https://academic.oup.com/mnras/article/433/4/3523/1750741
3. “Bayesian inference of solar and stellar magnetic fields in the weak-field approximation” (2011). *The Astrophysical Journal* 731, 27. https://doi.org/10.1088/0004-637X/731/1/27
4. Doumbouya, M., Vidard, A., and Zahm, O. (2026). “Certified Bayesian optimal experimental design: from Expected Information Gain to Signal-to-Noise Ratio.” arXiv:2609.32282. https://arxiv.org/abs/2609.32282
5. “Optimal experiment design with adjoint-accelerated Bayesian inference.” *Data-Centric Engineering*. https://www.cambridge.org/core/journals/data-centric-engineering/article/optimal-experiment-design-with-adjointaccelerated-bayesian-inference/DBF73676F5B13E2CB6F6DCC6D101ECF1

## 19. Next question emerging

Investigation 021 moves the inquiry from evaluating existing evidence to designing the next observation. It shows that the value of a measurement depends on the uncertainty or model distinction it is intended to address, and on whether the expected signal can be distinguished under realistic conditions.

A possible next investigation is to examine **measurement independence, correlated errors, and evidence fusion**: when multiple instruments or tracers are combined, how can we determine whether they contribute genuinely independent constraints, partially overlapping information, or shared systematic uncertainty?

This is a possible lead, not a fixed assignment.

---

**Investigation 021 records how the next observation can be selected to distinguish competing explanations, while preserving the limits of the models, instruments, and information criteria used to make that choice.**
