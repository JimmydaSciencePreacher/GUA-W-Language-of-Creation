# Investigation 023 — Model Misspecification and the Missing-Variable Problem

**Primary disciplines:** Statistical model checking, Bayesian inference, inverse-problem theory, astrophysics, observational astronomy, scientific measurement, causal inference, uncertainty quantification, and model validation.

**Investigation status:** Initial evidence-led investigation and Four-Question Study Method review recorded.

**Central question:** What happens when several observations agree with one another because they are interpreted through an incomplete model? How can investigators detect that the model omits a relevant physical component, process, population, or source of uncertainty—and distinguish that possibility from noise, calibration error, selection effects, or an incorrect parameter value?

**Scope:** This investigation follows 022. It examines model misspecification, omitted variables and latent components, likelihood and prior misspecification, posterior predictive checking, residual structure, out-of-sample prediction, model expansion, robustness, and the limits of model criticism. The primary scientific examples are drawn from astronomical inference. This record does not assume that every unexplained residual indicates a missing physical entity, that model expansion always improves inference, or that a statistical diagnostic can uniquely identify the cause of model failure.

## 1. Why this investigation follows 022

Investigation 022 asked whether multiple measurements provide independent constraints or share errors, information, and assumptions.

A further problem remains:

**What if the measurements are genuinely independent in important respects, but the model used to interpret all of them is incomplete?**

Imagine several instruments measure different observables. Their calibration errors are independently characterized. Their data are combined correctly. The analysis reports a consistent physical interpretation.

Yet all measurements are translated into physical conclusions using a forward model that omits a relevant component. The instruments may agree because the same omission is built into every interpretation.

This possibility does not mean the measurements are false. It means the inference may be conditional on an incomplete representation of the system.

Investigation 023 therefore separates two questions:

1. Are the observations and their errors represented adequately?
2. Does the physical and statistical model include the processes and components needed for the intended inference?

A model can handle measurement covariance correctly and still be misspecified. Conversely, a physically appropriate model can be undermined by an incorrect noise or calibration model.

## 2. What is model misspecification?

A model is misspecified when the assumptions or mathematical structure used to describe the data-generating process are inadequate for the inference being attempted.

The model may be wrong in several different ways:

- It may omit a physical component or process.
- It may use an incorrect functional relationship.
- It may assume the wrong noise distribution.
- It may omit correlations or shared nuisance variables.
- It may impose an unsuitable prior or parameter range.
- It may represent a heterogeneous population as if it were homogeneous.
- It may simplify geometry, radiative transfer, selection, or boundary conditions too aggressively.
- It may treat a derived proxy as if it were the physical quantity of interest.

Misspecification is not synonymous with a model having imperfect parameter estimates. A parameter can be estimated inaccurately even within a suitable model. Misspecification concerns the adequacy of the model family or its assumptions for representing the observations and target phenomenon.

The distinction is important because increasing the precision of an estimate cannot repair a model that excludes the process responsible for the discrepancy.

## 3. Likelihood misspecification and prior misspecification

Bayesian inference commonly combines a likelihood and a prior:

\[
p(\theta\mid D,M)
\propto
p(D\mid\theta,M)\,p(\theta\mid M)
\]

where:

- \(D\) is the observed data;
- \(\theta\) represents model parameters;
- \(M\) is the adopted model;
- \(p(D\mid\theta,M)\) is the likelihood;
- \(p(\theta\mid M)\) is the prior;
- \(p(\theta\mid D,M)\) is the posterior.

Two broad forms of misspecification follow.

### 3.1 Likelihood or data-model misspecification

The likelihood may fail to describe the actual signal, noise, or measurement process.

Examples include:

- assuming Gaussian noise when important tails or outliers are present;
- omitting correlated noise between measurements or frequency bins;
- neglecting calibration uncertainty;
- using an incorrect response function;
- ignoring selection or detection effects;
- simplifying a physical signal model so that it cannot reproduce observed features.

### 3.2 Prior or population-model misspecification

The prior may exclude plausible parameter values or impose an unsuitable distribution. In population inference, the assumed population distribution may fail to represent the actual population.

A narrow prior can make a posterior appear precise because the model has excluded alternatives before the data are evaluated. A population model that is adequate for a small sample may fail as the dataset grows and reveals features it could not represent.

These two categories can interact. A model may have an adequate signal likelihood but a restrictive prior, or a flexible prior but an inadequate likelihood. Both must be examined.

