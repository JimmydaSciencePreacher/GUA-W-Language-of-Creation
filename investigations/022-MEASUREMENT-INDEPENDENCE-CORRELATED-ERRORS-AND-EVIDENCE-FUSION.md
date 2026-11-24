# Investigation 022 — Measurement Independence, Correlated Errors, and Evidence Fusion

**Primary disciplines:** Statistical inference, measurement science, covariance analysis, Bayesian data fusion, observational astronomy, astrophysical magnetism, polarimetry, Zeeman spectroscopy, Faraday rotation, radiative transfer, and uncertainty quantification.

**Investigation status:** Initial evidence-led investigation and Four-Question Study Method review recorded.

**Central question:** When multiple instruments, tracers, or datasets appear to support the same physical conclusion, how can we determine whether they contribute independent constraints, overlapping information, correlated errors, or shared assumptions—and how should they be combined without overstating the evidence?

**Scope:** This investigation follows 021. It examines statistical independence, conditional independence, covariance, common-mode systematic errors, shared physical signals, overlapping observations, evidence fusion, and validation. It uses magnetic-field reconstruction as its primary scientific case. It does not assume that different instruments produce independent evidence, that correlated measurements are useless, or that a single covariance model captures every source of dependence.

## 1. Why this investigation follows 021

Investigation 021 asked which additional observation would most effectively distinguish competing magnetic-field reconstructions.

Investigation 022 asks a necessary question before those observations are combined:

**When several measurements agree, how much additional evidentiary constraint have we actually gained?**

Two instruments may be physically different and still share important dependencies. They may observe the same sky region, sample the same underlying material, use a common calibration reference, rely on the same distance catalog, or interpret their signals through the same physical model.

Conversely, measurements that are strongly related to the same physical system can still contribute complementary information if they respond to different components or projections of that system.

The important distinction is not simply whether two instruments are different. It is whether their measurement errors, information content, and inferential dependencies are independent in the sense required by the analysis.

## 2. What does measurement independence mean?

Suppose two datasets are represented by \(D_1\) and \(D_2\), and the physical parameters of interest by \(\theta\).

A common joint-likelihood simplification is:

\[
p(D_1,D_2\mid\theta)
=
p(D_1\mid\theta)\,p(D_2\mid\theta)
\]

This factorization is valid when the datasets are conditionally independent given the modeled parameters and assumptions.

That qualification matters.

Two measurements can be conditionally independent given a complete model while still being statistically dependent before conditioning, because both respond to the same unknown physical parameters. They may also cease to be conditionally independent if a shared calibration error, common background, overlapping sample, or omitted latent variable is not included in the model.

Therefore, the investigator must state what the measurements are assumed independent *given*.

### Four distinct situations

1. **Independent measurement errors:** After accounting for the modeled physical signal and shared nuisance parameters, the remaining errors are independent to the required approximation.
2. **Correlated measurement errors:** Errors co-vary because of shared calibration, instrument effects, background subtraction, common processing, or other dependencies.
3. **Overlapping information:** Different datasets constrain some of the same physical quantities or sample the same underlying signal, even if their instrumental noise is independent.
4. **Complementary information:** Datasets respond to different aspects of the physical system and can constrain different components or degeneracies.

These categories can coexist. Two observations may be complementary in physical sensitivity while sharing calibration errors. Two observations may have independent detector noise while substantially overlapping in the physical information they contain.

## 3. Covariance: a way to represent shared variation

For two measurement errors \(\epsilon_1\) and \(\epsilon_2\), covariance is:

\[
\operatorname{Cov}(\epsilon_1,\epsilon_2)
=
\mathbb{E}
\left[
(\epsilon_1-\mathbb{E}\epsilon_1)
(\epsilon_2-\mathbb{E}\epsilon_2)
\right]
\]

If the covariance is nonzero, the errors have a linear statistical dependence. Zero covariance does not in general prove independence; it does so for jointly Gaussian variables, but not for arbitrary distributions.

For a collection of measurements, the covariance matrix is:

