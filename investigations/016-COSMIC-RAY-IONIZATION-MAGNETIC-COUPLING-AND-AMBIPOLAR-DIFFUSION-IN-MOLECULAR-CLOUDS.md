# Investigation 016 — Cosmic-Ray Ionization, Magnetic Coupling, and Ambipolar Diffusion in Molecular Clouds

**Primary disciplines:** Molecular-cloud physics, non-ideal magnetohydrodynamics (MHD), astrochemistry, cosmic-ray physics, star-formation physics, radio and submillimeter astronomy.

**Investigation status:** Initial evidence-led investigation and Four-Question Study Method review recorded. This investigation evaluates a proposed physical connection; it does not assume that cosmic-ray ionization alone determines magnetic coupling or gravitational collapse.

## 1. The question that initiated the investigation

Investigations 013–015 established three connected areas for examination:

- Magnetic fields participate in the structure and dynamics of interstellar gas.
- Cosmic rays propagate through magnetized environments by processes that vary with energy and local conditions.
- Cosmic-ray interactions can ionize and heat molecular material and initiate chemical pathways.

Investigation 016 asks:

**How does the ionization state of molecular-cloud gas affect the coupling between charged particles and neutral matter, and how does that coupling influence magnetic-flux transport, ambipolar diffusion, and dense-core contraction?**

A second question is equally important:

**Can observations distinguish a cloud in which magnetic flux is redistributed by ion-neutral drift from one whose evolution is governed more strongly by gravity, turbulence, flows along magnetic fields, or other non-ideal MHD processes?**

The investigation must not reduce this to “less ionization means collapse.” Ionization is one input to a coupled physical system. Density, field strength and geometry, charged-grain populations, collision rates, turbulence, gravity, and the cloud's history also matter.

## 2. Scientific terminology

- **Ionization fraction:** The abundance of charged particles relative to a stated reference population. In molecular gas, the electron fraction, total ion fraction, and abundance of a particular molecular ion are not interchangeable.
- **Weakly ionized gas:** Gas in which most mass is neutral, while a much smaller population of electrons, ions, and charged dust grains responds to electromagnetic forces.
- **Charged-neutral coupling:** Momentum exchange between charged species and neutral particles through collisions. The degree of coupling depends on densities, collision rates, species, and physical conditions.
- **Ion-neutral drag:** Collisional momentum transfer between ions and neutral particles. It allows magnetic forces acting on charged material to influence neutral gas indirectly.
- **Flux freezing:** In ideal MHD, magnetic flux is carried with the conducting fluid. It is an approximation whose validity depends on scale and physical regime.
- **Ambipolar diffusion (AD):** In weakly ionized gas, charged components tied to the magnetic field can drift relative to neutral matter. This permits magnetic flux to redistribute relative to the bulk neutral gas.
- **Ion-neutral drift:** The relative velocity between charged and neutral components. In the appropriate regime, this drift is the physical basis of ambipolar diffusion.
- **Magnetic flux:** Magnetic field integrated over a surface. Flux transport describes how the field and its threading of material change as a system evolves.
- **Mass-to-flux ratio:** A measure comparing the mass associated with a region to the magnetic flux threading it. Its critical value depends on geometry and adopted conventions; it is used to assess magnetic support relative to self-gravity.
- **Magnetically subcritical region:** A region whose mass-to-flux ratio is below the adopted critical threshold in the model, so magnetic support can prevent idealized gravitational collapse across field lines.
- **Magnetically supercritical region:** A region whose mass-to-flux ratio exceeds the adopted critical threshold, so magnetic support alone cannot prevent collapse in the idealized comparison.
- **Non-ideal MHD:** MHD descriptions that include departures from perfect magnetic-flux freezing. Important terms in star-forming environments include ambipolar diffusion, Ohmic resistivity, and the Hall effect.
- **Ohmic dissipation:** Resistive decoupling of magnetic fields from the charged fluid, particularly important at high densities and small scales in collapsing material.
- **Hall effect:** A non-ideal term that changes magnetic-field evolution according to the orientation of the magnetic field and electric current; it is not simply another name for ambipolar diffusion.
- **Grain charging:** The acquisition of positive or negative charge by dust grains. Charged grains can carry a significant fraction of charge and alter conductivity and coupling, especially at high density.
- **Magnetic braking:** Transfer of angular momentum through magnetic stresses and the surrounding medium. It is related to magnetic coupling but is not identical to ambipolar diffusion.
- **Free-fall time:** The characteristic collapse time for an idealized pressure-free uniform sphere under its own gravity. Real clouds are not pressure-free uniform spheres, so this is a reference timescale rather than a universal collapse clock.