## 4. The missing-variable problem

A missing variable is a relevant quantity, component, or process that is absent from the model.

The phrase covers several distinct situations:

1. **Omitted physical component:** A real source, material phase, field component, population, or emission contribution is not represented.
2. **Omitted process:** A relevant interaction, transport process, reaction, feedback mechanism, or time dependence is absent.
3. **Unmodeled heterogeneity:** The system contains subpopulations or spatial regions with different properties, but the model treats them as one uniform population.
4. **Latent variable:** A relevant quantity affects the observations but is not directly measured.
5. **Omitted nuisance variable:** A calibration, background, selection, or environmental factor influences the measurement but is not represented.
6. **Unobserved confounder:** In a causal analysis, an unmeasured variable influences both a proposed cause and an outcome, potentially distorting the inferred relationship.

These cases should not be collapsed into one generic explanation. An omitted physical component is not the same thing as a missing calibration parameter. A latent variable may be a useful mathematical representation without establishing that a separately identifiable physical object exists.

A residual can indicate that a model is inadequate, but it does not identify which of these explanations is responsible.

## 5. Why several agreeing witnesses can still share an incomplete model

Consider several instruments that measure different aspects of an astronomical object.

Their raw data may be independent in the relevant error model. Yet the analysis may use the same assumed geometry, source distribution, or radiative-transfer simplification to convert those observations into physical quantities.

The reasoning chain can be represented as:

\[
\text{Physical system}
\rightarrow
\text{Instrument-specific signals}
\rightarrow
\text{Data processing}
\rightarrow
\text{Shared model assumptions}
\rightarrow
\text{Inferred physical description}
\]

Independence at one point in this chain does not guarantee independence at every later point.

If a shared assumption is wrong, multiple analyses can inherit the same bias even when their instruments and random errors differ.

This is not evidence that agreement is meaningless. Agreement can still be valuable. The correct conclusion is narrower:

**Agreement among measurements does not, by itself, test assumptions that all interpretations share.**

To test a shared assumption, investigators need observations or analyses whose predictions respond differently to that assumption, or independent ways of varying and validating it.

## 6. Residuals: where the model and observations differ

A residual is a difference between an observed result and a model prediction. In a simple notation:

\[
r_i = y_i - \hat{y}_i
\]

where \(y_i\) is an observation and \(\hat{y}_i\) is the corresponding model prediction.

Residuals are not automatically evidence of a missing variable. They can arise from random noise, calibration error, an incorrect parameter estimate, data processing, selection effects, or an inadequate model.

The pattern of residuals can nevertheless provide clues.

Examples include:

- residuals that vary systematically with wavelength;
- spatially coherent residual structures in an image or map;
- discrepancies that grow with signal strength;
- residuals correlated with observing time or detector position;
- errors concentrated in a particular source population;
- unexplained features that persist across independent instruments;
- residuals that change when a shared assumption is altered.

A model that leaves structured residuals may be failing to represent some systematic feature of the data. The next task is to investigate possible causes rather than immediately naming a missing physical component.

## 7. Posterior predictive checking

A posterior predictive check asks whether data generated under the fitted model resemble the observed data in relevant ways.

A simplified posterior predictive distribution is:

\[
p(D_{\mathrm{rep}}\mid D,M)
=
\int
p(D_{\mathrm{rep}}\mid\theta,M)
p(\theta\mid D,M)
\,d\theta
\]

where \(D_{\mathrm{rep}}\) represents replicated data generated from the model using parameter values drawn from the posterior.

The investigator compares observed data with these replicated datasets using selected diagnostic features or test statistics.

Questions include:

- Does the model reproduce the observed distribution?
- Does it reproduce spatial or temporal correlations?
- Does it reproduce the frequency of extreme values?
- Does it reproduce the structure of residuals?
- Does it reproduce the relationship between multiple observables?
- Does it reproduce the relevant selection and detection patterns?

A useful check must examine features relevant to the scientific question. A model can reproduce a histogram while failing to reproduce spatial structure. It can match an average while missing a tail, subpopulation, or correlation.

### An essential limitation

Passing posterior predictive checks does not prove that a model is correct or complete. A diagnostic may fail to examine the feature that exposes the model's deficiency. Different physical models may generate observationally similar data.

Posterior predictive checks are tools for finding possible inadequacy, not certificates of truth.

## 8. Out-of-sample prediction and independent tests

A model can fit the data used to construct it while failing to predict data not used in fitting.

