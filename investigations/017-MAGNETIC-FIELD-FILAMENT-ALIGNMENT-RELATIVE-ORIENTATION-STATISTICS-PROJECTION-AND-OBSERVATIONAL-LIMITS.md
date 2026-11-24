# Investigation 017 — Magnetic-Field and Filament Alignment: Relative-Orientation Statistics, Projection, and Observational Limits

**Primary disciplines:** Molecular-cloud astrophysics, magnetohydrodynamics (MHD), dust polarimetry, radio and submillimetre astronomy, statistical methods, radiative transfer.

**Investigation status:** Initial evidence-led investigation and Four-Question Study Method review recorded. This is a focused follow-up to Investigations 007, 008, and 013. It does not repeat the general study of cloud formation or filament formation. It examines how relative orientation is measured, what the measurements can support, and where projection and tracer selection limit interpretation.

## 1. Why this investigation is necessary

The earlier investigations already examined:

- **007:** the combined roles of pressure, gravity, magnetic fields, turbulence, and external forces in interstellar-cloud structure;
- **008:** filament geometry, possible formation pathways, accretion, fragmentation, dense cores, and observational identification;
- **013:** magnetic-field geometry, polarization, turbulence, and the movement of interstellar matter;
- **016:** ionization, charged-neutral coupling, ambipolar diffusion, and magnetic-flux transport.

Investigation 008 identified the relative orientation between filaments and magnetic fields as one relevant observation. It also warned that polarization is projected and does not by itself establish the three-dimensional field or the cause of a filament.

A narrower question now emerges:

**When a molecular-cloud filament appears parallel or perpendicular to the magnetic field in an astronomical map, what has actually been measured, how is that relationship quantified, and how reliably does the projected pattern reveal the three-dimensional physical relationship?**

A second question follows:

**When the preferred relative orientation changes with column density or tracer, does that demonstrate a change in the dominant physical process—or can projection, optical depth, resolution, and line-of-sight mixing produce or modify the apparent transition?**

This is not a new claim that magnetic fields create every filament. It is an investigation of the evidence used to infer how magnetic fields and gas structures are related.

## 2. Scientific terminology

- **Dust polarization:** Linear polarization of thermal emission from non-spherical dust grains that are aligned with respect to the local magnetic field under suitable conditions. The observed polarization orientation is generally perpendicular to the plane-of-sky magnetic-field orientation for thermal dust emission.
- **Plane-of-sky magnetic field (B⊥):** The component of the magnetic-field direction projected onto the observer's sky plane. Dust polarization can provide an estimate of its orientation, not a complete three-dimensional vector.
- **Line-of-sight (LOS):** The direction between the source and observer. Observed emission and polarization may combine contributions from multiple depths along this direction.
- **Column density (N):** The number of particles integrated along a line of sight per unit area. It is not the same as local volume density.
- **Column-density gradient (∇N):** The direction and magnitude of the spatial change in column density on the map. The gradient is perpendicular to a local constant-column-density contour.
- **Relative orientation:** The angle between two projected directions, such as the inferred magnetic field and the tangent to a column-density contour or filament crest.
- **Histogram of Relative Orientations (HRO):** A statistical method that collects relative-orientation angles across a map or selected region and examines their distribution, often as a function of column density.
- **Projected Rayleigh Statistic (PRS):** A statistical measure used to assess whether a distribution of relative angles has a preferred orientation. Its exact convention and sign must be stated for the implementation used.
- **Rolling Hough Transform (RHT):** An image-analysis method for identifying and quantifying linear structures and their orientations in maps. It can provide a structural orientation field for comparison with polarization.
- **Stokes parameters (I, Q, U, V):** Quantities describing the intensity and polarization state of electromagnetic radiation. For linear dust polarization, Q and U are used to infer polarization fraction and angle; Stokes V describes circular polarization.
- **Polarization fraction:** The polarized intensity divided by total intensity, under the adopted measurement convention. It may vary because of field geometry, grain alignment, optical depth, and unresolved structure.
- **Beam convolution / beam averaging:** The effect of finite angular resolution, in which a telescope measurement averages emission over a finite area on the sky.
- **Optical depth (τ):** A measure of attenuation or opacity along a path. For a spectral line, an optically thick tracer may preferentially reveal a surface layer rather than the full depth of a cloud.
- **Tracer:** A measured spectral line, continuum signal, or other observable used to infer a gas component or physical condition. Different tracers can sample different densities, temperatures, and depths.
- **Alfvén Mach number (M_A):** The ratio of characteristic flow speed to Alfvén speed. Sub-Alfvénic flows are slower than the Alfvén speed; super-Alfvénic flows are faster. The classification is scale- and condition-dependent.
- **Projection effect:** A difference between the actual three-dimensional geometry and the two-dimensional appearance after projection onto the sky.
- **Line-of-sight confusion:** Superposition of distinct structures or field orientations at different distances that contribute to one observed pixel or spectrum.
- **HRO transition:** A change in the statistical preference of relative orientations, often evaluated across bins of column density or volume density. A transition in the statistic is an observational result; its physical explanation requires further evidence.

