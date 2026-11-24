# Investigation 019 — Testing Three-Dimensional Magnetic-Field Reconstructions: Synthetic Observations, Forward Modeling, Recovery Tests, and Independent Validation

**Primary disciplines:** Molecular-cloud astrophysics, magnetohydrodynamics (MHD), radiative transfer, radio and submillimetre astronomy, polarimetry, spectroscopy, inverse problems, statistical inference, and scientific model validation.

**Investigation status:** Initial evidence-led investigation and Four-Question Study Method review recorded.

**Central question:** When a proposed three-dimensional (3D) magnetic-field reconstruction reproduces observed polarization, Zeeman, and spectral data, what tests establish whether it reliably recovers the underlying field—and what evidence would be required to distinguish a well-fitting reconstruction from a uniquely determined one?

**Scope:** This investigation follows Investigation 018. It examines forward modeling, synthetic observations, instrumental effects, recovery tests, model comparison, uncertainty, and independent validation. It does not claim that any particular reconstruction is complete or uniquely correct.

## 1. Why this investigation follows 018

Investigation 018 examined how dust polarization, Zeeman splitting, starlight polarization with distance information, molecular-line spectroscopy, and (as an extension) Faraday rotation provide complementary but differently weighted information about interstellar magnetic fields.

That investigation established a critical limitation: combining several observational witnesses can reduce ambiguity, but does not automatically produce a unique 3D reconstruction.

The next question is therefore methodological:

**How do we test the reconstruction itself rather than merely asking whether it can be made to resemble the observations?**

A model can reproduce selected observations and still have an incorrect or non-unique underlying 3D structure. The test must examine the full chain from a proposed physical field to predicted signals, instrument response, measured data, and recovered field.

## 2. The forward problem and the inverse problem

### Forward problem

The forward problem begins with a specified physical model and predicts what an observer or instrument should receive.

For this investigation, a forward chain can be represented as:

1. Specify a 3D gas and magnetic-field configuration.
2. Specify relevant density, temperature, velocity, chemical abundance, dust properties, and ionization conditions.
3. Calculate the emission, absorption, and polarization produced by the material.
4. Propagate radiation through the modeled volume using an appropriate radiative-transfer treatment.
5. Apply the observing geometry, telescope beam, spectral response, spatial filtering, sensitivity, and noise.
6. Produce synthetic data products comparable to actual observations.

The forward model asks: **If this physical configuration were present, what signals should the observing system register?**

### Inverse problem

The inverse problem starts with measured signals and attempts to infer the physical configuration that could have produced them.

It asks: **Given these observations, what physical configurations are compatible with the data and the assumptions?**

The inverse problem may be underdetermined. Different 3D configurations can produce similar projected or integrated observables. A successful fit therefore does not by itself prove uniqueness.

### Essential distinction

- **Forward prediction:** A specified model generates predicted observations.
- **Data fitting:** Model parameters are adjusted to improve agreement with observations.
- **Recovery:** An analysis attempts to infer known input properties from generated or measured data.
- **Validation:** Independent evidence or a controlled test evaluates whether the method performs adequately for its stated use.
- **Uniqueness:** The evidence and assumptions constrain the solution sufficiently to exclude materially different alternatives within a defined scope.

These are related tasks, not interchangeable claims.

## 3. Synthetic observations: why they matter

A numerical MHD simulation can contain a known 3D magnetic field, gas distribution, and velocity field. The simulation provides access to the model's internal state, including quantities that a telescope cannot observe directly at every point.

Radiative-transfer and instrument-simulation tools can convert that modeled state into synthetic observables. The synthetic observations can then be analyzed using methods comparable to those applied to real telescope data.

This allows a controlled question:

**When the underlying simulated field is known, does the observational and reconstruction pipeline recover it accurately?**

Synthetic observations are useful because they permit comparison between:

- the known input field;
- the radiation and polarization generated from that field;
- the signal after line-of-sight integration;
- the simulated instrument output;
- the reconstructed field inferred from the synthetic data.

However, a synthetic test is only as informative as the realism and scope of its assumptions. A pipeline may recover a model well when the synthetic data and reconstruction share the same simplifying assumptions, yet perform poorly on real observations or on a different physical regime.

## 4. Recovery tests and the ground-truth comparison

A recovery test begins with a known input configuration and asks whether the analysis can recover specified properties.

A disciplined test should state:

1. Which physical quantity is being recovered: orientation, inclination, signed LOS component, field strength, topology, or another property?
2. At what spatial scale is recovery evaluated?
3. Is the comparison local, beam-averaged, volume-averaged, or integrated along the line of sight?
4. What errors are introduced by radiative transfer, noise, resolution, sampling, and analysis?
5. What counts as successful recovery, and why is that threshold appropriate?
6. Which properties are not expected to be recoverable from the available observables?