Out-of-sample tests help examine whether a model generalizes beyond the observations that determined its parameters.

Possible approaches include:

- holding out a subset of observations;
- predicting a different wavelength or frequency band;
- testing a new time interval;
- predicting a separate region or source population;
- comparing with a different tracer;
- using an independent instrument or analysis pipeline;
- testing predictions from synthetic data with known generating conditions.

The independence of a validation set must be examined carefully. A held-out subset can still share calibration, selection, processing, or model assumptions with the training data. A different instrument can still observe the same physical realization and rely on the same forward-model simplification.

A validation test is strongest when its dependence on the original fitting process is understood and its predicted result is specified before the validation data are examined.

## 9. Model expansion: adding a missing component without inventing one

When evidence suggests model inadequacy, investigators may consider expanding the model.

Possible changes include:

- adding a physically motivated component;
- representing a previously ignored process;
- allowing a population to contain multiple subpopulations;
- introducing a latent variable;
- modeling calibration or background uncertainty;
- replacing a restrictive noise distribution;
- adding spatial or temporal variation;
- improving the forward model or boundary conditions.

But model expansion creates a danger: a sufficiently flexible model can fit noise or absorb discrepancies without identifying their physical cause.

A responsible expansion should therefore state:

1. Which observed discrepancy motivates the change?
2. What physical or statistical mechanism could produce it?
3. What new parameters or assumptions are introduced?
4. What distinct predictions follow from the expanded model?
5. What independent observation could test those predictions?
6. Does the expanded model improve predictive performance rather than merely improve the fit to existing data?
7. Are the new parameters identifiable from the available observations?

An added term that improves a fit is not automatically a discovered physical component. It may be a useful approximation, a nuisance correction, or an overfitting device.

## 10. A model can be preferred and still be inadequate

Model selection often compares candidate models and asks which receives stronger support under a specified criterion.

But a relative preference does not establish absolute adequacy.

Suppose Model A fits better than Model B. If both fail to reproduce a systematic feature of the observations, Model A may simply be the less inadequate candidate.

The distinction is:

- **Relative comparison:** Which candidate performs better among those considered?
- **Adequacy assessment:** Does the candidate describe the observations well enough for the intended inference?
- **Completeness claim:** Have relevant physical components and processes been represented?

These are different questions.

The candidate set matters. If every candidate omits the same process, a model-selection procedure cannot select the omitted process unless the model space is expanded or a different test exposes the deficiency.

## 11. Published methodological evidence

### 11.1 Model failure and posterior predictive checks in gravitational-wave astronomy

Romero-Shaw, Thrane, and Lasky (2022) review model misspecification in Bayesian gravitational-wave astronomy. They distinguish deficiencies in likelihoods describing signals or noise from deficiencies in priors and population models.

Their review explains why a preferred model may still be a poor description of reality, and discusses visual inspection, posterior predictive checks, and other diagnostic approaches. It also cautions that no finite collection of checks detects every form of misspecification.

This is a methodological review using gravitational-wave examples. It is not a direct study of molecular-cloud magnetic-field reconstruction.

Source: Romero-Shaw, I. M., Thrane, E., and Lasky, P. D. (2022), “When models fail: An introduction to posterior predictive checks and model misspecification in gravitational-wave astronomy,” *Publications of the Astronomical Society of Australia* 39, e025. https://doi.org/10.1017/pasa.2022.24

### 11.2 Robust Bayesian regression under model misspecification

A 2025 astronomy methods paper develops a robust Bayesian linear-regression approach using Student's t-distributions. It examines outliers and misspecification of the noise model, and tests the method on simulated datasets with different degrees of misspecification.

The authors report that, in their tested simulations, the robust approach produced constraints that were systematically less biased than a similar model using normal distributions.

This demonstrates one possible response to certain noise-model deficiencies. It does not establish that Student's t-distributions are universally appropriate or that robust regression can repair omitted physical mechanisms.

Source: “An approach to robust Bayesian regression in astronomy” (2025), *RAS Techniques and Instruments*. https://doi.org/10.1093/rasti/rzaf035

### 11.3 Detecting misspecification in Bayesian inverse problems

Liu and colleagues (2025 preprint) propose a predictive-orientation approach to detecting model misspecification in Bayesian inverse problems. Their method compares a conventional Bayesian posterior with a predictive-oriented distribution and demonstrates the approach in simulation and a seismological inverse-problem case study.

