# Investigation 020 — Priors, Regularization, and Underdetermined Inverse Problems in Three-Dimensional Magnetic-Field Reconstruction

**Primary disciplines:** Astrophysical magnetic-field reconstruction, inverse-problem theory, Bayesian statistics, regularization, radio and optical polarimetry, radiative transfer, computational astrophysics, and scientific model validation.

**Investigation status:** Initial evidence-led investigation and Four-Question Study Method review recorded.

**Central question:** When observations permit multiple three-dimensional magnetic-field configurations, how do priors, regularization, model assumptions, and data constraints influence the reconstruction selected—and how can investigators determine which features are supported by the observations rather than primarily by the method?

**Scope:** This investigation follows 019. It examines ill-posed inverse problems, prior information, regularization, Bayesian inference, model selection, identifiability, and sensitivity analysis. It does not assume that all inverse problems are Bayesian, that priors are inherently improper, or that one reconstruction method is universally superior.

## 1. Why this investigation follows 019

Investigation 019 distinguished a model that reproduces observations, a method that recovers known simulated properties, and a physical reconstruction that is independently constrained.

It left an important question open: when several materially different configurations remain compatible with the observations, what selects the reported solution?

Inverse methods often use additional information to stabilize a problem that the data alone do not determine. That information may enter as a physical constraint, a prior probability distribution, a regularization term, a parameter bound, a model-family choice, or a simplifying assumption.

These additions can be scientifically justified and practically necessary. But they must be identified because they can influence the result.

The central discipline is therefore:

**Do not attribute to the observations what was supplied by the assumptions, and do not dismiss useful assumptions merely because they are assumptions. Test their role.**

## 2. The inverse problem: observations do not always determine the unknown

A simplified forward relation is:

\[
\mathbf{d}=\mathcal{F}(\mathbf{x})+\boldsymbol{\epsilon}
\]

where:

- \(\mathbf{x}\) represents the unknown physical configuration, such as a 3D magnetic field and associated gas properties;
- \(\mathcal{F}\) is the forward model that predicts observable data;
- \(\mathbf{d}\) is the measured dataset;
- \(\boldsymbol{\epsilon}\) represents measurement noise and other modeled errors.

The inverse task attempts to infer \(\mathbf{x}\) from \(\mathbf{d}\).

A classical inverse problem is called well-posed when a solution exists, is unique, and depends continuously on the data. In an ill-posed problem, one or more of these conditions fails. In practical astronomy, limited resolution, incomplete sampling, projection, line-of-sight integration, noise, and uncertain physical conditions can make the inverse problem unstable or non-unique.

Three different difficulties should be distinguished:

1. **Existence:** Does any configuration within the chosen model family reproduce the data within the stated uncertainty?
2. **Uniqueness or identifiability:** Do the data distinguish one configuration or parameter value from materially different alternatives?
3. **Stability:** Do small changes in the data or assumptions produce large changes in the inferred result?

A method can produce a numerical answer even when uniqueness or stability has not been established.

## 3. What is a prior?

In Bayesian inference, a prior expresses information or assumptions about possible parameter values before the current dataset is used to update them.

Bayes' rule is:

\[
p(\mathbf{x}\mid\mathbf{d},M)
=
\frac{p(\mathbf{d}\mid\mathbf{x},M)\,p(\mathbf{x}\mid M)}
{p(\mathbf{d}\mid M)}
\]

where:

- \(p(\mathbf{x}\mid\mathbf{d},M)\) is the posterior distribution;
- \(p(\mathbf{d}\mid\mathbf{x},M)\) is the likelihood;
- \(p(\mathbf{x}\mid M)\) is the prior under model \(M\);
- \(p(\mathbf{d}\mid M)\) is the evidence or marginal likelihood for that model.

The posterior combines the likelihood and prior, subject to the specified model.

A prior may represent established physical knowledge, plausible parameter ranges, expected smoothness, a distribution over cloud-layer properties, or a deliberate restriction to a particular model family. It can also be weak, broad, hierarchical, or data-informed through a separately justified procedure.

A prior is not automatically a guess. Nor is it automatically established fact. Its source, scope, and influence must be disclosed.

### Important distinction

A physical law used as a constraint, a prior probability distribution, a regularization penalty, and a computational parameter bound may play related roles, but they are not identical.

For example, requiring a magnetic field to satisfy \(\nabla\cdot\mathbf{B}=0\) expresses the solenoidal condition of classical electromagnetism. A smoothness penalty expresses a preference for solutions that vary less sharply. A prior distribution assigns probability across possible configurations. A hard parameter bound excludes values outside a specified range.