## 3. What is actually measured?

The measurement chain must be kept explicit.

### 3.1 Dust emission and polarization

Aligned dust grains emit linearly polarized thermal radiation. The telescope records intensity and polarization information. From the measured Stokes parameters, an observer derives a polarization fraction and a polarization angle.

For optically thin thermal dust emission under the usual alignment assumptions, the inferred plane-of-sky magnetic-field orientation is rotated by 90 degrees from the observed electric-vector polarization angle.

This rotation is a data interpretation step based on the emission and grain-alignment model. It is not a direct photograph of a magnetic field line.

The measurement is also weighted by the emitting dust along the line of sight. Different depths can contain different field orientations, temperatures, grain populations, and densities. Their combined signal can reduce polarization or shift the inferred angle.

### 3.2 Column density and structural orientation

Column-density maps may be inferred from dust emission and temperature estimates, extinction, or molecular-line data with additional assumptions. A column-density map is a projected integral, not a three-dimensional density map.

A filament can be characterized by its crest or local tangent. Another common method uses the gradient of column density. Because the gradient is perpendicular to a constant-column-density contour, it can be used to derive the contour's tangent direction.

The structural direction must be defined consistently. Comparing the magnetic field to the gradient without accounting for the 90-degree relation can reverse the interpretation of parallel and perpendicular alignment.

### 3.3 The observational distinction

A dust-polarization map and a column-density map do not measure the same physical quantity:

- polarization supplies a projected orientation related to the magnetic field;
- column density supplies an integrated measure of material along the line of sight;
- a filament-finding method supplies a projected structural orientation;
- a relative-orientation statistic summarizes the relation between these projected quantities.

The statistic is not itself a magnetic-field measurement, a density measurement, or a direct measurement of a causal force.

## 4. Quantifying relative orientation

### 4.1 The angle

Let **B⊥** represent the inferred plane-of-sky magnetic-field direction and let **t** represent the tangent to a local column-density contour or filament crest. The relative angle can be defined as:

\[
\phi = \cos^{-1}\!\left(
\frac{|\mathbf{B}_{\perp}\cdot\mathbf{t}|}
{|\mathbf{B}_{\perp}|\,|\mathbf{t}|}
\right)
\]

with the angle folded into the interval 0° to 90°.

Under this convention:

- 0° means parallel projected orientation;
- 90° means perpendicular projected orientation;
- intermediate angles indicate oblique projected orientation.

Equivalent formulations use the column-density gradient rather than the contour tangent. If the gradient is used, the interpretation must account for its perpendicular relation to the contour.

### 4.2 The histogram of relative orientations

The HRO collects the relative angles across selected map pixels or regions. It can be evaluated in bins of column density, allowing researchers to ask whether the preferred orientation changes as the projected material column increases.

One commonly used shape statistic compares the central part of the histogram with its edge regions. In a common convention, a positive value indicates a preference for parallel alignment and a negative value indicates a preference for perpendicular alignment. Other papers use different symbols or sign conventions, so the definition must accompany any reported value.

The HRO is a population statistic. It does not mean every individual filament or pixel shares the preferred orientation.

### 4.3 The projected Rayleigh statistic