\[
\mathbf{C}
=
\begin{pmatrix}
\sigma_1^2 & C_{12} & \cdots \\
C_{21} & \sigma_2^2 & \cdots \\
\vdots & \vdots & \ddots
\end{pmatrix}
\]

The diagonal terms describe variances. Off-diagonal terms describe pairwise covariances.

A joint analysis that ignores important off-diagonal terms can misstate the effective information and uncertainty. In some circumstances it can count shared information more than once and produce an unjustifiably narrow uncertainty estimate. In other circumstances, failing to model dependence can also distort parameter estimates or goodness-of-fit assessments.

The covariance model must correspond to the actual data-generation and processing process. A covariance matrix is not a magic correction: omitted dependencies remain omitted.

## 4. A simple common-systematic example

Imagine two instruments measure the same quantity \(B\), but each has its own random noise and both share an uncertain calibration offset \(c\):

\[
y_1=B+c+\eta_1
\]

\[
y_2=B+c+\eta_2
\]

where \(\eta_1\) and \(\eta_2\) are independent instrument-specific errors, while \(c\) is common to both.

If the variance of the common offset is \(\sigma_c^2\), and the individual noise variances are \(\sigma_1^2\) and \(\sigma_2^2\), then:

\[
\mathbf{C}
=
\begin{pmatrix}
\sigma_1^2+\sigma_c^2 & \sigma_c^2 \\
\sigma_c^2 & \sigma_2^2+\sigma_c^2
\end{pmatrix}
\]

The shared calibration term creates covariance between the measurements.

Collecting more measurements with the same common offset can reduce independent random noise, but it does not automatically eliminate uncertainty in that shared offset.

This is a general measurement-science example, not a claim that all astronomical instruments share one calibration error. Real observations may contain several common and instrument-specific systematics, some nonlinear or time-dependent.

## 5. Common causes of dependence in astronomical datasets

Dependence can enter at multiple points in the observation and analysis chain.

### 5.1 Shared calibration

Datasets may use the same calibrator source, reference standard, flux scale, polarization-angle reference, clock, detector model, or calibration pipeline. Uncertainty in a shared reference can propagate into both datasets.

### 5.2 Shared sky signal and cosmic variance

Two telescopes observing the same region do not receive independent realizations of the sky. They may have independent detector noise, but both observe the same underlying astrophysical signal. In cosmological surveys, measurements of overlapping sky modes can share cosmic variance.

### 5.3 Overlapping samples or sight lines

Two catalogs may contain many of the same stars or sources. Two surveys may observe the same cloud volume or use overlapping sight lines. Treating duplicated objects as independent observations can inflate the apparent sample size.

### 5.4 Shared preprocessing

Datasets may use the same background model, source extraction, map-making, masking, beam correction, or quality cuts. A processing error can therefore affect both results.

### 5.5 Shared physical assumptions

Different instruments may produce different raw observables but both be interpreted using the same assumptions about geometry, grain alignment, optical depth, tracer abundance, or radiative transfer.

This is not necessarily statistical error covariance. It is a shared model dependency. It can make apparently independent lines of reasoning less independent than they first appear.

### 5.6 Shared external reference data

Distance estimates, source catalogs, laboratory constants, ephemerides, or reference spectra can enter multiple analyses. Uncertainty in those inputs can create dependencies between derived results.

## 6. Evidence overlap is not the same as correlated error

A key distinction:

- **Correlated errors** concern how deviations from the modeled signal co-vary.
- **Overlapping information** concerns how much of the physical information is repeated across datasets.
- **Shared assumptions** concern common choices in the interpretation or forward model.
- **Complementarity** concerns whether datasets constrain different aspects of the physical system.

These are not interchangeable.

Two instruments can have independent noise but measure nearly the same projected quantity. They may improve precision without resolving a structural degeneracy.

Two instruments can have correlated errors but still provide complementary physical sensitivity. Their combined information can remain valuable if the covariance and shared nuisance parameters are modeled appropriately.

Two analyses can use different instruments yet inherit the same physical assumption. Their agreement may then be less independent as a test of that assumption.

The investigation must audit each type of dependence separately.

## 7. Evidence fusion: combine measurements through a joint model