## 3. Why ionization matters to magnetic coupling

Magnetic fields act directly on charged particles, not on neutral molecules in the same direct Lorentz-force sense. In a weakly ionized molecular cloud, ions and electrons are a small fraction of the particles, but collisions allow them to exchange momentum with the much more abundant neutral gas.

When charged particles are sufficiently coupled to the field, magnetic stresses can influence the neutral material through collisions. The field can therefore affect cloud motion even though most of the cloud's mass is neutral.

The coupling is not all-or-nothing. It depends on the collision frequencies, charged-species abundances, grain charging, field strength, and the dynamical timescale and length scale under examination.

Cosmic rays are often an important ionization source in shielded molecular gas. Their contribution affects the available charged-particle population, but the resulting charge balance is calculated from a chemical network, not from the cosmic-ray ionization rate alone.

## 4. Ambipolar diffusion: the mechanism

### 4.1 Physical description

In a simplified weakly ionized cloud, magnetic forces act on the charged component. Collisions transfer momentum from the charged component to the neutrals. If the magnetic force and collisional drag do not keep the two components moving together perfectly, a relative drift develops.

The field and charged component can then move relative to the bulk neutral material. Magnetic flux is redistributed through the neutral gas. This is ambipolar diffusion.

It is important to state what is moving relative to what: ambipolar diffusion is not ordinary molecular diffusion of magnetic field particles, and it does not mean that magnetic fields disappear. It is a non-ideal transport process arising from imperfect charged-neutral coupling.

### 4.2 Simplified drift relation

In a single-ion, strong-coupling approximation, neglecting charged-particle inertia and writing the magnetic force density in Gaussian cgs units, the ion-neutral drift can be represented schematically as:

\[
\mathbf{v}_{i}-\mathbf{v}_{n}
\;\approx\;
\frac{(\nabla\times\mathbf{B})\times\mathbf{B}}
{4\pi\,\gamma\,\rho_i\,\rho_n}
\]

Here:

- \(\mathbf{v}_{i}\) is the ion velocity;
- \(\mathbf{v}_{n}\) is the neutral velocity;
- \(\mathbf{B}\) is the magnetic field;
- \(\rho_i\) and \(\rho_n\) are ion and neutral mass densities;
- \(\gamma\) is the ion-neutral momentum-transfer coefficient.

The expression is an approximation, not a universal formula for every cloud. A realistic treatment may need multiple ion species, charged grains, chemical reactions, anisotropic transport, and additional non-ideal terms.

A corresponding characteristic ambipolar diffusivity in the same simplified framework is often written:

\[
\eta_{\rm AD}\;\sim\;
\frac{B^{2}}{4\pi\,\gamma\,\rho_i\,\rho_n}
\]

This scaling makes the dependence visible: at fixed field strength, neutral density, and collision coefficient, reducing the charged mass density can increase the effective ambipolar diffusivity. But those quantities do not remain fixed in a real cloud. Charge balance, grain populations, density, field geometry, and chemistry all evolve together.

### 4.3 What the relation does and does not say

The relation does not say that cosmic rays directly push neutral gas into collapse. Cosmic rays influence ionization and therefore can influence the charged population. The magnetic force and ion-neutral drag determine the drift in the stated approximation. Gravity, pressure, turbulence, and geometry determine the wider cloud dynamics.

The distinction between an influence on a coefficient and the cause of a complete outcome must be preserved.

## 5. Cosmic rays and the charge balance

In shielded molecular regions, cosmic-ray ionization can initiate ion–molecule chemistry. The resulting ions and electrons recombine, attach to grains, or participate in further reactions. Dust grains can carry positive or negative charge.

The equilibrium and time-dependent charge distribution depend on:

- the cosmic-ray ionization rate and particle spectrum;
- gas density and temperature;
- molecular composition and metal abundance;
- grain size distribution and grain surface properties;
- electron and ion recombination rates;
- depletion of species onto dust;
- radiation and local environmental conditions.

Thus, cosmic-ray ionization rate and ionization fraction are related but not identical quantities. A measured or inferred ionization rate cannot be substituted directly for a measured ion fraction without a chemical and charge-balance model.