The PRS provides another statistical test for preferred relative orientation. It can summarize whether the distribution is biased toward parallel or perpendicular configurations, depending on the angle definition and statistic convention.

HRO and PRS are not interchangeable labels for one identical calculation. Their definitions, weighting, sample selection, and sign conventions must be stated.

### 4.4 Why statistics help—and why they do not settle causation

A map may contain thousands of pixels with noisy local angles. A statistical method can reveal a population-level preference that is not obvious from visual inspection.

But a statistical preference does not by itself establish:
- the true three-dimensional orientation;
- the local magnetic-field strength;
- whether the magnetic field caused the structure;
- whether gravity or turbulence is dynamically dominant;
- whether all regions in the sample share the same history.

The statistic quantifies a projected relationship. The physical explanation requires independent evidence and comparison with models.

## 5. The Planck result: a column-density-dependent change

Planck Collaboration Intermediate Results XXXV (2016) used the HRO method to compare magnetic-field orientations inferred from Planck dust polarization with column-density structures in ten nearby molecular clouds and two test fields.

The study reported that in most of the analyzed regions the preferred projected orientation changed with column density: lower-column-density structures were more often parallel to the inferred magnetic field, while higher-column-density structures were more often perpendicular. The reported transition occurred near:

\[
\log_{10}(N_{\mathrm H}/\mathrm{cm}^{-2}) \approx 21.7
\]

This is a result for the selected clouds, data, scales, and analysis. It is not a universal threshold for every molecular cloud.

The authors also noted that projection tends to produce more parallel-looking orientations in two-dimensional observations than are present in the underlying three-dimensional distribution. That makes the observed transition particularly important to interpret with care.

Source: Planck Collaboration (2016), “Planck intermediate results. XXXV. Probing the role of the magnetic field in the formation of structure in molecular clouds,” *Astronomy & Astrophysics* 586, A138. https://doi.org/10.1051/0004-6361/201525896

## 6. A critical test: the tracer can change the answer

Mazzei et al. (2023) compared synthetic dust polarization with synthetic molecular-line observations generated from a three-dimensional turbulent, collapsing-cloud MHD simulation.

Their study is particularly useful because it examines what an observer would infer after radiative transfer and projection, rather than comparing only the underlying simulation variables.

Key findings include:

- In their trans-Alfvénic, more strongly magnetized simulation, a transition to perpendicular alignment appeared above a density of roughly 4 × 10³ cm⁻³.
- The transition was recovered in most synthetic observations of optically thin molecular tracers.
- For optically thick ¹²CO, the transition did not appear; the projected statistic remained preferentially parallel in the modeled observer space.
- The authors found that the τ = 1 surface for ¹²CO was largely in front of the cloud mid-plane, so the line mainly sampled lower-volume-density material rather than the dense interior.
- In their super-Alfvénic simulation, the field was more tangled and the observed tracers tended toward no clear preference for either orientation.
- Viewing geometry also affected the result.

This is a strong demonstration that a tracer-dependent orientation pattern can arise because different observations sample different physical layers. A difference between tracers is not automatically evidence that the magnetic field changed its underlying behavior between those layers.

The result is model-dependent and does not establish that all clouds follow the same transition.

Source: Mazzei, R., Li, Z.-Y., Chen, C.-Y., Fissel, L. & Chen, M. (2023), “Relative alignment between magnetic fields and molecular gas structure in molecular clouds,” *Monthly Notices of the Royal Astronomical Society* 521, 3830–3846. https://doi.org/10.1093/mnras/stad733

## 7. An important exception: a further return to parallel alignment

The Serpens South study by Kusune et al. (2020) reported a further change in relative orientation in parts of that cloud. After the commonly reported transition from parallel to perpendicular alignment at higher column density, the authors found a return to parallel alignment at very high visual extinction, approximately A_V ≳ 21 magnitudes in the observed regions.

They interpreted the further transition in relation to gas flow and the onset of magnetically supercritical conditions, allowing gravitational collapse and cluster formation even with relatively strong magnetic fields.

This is a particular observational case and interpretation. It does not establish a universal three-stage orientation sequence for all clouds.