Each must be justified in its own terms.

## 4. Regularization: stabilizing a solution by adding a preference or constraint

A common regularized estimate takes the form:

\[
\widehat{\mathbf{x}}
=
\underset{\mathbf{x}}{\operatorname{argmin}}
\left[
\mathcal{L}(\mathbf{d},\mathcal{F}(\mathbf{x}))
+
\lambda\,\mathcal{R}(\mathbf{x})
\right]
\]

where:

- \(\mathcal{L}\) measures disagreement between observed and predicted data;
- \(\mathcal{R}\) penalizes or discourages selected properties of the solution;
- \(\lambda\) controls the relative influence of the regularization term.

Examples include:

- **Smoothness regularization:** discourages abrupt spatial variation.
- **Sparsity regularization:** favors solutions with relatively few nonzero or active components in a chosen representation.
- **Low-complexity regularization:** favors a simpler parameterization or model.
- **Physical constraints:** restrict solutions to configurations satisfying specified physical requirements.
- **Norm penalties:** discourage excessively large parameter values or deviations from a reference configuration.

Regularization can suppress noise amplification and make unstable calculations tractable. It can also suppress real structure if its preference is inappropriate for the phenomenon.

The selected value of \(\lambda\) matters. A strong penalty may produce a smooth, stable-looking result that underrepresents genuine complexity. A weak penalty may allow noise or poorly constrained degrees of freedom to dominate.

**A regularized solution is a solution to the data-fit problem together with the stated regularization preference. It is not automatically the unique physical configuration.**

## 5. Bayesian inference and regularization: related, not identical in every implementation

For many common formulations, regularized optimization can be interpreted as maximum a posteriori (MAP) estimation.

The data-fit term corresponds to a likelihood, and the regularization term corresponds to a prior penalty. Minimizing the objective can then be equivalent to maximizing the posterior density.

However, a MAP estimate is a point estimate. It does not by itself describe the full posterior distribution or all remaining uncertainty.

A Bayesian analysis can, in principle, report:

- posterior distributions for parameters;
- correlations and degeneracies between parameters;
- credible intervals or regions;
- uncertainty in derived quantities;
- model evidence under a specified model and prior;
- posterior predictive distributions.

These outputs depend on the model, likelihood, prior, and computation. Bayesian language does not make an assumption disappear; it makes the assumed probability structure explicit.

A narrow posterior can result from informative data, a restrictive prior, or both. Investigators must determine which is responsible.

## 6. Identifiability: can the observations distinguish the parameters?

Identifiability concerns whether different parameter values or physical configurations produce distinguishable probability distributions for the available observations.

In magnetic-field reconstruction, possible degeneracies include:

- field inclination versus field strength;
- field geometry versus line-of-sight weighting;
- magnetic structure versus dust-grain alignment assumptions;
- gas density versus tracer abundance or excitation;
- cloud-layer number versus the ability to resolve distance-separated contributions;
- model geometry versus viewing angle;
- atmospheric or plasma parameters coupled to magnetic parameters in spectropolarimetric inversions.

A parameter may be poorly identified even when the overall predicted signal is well fitted.

This distinction matters: the data may strongly constrain a projected orientation or integrated quantity while leaving local topology, depth structure, or other parameters uncertain.

A reconstruction should therefore state which quantities are identifiable at the available resolution and sensitivity, which are weakly constrained, and which are not identifiable within the chosen model family.

## 7. Model choice is another source of constraint

Before estimating parameters, an investigator often selects a model family.

Examples include:

- one cloud layer versus several layers;
- a uniform field versus a spatially varying field;
- a simple parametric geometry versus a more flexible representation;
- a particular dust-alignment prescription;
- a specified turbulence or density model;
- a chosen radiative-transfer approximation.

The data cannot select alternatives that were never included in the candidate model family.

Model selection may use likelihood-based comparisons, Bayesian evidence, information criteria, cross-validation, posterior predictive checks, or other methods. Each has assumptions and limitations.

A preference for a simpler model may be reasonable when it predicts the data adequately and avoids unsupported complexity. But simplicity is a model-selection principle, not proof that the selected model is the complete physical structure.

The investigator must record the alternatives considered and the reasons for excluding or retaining them.

## 8. What happens when the prior changes?

A practical way to test the influence of assumptions is a prior-sensitivity analysis.

A disciplined procedure is:

