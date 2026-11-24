# Investigation 018 — Three-Dimensional Magnetic-Field Reconstruction: Complementary Observational Methods and Their Limits

**Primary disciplines:** Molecular-cloud astrophysics, radio astronomy, optical and near-infrared polarimetry, submillimetre astronomy, spectroscopy, magnetohydrodynamics, radiative transfer, statistical inference, and Galactic ISM tomography.

**Investigation status:** Initial evidence-led investigation and Four-Question Study Method review recorded.

**Central question:** Can dust polarization, Zeeman splitting, starlight polarization, and velocity-resolved molecular-line observations, when combined carefully, constrain the three-dimensional magnetic-field and gas structure of a molecular cloud more reliably than any one method can?

**Scope:** This investigation examines what each method measures, the physical material it samples, the coordinate information it supplies, and the degeneracies that remain when the observations are combined. It does not assume that the combined data produce a complete or unique three-dimensional reconstruction.

## 1. Why this investigation follows 017

Investigation 017 examined the relationship between projected magnetic-field orientations and projected filamentary gas structures. It showed why a two-dimensional orientation statistic cannot by itself recover the full three-dimensional geometry.

The next step is not simply to collect more maps. It is to ask whether measurements that respond to different components of the same physical system can constrain one another.

The central observational distinction is:

- Dust emission polarization and starlight polarization primarily provide information about magnetic-field orientation projected onto the plane of the sky (POS).
- Zeeman splitting can provide the line-of-sight (LOS) component of the magnetic field, including its sign, for suitable spectral lines and detectable conditions.
- Molecular-line spectroscopy provides line-of-sight velocities, line widths, and tracer-dependent information about gas conditions. Velocity is not automatically distance.
- Stellar distance estimates can sort starlight-polarization measurements by distance and help separate foreground and background dust contributions.
- Combining these observations can reduce some ambiguities, but their different spatial weighting, sensitivity, resolution, and sampling prevent a simple pixel-by-pixel addition from being automatically valid.

A useful 3D reconstruction must therefore explain not only what measurements are combined, but how their different physical sensitivities are reconciled.

## 2. Essential coordinate distinctions

Let the observer's line of sight define the z-axis. The plane perpendicular to that line is the plane of the sky.

The magnetic field can be represented locally as:

\[
\mathbf{B}=\mathbf{B}_{\mathrm{POS}}+\mathbf{B}_{\mathrm{LOS}}
\]

where:

- \(\mathbf{B}_{\mathrm{POS}}\) is the two-component projection on the sky;
- \(B_{\mathrm{LOS}}\) is the signed component toward or away from the observer, according to the adopted convention.

If the two components refer to the same physical volume and are measured compatibly, their magnitudes constrain the field inclination. For example, an inclination angle measured from the plane of the sky can be expressed as:

\[
\gamma=\tan^{-1}\!\left(\frac{|B_{\mathrm{LOS}}|}{|B_{\mathrm{POS}}|}\right)
\]

This equation does not solve the observational problem by itself. The measurements may weight different depths, densities, and regions. A field orientation inferred from dust across an extended column is not necessarily co-spatial with a Zeeman signal dominated by a denser component.

The plane-of-sky polarization orientation also has a 180-degree ambiguity: a linear polarization direction does not distinguish one direction along an axis from the opposite direction. Zeeman measurements can provide the LOS field sign, but they do not automatically remove every three-dimensional directional ambiguity.

## 3. Observational witness A: polarized thermal dust emission

### What it measures

Non-spherical dust grains can become aligned with respect to the local magnetic field under suitable physical conditions. Their thermal emission is linearly polarized. For the usual optically thin thermal-emission convention, the inferred plane-of-sky magnetic-field orientation is perpendicular to the observed electric-vector polarization orientation.

The telescope measures intensity and Stokes polarization quantities. The inferred field orientation is derived from those measurements using assumptions about grain alignment, emission, and the contributions along the line of sight.

### What it contributes