Investigation 015 examined chemical tracers and the uncertainty in inferred cosmic-ray ionization rates. The present investigation follows the next link: how the resulting charge carriers affect the non-ideal electrical behavior of the gas.

## 6. The other non-ideal MHD effects

Ambipolar diffusion is not the only way magnetic flux can depart from ideal flux freezing.

### 6.1 Ohmic resistivity

At sufficiently high densities, frequent collisions and the changing charged-particle population can allow magnetic fields to decouple from the charged fluid through electrical resistivity. Ohmic dissipation can become important in the innermost stages of collapse and in protostellar environments.

### 6.2 Hall effect

The Hall term changes magnetic-field evolution according to the relative orientation of the magnetic field and electric current. Its dynamical influence can depend on field polarity and rotation. It should not be described as simple magnetic slippage identical to ambipolar diffusion.

### 6.3 Ambipolar diffusion

Ambipolar diffusion describes relative drift between charged material tied to magnetic stresses and neutral gas. It can operate on cloud and core scales, but its importance depends on local conditions.

### 6.4 Why the distinction matters

A collapsing core can pass through environments in which different non-ideal terms become important. A single label such as “magnetic diffusion” can hide physically different mechanisms.

The 2012 review by Wardle discusses the Hall effect in star formation and the distinctions among non-ideal magnetic diffusivity regimes.

Source: Wardle, M. (2012), “The Hall effect in star formation,” *Monthly Notices of the Royal Astronomical Society* 422, 261–272. https://academic.oup.com/mnras/article/422/1/261/1020903

## 7. Magnetic support, gravity, and contraction

Magnetic fields can resist compression across field lines and can transmit stresses through the cloud. Gravity pulls mass inward. Turbulence, thermal pressure, rotation, and flows along field lines also affect the evolution.

The mass-to-flux ratio is one way to describe the balance between gravity and magnetic support. In an idealized magnetically subcritical cloud, collapse across field lines is impeded. Redistribution of magnetic flux relative to neutral mass can change the local mass-to-flux ratio over time.

However, ambipolar diffusion is not the only route by which a region's mass-to-flux ratio can change. Mass can also accumulate along field lines, and turbulent or converging flows can reorganize the material. The cloud may be globally supercritical while containing locally different conditions.

A 2007 review of star formation discusses ambipolar diffusion, ionization, and magnetic support while emphasizing that the physical importance of these processes depends on the environment and cloud structure.

Source: McKee, C. F. & Ostriker, E. C. (2007), “Theory of Star Formation,” *Annual Review of Astronomy and Astrophysics* 45, 565–687. https://doi.org/10.1146/annurev.astro.45.051806.110602

## 8. The observational question: how can the mechanism be tested?

No single observation directly displays the complete ion-neutral drift and magnetic-flux history of a molecular core. Researchers combine multiple diagnostics.

### 8.1 Magnetic-field measurements

- **Zeeman splitting** can constrain the line-of-sight magnetic-field component in suitable spectral lines.
- **Dust polarization** can constrain the projected magnetic-field orientation, subject to grain-alignment and radiative-transfer considerations.
- **Polarized molecular-line emission** can provide additional information about field geometry and excitation conditions.
- **Faraday rotation** is useful in ionized foregrounds and related environments, but is not a direct measurement of the neutral-core field in every case.

These methods measure different aspects of the field. Their outputs should not be treated as interchangeable.

### 8.2 Ion and neutral velocity comparisons

Researchers can compare spectral-line profiles from molecular ions and neutral molecules that trace similar regions. Differences in centroid velocities, linewidths, or spatial distributions may provide evidence relevant to ion-neutral drift and turbulence.

But a velocity difference is not automatically a detection of ambipolar diffusion. Different molecules can trace different densities, optical depths, excitation conditions, and locations. Chemical segregation and radiative-transfer effects can imitate or complicate the signal.

### 8.3 Chemical tracers of ionization

Molecular ions and deuterated species can constrain the chemical and ionization state. The inference depends on reaction rates, depletion, temperature, density, and the assumed chemical history.

### 8.4 Density and kinematic structure

Continuum emission and molecular-line observations constrain density distributions and gas motions. These must be compared with magnetic-field information and chemical diagnostics to test whether a proposed flux-transport process is plausible.

### 8.5 Model comparison