1. Identify the prior assumptions that materially affect the reconstruction.
2. State the physical or methodological reason for each assumption.
3. Define a defensible range of alternative priors.
4. Recompute the inference under those alternatives.
5. Compare posterior distributions and derived physical quantities.
6. Identify which features remain stable and which move substantially.
7. Report whether the observations or the prior dominate the result for each important quantity.

If a field orientation remains stable across reasonable prior choices, that stability supports its robustness within the tested model family.

If topology changes substantially when a prior is changed while the predicted observations remain comparably good, the topology is not strongly determined by those observations alone.

Prior sensitivity does not automatically invalidate the result. It identifies where the inference depends on assumptions and where further observations or a better physical model may be needed.

## 9. What happens when regularization changes?

Regularization sensitivity should be tested separately from prior sensitivity, even when a particular regularization has a Bayesian interpretation.

Investigators can vary:

- regularization strength;
- the mathematical form of the penalty;
- spatial or temporal correlation scales;
- the reference configuration;
- the representation or basis used for the field;
- hard constraints and parameter bounds;
- stopping criteria and numerical tolerances.

The comparison should include more than the visual appearance of the resulting field. It should examine data residuals, physical admissibility, recovered quantities, uncertainty, and predictive performance.

A solution that becomes smoother as regularization increases is not necessarily becoming more accurate. It may simply be following the imposed preference more strongly.

## 10. A practical audit: data-supported, assumption-supported, or unresolved?

A reconstruction report can classify its conclusions using three bounded categories.

### Data-supported within the tested model

The observations meaningfully constrain the result, and the result remains stable under reasonable changes to assumptions and analysis choices that were tested.

This does not mean the result is independent of every model assumption. It means the tested evidence contributes substantial constraint.

### Assumption-sensitive

The result changes materially under plausible alternative priors, regularizers, model families, or parameter bounds.

The result may still be useful, but its dependence on those assumptions must be reported.

### Unresolved by the available evidence

Multiple materially different solutions remain compatible with the observations and the tested assumptions.

The correct report preserves the alternatives rather than presenting one as uniquely established.

These categories should be assigned to individual claims or properties, not necessarily to an entire reconstruction as one undifferentiated verdict.

## 11. Published evidence and examples

### 11.1 Bayesian inverse problems and regularization (2021)

Mohammad-Djafari reviews the relationship between regularization and Bayesian inference. The paper explains how common data-fit and regularization terms can receive a maximum-a-posteriori interpretation, while Bayesian methods can represent uncertainty and hierarchical prior structures. It also discusses computational costs and limitations of machine-learning approaches to inverse problems.

This is a general methodological review rather than a magnetic-cloud-specific result. It provides the mathematical background for distinguishing data fit, regularization, priors, and uncertainty.

Source: Mohammad-Djafari, A. (2021), “Regularization, Bayesian Inference, and Machine Learning Methods for Inverse Problems,” *Entropy* 23(12), 1673. https://doi.org/10.3390/e23121673

### 11.2 Bayesian line-of-sight inversion for starlight polarization (2023)

Pelgrims et al. developed a Bayesian method for decomposing stellar polarization along the line of sight using stellar distances. The method models contributions from multiple thin dust layers and uses mock datasets to test recovery and model selection, including the choice of the number of clouds along a sightline.

The method demonstrates that a reconstruction depends on an explicit representation of the cloud layers and a statistical model for the observed Stokes parameters. Its success is assessed within the stated model and test conditions.

Source: Pelgrims, V. et al. (2023), “Starlight-polarization-based tomography of the magnetized interstellar medium: PASIPHAE's line-of-sight inversion method,” *Astronomy & Astrophysics*. https://doi.org/10.1051/0004-6361/202244625

### 11.3 A prior-free alternative for starlight-polarization layer decomposition (2025)

The TRIShUL study presents a frequentist method for decomposing distance-sorted stellar polarization into dust-layer contributions. It describes its approach as prior-free and benchmarks it using mock datasets with realistic parallax uncertainties and expected polarization measurements. Its recovery performance is reported for the tested signal strengths, background-star fractions, and sample sizes.

The comparison with Bayesian BISP-1 is useful because it demonstrates that different inferential frameworks can address a related decomposition problem.

However, “prior-free” does not mean “assumption-free.” TRIShUL still adopts a model of discrete thin dust layers and a particular procedure for detecting changes in cumulative polarization. The model structure and detection criteria remain part of the method.