It is important because it prevents a simplistic rule such as “high density always means perpendicular alignment.” The relative orientation can depend on local dynamics, field geometry, and the region being sampled.

Source: Kusune, T. et al. (2020), “Magnetized filamentary gas flows feeding the young embedded cluster in Serpens South,” *Nature Astronomy* 4, 34–41. https://doi.org/10.1038/s41550-020-1172-6

## 8. Projection, line-of-sight integration, and the missing dimension

### 8.1 Three-dimensional geometry becomes two-dimensional evidence

The observer receives a two-dimensional map. The underlying cloud is three-dimensional.

A filament aligned with the magnetic field in three dimensions will remain parallel when projected. But a genuinely perpendicular three-dimensional relationship can appear less than perpendicular after projection, depending on the inclination of the structures and field to the line of sight.

Thus, projected parallel alignment and projected perpendicular alignment do not carry equal geometric certainty.

### 8.2 Multiple structures can occupy one pixel

A telescope beam may combine emission from:
- several filaments at different distances;
- foreground and background dust;
- multiple magnetic-field orientations;
- gas at different temperatures and densities.

The observed polarization angle is an integrated, weighted result. It may not represent the local field at the density peak or filament crest.

### 8.3 Polarization fraction and field inclination

A low polarization fraction may arise from tangled fields, unresolved changes in orientation, field inclination relative to the sky plane, grain-alignment efficiency, optical depth, or combinations of these effects.

It is therefore unsafe to interpret low polarization fraction as a direct measurement of weak magnetic-field strength.

### 8.4 Resolution and beam averaging

If a telescope beam is larger than the structures being studied, distinct orientations are averaged together. Smoothing a map changes the scales at which gradients and angles are calculated.

A valid comparison requires matching the effective angular resolution of the polarization and structural data. A change in beam size can change the HRO distribution even when the underlying cloud is unchanged.

### 8.5 Dust grain alignment

The ability of grains to produce polarized emission depends on grain properties and the local radiation environment. In dense regions, changes in grain alignment can affect the observed polarization signal. A missing or weak polarization measurement does not prove that a magnetic field is absent.

A 2021 study explicitly examined why magnetic-field alignment can be difficult to observe, emphasizing projection and the limitations of polarization as a direct three-dimensional field reconstruction.

Source: “Alignment of the magnetic field in star-forming regions and why it might be difficult to observe” (2021), *Monthly Notices of the Royal Astronomical Society*. https://doi.org/10.1093/mnras/stab2157

## 9. How to distinguish a physical transition from an observational one

A persuasive interpretation should test more than one observable.

| Possible explanation | Evidence that would help test it | Caution |
|---|---|---|
| Magnetic field guides low-density flows | Field orientation, velocity structure, and density morphology measured on matched scales | Alignment alone does not establish the direction or rate of flow. |
| Gravity becomes more influential at higher density | Dense-gas kinematics, mass distribution, gravitational estimates, and field geometry | Density alone does not prove gravitational dominance. |
| Turbulence tangles the field | Velocity dispersion, polarization-angle dispersion, scale dependence, and MHD model comparison | Apparent disorder can also result from projection and unresolved components. |
| A tracer samples only a cloud surface | Optical-depth estimates, multiple transitions, isotopologues, and radiative-transfer modeling | One line may not represent the entire cloud. |
| Line-of-sight mixing changes the apparent angle | Distance-resolved components, velocity decomposition, starlight polarization, and synthetic observations | Separation may remain incomplete where components overlap in velocity and distance. |
| Beam averaging erases a preferred direction | Reanalysis at matched and multiple resolutions | Smoothing can reveal or hide a pattern; it does not recover all unresolved structure. |
| Dust alignment changes with environment | Multiwavelength polarization and grain/radiative-transfer modeling | A change in polarization fraction is not a unique grain-alignment diagnostic. |

### A minimum comparison discipline

1. Define the structural orientation method before comparing it with the magnetic-field map.
2. State whether the field orientation is inferred from dust emission, extinction, or another method.
3. Match the angular resolution and sky coverage of the datasets.
4. State the column-density or volume-density bins and the sample selection.
5. Compare more than one molecular tracer where possible, including optical-depth differences.
6. Examine polarization fraction and uncertainty, not only polarization angle.
7. Compare projected observations with synthetic observations from three-dimensional simulations.
8. State what independent measurement would distinguish competing physical explanations.