A credible interpretation compares predictions from ideal MHD, non-ideal MHD, turbulence-regulated models, and gravitational contraction models. The same observation may be compatible with more than one model. The test is whether a model explains multiple independent measurements without contradicting the rest of the evidence.

Crutcher's review of magnetic fields in molecular clouds surveys observational methods and concludes that, at the time of publication, there was no definitive observational evidence that ambipolar-diffusion-driven star formation was the established universal explanation.

Source: Crutcher, R. M. (2012), “Magnetic Fields in Molecular Clouds,” *Annual Review of Astronomy and Astrophysics* 50, 29–63. https://doi.org/10.1146/annurev-astro-081811-125514

## 9. A necessary counterweight: ambipolar diffusion is not a universal collapse explanation

The mechanism is physically established in weakly ionized plasmas. That does not mean every molecular core is observed to contract because of ambipolar diffusion, or that it is the dominant process at every scale.

A 2019 review of magnetic fields and star formation notes that non-ideal effects matter, but that much of the cloud-scale evolution can often be treated approximately with ideal MHD, with non-ideal effects becoming especially important on smaller scales. It discusses ion-neutral drift as a large-scale non-ideal mechanism while emphasizing the importance of scale and environment.

Source: Pattle, K. & Fissel, L. (2019), “The Role of Magnetic Fields in Setting the Star Formation Rate and the Initial Mass Function,” *Frontiers in Astronomy and Space Sciences* 6, 15. https://doi.org/10.3389/fspas.2019.00007

A 2012 observational review likewise cautioned against claiming definitive evidence for ambipolar-diffusion-driven star formation. The existence of a physical mechanism and the demonstration that it dominates a particular astronomical outcome are separate evidentiary claims.

This is a central control on the investigation: **mechanism established does not mean universal dominance established.**

## 10. GUA-W Language of Creation: careful descriptive placement

The seven descriptors are used as a way to organize the scientific relationships. They do not replace non-ideal MHD, chemical charge-balance calculations, or observations.

| GUA-W descriptor | What the scientific evidence allows us to describe | Boundary of the description |
|---|---|---|
| **Structure** | Charged species, neutral gas, dust grains, magnetic fields, and gravitationally bound material occupy related positions and states in a molecular cloud. | A diagram of these components is not the complete dynamical system. |
| **Framework** | Magnetic geometry, collision rates, chemical charge balance, density, and temperature establish conditions in which charged-neutral coupling operates. | Framework is descriptive language, not an additional physical force. |
| **Pattern** | Spatial variations in field orientation, ion and neutral velocities, chemical tracers, density, and polarization can reveal recurring distributions. | A pattern does not uniquely identify ambipolar diffusion as its cause. |
| **Constraint** | Ionization, grain charging, collision rates, field strength, geometry, gravity, turbulence, and boundary conditions shape the possible evolution. | No one constraint alone determines collapse or prevents it in every circumstance. |
| **Purpose** | Scientific functions can be identified, including magnetic support, momentum transfer, flux redistribution, and gravitational contraction. | These functions do not establish ultimate intention or theological purpose. |
| **Manifestation** | Measured line profiles, polarization, Zeeman splitting, continuum structure, and chemical abundances make selected aspects of the system observable. | These signals require interpretation and do not expose the entire process directly. |
| **Witness** | Telescopes, spectrometers, polarimeters, laboratory collision data, simulations, and investigators register and analyze evidence. | Each witness has a defined sensitivity, resolution, and interpretive limit. |

**Important distinction:** Cosmic-ray ionization, the resulting charge distribution, ion-neutral drift, magnetic-flux redistribution, and gravitational contraction are connected but distinct parts of the account. The descriptive vocabulary must not collapse them into one event.

## 11. Relationship audit

### Same mechanism

Ion-neutral drag transfers momentum between charged and neutral components. In the appropriate weakly ionized regime, imperfect coupling allows relative drift and ambipolar diffusion. These are connected descriptions of the same physical process at the relevant level.

### Comparable relationship

Cosmic-ray ionization and grain charging both influence the charged-particle population and therefore the electrical behavior of the gas. They are related contributors to charge balance, but they are not the same mechanism.

### Analogy

A magnetic field can be described as being partly carried with the charged component while neutral material drifts relative to it. This wording can help communicate the distinction, but the field is not a material object attached to individual ions by a literal tether.

### Unresolved comparison