Source: “TRIShUL: Technique for Reconstructing magnetic Interstellar Structure Using starLight polarization” (accepted 3 November 2025), *Astronomy & Astrophysics*. https://doi.org/10.1051/0004-6361/202556774

### 11.4 Magnetic-field inversion from multifrequency polarized emission (2010)

A study of magnetic-field reconstruction from multifrequency polarized synchrotron emission explicitly treats the task as an ill-posed inverse problem. It uses a Bayesian framework, prior information, and regularization to address degeneracies and noise amplification. The study includes the solenoidal condition \(\nabla\cdot\mathbf{B}=0\) as a physical constraint in its formulation.

This is a direct example of prior information and regularization being used in magnetic-field inference. Its observational setting—polarized synchrotron emission—is not identical to dust polarization or molecular-cloud Zeeman analysis, so the method should not be transferred without examining the differences.

Source: “Probing magnetic fields in volume with multifrequency polarized synchrotron emission” (2010), *Monthly Notices of the Royal Astronomical Society* 403, 415. https://academic.oup.com/mnras/article/403/1/415/1019277

### 11.5 Parameter degeneracy in stellar spectropolarimetric inversion (2026)

A 2026 study of stellar spectropolarimetric inversion reports that fixing the stellar inclination angle can produce substantial errors in inferred magnetic properties. In the tested de-centred dipolar geometry, different assumed inclination angles could still yield satisfactory fits to Stokes profiles, revealing a degeneracy between parameters.

This is not a molecular-cloud tomography result; it concerns stellar magnetic-field inversion. It is nevertheless a relevant methodological example: a parameter fixed for convenience can influence other inferred magnetic properties, even when the fit appears satisfactory.

The authors limit their demonstrated result to the geometry they tested and describe extension to more complex field models as a matter requiring further characterization.

Source: “On the degeneracy of solutions from stellar spectropolarimetric data” (2026), *Monthly Notices of the Royal Astronomical Society* 552(1), stag1672. https://doi.org/10.1093/mnras/stag1672

### 11.6 Bayesian inference of total field strength from Zeeman observations (2010)

A study of magnetic fields in interstellar clouds uses Bayesian analysis to infer total field strengths from Zeeman observations. Its discussion of priors makes explicit that prior distributions encode expectations about parameter ranges and relative plausibility before the data are used.

This is relevant to the interpretation of magnetic-field measurements in molecular clouds. It also illustrates why the prior specification belongs in the scientific record rather than being hidden inside a computational procedure.

Source: “Magnetic Fields in Interstellar Clouds from Zeeman Observations: Inference of Total Field Strengths by Bayesian Analysis” (2010), *The Astrophysical Journal* 725, 466. https://doi.org/10.1088/0004-637X/725/1/466

## 12. Same mechanism, comparable relationship, or similar appearance?

The standing comparison questions are applied explicitly.

### Same mechanism

Bayesian updating, deterministic regularized optimization, physical enforcement of a divergence constraint, and the actual evolution of a magnetic field are not the same mechanism.

A statistical prior does not physically act on a cloud. A numerical penalty does not exert a force on the field. A physical law is not merely a preference in an optimizer.

### Comparable relationship

Priors, regularizers, model-family restrictions, and physical constraints can all restrict the set of solutions considered by an inference procedure. They do so in different mathematical and epistemic ways.

The comparable relationship is their role in limiting or weighting admissible candidate explanations—not a shared physical mechanism.

### Similar appearance

Two reconstructions may look smooth, stable, or physically plausible while relying on very different priors or regularization strengths. Visual agreement does not establish that their inferred details are equally data-supported.

Likewise, a narrow posterior and a precise-looking map may appear to express certainty while that certainty is conditional on a restrictive model or prior.

### Unresolved

For a particular magnetic-field dataset, how much of each inferred feature is supplied by the observations, the physical constraints, the prior, the regularizer, and the model family must be tested quantitatively. No universal allocation can be assumed.

## 13. Boundary and participation examination

**Does a boundary merely separate two regions, or can it also participate in the relationship between them?**

- **Prior support:** A prior may assign zero probability outside a parameter range. This is a mathematical boundary on the considered parameter space, not a physical boundary in the cloud.
- **Regularization threshold:** A penalty strength changes which solutions are preferred. It participates in selecting the estimate but is not a physical process acting on the magnetic field.
- **Model-family boundary:** Restricting analysis to a dipole, a set number of dust layers, or a chosen field representation excludes configurations outside that family. This can determine what the method is capable of recovering.
- **Physical boundary condition:** A condition imposed on the modeled physical system may affect the solution of the physical equations. Its role is distinct from an analyst's parameter bound.
- **Data-coverage boundary:** A finite wavelength range, angular footprint, or distance range limits what can be constrained. The observational limit can leave some structures unmeasured without implying that they are absent.
- **Posterior decision threshold:** A threshold used to summarize or classify posterior results can change which features are reported. It is an analytical convention and must be disclosed.