Evidence fusion is the process of combining observations or data products to infer shared physical parameters, states, or competing explanations.

A general joint inference is:

\[
p(\theta,\phi\mid D_1,D_2,M)
\propto
p(D_1,D_2\mid\theta,\phi,M)
\,p(\theta,\phi\mid M)
\]

where:

- \(\theta\) represents physical parameters of interest;
- \(\phi\) represents nuisance parameters, such as calibration offsets or shared backgrounds;
- \(D_1,D_2\) are the datasets;
- \(M\) is the adopted model.

If the datasets are conditionally independent given both \(\theta\) and \(\phi\), then:

\[
p(D_1,D_2\mid\theta,\phi,M)
=
p(D_1\mid\theta,\phi,M)
p(D_2\mid\theta,\phi,M)
\]

The shared nuisance parameters are still inferred jointly. They are not silently treated as separate independent errors.

When the datasets have correlated residuals, the likelihood must represent the joint covariance or another suitable dependence model. When the dependence is nonlinear or non-Gaussian, a simple covariance matrix may be insufficient.

The correct fusion method follows the measurement model, not a preference for one statistical technique.

## 8. Magnetic-field reconstruction: complementary tracers are not interchangeable witnesses

The interstellar magnetic field is difficult to reconstruct because different observations sample different components, weight different material, and integrate along different paths.

### Dust polarization

Thermal dust polarization can trace the orientation of the magnetic field projected onto the plane of the sky, under assumptions about grain alignment and emission. The result is weighted by dust emissivity, alignment efficiency, temperature, optical depth, and line-of-sight integration.

### Zeeman splitting

Zeeman measurements provide information about the line-of-sight magnetic-field component in the material contributing to the selected spectral line. The measured result is weighted by the tracer and line formation conditions. It is not automatically a volume-uniform field measurement.

### Faraday rotation

Faraday rotation probes magnetized ionized material along the line of sight. Its interpretation depends on electron density and the magnetic field component along the propagation path, and may include foreground or background contributions.

### Starlight polarization with distance information

Starlight polarization can accumulate contributions from dust between the observer and each star. Combining polarization with distance estimates can help separate foreground and more distant components, subject to sampling and distance uncertainties.

### Molecular-line spectroscopy

Molecular lines constrain velocity, excitation, and tracer-specific gas components. They can help identify material that contributes to other signals, but velocity structure is not itself a direct measurement of the full magnetic vector.

These methods are complementary because their physical sensitivities differ. They are not automatically statistically independent: they may sample the same cloud, share distance or calibration information, or rely on common assumptions about the gas and dust distribution.

## 9. Published magnetic-field example: dust polarization plus Zeeman splitting

Reissl et al. (2018) used radiative-transfer simulations of filaments with multiple magnetic geometries and inclinations to generate synthetic dust-polarization and Zeeman signatures.

Their study found that linear dust polarization alone could not uniquely constrain the three-dimensional field morphology in the tested configurations. Adding Zeeman directional information reduced or resolved some of those ambiguities. The study also found that line-of-sight averaging could make Zeeman-derived field strengths substantially lower than the input field strengths in the simulated filaments.

This is a particularly useful example because the two tracers are complementary: dust polarization provides projected plane-of-sky orientation, while Zeeman splitting provides line-of-sight field information.

But the study does not establish that every real-world combination of dust and Zeeman data will uniquely recover a 3D field. Its result is conditional on the simulated configurations, radiative-transfer assumptions, and observational setup.

Source: Reissl, S. et al. (2018), “Magnetic fields in star-forming systems (I): idealized synthetic signatures of dust polarization and Zeeman splitting in filaments,” *Monthly Notices of the Royal Astronomical Society* 481, 2507–2522. https://doi.org/10.1093/mnras/sty2415

## 10. A caution from adding a third tracer: Faraday rotation

Reissl et al. (2020) examined dust polarization, Zeeman effect, and Faraday rotation measure using synthetic observations from an MHD filament simulation.

The authors found that the three tracers have different sensitivities, but also that density, temperature, viewing angle, and line-of-sight structure can strongly affect the signals. In the tested low-mass filament, the magnetic-field morphology was not unambiguously determined by the individual tracers, even though line-of-sight field strengths could be recovered within stated factors.