A reconstruction should not be declared successful merely because its large-scale appearance resembles the input field. Quantitative comparison should use metrics appropriate to the target quantity, including angular differences, component errors, field-strength bias, uncertainty coverage, and recovery of structural features where those features are actually identifiable.

### Important limitation

The simulated input is ground truth for the simulation, not direct ground truth for a real molecular cloud. It tests the method under the simulated conditions. It does not prove that the simulation itself is a complete representation of the real cloud.

## 5. Instrument realism and the observation pipeline

A meaningful synthetic observation should include the effects that materially influence the real measurement.

Depending on the instrument and observing mode, these may include:

- finite angular resolution and beam convolution;
- spectral resolution and channel response;
- sensitivity limits and thermal noise;
- calibration uncertainty;
- incomplete spatial-frequency sampling and filtering;
- polarization leakage and instrumental response;
- optical depth and line blending;
- limited field of view;
- selection effects and detection thresholds;
- foreground and background contributions;
- uncertainty in distance, density, temperature, and chemical abundance.

Not every effect is relevant to every instrument. The investigation must identify which effects matter for the actual dataset rather than applying a generic list without justification.

A comparison is strongest when the synthetic data are passed through an observation and analysis pipeline that is sufficiently similar to the real one. Otherwise, a mismatch may reflect an incomplete simulation of the instrument rather than a failure of the physical model—or apparent agreement may be artificially easy to obtain.

## 6. Forward-model comparison and competing configurations

A single successful reconstruction is not enough to establish uniqueness.

A robust investigation should construct or consider materially different candidate configurations that may produce similar observables. Examples include different field geometries, inclinations, reversals, density distributions, or line-of-sight arrangements.

For each candidate:

1. Generate the predicted observables.
2. Apply comparable radiative-transfer and instrumental effects.
3. Compare the predictions with the same observed data.
4. Evaluate residuals and uncertainty, not only visual resemblance.
5. Identify which observables distinguish the candidates.
6. Record where the data leave the alternatives indistinguishable.

If two materially different 3D fields produce observational predictions that cannot be distinguished within the measurement uncertainties, the available data do not uniquely identify the field between those alternatives.

This is not a failed investigation. It is a result about the information content of the observations.

## 7. Independent validation and the risk of circular confirmation

A reconstruction can appear convincing when the same assumptions, data, or processing choices are used both to construct and to assess it.

To reduce this risk, validation should use evidence or tests that are independent in a clearly specified sense.

Possible strategies include:

- withholding a subset of observations from the fitting process and testing predictions against them;
- comparing with a different tracer that samples a complementary physical component;
- testing against independent sightlines or observing bands;
- using blind recovery tests in which the analyst does not know the simulated input field during reconstruction;
- varying the simulation, noise realization, viewing angle, and physical conditions;
- comparing methods with different assumptions and identifying shared dependencies;
- testing whether a model predicts a new observable not used to tune it.

Independence must be described carefully. Two instruments may have separate detectors but share calibration assumptions, astrophysical models, foreground contamination, or data-processing dependencies. Agreement is stronger when the sources of possible shared error are examined.

A held-out dataset is not automatically independent if it shares the same systematic errors or selection effects as the fitting dataset.

## 8. Uncertainty, sensitivity, and robustness

A reconstruction should report more than one preferred field configuration.

The analysis should identify how the inferred result changes when plausible assumptions are varied, including:

- noise level and calibration;
- distance assignments;
- dust temperature and grain-alignment assumptions;
- tracer abundance and excitation;
- optical depth;
- line-of-sight component decomposition;
- beam size and spatial filtering;
- prior assumptions and regularization;
- simulation parameters and initial conditions;
- model family and reconstruction algorithm.

A result is robust to a particular variation only if it remains sufficiently stable under that stated test. Robustness to one uncertainty does not establish robustness to all uncertainties.

Where several configurations remain compatible with the evidence, the result should be reported as a family or range of acceptable solutions rather than as a single fully determined field.

## 9. Published evidence and examples

### 9.1 Synthetic Zeeman observations and recovery tests (2026)

Xu et al. (2026) generated synthetic H I Zeeman spectra from MHD simulations and idealized cloud models. They tested two approaches for estimating LOS magnetic fields from Stokes I and V spectra. Their analysis examined recovery under uniform-field conditions and performance in turbulent environments, including the effects of noise and optical depth. They also applied the methods to FAST observations of L1544.