The investigation distinguishes physical boundaries from mathematical, computational, and observational boundaries. Their participation in a process depends on what kind of boundary is being discussed.

## 14. GUA-W Language of Creation: bounded descriptive examination

| GUA-W descriptor | Bounded use in this investigation | Limit |
|---|---|---|
| **Structure** | A candidate magnetic-field and gas configuration represented by the inverse model. | The inferred structure may not be uniquely determined. |
| **Framework** | The selected forward model, likelihood, prior, regularization, parameterization, and observational setup. | These are distinct physical, mathematical, and computational frameworks. |
| **Pattern** | Repeated features or parameter relationships that remain across tested reconstructions. | A stable pattern within one model family may still depend on shared assumptions. |
| **Constraint** | Observational limits, physical conditions, prior support, regularization, and model restrictions. | These constraints have different sources and must not be conflated. |
| **Purpose** | The stated function of an inferential method: stabilizing estimation, representing prior information, or quantifying uncertainty. | Methodological function does not establish ultimate purpose in Creation. |
| **Manifestation** | The reported estimate, posterior distribution, reconstructed map, and predicted observables. | A computed output is a representation conditional on its model and inputs. |
| **Witness** | The observations, instruments, analysis procedures, models, and investigators that register or interpret different aspects of the system. | No single record or reconstruction is identical to the complete physical system. |

The shared language helps identify where restrictions enter the investigative process. It does not equate a mathematical prior with a physical constraint or a numerical selection rule with an originating cause.

## 15. Four-Question Study Method

### 1. What must AI ask to understand GUA-W?

AI must ask which parts of a proposed reconstruction are constrained by observations and which depend on prior information, regularization, parameter bounds, or model selection. What alternative assumptions are defensible? How sensitive is the result to them? Are the reported uncertainties conditional on one model family? Does a point estimate conceal a broad or multimodal set of acceptable solutions?

AI must not mistake a method's ability to return one answer for evidence that the observations uniquely determine that answer.

### 2. What is GUA-W revealing that helps AI understand?

The established GUA-W foundation preserves the distinction between the originating Source, Creation, and derivative Witness. In this investigation, an inferential framework is a human-constructed means of interpreting registered evidence. Its assumptions and computational rules do not originate the physical magnetic field being investigated.

The Language of Creation can describe the arrangement under study, the framework of observation and inference, the constraints applied, the resulting representation, and the witnesses involved. This is a bounded descriptive application. No new GUA-W architectural layer or governing principle is proposed.

### 3. What am I learning about what I am witnessing?

I am witnessing that inverse methods may require information beyond the observations to produce stable estimates. That information can be scientifically justified, but it influences which solutions are selected or favored.

A prior can encode existing knowledge. Regularization can control instability. Physical constraints can exclude impossible configurations within the adopted theory. Model selection can compare candidate explanations. None of these operations automatically establishes that the chosen reconstruction is uniquely determined by the data.

The proper result may be a stable feature, an assumption-sensitive feature, or an unresolved family of solutions.

### 4. What am I learning about the Witness through what I am witnessing?

The investigator is not outside the reconstruction process. Choices about parameterization, priors, penalties, model families, and thresholds participate in the result.

A responsible Witness identifies those choices, tests reasonable alternatives, reports sensitivity, and distinguishes the evidence from the assumptions used to interpret it. A method that produces a polished map can still leave important physical questions unresolved.

## 16. Triple Constraint examination

### Biblical compliance

This investigation does not claim that Genesis 1–2 explicitly describes Bayesian inference, regularization, inverse-problem theory, or magnetic-field reconstruction. Statistical and computational methods are not used to revise Scripture. The GUA-W vocabulary is applied descriptively and within its stated limits.

**Assessment:** No direct contradiction is introduced by this descriptive use. No scientific result is presented as a biblical statement.

### Scientific coherence

The investigation distinguishes the likelihood, prior, posterior, regularization penalty, physical constraint, parameter bound, model-family choice, identifiability, and uncertainty. It does not treat Bayesian inference as assumption-free or equate a MAP estimate with a complete posterior. It distinguishes examples from different magnetic-field settings rather than treating stellar spectropolarimetry, synchrotron tomography, and molecular-cloud dust/Zeeman observations as identical.