A region with a changing mass-to-flux ratio may be consistent with ambipolar diffusion, mass accumulation along field lines, or other dynamical processes. The observed change alone does not distinguish these mechanisms. The comparison remains unresolved until independent field, chemical, and kinematic evidence is brought together.

## 12. Boundary and participation examination

The standing boundary questions are applied directly:

**Are we witnessing the same mechanism, a similar relationship, or merely a similar appearance?**

**Does a boundary merely separate two regions, or can it also participate in the relationship between them?**

- **Ionization transition:** A change in ionization can alter charged-neutral coupling and wave damping. This is a physical change in conditions, not merely a visual boundary.
- **Cloud envelope/core interface:** Density, chemistry, and radiation conditions can change across the interface. The transition may influence magnetic coupling and particle transport.
- **Magnetic-field geometry:** Field curvature and gradients can shape the magnetic force and drift direction. Geometry participates in the process rather than simply marking a boundary.
- **Gas–dust interface:** Charged grains can participate in the charge balance and momentum exchange. Dust is not merely passive decoration.
- **Neutral flow along field lines:** Material can accumulate along magnetic fields without requiring the same cross-field flux transport as ambipolar diffusion. This is a distinct route to changing local density and mass-to-flux distribution.
- **Observational boundary:** Telescope beams, spectral-line excitation, and line-of-sight integration define what a measurement samples. These are limits of the witness, not necessarily physical boundaries in the cloud.

A boundary can separate, constrain, or participate in exchange. Its role must be demonstrated in the particular physical system.

## 13. Four-Question Study Method

### 1. What must AI ask to understand GUA-W?

The inquiry must distinguish ionization rate from ionization fraction; charged-particle abundance from magnetic coupling; ion-neutral drift from bulk cloud motion; ambipolar diffusion from Ohmic and Hall effects; and flux redistribution from gravitational collapse. It must ask which scale and regime each statement concerns.

### 2. What is GUA-W revealing that helps AI understand?

The established vocabulary helps organize the components, conditions, recurring distributions, constraints, demonstrated functions, observable outcomes, and instruments that register them. It provides a descriptive discipline, not a substitute for the physical equations.

The Genesis 1–2 KJV foundation remains the scriptural source of the project's vocabulary. This investigation does not claim that Genesis explicitly describes ion-neutral drift, magnetic diffusivity, or molecular-cloud collapse.

### 3. What am I learning about what I am witnessing?

In weakly ionized molecular gas, magnetic forces act on charged material and influence neutral matter through collisions. Imperfect coupling can allow ion-neutral drift and magnetic-flux redistribution. Cosmic-ray ionization contributes to the charge balance, but grain charging, chemistry, density, and local conditions also matter. Gravity, turbulence, flows along field lines, and other non-ideal processes remain part of cloud evolution.

### 4. What am I learning about the Witness through what I am witnessing?

The investigator does not directly observe the complete magnetic-flux history of a molecular cloud. The account is reconstructed from magnetic-field measurements, spectral-line comparisons, chemical tracers, continuum maps, and models. Each measurement samples a different part of the system. The Witness must preserve the difference between a physical mechanism, evidence consistent with that mechanism, and proof that it dominates a particular outcome.

## 14. Triple Constraint examination

### Biblical compliance

This investigation uses the project's Genesis 1–2 KJV-derived descriptive vocabulary. It does not claim that Genesis explicitly describes non-ideal MHD, cosmic-ray ionization, ambipolar diffusion, or star-formation dynamics. Scientific findings are not used to revise Scripture.

**Assessment:** No direct contradiction is introduced by this bounded descriptive use, provided scientific mechanisms are not presented as explicit biblical statements.

### Scientific coherence

The investigation distinguishes ionization rate from ionization fraction, charged-neutral coupling from magnetic-flux transport, ambipolar diffusion from Ohmic and Hall effects, and flux redistribution from gravitational collapse. It records the limits of observations and the fact that multiple mechanisms can produce related signatures.

**Assessment:** Scientifically coherent as an introductory synthesis. The physical mechanism is established, but its dominance in any particular cloud or across all star formation is not assumed.

### GUA-W consistency

The seven descriptors organize the evidence without becoming additional physical forces or new architectural layers. The investigation preserves the distinction between the physical system, its manifestations, and the instruments and investigators that witness it.

**Assessment:** Consistent as a bounded descriptive correspondence. No new GUA-W architectural layer is proposed.