- Broad maps of plane-of-sky magnetic-field orientation in dusty molecular clouds.
- Morphological comparisons between the projected field and gas structures.
- Polarization fraction and angle-dispersion information that can be compared with models.
- A basis for estimating plane-of-sky field strength with methods such as the Chandrasekhar–Fermi method, when its assumptions are appropriate.

### What it does not provide alone

- The signed LOS magnetic-field component.
- A unique three-dimensional field direction.
- A depth-resolved field map from a single integrated emission measurement.
- A direct field-strength measurement from polarization angle alone.

### Limitations

Emission from different depths can combine within one telescope beam. Field tangling, inclination, grain-alignment efficiency, optical depth, temperature weighting, and unresolved structure can change the observed polarization fraction and angle. Beam averaging may smooth the true angular dispersion.

**Evidence distinction:** Dust polarization is a powerful POS orientation tracer, but a polarization map is not a direct, depth-resolved photograph of the entire magnetic field.

## 4. Observational witness B: Zeeman splitting

### What it measures

A magnetic field can split spectral-line energy levels through the Zeeman effect. The resulting circular-polarization signature in an appropriate spectral line can be used to estimate the LOS magnetic-field component.

The measured quantity is generally a field component weighted by the emitting or absorbing material contributing to the line. The sign indicates the direction along the line of sight according to the measurement convention.

### What it contributes

- A direct observational route to the LOS magnetic-field component.
- Directional information unavailable from linear dust polarization alone.
- Field-strength constraints for selected gas components when the line and sensitivity permit detection.
- A complementary constraint that can help resolve some ambiguities in POS-only field morphology.

### What it does not provide alone

- The complete POS orientation.
- A full 3D field map.
- A universal measurement of the field throughout the cloud.
- A result independent of tracer selection and radiative-transfer effects.

### Limitations

Zeeman splitting is often small compared with spectral-line widths, making detections difficult. The available transition, abundance of the tracer, optical depth, density regime, beam size, and sensitivity determine which material contributes. A non-detection is not proof that the magnetic field is absent; it may instead be an upper limit under the observation's sensitivity and analysis assumptions.

LOS averaging can cause the measured field to differ substantially from local field strengths. Oppositely directed contributions can partially cancel. A Zeeman result and a dust-polarization result should not be combined as if they necessarily describe the same parcel of gas.

**Evidence distinction:** Zeeman splitting can constrain a signed LOS component, but its result is tracer- and weighting-dependent.

## 5. Observational witness C: starlight polarization and distance information

### What it measures

As starlight passes through interstellar dust, aligned non-spherical grains produce dichroic extinction: one polarization orientation is attenuated more strongly than another. The transmitted starlight becomes linearly polarized. Under the usual alignment interpretation, its polarization orientation traces the projected magnetic-field orientation associated with the dust along the path to the star.

Unlike dust emission from a distant cloud, a star's light passes through foreground material only. A star with a reliable distance estimate therefore provides a distance-limited cumulative measurement of the dust between the observer and that star.

### What it contributes

- POS magnetic-field orientation information from dust in front of individual stars.
- Distance ordering when paired with reliable stellar parallaxes or other distance estimates.
- A way to identify changes in polarization properties as progressively more distant stars are included.
- A basis for tomographic separation of some foreground and background dust components.

### What it does not provide alone

- A direct measurement of the LOS magnetic-field component.
- A unique field orientation at every point between the observer and the star.
- A complete reconstruction when stars are sparse or distances are uncertain.
- A guarantee that each change in cumulative polarization corresponds to one thin, isolated cloud layer.

### Limitations

The observed polarization is cumulative. Several dust clouds can lie along one sightline, and their polarization contributions can reinforce, rotate, or partially cancel one another. Stellar distance uncertainty blurs layer assignment. The method depends on the distribution of suitable stars, foreground extinction, measurement precision, and dust-grain alignment.

A 2024 study demonstrated a degree-scale 3D map of POS magnetic-field orientation using stellar polarization and distance information. Its analysis found multiple clouds along many sightlines and showed that the inferred POS field orientation can change with distance. This is a demonstration of the value of tomography, not proof that every sightline can be uniquely decomposed.