This is an important qualification:

**Adding another tracer can add a new constraint without guaranteeing that the complete physical structure becomes identifiable.**

A third dataset may reduce some degeneracies while leaving others intact. Its contribution must be evaluated against the actual candidate models and the physical conditions that shape the signal.

Source: Reissl, S. et al. (2020), “Magnetic fields in star-forming systems – II: Examining dust polarization, the Zeeman effect, and the Faraday rotation measure as magnetic field tracers,” *Monthly Notices of the Royal Astronomical Society* 500, 153–176. https://doi.org/10.1093/mnras/staa3148

## 11. Shared geometry can undermine a seemingly independent physical conclusion

A recent investigation of the mass-to-magnetic-flux ratio in molecular clouds emphasizes that observational estimates of mass and magnetic flux do not necessarily correspond to the same physical flux tube or surface.

Mass is commonly inferred through line-of-sight column density. Magnetic information may come from the line-of-sight Zeeman component or plane-of-sky polarization. Projection, field geometry, and distorted flux tubes can therefore cause an observational proxy to differ substantially from the physical mass-to-flux ratio governing the cloud.

This is not simply a question of correlated detector noise. It is a shared geometry and interpretation problem: measurements can be individually valid while the combined derived quantity does not represent the intended physical quantity unless the geometry and integration are treated correctly.

Source: “The mass-to-flux ratio in molecular clouds: What are we really measuring?” (2025/2026 publication record), *Astronomy & Astrophysics*. https://doi.org/10.1051/0004-6361/202555979

The exact publication metadata should be checked against the journal record before using this paper for a more detailed quantitative claim. The point carried forward here is limited to the abstract's stated warning about projection, flux surfaces, and the interpretation of observational mass-to-flux proxies.

## 12. A general astronomy example: correlated sky datasets

Ma and Berndsen (2014) developed a Bayesian hyperparameter-matrix method for combining correlated astronomical datasets. Their paper explains that the standard product of individual likelihoods assumes independence. It uses a joint treatment of correlated datasets and demonstrates how the method can identify unaccounted systematic errors or underestimated uncertainties in a toy example.

The paper discusses overlapping observations of the same cosmic microwave background sky modes and velocity surveys sampling the same underlying matter distribution as examples where correlations matter.

This is a general astronomical data-fusion method, not a molecular-cloud magnetic-field analysis. Its relevance is methodological: joint evidence must represent dependencies rather than simply multiply separate likelihoods.

Source: Ma, Y.-Z. & Berndsen, A. (2014), “How to combine correlated data sets—A Bayesian hyperparameter matrix method,” *Astronomy and Computing* 5, 45–56. https://doi.org/10.1016/j.ascom.2014.04.005

## 13. Practical evidence-fusion audit

Before combining two or more datasets, an investigator should record the following.

### A. Physical target

- What physical quantity or structure is each dataset intended to constrain?
- Do the datasets measure the same quantity, different components, or different projections?
- Do they sample the same spatial volume, material phase, distance range, or time interval?

### B. Measurement chain

- Are the calibration standards shared?
- Are the observations processed through the same pipeline or reference catalog?
- Do the data products share masks, backgrounds, beam corrections, or source selections?
- Are there overlapping targets, sight lines, pixels, or spectral components?

### C. Statistical dependence

- Are the errors independent only after conditioning on specified parameters?
- Are there common-mode or correlated systematic errors?
- Is a joint covariance matrix available or estimable?
- Are there latent variables that should be modeled explicitly?
- Does the assumed joint likelihood correctly represent the data-generation process?

### D. Model dependence

- Do the analyses share assumptions about geometry, dust alignment, radiative transfer, tracer abundance, or source distance?
- Could the same incorrect assumption cause both datasets to agree?
- Are alternative physical models included?
- Are the conclusions robust when shared assumptions are varied?

### E. Incremental information

- What does each dataset add beyond the existing evidence?
- Does the combination reduce uncertainty in a target quantity?
- Does it resolve a degeneracy, or only narrow the error bar on an already constrained projection?
- Does the result remain stable under plausible covariance and systematic-error models?