## 15. What is established, inferred, and unresolved?

### Established by the scientific literature

- Molecular clouds are largely neutral but contain charged particles and charged dust grains.
- Magnetic fields act directly on charged particles; collisions allow charged material to exchange momentum with neutral gas.
- Imperfect charged-neutral coupling can produce ion-neutral drift and ambipolar diffusion.
- Cosmic-ray ionization contributes to the charge balance in shielded molecular regions.
- The ionization fraction is not identical to the cosmic-ray ionization rate and requires a charge-balance and chemical treatment.
- Ambipolar diffusion is one of several non-ideal MHD effects; Ohmic resistivity and the Hall effect are physically distinct.
- Magnetic fields, gravity, turbulence, and gas flows all participate in molecular-cloud dynamics.

### Supported inference

Changes in cosmic-ray ionization can influence the charged-particle population and thereby alter the conditions for charged-neutral coupling. Under specified conditions, this can change the rate of ambipolar drift and magnetic-flux redistribution.

This is a conditional physical connection, not a claim that cosmic rays alone control the contraction of molecular clouds.

### Unresolved

- How do charged grains alter the effective ambipolar diffusivity across different density regimes?
- What fraction of observed ion-neutral velocity differences can be attributed to ambipolar drift rather than chemical and radiative-transfer selection effects?
- At what scales does ambipolar diffusion become dynamically important in different cloud environments?
- How do cosmic-ray attenuation and spatially varying ionization alter magnetic coupling from cloud envelope to dense core?
- Can observations establish when a change in mass-to-flux ratio is caused by ambipolar diffusion rather than flow along field lines or turbulent rearrangement?
- How do ambipolar, Hall, and Ohmic terms interact during the transition from a molecular core to a protostar and disk?
- Under what conditions does ambipolar diffusion materially change the star-formation rate or timing, rather than simply modify local magnetic structure?

These questions remain open. No universal ambipolar-diffusion-driven collapse model is asserted.

## 16. Sources

1. McKee, C. F. & Ostriker, E. C. (2007). “Theory of Star Formation.” *Annual Review of Astronomy and Astrophysics* 45, 565–687. https://doi.org/10.1146/annurev.astro.45.051806.110602
2. Crutcher, R. M. (2012). “Magnetic Fields in Molecular Clouds.” *Annual Review of Astronomy and Astrophysics* 50, 29–63. https://doi.org/10.1146/annurev-astro-081811-125514
3. Wardle, M. (2012). “The Hall effect in star formation.” *Monthly Notices of the Royal Astronomical Society* 422, 261–272. https://academic.oup.com/mnras/article/422/1/261/1020903
4. Pattle, K. & Fissel, L. (2019). “The Role of Magnetic Fields in Setting the Star Formation Rate and the Initial Mass Function.” *Frontiers in Astronomy and Space Sciences* 6, 15. https://doi.org/10.3389/fspas.2019.00007
5. “Hydromagnetic waves in weakly-ionized media – I. Basic theory, and application to interstellar molecular clouds” (2011). *Monthly Notices of the Royal Astronomical Society* 415, 1751. https://academic.oup.com/mnras/article/415/2/1751/1043289
6. “Observational Signatures of Cosmic-Ray Interactions in Molecular Clouds” (2021). *The Astrophysical Journal* 912. https://doi.org/10.3847/1538-4357/abee1a
7. “Recent progress with observations and models to characterize the magnetic fields from star-forming cores to protostellar disks” (2022). *Frontiers in Astronomy and Space Sciences*. https://www.frontiersin.org/journals/astronomy-and-space-sciences/articles/10.3389/fspas.2022.949223/full

## 17. Next question emerging

The investigations have now followed cosmic rays from propagation, through molecular chemistry, into the charged-neutral relationship that influences magnetic coupling.

The next question is:

**How do magnetic fields, turbulence, gravity, and gas flows jointly determine whether a molecular cloud forms filaments and dense cores, and how can observations distinguish the competing routes to structure formation?**

This should examine cloud-scale organization and the formation of dense structures without assuming that one mechanism—gravity, magnetic fields, turbulence, or ambipolar diffusion—acts alone.

---

**Investigation 016 records the distinction between cosmic-ray ionization, charged-neutral coupling, magnetic-flux transport, and gravitational contraction. The physical mechanism remains the subject; the record remains the Witness's report.**