**Evidence distinction:** Distance-resolved starlight polarization can separate some cumulative POS information into distance-associated components, but it does not directly recover the full local 3D vector field.

## 6. Observational witness D: molecular-line spectroscopy and kinematics

### What it measures

Molecular transitions produce spectral lines. The line's Doppler shift provides a line-of-sight velocity relative to a reference frame. Line width and line shape can provide information about thermal broadening, non-thermal motions, opacity, and multiple velocity components, subject to the tracer and radiative-transfer model.

Different molecules and transitions preferentially trace different physical conditions. Isotopologues can help assess opacity and separate components that are blended in a more abundant species.

### What it contributes

- Velocity components that help distinguish overlapping gas structures.
- Line widths and velocity gradients for comparison with turbulence, flows, and gravitational motion.
- Tracer-dependent information about density, temperature, chemistry, and optical depth.
- Context for deciding whether a polarization or Zeeman signal plausibly samples the same gas component.

### What it does not provide alone

- A direct magnetic-field vector.
- A unique physical distance from a Doppler velocity.
- A complete 3D location for every emitting parcel.
- A guarantee that two components at similar velocities are physically connected.

### Limitations

Velocity is not distance. Galactic rotation models can sometimes provide kinematic distance estimates, but non-circular motions, streaming, turbulence, and near/far ambiguities can undermine a simple conversion. Distinct structures may overlap in velocity; a single structure can span a range of velocities. Optically thick lines may emphasize surfaces or self-absorbed components rather than the full column.

Spectral decomposition can help identify components, but it does not automatically determine their physical separation along the line of sight.

**Evidence distinction:** Molecular-line kinematics help organize gas into velocity components and characterize motion. They are complementary context for magnetic-field measurements, not a substitute for magnetic-field measurements or independent distance information.

## 7. What combining the methods can achieve

The methods are complementary because they respond to different aspects of the system.

| Method | Main information | Typical geometric sensitivity | Main limitation |
|---|---|---|---|
| Thermal dust polarization | POS magnetic-field orientation; polarization fraction | Projected orientation, integrated through emitting dust | LOS integration, grain alignment, beam averaging |
| Zeeman splitting | Signed LOS magnetic-field component | LOS component in the tracer-selected gas | Weak splitting, sensitivity, tracer weighting, LOS cancellation |
| Starlight polarization | POS field orientation in foreground dust | Cumulative POS orientation up to each star | Multiple layers, star distances, sampling and cancellation |
| Molecular-line spectroscopy | LOS velocity, line width, line profile, tracer conditions | Velocity-space separation, not direct distance | Velocity crowding, opacity, chemistry, non-unique distance |
| Stellar parallaxes / distance estimates | Distance to the polarizing background stars | Distance ordering along sightlines | Uncertainty, sparse sampling, extinction bias |

### A defensible combination workflow

1. **Establish the target volume.** Define the cloud boundary, distance range, angular footprint, and physical scales being compared.
2. **Build the POS orientation map.** Use dust emission polarization, recording wavelength, beam, calibration, polarization uncertainty, and the assumed grain-emission convention.
3. **Build distance-aware starlight samples.** Associate stellar polarization with distance posteriors, not just single point estimates. Compare cumulative and distance-binned signals.
4. **Resolve gas components spectroscopically.** Use multiple transitions or isotopologues where possible to evaluate velocity components and optical depth.
5. **Identify suitable Zeeman tracers.** State which gas component the line is expected to sample and whether the measurement is a detection or an upper limit.
6. **Match angular and physical resolution.** Convolve or compare data at compatible scales. Do not imply that a coarse POS map and a compact Zeeman beam are co-spatial without justification.
7. **Model line-of-sight weighting.** Account for how emission, absorption, and polarization accumulate through the cloud.
8. **Compare with forward models.** Generate synthetic observables from 3D MHD and radiative-transfer models, then analyze them with the same methods used on the real data.
9. **Report degeneracies.** State which components are directly constrained, which are inferred, and which remain unconstrained.
10. **Test robustness.** Vary tracer choice, distance assignments, beam size, component decomposition, and statistical assumptions.