## 10. GUA-W Language of Creation: bounded descriptive examination

The established vocabulary is applied to the evidence without treating the terms as additional physical mechanisms or assuming that every category must map one-to-one onto a scientific quantity.

| GUA-W descriptor | What the investigation can describe | Boundary of the description |
|---|---|---|
| **Structure** | The actual arrangement of dust, gas, magnetic-field orientation, filaments, and substructures represented in a stated map or model. | A two-dimensional map is not the complete three-dimensional structure. |
| **Framework** | The observational and physical conditions under which polarization, column density, and molecular-line tracers are produced and measured. | The instrument setup and physical environment are different kinds of framework and must be named. |
| **Pattern** | A statistically preferred relative orientation across selected pixels, regions, or density bins. | A statistical pattern does not uniquely identify its cause or apply universally. |
| **Constraint** | Projection, optical depth, beam size, line-of-sight integration, grain alignment, sensitivity, and sample selection limit what can be inferred. | A measurement limit is not necessarily a physical constraint acting on the cloud. |
| **Purpose** | The scientific function of HRO or PRS is to quantify orientation distributions and compare observations with models. | The usefulness of a statistic does not establish an ultimate purpose for the physical structure. |
| **Manifestation** | Polarization angles, column-density gradients, filament orientations, and their statistical relationship become measurable in the selected dataset. | The measured manifestation is a projected and instrument-dependent record. |
| **Witness** | Polarimeters, telescopes, detectors, image-processing algorithms, statistical analyses, simulations, and investigators register different aspects of the phenomenon. | No single witness supplies the entire physical account. |

**Descriptive finding:** The GUA-W vocabulary helps distinguish the physical arrangement, the conditions of observation, the recurring projected relationship, the limits on inference, and the instruments that register the result. It does not replace the HRO calculation or prove a causal relationship between magnetic fields and filaments.

## 11. Relationship audit

### Same mechanism

The 90-degree relationship between a column-density gradient and the tangent to a constant-column-density contour is a geometric relation by definition. It is not a separate astrophysical force or a causal process.

### Comparable relationship

A magnetic-field orientation and a filament orientation can exhibit a measurable angular relationship. The comparison is between two projected directions; it does not mean the field and filament are the same physical entity or that one necessarily caused the other.

### Analogy

A histogram can be described as a statistical witness to a population-level relationship. This is an analogy for the role of a measurement record; the histogram is not a conscious witness and does not create the underlying cloud arrangement.

### Unresolved causal relationship

A transition from parallel to perpendicular alignment may be consistent with changes in the relative influence of magnetic fields, gravity, or turbulence. It may also be affected by projection, tracer opacity, and line-of-sight integration. The transition alone does not establish which explanation dominates.

## 12. Boundary and participation examination

The two recurring questions are applied directly:

**Are we witnessing the same mechanism, a similar relationship, or merely a similar appearance?**

**Does a boundary merely separate two regions, or can it also participate in the relationship between them?**

- **Filament crest and envelope:** A density contour defines a structural interface for analysis. Gas can cross it through accretion or turbulent motion; it is not necessarily a closed material boundary.
- **Optical-depth surface:** The τ ≈ 1 surface can determine which depths contribute most strongly to an optically thick line. It participates in selecting the observable layer through radiative transfer; it is not necessarily the physical edge of the cloud.
- **Telescope beam:** The beam defines a measurement footprint and averages signals. It is a boundary of observational resolution, not a physical wall in the gas.
- **Line-of-sight layers:** Foreground, interior, and background material can contribute to the same observed pixel. Their superposition participates in the measured polarization and emission.
- **Density-bin boundary:** A threshold used to divide low- and high-column-density pixels is an analytical choice. A statistical change near that threshold does not prove a sharp physical discontinuity.
- **Cloud boundary:** The chosen contour may be based on extinction, emission, or a column-density threshold. Material can cross it, and the selected edge need not be a permanent physical surface.