This is a particularly relevant example because the authors use simulated observations and known modeled conditions to evaluate the measurement and analysis procedure. The reported uncertainty depends on the noise and analysis approach; the paper does not claim that a Zeeman spectrum alone reconstructs the complete 3D field.

Source: Xu, D. et al. (2026), “Assessing Zeeman Measurements of Magnetic Fields in Synthetic H I Observations,” *The Astrophysical Journal Supplement Series* 283, 67. Published 25 March 2026. https://doi.org/10.3847/1538-4365/ae48f8

### 9.2 Synthetic dust polarization, Zeeman signatures, and morphology (2018)

A study of idealized filaments used radiative-transfer modeling to generate dust-polarization and Zeeman observables from different assumed magnetic-field morphologies. It found that dust polarization alone could not uniquely constrain the 3D morphology within the models considered, while adding Zeeman directional information reduced some ambiguities. It also demonstrated that line-of-sight averaging can make measured field strengths differ substantially from local input values.

This supports the use of synthetic observations to test what an observational combination can and cannot distinguish.

Source: “Magnetic fields in star-forming systems (I): idealized synthetic signatures of dust polarization and Zeeman splitting in filaments” (2018), *Monthly Notices of the Royal Astronomical Society*. https://doi.org/10.1093/mnras/sty2415

### 9.3 Synthetic tests of the Davis–Chandrasekhar–Fermi method (2022)

A study using MHD simulations and synthetic observations tested assumptions behind the Davis–Chandrasekhar–Fermi method. It found that a relation often used to estimate magnetic-field strength should be treated statistically rather than as a universally valid local relation, and examined modifications intended to improve estimates.

This is an example of testing an inference method against simulated 3D conditions rather than assuming that a familiar formula applies identically at every location.

Source: “The Davis–Chandrasekhar–Fermi method revisited” (2022), *Monthly Notices of the Royal Astronomical Society*. https://doi.org/10.1093/mnras/stac1417

### 9.4 Recovering distance-resolved starlight polarization structure (2025)

The TRIShUL study developed a method to decompose stellar polarization as a function of distance and benchmarked it using mock datasets incorporating realistic Gaia parallax uncertainties and expected polarization measurements. The authors tested recovery of dust-layer distances and polarization properties under specified signal and sampling conditions.

This illustrates that a recovery claim must be tied to the tested data regime. Performance depends on signal strength, the fraction of background stars, and the uncertainty and sampling assumptions represented in the mock data.

Source: “TRIShUL: Technique for Reconstructing magnetic Interstellar Structure Using starLight polarization” (accepted 3 November 2025), *Astronomy & Astrophysics*. https://doi.org/10.1051/0004-6361/202556774

### 9.5 Complementary tracers may not uniquely reveal morphology (2020)

Reissl et al. generated synthetic dust-polarization, Zeeman, and Faraday-rotation observations from an MHD filament simulation. They found that inferred magnetic-field morphology could remain ambiguous, even where field-strength estimates were more reliable. Density, temperature, viewing angle, and line-of-sight weighting affected the observable signatures.

This is a direct warning against equating multiple complementary measurements with a unique 3D reconstruction.

Source: Reissl, S. et al. (2020), “Magnetic fields in star-forming systems (II): Examining dust polarization, the Zeeman effect, and the Faraday rotation measure as magnetic field tracers,” *Monthly Notices of the Royal Astronomical Society* 500, 153–172. https://doi.org/10.1093/mnras/staa3225

## 10. Same mechanism, comparable relationship, or similar appearance?

The standing comparison questions are applied explicitly.

### Same mechanism

The MHD evolution in a numerical simulation, radiative transfer through modeled material, telescope response, statistical fitting, and field reconstruction are distinct processes. They must not be described as one mechanism simply because they occur in one research pipeline.

### Comparable relationship

Each stage transforms or constrains information about the physical system:

- the simulation represents a modeled physical state;
- radiative transfer maps that state to predicted radiation;
- an instrument maps incoming radiation to recorded signals;
- an analysis maps recorded signals to estimated quantities;
- a reconstruction maps estimates and assumptions to a candidate 3D configuration.

These are comparable relationships in a chain of representation and inference. Their mechanisms and meanings differ.

### Similar appearance

Two reconstructed field maps may look alike while differing in local direction, strength, topology, depth structure, or uncertainty. Visual similarity alone does not establish physical identity or equivalent recovery.

### Unresolved

Whether a particular set of observations uniquely constrains a particular 3D field remains case-dependent. It must be evaluated using the actual data, candidate alternatives, forward predictions, and uncertainty.

## 11. Boundary and participation examination