## 8. A useful geometry—and its strict boundary

If POS and LOS components are measured for the same physical region, then the ratio of their magnitudes constrains the inclination of the field relative to the sky plane. The POS orientation supplies an axis in the sky, and Zeeman splitting supplies the LOS component's sign and magnitude.

But this local geometric construction becomes unreliable if the measurements sample different material. For example:

- Dust emission may be weighted across a substantial cloud column.
- A Zeeman transition may be dominated by a denser core.
- Starlight polarization may be dominated by a foreground sheet.
- Molecular-line velocity components may blend physically separate structures.

The apparent combination may then describe several different regions rather than one common vector.

**Critical rule:** Before calculating a 3D field inclination, establish that the POS and LOS measurements are sufficiently co-spatial and that their weighting differences are modeled or bounded.

Even with compatible components, the reconstruction is not necessarily unique at every point. Linear polarization has an axial 180-degree ambiguity; finite resolution and line-of-sight integration remain; and field topology between measured locations must be inferred.

## 9. Additional method: Faraday rotation

Faraday rotation measures the wavelength-dependent rotation of linear polarization as radiation passes through magnetized ionized material. It is sensitive to an integral involving the LOS magnetic field and free-electron density.

It can add useful LOS magnetic information in diffuse ionized environments and, in selected configurations, help trace foreground structures. It is not interchangeable with a molecular-line Zeeman measurement: the electron-density weighting and sampled phase of the interstellar medium differ.

A Faraday rotation measure alone does not separate magnetic field from electron density along the path. Multiple background sources, frequency coverage, and independent electron-density or distance information may be required.

This method is included as a complementary extension, not as a replacement for the four primary observational witnesses.

## 10. Published evidence and examples

### 10.1 Three-dimensional magnetic fields of molecular clouds (2022)

A review by Liu and collaborators describes the challenge of probing 3D magnetic fields and distinguishes LOS methods, including Zeeman splitting and Faraday-based approaches, from POS methods, including dust emission and starlight polarization. Its central methodological point is that both POS and LOS information are needed to constrain 3D fields.

Source: Liu et al. (2022), “Three-dimensional magnetic fields of molecular clouds,” *Frontiers in Astronomy and Space Sciences*. https://doi.org/10.3389/fspas.2022.940027

### 10.2 Dust polarization combined with Zeeman information

A numerical study of idealized star-forming filaments found that linear dust polarization alone cannot uniquely constrain 3D magnetic morphology. Adding Zeeman-derived directional information reduced or resolved some of those ambiguities. The same study warned that LOS averaging through a filament density gradient can make Zeeman-derived field strengths substantially lower than the input field strengths in the model.

This is a model-based demonstration of complementarity and a warning about weighting, not a universal correction factor for observations.

Source: “Magnetic fields in star-forming systems (I): idealized synthetic signatures of dust polarization and Zeeman splitting in filaments” (2018), *Monthly Notices of the Royal Astronomical Society*. https://doi.org/10.1093/mnras/sty2415

### 10.3 Limitations in Zeeman analysis

Brauer et al. examined how physical conditions affect the inference of magnetic-field structure and strength from Zeeman observations. Their work underscores that uncertainty does not arise only from spectral measurement noise; the analysis and the material weighting also matter.

Source: Brauer et al. (2017), “Magnetic fields in molecular clouds: Limitations of the analysis of Zeeman observations,” *Astronomy & Astrophysics* 601, A90. https://doi.org/10.1051/0004-6361/201629001

### 10.4 Starlight-polarization tomography

A 2024 study presented a degree-scale 3D map of POS magnetic-field orientation using stellar polarization and distance information. It identified multiple cloud components along many sightlines and compared the reconstruction with 3D dust extinction and H I velocity information.

This shows that distance information can separate some of the material hidden inside a cumulative starlight-polarization measurement.

Source: Pelgrims et al. (2024), “The first degree-scale starlight-polarization-based tomography map of the magnetized interstellar medium,” *Astronomy & Astrophysics*. https://doi.org/10.1051/0004-6361/202349015