This is relevant because inverse problems can produce apparently precise reconstructions under a misspecified forward model. The work is a preprint and a seismological application, not an established magnetic-field result. Its method should be treated as a developing diagnostic, not a universal test.

Source: Liu, Q. et al. (2025), “Detecting Model Misspecification in Bayesian Inverse Problems via Variational Gradient Descent,” arXiv:2512.01667. https://arxiv.org/abs/2512.01667

## 12. Applying the question to magnetic-field reconstruction

The preceding investigations focused on three-dimensional magnetic-field and gas structure. Model misspecification can arise at several points in that reconstruction.

### 12.1 Dust polarization

A model may assume a simplified grain-alignment prescription, uniform dust properties, or a limited line-of-sight geometry.

If those assumptions are inadequate, the inferred plane-of-sky magnetic orientation or its relation to the gas distribution may be biased.

An unexplained polarization pattern does not automatically demonstrate a new magnetic component. It may reflect optical depth, grain alignment, temperature weighting, unresolved structure, or an inadequate emission model.

### 12.2 Zeeman measurements

A model may simplify line formation, assume a particular density or excitation structure, or treat a measured line-of-sight field as representative of a larger volume.

If the tracer samples only selected material, the inferred field may not represent the full cloud.

A discrepancy between Zeeman and dust-polarization inferences could indicate projection, line-of-sight weighting, distinct material components, calibration, or model limitations. The cause must be tested.

### 12.3 Faraday rotation

A model may simplify electron-density structure, foreground contributions, or the distribution of magnetized plasma.

If those contributions are omitted, the inferred magnetic properties can be misleading even when the rotation measurement itself is precise.

### 12.4 Molecular-line kinematics

A model may assume a single velocity component where multiple components overlap along the line of sight, or may use a tracer whose abundance and excitation vary across the cloud.

An apparent mismatch between gas kinematics and magnetic morphology could reflect an incomplete velocity or chemical model rather than a failure of magnetic coupling.

### 12.5 Three-dimensional geometry

A model may assume a simple field topology, a fixed inclination, or a restricted family of configurations. If the actual system lies outside that family, inference can return a best-fitting configuration that is not physically representative.

The central issue is not whether the model can be made more complicated. It is whether the proposed additional structure is supported by observations that distinguish it from competing explanations.

## 13. A practical missing-variable investigation

When a discrepancy appears, use the following sequence.

### Step 1 — Describe the discrepancy

State exactly what the model fails to reproduce. Identify the data, measurement conditions, diagnostic, and uncertainty.

### Step 2 — Audit the measurement chain

Revisit calibration, noise, selection, preprocessing, covariance, and data quality. Do not attribute an instrumental or statistical failure to new physics prematurely.

### Step 3 — Audit the forward model

Ask which physical components, processes, geometries, boundary conditions, or time dependencies are represented and which are simplified or absent.

### Step 4 — Generate competing explanations

Include alternatives such as random variation, calibration error, selection effects, parameter error, model misspecification, and an omitted physical component. Do not begin with only the preferred missing-variable hypothesis.

### Step 5 — Derive discriminating predictions

Each explanation should predict something different where possible. Identify which observation, diagnostic, or analysis would distinguish them.

### Step 6 — Test robustness

Vary priors, noise assumptions, nuisance parameters, model complexity, and plausible physical alternatives. Record which conclusions remain stable.

### Step 7 — Validate beyond the fitting data

Use an independent measurement or a genuinely out-of-sample prediction where feasible. Trace shared dependencies before calling it independent.

### Step 8 — Preserve unresolved causes

If several explanations remain observationally equivalent, report the model as inadequate or the cause as unresolved. Do not convert a residual into a named physical discovery without discriminating evidence.

## 14. Same mechanism, comparable relationship, or similar appearance?

### Same mechanism

A statistical residual, a missing latent variable, a dust-grain alignment process, a Zeeman interaction, and a magnetic-field structure are not the same mechanism. A diagnostic identifies a discrepancy; it does not physically generate the omitted component.

### Comparable relationship

Different instruments and analyses can reveal that a shared model assumption is inadequate when their predictions fail in related but distinguishable ways. Independent tests can expose a common limitation in the interpretation chain.

The comparable relationship is model checking across multiple observations, not an assertion that the observations share one physical process.

### Similar appearance

Several datasets may show the same residual pattern because they share an omitted assumption. That resemblance may be a clue, but it does not prove a common omitted physical cause.