A boundary may be a physical interface, an active radiative-transfer surface, a measurement limit, or an analytical threshold. These must not be conflated.

## 13. Four-Question Study Method

### 1. What must AI ask to understand GUA-W?

AI must ask what is actually measured before interpreting the alignment. Is the field orientation inferred from dust polarization? Is the structure direction derived from a filament crest or a column-density gradient? Is the map a two-dimensional projection? What are the beam size, optical depth, line-of-sight contributions, uncertainty, and sample limits?

AI must also ask whether the proposed relationship has already been examined in Investigations 007, 008, and 013. The present investigation is not a repeat of those studies; it narrows their unresolved measurement and inference problem.

### 2. What is GUA-W revealing that helps AI understand?

The completed GUA-W foundation identifies the Author as Original Cause, the Word as the originating Word, Creation as what is made, and Witness as derivative registration and testimony. The architecture is not being extended or redesigned by this scientific investigation.

The established Language of Creation distinguishes structure, framework, pattern, constraint, purpose, manifestation, and witness. In this case, those terms help organize what is mapped, what conditions shape the observation, what statistical pattern appears, what limits inference, and what registers the result.

The vocabulary is useful only where it clarifies the evidence. It does not make the observed alignment a new GUA-W stage or a scientific proof of a theological claim.

### 3. What am I learning about what I am witnessing?

I am witnessing a measurable relationship between projected magnetic-field orientations and projected gas structures. Statistical methods can reveal population-level changes in that relationship across column-density bins. The Planck analysis reported a parallel-to-perpendicular transition in most of its selected nearby clouds. Synthetic observations show that magnetic-field strength, viewing angle, and tracer optical depth can affect whether the transition appears. A particular cloud, Serpens South, shows a further reported return to parallel alignment in some very high-extinction regions.

The evidence therefore supports a real and useful diagnostic relationship, but not a universal orientation rule or a unique causal interpretation.

### 4. What am I learning about the Witness through what I am witnessing?

The observer does not receive the full three-dimensional cloud directly. The witness receives radiation after emission, absorption, projection, integration, instrumental averaging, and analysis. A statistical result can be mathematically correct for the data while remaining incomplete as a description of the physical system.

The investigator must therefore report the exact observable, the method, the scale, and the inference boundary. A failure to see an orientation preference does not prove that no physical relationship exists; a detected preference does not prove a unique mechanism.

## 14. Triple Constraint examination

### Biblical compliance

This investigation uses the project's Genesis 1–2 KJV-derived descriptive vocabulary as a way of organizing the scientific evidence. It does not claim that Genesis explicitly describes dust polarization, magnetic-field orientation statistics, optical depth, or HRO analysis. Scientific observations are not used to revise Scripture.

**Assessment:** No direct contradiction is introduced by this bounded descriptive use. The scientific result is not presented as a biblical statement.

### Scientific coherence

The investigation distinguishes the measured polarization angle from the inferred plane-of-sky magnetic-field orientation; column density from volume density; column-density gradient from filament tangent; projected orientation from three-dimensional geometry; and statistical association from causal explanation. It includes optical-depth and projection effects demonstrated in synthetic observations and records a cloud-specific exception to a simple universal transition.

**Assessment:** Scientifically coherent as a focused review of relative-orientation diagnostics. A particular alignment pattern remains insufficient to identify one unique dynamical cause.

### GUA-W consistency

The completed architecture remains unchanged. The seven descriptors are used as a bounded descriptive vocabulary and are not converted into physical forces, new architectural stages, or claims of scientific confirmation.

**Assessment:** Consistent as a descriptive application. No architectural expansion is proposed.

## 15. What is established, inferred, and unresolved?

### Established by the cited scientific literature

- Dust polarization can provide an estimate of the plane-of-sky magnetic-field orientation under stated grain-alignment and emission assumptions.
- Column-density maps and filament-finding methods provide projected information about gas structure.
- HRO and PRS methods quantify statistical relationships between projected field and structure orientations.
- Planck Collaboration XXXV (2016) reported a change from mostly parallel to mostly perpendicular projected alignment with increasing column density in most of its selected nearby molecular-cloud regions.
- Three-dimensional MHD simulations and synthetic observations show that viewing geometry, magnetic-field strength, and tracer opacity can affect the observed relative-orientation statistics.
- Optically thick and optically thin tracers can produce different apparent alignment results because they sample different cloud depths and densities.
- A particular study of Serpens South reported a further return to parallel alignment at very high visual extinction in parts of that cloud.