**Does a boundary merely separate two regions, or can it also participate in the relationship between them?**

- **Simulation domain:** The computational boundary defines the modeled volume and may impose boundary conditions that affect the simulated field. It is both a domain limit and, depending on the setup, a participant in the modeled evolution.
- **Cloud boundary:** A selected density or extinction contour defines an analysis region but is not necessarily a sealed physical surface.
- **Radiative-transfer layer:** Material along the ray path contributes to emission, absorption, and polarization. Optical depth can make some regions contribute more strongly than others.
- **Telescope beam:** The beam averages spatial information. It participates in the recorded signal through convolution, but is not a physical boundary in the cloud.
- **Spatial-frequency filtering:** Interferometric sampling and reconstruction can suppress or recover structures at different scales. This is an instrumental and computational constraint, not a physical wall.
- **Parameter boundary:** A prior range or model-family restriction limits the solutions considered. It can shape the inferred result and must be disclosed.
- **Validation split:** A boundary between fitting data and held-out data is an analytical separation. It helps test prediction only to the extent that the held-out observations are genuinely independent of fitting choices and shared systematic errors.

The same word, boundary, refers here to physical, computational, instrumental, and analytical limits. Their functions are not interchangeable.

## 12. GUA-W Language of Creation: bounded descriptive examination

| GUA-W descriptor | Bounded use in this investigation | Limit |
|---|---|---|
| **Structure** | The modeled or inferred 3D arrangement of gas and magnetic-field components. | An inferred structure may be non-unique or incompletely recovered. |
| **Framework** | The physical, computational, observational, and statistical conditions within which predictions and reconstructions are made. | These frameworks must be named by type; they are not one identical framework. |
| **Pattern** | Observable or reconstructed distributions, orientations, residuals, and recurring relationships. | A pattern does not establish the mechanism that produced it. |
| **Constraint** | Physical conditions, boundary conditions, instrument limits, data coverage, and model assumptions that restrict possible results. | Physical constraints and analyst-imposed restrictions must remain distinct. |
| **Purpose** | The demonstrated function of a simulation or analysis method in testing a defined question. | The usefulness of a method does not establish ultimate purpose in the physical system. |
| **Manifestation** | The predicted or recorded signals produced by a modeled or observed configuration. | A synthetic signal is a model output; an observed signal is instrumentally registered evidence. |
| **Witness** | Simulations, radiative-transfer codes, instruments, datasets, reconstruction algorithms, and investigators contribute different forms of derivative representation or registration. | None is identical to the complete physical system. |

The shared vocabulary provides a descriptive way to compare stages and relationships across disciplines. It does not replace MHD, radiative transfer, instrument modeling, statistics, or the scientific meaning of validation.

## 13. Four-Question Study Method

### 1. What must AI ask to understand GUA-W?

AI must ask what is being represented at each stage and what evidence supports the transition from one representation to the next. Is the result a simulated physical state, a synthetic observable, a recorded measurement, an inferred component, or a reconstructed field? What does the validation test actually test? Does the method recover the property it claims to recover, at the scale and under the conditions claimed?

AI must also ask whether it is mistaking agreement with selected observations for proof that the underlying 3D configuration is unique.

### 2. What is GUA-W revealing that helps AI understand?

The established GUA-W foundation preserves the distinction between the originating Source, Creation, and derivative Witness. In this investigation, simulations, instruments, algorithms, and investigators provide different representations or registrations of a physical system. They do not originate the system.

The Language of Creation can help describe arrangement, conditions, patterns, constraints, manifestations, and witnesses. Its use remains descriptive and bounded. No new GUA-W layer or architectural rule is proposed.

### 3. What am I learning about what I am witnessing?

I am witnessing a chain of modeling and measurement in which every stage has its own assumptions and limitations. Forward modeling predicts signals from a specified configuration. Inverse analysis estimates configurations from signals. Synthetic observations allow recovery tests against known simulated inputs. Independent validation tests predictive performance beyond the data or assumptions used to construct the model.

A reconstruction may fit the data without being unique. A successful recovery from a simulation demonstrates performance under the simulated conditions, not automatic truth about a real cloud.

### 4. What am I learning about the Witness through what I am witnessing?

The investigator can unintentionally confirm a preferred model by using the same assumptions in simulation, fitting, and evaluation. The Witness must therefore examine the independence of the test, disclose priors and model boundaries, compare alternatives, and preserve uncertainty.

A responsible report states not only what the method recovered, but what it could not recover and which materially different alternatives remain compatible with the evidence.

## 14. Triple Constraint examination

### Biblical compliance