A residual that looks like an additional component may also arise from incorrect geometry, selection, calibration, or an unsuitable noise model.

### Unresolved

A particular discrepancy does not identify its cause by appearance alone. The missing-variable explanation must be compared with competing explanations and tested through predictions that could distinguish them.

## 15. Boundary and participation examination

**Does a boundary merely separate two regions, or can it also participate in the relationship between them?**

- **Physical interface:** A shock, cloud surface, ionization front, or phase boundary can affect transport, chemistry, emission, and magnetic coupling. Its physical role must be established for the system under study.
- **Model-domain boundary:** A computational domain or parameter range can exclude physical configurations. This is a limitation of the representation, not necessarily a boundary in the astronomical object.
- **Selection boundary:** A detection threshold, mask, or sample cut determines which observations enter the analysis. It can create apparent population differences or hide a low-signal component.
- **Resolution boundary:** An instrument beam or spectral channel can blend distinct components. The unresolved components may still contribute to the measured signal.
- **Inference boundary:** A model family separates represented explanations from excluded alternatives. It participates in what the analysis can conclude, but it does not establish that excluded alternatives are physically absent.

The investigator must distinguish a physical boundary that participates in the system from an analytical boundary that participates in the measurement or inference process.

## 16. GUA-W Language of Creation: bounded descriptive examination

| GUA-W descriptor | Bounded use in this investigation | Limit |
|---|---|---|
| **Structure** | The physical system the model attempts to represent, including potentially unresolved components and relationships. | A model is not the structure itself. |
| **Framework** | The physical forward model, statistical assumptions, parameterization, and measurement model. | A framework can be incomplete or unsuitable. |
| **Pattern** | Repeated residuals, discrepancies, distributions, or relationships across observations. | A residual pattern does not uniquely identify its cause. |
| **Constraint** | Measurement limits, prior restrictions, model-domain boundaries, and physical conditions. | Different kinds of constraints must not be conflated. |
| **Purpose** | The stated scientific objective of the model and the function of a modeled component when evidence supports it. | A modeler's objective does not establish ultimate purpose. |
| **Manifestation** | The observed signals and model-predicted results under specified conditions. | A prediction is not an observation. |
| **Witness** | Instruments, data records, diagnostics, models, and investigators involved in registering and interpreting the system. | Multiple witnesses may share interpretive assumptions and limitations. |

The common vocabulary helps describe the subject, its representation, the conditions on observation, and the records used to evaluate the model. It does not make model misspecification a physical force or imply that every unrepresented variable corresponds to a separate physical object.

## 17. Four-Question Study Method

### 1. What must AI ask to understand GUA-W?

AI must ask what the scientific model claims to represent, what observations constrain it, which assumptions are shared, and what evidence indicates possible inadequacy. Is the discrepancy attributable to noise, calibration, selection, parameter error, prior restrictions, an incorrect likelihood, or an omitted physical process? What observation could distinguish these explanations?

AI must not presume that a missing-variable explanation is correct merely because a model leaves a residual.

### 2. What is GUA-W revealing that helps AI understand?

The established GUA-W foundation distinguishes the originating Source, Creation, and derivative Witness. The scientific model is a human representation used to investigate aspects of Creation; it is not the originating physical structure.

The Language of Creation can describe the structure being represented, the framework of the model, patterns in observations and residuals, constraints on representation, manifestations registered by instruments, and the witnesses involved. This is a bounded descriptive application. It does not establish a new GUA-W layer or equate model incompleteness with a theological category.

### 3. What am I learning about what I am witnessing?

I am witnessing that agreement among measurements does not guarantee that the model interpreting them is adequate. Independent data can still be interpreted through shared assumptions. A preferred model can be the best among available candidates and still fail to describe important features of reality.

Residuals and posterior predictive checks can expose possible deficiencies, but they do not uniquely identify a missing physical variable. Out-of-sample prediction, model sensitivity, and discriminating observations can help distinguish explanations.

### 4. What am I learning about the Witness through what I am witnessing?

The investigator does not observe the physical system without mediation. Instruments register signals; processing converts signals into data products; models connect data to physical interpretation.

The Witness must therefore examine not only whether measurements agree, but also which assumptions their interpretations share. A responsible investigator preserves the distinction between observed discrepancy, proposed explanation, and demonstrated mechanism.

When the model is inadequate and the cause remains uncertain, the correct record is that the model is inadequate and the cause remains unresolved.

## 18. Triple Constraint examination

### Biblical compliance