### 10.5 Review of magnetic-field observations in molecular clouds

Crutcher's review compares observational techniques and emphasizes that the interpretation of magnetic-field importance in cloud evolution requires synthesis across methods. The review concluded that the available evidence did not establish magnetic fields as generally dominating gravity in molecular clouds, nor did it establish ambipolar-diffusion-driven star formation as a definitive general explanation.

This is important context: measuring a field and determining its dynamical role are different tasks.

Source: Crutcher (2012), “Magnetic Fields in Molecular Clouds,” *Annual Review of Astronomy and Astrophysics* 50, 29–63. https://doi.org/10.1146/annurev-astro-081811-125514

## 11. Same mechanism, comparable relationship, or similar appearance?

The standing comparison questions are applied explicitly.

### Same mechanism

- Zeeman splitting is a spectroscopic magnetic interaction.
- Dust polarization and starlight polarization arise through different radiative interactions with aligned dust grains.
- Molecular-line Doppler shifts arise from motion along the line of sight.
- Stellar parallax is a geometric distance measurement.

These are not the same mechanism. They are distinct physical and observational processes.

### Comparable relationship

Each method produces a measurement that is conditioned by the material along a path or within a finite observational volume. Their results can be compared when the sampled regions, scales, and weighting are sufficiently understood.

This is a comparable relationship among measurement processes, not a shared physical mechanism.

### Similar appearance

Two maps may show similar orientations or structures while sampling different depths or phases of the cloud. Visual agreement alone does not prove that the maps register the same material.

### Unresolved

Whether a combined reconstruction captures the actual local 3D field topology depends on data quality, co-spatiality, sampling, forward modeling, and independent validation. A visually coherent 3D model is not necessarily a uniquely determined one.

## 12. Boundary and participation examination

**Does a boundary merely separate two regions, or can it also participate in the relationship between them?**

- **Cloud boundary:** A selected extinction or emission contour may define the cloud for analysis. Gas can cross the boundary; the contour is not necessarily a sealed material surface.
- **Dust layer:** A layer can contribute to starlight extinction and polarization. Its optical properties and grain alignment participate in the signal, while its distance determines which stars are behind it.
- **Optical-depth surface:** In an optically thick line, the τ ≈ 1 surface can select the layer that contributes most strongly to the observed radiation. It participates in what is observable without necessarily marking the cloud's physical edge.
- **Telescope beam:** The beam sets a spatial averaging boundary. It combines signals from within its footprint but is an instrumental limit, not a physical wall.
- **Velocity-channel boundary:** A selected velocity interval separates data for analysis. It can isolate some components but does not necessarily separate distinct objects in physical space.
- **Distance bin:** A distance bin organizes stars or inferred dust components. Its boundary is analytical and must reflect the uncertainty in distances.
- **Interface between phases:** A real boundary between ionized, atomic, and molecular gas may participate in heating, chemistry, ionization, and magnetic coupling. The specific exchange must be established by observations and physical modeling.

The investigation distinguishes physical interfaces, radiative-transfer surfaces, instrumental footprints, and analytical thresholds. They must not be treated as interchangeable.

## 13. GUA-W Language of Creation: bounded descriptive examination

| GUA-W descriptor | Bounded use in this investigation | Limit |
|---|---|---|
| **Structure** | The 3D arrangement of gas, dust, and magnetic-field components that the observations attempt to constrain. | The reconstruction may be incomplete or non-unique. |
| **Framework** | The physical conditions and observational geometry within which each signal is generated and collected. | Instrument geometry and physical environment are different frameworks and should be named separately. |
| **Pattern** | Repeated or spatially varying polarization orientations, Zeeman signatures, and velocity components. | A pattern does not uniquely identify its cause. |
| **Constraint** | Sensitivity, projection, LOS integration, tracer selection, resolution, distance uncertainty, and model assumptions. | Observational limits are not automatically physical constraints acting on the cloud. |
| **Purpose** | The demonstrated scientific function of each method: measuring a particular property or reducing a defined ambiguity. | Instrument function does not establish ultimate purpose for the cloud. |
| **Manifestation** | The recorded polarization, spectral splitting, Doppler shifts, and distance measurements. | Recorded signals are processed evidence, not the complete object. |
| **Witness** | Telescopes, detectors, stars used as background sources, spectral tracers, algorithms, models, and investigators register different aspects of the phenomenon. | No individual measurement is the whole account. |