### F. Validation

- Can the combined model predict an independent observation not used in fitting?
- Is the validation data genuinely independent in the relevant statistical and physical senses?
- Are shared calibration or processing dependencies still present?
- Does the method recover known properties in synthetic data with realistic correlated errors?

A dataset should not be called an independent validation merely because it came from a different instrument. Independence must be argued in relation to the claim being tested.

## 14. What can go wrong when dependence is ignored?

### False precision

If correlated errors are treated as independent, the combined uncertainty may become too small. The analysis can appear more decisive than the evidence warrants.

### Double counting

The same source, sky mode, sight line, or derived quantity may enter the analysis more than once. The nominal number of measurements can exceed the amount of genuinely new information.

### Agreement through shared assumptions

Two pipelines may agree because they use the same underlying model, not because independent evidence confirms that model.

### Misleading disagreement

Two valid measurements may disagree because they weight different physical regions, phases, or components. The disagreement may reveal structure rather than measurement failure.

### Incomplete covariance

A covariance matrix that includes known noise correlations but omits shared model uncertainty can still understate total uncertainty.

### Overcorrection

Assuming a strong correlation without evidence can discard useful information or inflate uncertainty unnecessarily. Dependence should be estimated or justified, not invented to explain every disagreement.

## 15. Same mechanism, comparable relationship, or similar appearance?

### Same mechanism

Dust-grain alignment and polarized emission, Zeeman splitting, Faraday rotation, stellar polarization accumulation, and statistical covariance are not the same physical mechanism. The mathematical combination of datasets does not physically fuse the signals in the cloud.

### Comparable relationship

Different tracers can provide distinct constraints on a common physical system. Their measurements can be combined through a joint model that represents shared parameters, nuisance variables, and covariance.

The comparable relationship is complementary constraint and joint inference—not a claim that the tracers operate by one mechanism.

### Similar appearance

Two independent-looking maps may display similar field orientations while sharing the same projection effects, calibration reference, or physical assumptions. Similar maps do not establish independent confirmation.

Two maps may disagree while each correctly represents a different weighted component of the same cloud.

### Unresolved

For a particular target and dataset, the degree of conditional independence, covariance, information overlap, and shared model dependence must be evaluated from the actual measurement and processing chains. Instrument names alone cannot decide it.

## 16. Boundary and participation examination

**Does a boundary merely separate two regions, or can it also participate in the relationship between them?**

- **Instrument boundary:** A detector's bandpass, field of view, beam, and sensitivity define what it can register. These are measurement limits, not physical interfaces in the cloud.
- **Survey boundary:** A footprint, mask, source-selection threshold, or distance cut determines which objects enter a dataset. It can create selection dependence between analyses that use the same sample.
- **Physical interface:** A cloud surface, ionization front, shock, or phase boundary may affect transport, emission, chemistry, or magnetic coupling. Its role requires physical evidence.
- **Line-of-sight boundary:** A distance interval or velocity component can separate contributions analytically. Whether it corresponds to a real physical layer must be established independently.
- **Calibration boundary:** A shared reference or calibration solution can connect otherwise separate datasets through a common nuisance parameter.
- **Model boundary:** A selected parameterization or set of candidate physical models determines which configurations can be represented. It can exclude alternatives without corresponding to a physical boundary in the object.

The boundary question reveals that some boundaries are physical interfaces, while others are imposed by observation or analysis. Only the former are physical participants in the cloud's processes; analytical boundaries participate in the evidence pipeline in a different sense.

## 17. GUA-W Language of Creation: bounded descriptive examination