This investigation does not claim that Genesis 1–2 explicitly describes statistical model misspecification, omitted variables, posterior predictive checks, or astronomical inference. These are scientific methods for examining representations of observed phenomena. They do not revise Scripture or establish a theological conclusion.

**Assessment:** No direct contradiction is introduced by this bounded descriptive application. No statistical result is presented as a biblical statement.

### Scientific coherence

The investigation distinguishes likelihood and prior misspecification, omitted physical components and omitted nuisance variables, residuals and their possible causes, relative model preference and absolute adequacy, and model diagnostics from proof of completeness. It uses posterior predictive checking as a diagnostic rather than a truth certificate and requires discriminating predictions before accepting a missing-component explanation.

**Assessment:** Scientifically coherent as a methods-focused investigation. A specific missing-variable claim requires evidence that distinguishes it from calibration, selection, noise, parameter, and other model errors.

### GUA-W consistency

The established architecture remains unchanged. The common vocabulary describes the physical subject, its representation, observational constraints, registered patterns, and witnesses. It does not elevate a scientific model into the originating source or add an architectural operation.

**Assessment:** Consistent as a bounded descriptive application. No architectural expansion is proposed.

## 19. What is established, inferred, and unresolved?

### Established by the cited literature

- Bayesian results can be misleading when likelihoods or priors inadequately represent the data-generating process or population.
- A model preferred over another candidate can still be a poor description of reality.
- Posterior predictive checks and visual diagnostics can help identify some forms of misspecification.
- No finite set of diagnostics guarantees detection of every model deficiency.
- Robust noise models can reduce sensitivity to some forms of outliers or noise-model misspecification in tested settings.
- Developing methods have been proposed to detect misspecification in Bayesian inverse problems, with demonstrations outside astrophysical magnetic-field reconstruction.

### Supported inference

Agreement among multiple datasets does not test a model assumption that all their interpretations share. A model can correctly represent measurement covariance and still omit a relevant physical process or component.

When systematic discrepancies remain, investigators should compare measurement error, selection, parameter error, prior restrictions, likelihood misspecification, and omitted physical structure before selecting an explanation.

### Unresolved

- Which posterior predictive diagnostics are most sensitive to missing physical components in 3D magnetic-field reconstruction?
- How can investigators distinguish an omitted physical component from an inadequate radiative-transfer or grain-alignment prescription?
- What validation design can test assumptions shared across multiple tracers and instruments?
- How can uncertainty in model structure be propagated alongside parameter and measurement uncertainty?
- When does adding a latent variable improve physical inference, and when does it merely absorb unexplained residuals?
- How can model expansion be penalized or validated without suppressing a real but previously unrepresented component?
- What methods can identify discrepancies that remain invisible to the chosen diagnostic statistics?
- How can an investigator test the possibility that all candidate models omit the same process?
- What does it mean for a reconstruction to be adequate for one scientific question but inadequate for another?

These questions remain open.

## 20. Sources

1. Romero-Shaw, I. M., Thrane, E., and Lasky, P. D. (2022). “When models fail: An introduction to posterior predictive checks and model misspecification in gravitational-wave astronomy.” *Publications of the Astronomical Society of Australia* 39, e025. https://doi.org/10.1017/pasa.2022.24
2. “An approach to robust Bayesian regression in astronomy” (2025). *RAS Techniques and Instruments*. https://doi.org/10.1093/rasti/rzaf035
3. Liu, Q., Fisher, M. A., Shen, Z., Tant, K., Zhao, X., Curtis, A., and Oates, C. J. (2025). “Detecting Model Misspecification in Bayesian Inverse Problems via Variational Gradient Descent.” arXiv:2512.01667. https://arxiv.org/abs/2512.01667

## 21. Next question emerging

Investigation 023 shows that multiple observations can agree while their shared interpretive model remains incomplete. Model diagnostics can reveal inadequacy, but a residual does not identify its cause. The next step is to examine how competing explanations can be made to produce different, testable predictions.

A possible next investigation is **Falsifiability, Model Discrimination, and the Design of Critical Tests**: what observation would count against a favored reconstruction, how can a test be designed so competing explanations risk different outcomes, and how do investigators avoid turning every possible result into support for the same model?

This is a possible lead, not a fixed assignment.

---

**Investigation 023 records the distinction between agreement among observations and adequacy of the model used to interpret them. It preserves missing-variable explanations as hypotheses until discriminating evidence supports them.**