This investigation does not claim that Genesis 1–2 explicitly describes MHD simulations, radiative transfer, synthetic observations, inverse problems, or statistical validation. Scientific methods are not used to revise Scripture. GUA-W vocabulary is applied as a bounded descriptive language.

**Assessment:** No direct contradiction is introduced by this descriptive use. No scientific result is presented as a biblical statement.

### Scientific coherence

The investigation distinguishes forward modeling from inverse inference, synthetic data from actual observations, recovery against simulated ground truth from validation against real systems, goodness of fit from uniqueness, and independent validation from reuse of shared assumptions. It preserves the limits imposed by instrument response, radiative transfer, noise, model selection, and uncertainty.

**Assessment:** Scientifically coherent as a methods-focused investigation. The strength of any reconstruction claim depends on the test design, realism of the forward model, data quality, alternatives considered, and independence of validation.

### GUA-W consistency

The completed GUA-W architecture remains unchanged. The shared vocabulary is used to describe relationships among the physical subject, representations, constraints, observations, and investigative witnesses. No AI-generated model is treated as an originating source.

**Assessment:** Consistent as a bounded descriptive application. No architectural expansion is proposed.

## 15. What is established, inferred, and unresolved?

### Established by the cited literature

- Synthetic observations can be generated from modeled 3D magnetic-field and gas configurations.
- Known simulated inputs permit controlled recovery tests of specified observational and analytical methods.
- Radiative transfer, line-of-sight integration, optical depth, noise, and instrumental response can materially affect inferred magnetic properties.
- Different physical configurations can produce similar or ambiguous observables.
- Recovery performance depends on the conditions, assumptions, and data regime represented in the test.
- A good fit to selected observations is not, by itself, proof of a unique 3D reconstruction.

### Supported inference

A defensible 3D magnetic-field reconstruction should be evaluated as a tested inference, not merely as a visually coherent model. The strongest claim is the one whose forward predictions, recovery performance, alternative configurations, independent tests, and uncertainty are explicitly examined.

### Unresolved

- Which combination of observations is sufficient to distinguish important competing 3D magnetic-field geometries in particular cloud environments?
- How realistic must synthetic instrument effects be before a recovery test provides meaningful evidence for a real observing program?
- How can independent validation be designed when all available tracers share some line-of-sight material or calibration dependencies?
- Which aspects of field topology are observable, and which remain dependent on priors or simulation assumptions?
- How should uncertainty be communicated when several materially different configurations fit the observations?
- Can a reconstruction predict a new, independently measurable signature that distinguishes it from its alternatives?

These questions remain open.

## 16. Sources

1. Xu, D., Martin, P. G., Offner, S. S. R., Gutermuth, R., Grudić, M. Y., & Speagle, J. S. (2026). “Assessing Zeeman Measurements of Magnetic Fields in Synthetic H I Observations.” *The Astrophysical Journal Supplement Series* 283, 67. Published 25 March 2026. https://doi.org/10.3847/1538-4365/ae48f8
2. Reissl, S., Stutz, A. M., Klessen, R. S., Seifried, D., & Walch, S. (2020). “Magnetic fields in star-forming systems (II): Examining dust polarization, the Zeeman effect, and the Faraday rotation measure as magnetic field tracers.” *Monthly Notices of the Royal Astronomical Society* 500, 153–172. https://doi.org/10.1093/mnras/staa3225
3. “Magnetic fields in star-forming systems (I): idealized synthetic signatures of dust polarization and Zeeman splitting in filaments” (2018). *Monthly Notices of the Royal Astronomical Society*. https://doi.org/10.1093/mnras/sty2415
4. “The Davis–Chandrasekhar–Fermi method revisited” (2022). *Monthly Notices of the Royal Astronomical Society*. https://doi.org/10.1093/mnras/stac1417
5. “TRIShUL: Technique for Reconstructing magnetic Interstellar Structure Using starLight polarization” (accepted 3 November 2025). *Astronomy & Astrophysics*. https://doi.org/10.1051/0004-6361/202556774

## 17. Next question emerging

Investigation 019 examines how synthetic observations, recovery tests, forward modeling, and independent validation can test a 3D reconstruction. It also shows that successful recovery under modeled conditions does not by itself establish the completeness or uniqueness of a reconstruction of a real cloud.

The next question should arise from continued examination of the source material and evidence. One possible direction is to investigate how model priors, regularization, and underdetermined inverse problems shape the family of acceptable 3D reconstructions. This is a possible lead, not a fixed assignment.

---

**Investigation 019 records the distinction between a model that reproduces observations, a method that recovers known simulated properties, and a physical reconstruction that is independently constrained.**