### Supported inference

Relative-orientation statistics are useful diagnostics of the relationship between magnetic-field orientation and gas structure. When interpreted together with density, velocity, field-strength, optical-depth, and geometric information, they can help constrain competing models of molecular-cloud dynamics.

### Unresolved

- How reliably can three-dimensional field–structure alignment be reconstructed from combined dust polarization, Zeeman measurements, and velocity-resolved molecular tracers?
- How much of the observed transition in a given cloud is caused by changing dynamics, and how much by line-of-sight mixing or tracer selection?
- How do HRO results change when filament orientation is measured by different algorithms or at different spatial scales?
- Under what conditions does a low polarization fraction indicate field tangling rather than inclination, grain-alignment changes, or unresolved structure?
- Can multiwavelength polarization separate changes in grain alignment from changes in magnetic-field geometry?
- How general is the further return to parallel alignment observed in Serpens South?
- What combination of independent observations is sufficient to distinguish magnetic regulation from gravity-dominated or turbulence-dominated structure formation?

These questions remain open. No universal transition threshold, alignment sequence, or single causal explanation is asserted.

## 16. Sources

1. Planck Collaboration (2016). “Planck intermediate results. XXXV. Probing the role of the magnetic field in the formation of structure in molecular clouds.” *Astronomy & Astrophysics* 586, A138. https://doi.org/10.1051/0004-6361/201525896
2. Soler, J. D. et al. (2013). “An Imprint of Molecular Cloud Magnetization in the Morphology of the Dust Polarized Emission.” *The Astrophysical Journal* 774, 128. https://doi.org/10.1088/0004-637X/774/2/128
3. Mazzei, R., Li, Z.-Y., Chen, C.-Y., Fissel, L. & Chen, M. (2023). “Relative alignment between magnetic fields and molecular gas structure in molecular clouds.” *Monthly Notices of the Royal Astronomical Society* 521, 3830–3846. https://doi.org/10.1093/mnras/stad733
4. Kusune, T. et al. (2020). “Magnetized filamentary gas flows feeding the young embedded cluster in Serpens South.” *Nature Astronomy* 4, 34–41. https://doi.org/10.1038/s41550-020-1172-6
5. “Alignment of the magnetic field in star-forming regions and why it might be difficult to observe” (2021). *Monthly Notices of the Royal Astronomical Society*. https://doi.org/10.1093/mnras/stab2157
6. “FilDReaMS — II. Application to the analysis of the relative orientations between filaments and the magnetic field in four Herschel fields” (2022). *Astronomy & Astrophysics*. https://doi.org/10.1051/0004-6361/202244550
7. Mazzei, R. et al. (2023). “Relative alignment between magnetic fields and molecular gas structure in molecular clouds.” *Monthly Notices of the Royal Astronomical Society* 521, 3830–3846. https://doi.org/10.1093/mnras/stad733
8. “Characterizing magnetic fields of nearby molecular clouds using submillimeter polarization observations” (2021). *Monthly Notices of the Royal Astronomical Society* 503, 5006. https://academic.oup.com/mnras/article/503/4/5006/6174008

## 17. Next question emerging

The investigation has now separated the physical cloud from the projected map and the statistical relationship inferred from that map.

The next question is:

**How can astronomers reconstruct the three-dimensional magnetic-field and gas structure of a molecular cloud by combining dust polarization, Zeeman splitting, starlight polarization, and velocity-resolved molecular-line observations?**

The next investigation should focus on the complementarity of these measurement methods, their distinct sensitivities, and whether their combination reduces the degeneracies identified here. It should not assume that any one method, or even their combination, yields a complete three-dimensional reconstruction.

---

**Investigation 017 records the distinction between the physical cloud, the projected observations, the statistical orientation pattern, and the causal interpretation. The scientific phenomenon remains the subject; the record remains the Witness's report.**