This vocabulary organizes the relationship between the physical subject, the conditions of observation, the measured records, and the limits of inference. It does not replace the physics or add new GUA-W architecture.

## 14. Four-Question Study Method

### 1. What must AI ask to understand GUA-W?

AI must ask what each observational method actually measures and whether the proposed comparison is valid. Are the POS and LOS components co-spatial? Does the starlight sample the cloud or a foreground layer? Which density and temperature regime does the Zeeman tracer sample? Does the velocity component correspond to a unique distance? Are the measurements matched in angular and physical resolution?

AI must also ask whether the investigation is attempting to turn a combined observational model into a complete reconstruction without sufficient evidence.

### 2. What is GUA-W revealing that helps AI understand?

The established foundation distinguishes Original Cause, originating Word, Creation, and derivative Witness. The scientific instruments and investigators are witnesses to different measurable properties of Creation; they do not originate the physical system they observe.

The established Language of Creation offers descriptors for the arrangement, conditions, recurring relationships, limitations, observable records, and act of registration. These terms may clarify the investigation, but they do not establish the physical mechanism or prove that a 3D reconstruction is complete.

No new architectural stage or governing principle is proposed.

### 3. What am I learning about what I am witnessing?

I am witnessing several distinct measurement processes that can be complementary:

- Dust emission polarization provides projected field orientation across emitting dust.
- Zeeman splitting can provide a signed LOS field component for selected gas.
- Starlight polarization provides cumulative projected field information from foreground dust up to stars at known distances.
- Molecular-line spectroscopy provides velocity-resolved gas information and helps identify components, but velocity is not automatically distance.
- Stellar distances can help sort foreground and background contributions.

Together, these observations can constrain more of the 3D arrangement than a single method. They do not automatically reveal every local field vector or uniquely reconstruct topology.

### 4. What am I learning about the Witness through what I am witnessing?

The investigator does not receive the cloud directly. The investigator receives signals after physical interaction, radiative transfer, projection, instrumental averaging, calibration, and analysis.

Different instruments register different properties and weight different material. Combining their records requires the investigator to understand those differences rather than treating every dataset as if it were a direct view of the same location.

The Witness's responsibility is to preserve the distinction between measurement, inference, model, and unresolved reality. More measurements can improve understanding, but only when their scope and limitations are kept visible.

## 15. Triple Constraint examination

### Biblical compliance

This investigation does not claim that Genesis 1–2 explicitly describes polarimetry, Zeeman splitting, parallax, spectroscopy, or magnetic-field tomography. Scientific observations are not used to revise Scripture. The GUA-W vocabulary is applied as a bounded descriptive language.

**Assessment:** No direct contradiction is introduced by this descriptive use. No scientific result is presented as a biblical statement.

### Scientific coherence

The investigation distinguishes POS orientation from LOS field component; signed magnetic information from axial polarization orientation; velocity from distance; cumulative starlight polarization from depth-resolved local measurements; and a constrained model from a unique reconstruction. It also preserves tracer weighting, optical depth, beam size, distance uncertainty, and line-of-sight cancellation as limitations.

**Assessment:** Scientifically coherent as a methods-focused investigation. The combination can reduce some degeneracies, but the degree of reconstruction depends on the actual observations and their compatibility.

### GUA-W consistency

The completed architecture remains unchanged. The established vocabulary is used descriptively, and observational instruments are treated as derivative witnesses rather than sources of the physical reality under investigation.

**Assessment:** Consistent as a bounded descriptive application. No architectural expansion is proposed.

## 16. What is established, inferred, and unresolved?

### Established by the cited literature