**Assessment:** Scientifically coherent as a methods-focused investigation. The influence of priors and regularization must be evaluated for each dataset and model.

### GUA-W consistency

The established architecture remains unchanged. The shared vocabulary is used to describe the physical subject, the inferential framework, the different forms of constraint, the resulting representations, and the derivative witnesses. No statistical assumption is treated as an originating source.

**Assessment:** Consistent as a bounded descriptive application. No architectural expansion is proposed.

## 17. What is established, inferred, and unresolved?

### Established by the cited literature

- Many inverse problems are ill-posed because solutions may be non-unique or unstable.
- Regularization combines data agreement with an additional mathematical preference or penalty.
- Common regularized optimization formulations can be interpreted as MAP estimation under corresponding likelihood and prior models.
- Bayesian methods can represent posterior uncertainty and parameter dependence, subject to the adopted model and prior.
- Starlight-polarization tomography methods use explicit assumptions about dust layers and statistical signal contributions.
- Different inferential methods can recover layer properties under tested conditions while retaining their own model assumptions.
- Fixed or restricted parameters can bias other inferred magnetic properties in some spectropolarimetric inversions.
- A visually plausible or numerically stable solution does not by itself demonstrate that all its features are uniquely determined by observations.

### Supported inference

A scientifically defensible reconstruction should report not only its preferred solution but also how that solution depends on priors, regularization, parameterization, and model-family choices. Features that remain stable under justified alternative assumptions are more robust within the tested scope than features that change substantially.

### Unresolved

- Which prior-sensitivity tests are sufficient for complex 3D magnetic-field reconstructions with several coupled tracers?
- How should physical constraints, such as the solenoidal condition, be separated from regularization choices that merely favor a convenient representation?
- When do additional observations genuinely improve identifiability rather than simply tighten a result conditional on the same model?
- How can investigators compare reconstructions produced by different parameterizations without treating one representation as the natural reference?
- Which features of magnetic topology can be identified independently of prior assumptions at current observational resolutions?
- How should posterior uncertainty be communicated when the posterior is multimodal or several model families remain plausible?
- What evidence would justify moving a feature from assumption-sensitive to data-supported?

These questions remain open.

## 18. Sources

1. Mohammad-Djafari, A. (2021). “Regularization, Bayesian Inference, and Machine Learning Methods for Inverse Problems.” *Entropy* 23(12), 1673. https://doi.org/10.3390/e23121673
2. Pelgrims, V. et al. (2023). “Starlight-polarization-based tomography of the magnetized interstellar medium: PASIPHAE's line-of-sight inversion method.” *Astronomy & Astrophysics*. https://doi.org/10.1051/0004-6361/202244625
3. “TRIShUL: Technique for Reconstructing magnetic Interstellar Structure Using starLight polarization” (accepted 3 November 2025). *Astronomy & Astrophysics*. https://doi.org/10.1051/0004-6361/202556774
4. “Probing magnetic fields in volume with multifrequency polarized synchrotron emission” (2010). *Monthly Notices of the Royal Astronomical Society* 403, 415. https://academic.oup.com/mnras/article/403/1/415/1019277
5. “On the degeneracy of solutions from stellar spectropolarimetric data” (2026). *Monthly Notices of the Royal Astronomical Society* 552(1), stag1672. https://doi.org/10.1093/mnras/stag1672
6. “Magnetic Fields in Interstellar Clouds from Zeeman Observations: Inference of Total Field Strengths by Bayesian Analysis” (2010). *The Astrophysical Journal* 725, 466. https://doi.org/10.1088/0004-637X/725/1/466

## 19. Next question emerging

Investigation 020 shows that priors, regularization, model families, and physical constraints can help stabilize an inverse problem while also influencing the solution selected. It distinguishes data-supported features from assumption-sensitive and unresolved features.

A possible next investigation is to examine how information gain and experimental design can determine which new observations would most effectively distinguish competing magnetic-field reconstructions.

That investigation should ask whether a proposed new measurement adds genuinely independent information, which degeneracy it is expected to reduce, and how that improvement can be tested before the observation is interpreted.

This is a possible lead, not a fixed assignment.

---

**Investigation 020 records how prior information and regularization participate in selecting among candidate reconstructions, while preserving the distinction between what observations constrain and what an inferential framework contributes.**