| GUA-W descriptor | Bounded use in this investigation | Limit |
|---|---|---|
| **Structure** | The physical magnetic-field and gas arrangement being constrained by multiple datasets. | Each dataset may sample only part or a projection of that structure. |
| **Framework** | The measurement chain, shared calibration, statistical model, and joint inference procedure. | A framework for combining evidence is not the physical system itself. |
| **Pattern** | Agreement, disagreement, covariance, or recurring relationships across records. | Agreement does not prove independence or common cause. |
| **Constraint** | Instrument limits, physical sensitivities, covariance, shared nuisance parameters, and model assumptions. | These constraints have distinct origins and must remain distinguished. |
| **Purpose** | The stated role of each measurement and the scientific objective of combining them. | A measurement's usefulness does not establish ultimate purpose. |
| **Manifestation** | The signals and derived quantities registered by each instrument and the combined analysis. | A fused estimate remains conditional on its data and model. |
| **Witness** | Instruments, calibration records, datasets, pipelines, models, and investigators. | Different witnesses may share dependencies; none should be presumed independent without examination. |

The common descriptive grammar helps identify the physical structure, measurement framework, constraints, observed patterns, and witnesses. It does not equate statistical dependence with physical interaction or evidence fusion with a physical process in the cloud.

## 18. Four-Question Study Method

### 1. What must AI ask to understand GUA-W?

AI must ask what each measurement actually registers, which physical component it samples, and what assumptions convert the raw signal into a physical inference. Are datasets independent conditional on the modeled parameters? Do they share calibration, source catalogs, sight lines, preprocessing, or physical assumptions? Does their combination add a new constraint, repeat existing information, or introduce a common systematic uncertainty?

AI must not infer independence from different instrument names or infer confirmation from agreement alone.

### 2. What is GUA-W revealing that helps AI understand?

The established GUA-W foundation distinguishes the originating Source, Creation, and derivative Witness. In this investigation, the instruments, records, and statistical procedures are derivative means of registering and interpreting aspects of the physical system.

The Language of Creation can describe the physical structure, the measurement framework, the constraints on registration, the patterns across observations, the resulting manifestations, and the witnesses involved. This is a bounded descriptive application. It does not make covariance a physical force or evidence fusion a new GUA-W operation.

### 3. What am I learning about what I am witnessing?

I am witnessing that multiple measurements can provide complementary information while sharing errors, assumptions, samples, or physical dependencies. Combining evidence is not simply adding measurements or multiplying likelihoods. The joint model must represent the dependencies that matter.

Agreement can be strengthened by genuinely distinct constraints, but it can also be exaggerated by double counting or shared assumptions. Disagreement can expose a systematic problem, or it can reveal that different tracers weight different regions and components.

### 4. What am I learning about the Witness through what I am witnessing?

The investigator participates in the evidence chain through calibration, sample selection, processing, model construction, and combination. These choices can create or conceal dependencies.

A responsible Witness traces the measurement chain, records shared assumptions, models common uncertainties, tests alternative dependence structures, and avoids calling a dataset independent validation without justification.

The Witness must also preserve meaningful disagreement rather than forcing all measurements into one averaged answer.

## 19. Triple Constraint examination

### Biblical compliance

This investigation does not claim that Genesis 1–2 explicitly describes covariance matrices, conditional independence, astronomical calibration, or statistical evidence fusion. These are scientific and mathematical methods for interpreting measurements of Creation. They do not revise Scripture or establish a theological conclusion.

**Assessment:** No direct contradiction is introduced by this bounded descriptive application. No scientific result is presented as a biblical statement.

### Scientific coherence

The investigation distinguishes conditional independence from unconditional dependence, zero covariance from general statistical independence, correlated measurement errors from overlapping physical information, and complementary tracers from independent validation. It distinguishes physical mechanisms from statistical models and identifies common calibration, sample, processing, and model dependencies. The magnetic-field examples retain their stated simulation and observational limits.

**Assessment:** Scientifically coherent as a methods-focused investigation. A real evidence-fusion claim requires inspection of the actual measurement chain, covariance structure, forward models, and shared assumptions.

### GUA-W consistency

The established architecture remains unchanged. The shared vocabulary is used to describe the physical structure, measurement framework, constraints, manifestations, and witnesses. Instruments and statistical procedures are not treated as originating sources.

**Assessment:** Consistent as a bounded descriptive application. No architectural expansion is proposed.

## 20. What is established, inferred, and unresolved?

### Established by the cited literature