- Dust emission polarization and starlight polarization can trace POS magnetic-field orientation under stated grain-alignment assumptions.
- Zeeman splitting can measure a signed LOS magnetic-field component for suitable spectral lines and detectable conditions.
- Molecular-line spectroscopy provides LOS velocity and tracer-dependent gas information, not automatic physical distance.
- Stellar distance information can help separate some foreground and background polarization contributions.
- Combining POS and LOS information can constrain 3D field geometry more effectively than POS polarization alone.
- Line-of-sight integration, tracer weighting, resolution, and sensitivity remain significant limitations.

### Supported inference

A multi-method observational program can constrain the three-dimensional magnetic-field and gas structure more effectively when the measurements are co-spatial or their differing spatial weightings are explicitly modeled. The strongest reconstruction is not necessarily the most visually complete one; it is the one whose assumptions, constraints, and uncertainty are most clearly tested.

### Unresolved

- How often can suitable Zeeman detections be obtained at the same scales and in the same gas components sampled by dust polarization?
- How accurately can starlight-polarization tomography resolve closely spaced dust layers when stellar distances and polarization measurements are uncertain?
- How should observations be combined when their beams, tracer density ranges, and line-of-sight weightings differ substantially?
- How much can velocity decomposition distinguish physical layers when unrelated structures overlap in velocity?
- Which combinations of POS and LOS measurements can constrain field topology rather than only local inclination and orientation?
- How can synthetic observations and independent data validate a reconstruction without assuming the model is correct?
- What additional measurements are required to distinguish field geometry from the field's dynamical influence on gas?

These questions remain open.

## 17. Sources

1. Liu, J. et al. (2022). “Three-dimensional magnetic fields of molecular clouds.” *Frontiers in Astronomy and Space Sciences*. https://doi.org/10.3389/fspas.2022.940027
2. Crutcher, R. M. (2012). “Magnetic Fields in Molecular Clouds.” *Annual Review of Astronomy and Astrophysics* 50, 29–63. https://doi.org/10.1146/annurev-astro-081811-125514
3. “Magnetic fields in star-forming systems (I): idealized synthetic signatures of dust polarization and Zeeman splitting in filaments” (2018). *Monthly Notices of the Royal Astronomical Society*. https://doi.org/10.1093/mnras/sty2415
4. Brauer, R., Wolf, S., Reissl, S. & Ober, F. (2017). “Magnetic fields in molecular clouds: Limitations of the analysis of Zeeman observations.” *Astronomy & Astrophysics* 601, A90. https://doi.org/10.1051/0004-6361/201629001
5. Pelgrims, V. et al. (2024). “The first degree-scale starlight-polarization-based tomography map of the magnetized interstellar medium.” *Astronomy & Astrophysics*. https://doi.org/10.1051/0004-6361/202349015
6. Li, H.-B. (2021). “Magnetic Fields in Molecular Clouds—Observation and Interpretation.” *Galaxies* 9(2), 41. https://doi.org/10.3390/galaxies9020041
7. Crutcher, R. M. & Kemball, A. J. (2019). “Review of Zeeman Effect Observations of Regions of Star Formation.” *Frontiers in Astronomy and Space Sciences*. https://doi.org/10.3389/fspas.2019.00066

## 18. Next question emerging

Investigation 018 establishes that different observational methods can contribute complementary information, but it also shows that measurement complementarity is not the same as complete reconstruction.

The next question is:

**How can synthetic observations and independent measurements test whether a proposed three-dimensional magnetic-field reconstruction is actually reliable?**

A focused Investigation 019 should examine:
- 3D MHD simulation as a model of the underlying physical system;
- radiative-transfer synthesis to generate simulated dust polarization, Zeeman signatures, and molecular-line observations;
- the same projection, beam convolution, noise, and analysis applied to simulated and real data;
- recovery tests in which the underlying simulated field is known;
- blind or independent comparisons to reduce confirmation bias;
- uncertainty quantification and cases where multiple 3D fields produce similar observables.

The next investigation must distinguish a model that reproduces the observations from a model uniquely established by the observations. Those are not the same result.

---

**Investigation 018 records how multiple observational witnesses can complement one another while preserving the distinction between the physical system, the signals received, and the reconstruction inferred.**