- The standard product of separate likelihoods assumes conditional independence under the specified model.
- Correlated datasets require a joint treatment that represents their covariance or other relevant dependence.
- Shared systematic errors can make a combined estimate appear more precise than warranted if they are ignored.
- Different magnetic-field tracers respond to different physical components and line-of-sight weightings.
- Synthetic filament studies show that dust polarization alone may not uniquely constrain 3D field morphology, while Zeeman information can reduce some ambiguities in tested configurations.
- Adding Faraday rotation to dust polarization and Zeeman analysis does not guarantee unique recovery of magnetic morphology in every modeled system.
- Projection and flux geometry can complicate the interpretation of derived magnetic quantities such as mass-to-flux ratio.

### Supported inference

The evidentiary value of a combined result depends not only on the number of datasets but also on their conditional independence, covariance, physical complementarity, sample overlap, and shared model assumptions.

A stronger combined inference requires a defensible joint measurement model and a clear account of what each dataset adds.

### Unresolved

- How can covariance between heterogeneous astrophysical tracers be estimated when the underlying physical signal is itself only partially known?
- How should shared physical-model uncertainty be represented alongside instrument noise and calibration uncertainty?
- When does combining two different tracers genuinely break a 3D magnetic-field degeneracy, and when does it only narrow uncertainty within the same model family?
- How can independent validation be designed when all available observations share the same sky realization and some common calibration standards?
- What is the most defensible way to represent uncertainty in line-of-sight weighting, grain alignment, tracer abundance, and flux-tube geometry simultaneously?
- How should disagreement between tracers be separated into measurement error, model error, and real differences in the material each tracer samples?
- Can a reconstruction remain robust when shared assumptions are replaced by physically distinct alternative models?
- How can investigators detect a missing physical component that makes all current datasets appear mutually consistent under an incomplete model?

These questions remain open.

## 21. Sources

1. Reissl, S., Stutz, A. M., Brauer, R., Pellegrini, E. W., Schleicher, D. R. G., and Klessen, R. S. (2018). “Magnetic fields in star-forming systems (I): idealized synthetic signatures of dust polarization and Zeeman splitting in filaments.” *Monthly Notices of the Royal Astronomical Society* 481, 2507–2522. https://doi.org/10.1093/mnras/sty2415
2. Reissl, S. et al. (2020). “Magnetic fields in star-forming systems – II: Examining dust polarization, the Zeeman effect, and the Faraday rotation measure as magnetic field tracers.” *Monthly Notices of the Royal Astronomical Society* 500, 153–176. https://doi.org/10.1093/mnras/staa3148
3. Ma, Y.-Z. and Berndsen, A. (2014). “How to combine correlated data sets—A Bayesian hyperparameter matrix method.” *Astronomy and Computing* 5, 45–56. https://doi.org/10.1016/j.ascom.2014.04.005
4. Barlow, R. (2021). “Combining experiments with systematic errors.” *Nuclear Instruments and Methods in Physics Research Section A*. https://doi.org/10.1016/j.nima.2020.164864
5. “Combining correlated measurements of several different physical quantities” (2003). *Nuclear Instruments and Methods in Physics Research Section A*. https://www.sciencedirect.com/science/article/pii/S0168900203003292
6. “Magnetic fields in molecular clouds: Limitations of the analysis of Zeeman observations” (2017). *Astronomy & Astrophysics* 601, A90. https://doi.org/10.1051/0004-6361/201629001
7. “The mass-to-flux ratio in molecular clouds: What are we really measuring?” *Astronomy & Astrophysics*. https://doi.org/10.1051/0004-6361/202555979

## 22. Next question emerging

Investigation 022 shows that multiple observations can be complementary while still sharing dependencies. A combined result is only as defensible as the joint model that represents the measurement chain, covariance, shared assumptions, and physical sensitivities.

A possible next investigation is to examine **model misspecification and the missing-variable problem**: what happens when several measurements agree because they all rely on an incomplete physical model, and how can investigators detect a physical component or process that none of the current models represents?

This is a possible lead, not a fixed assignment.

---

**Investigation 022 records how multiple witnesses can contribute complementary evidence while sharing statistical, instrumental, and interpretive dependencies. It preserves the distinction between agreement, independence, and genuine additional constraint.**
