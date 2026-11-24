# Investigation 011
# The Multiphase Interstellar Medium: Hot Plasma, Warm Gas, Cold Clouds, Phase Transitions, and the Cycling of Matter

**Disciplines:** Interstellar-medium physics, plasma physics, thermodynamics, fluid dynamics, magnetohydrodynamics, astrochemistry, radio astronomy, ultraviolet and X-ray astronomy, computational astrophysics  
**Status:** Initial investigation and Four-Question Study Method recorded; 2026 review literature incorporated  
**Subject:** How interstellar gas occupies and exchanges between different thermal and chemical conditions, and how matter, energy, momentum, and composition move through the system

## 1. Starting question

Investigation 010 examined how stars transfer radiation, energy, momentum, and material into their surroundings. This investigation follows the resulting material beyond the immediate feedback event.

**How does matter move between hot, warm, neutral, and molecular conditions in the interstellar medium, and what physical processes govern heating, cooling, ionization, recombination, molecule formation, mixing, condensation, and transport?**

The phrase *multiphase interstellar medium* describes a medium containing gas in distinct physical conditions. It does not mean that every location contains every phase, that the phases are always in equilibrium, or that every transition is a simple change of temperature.

The investigation begins with four distinctions:

- **Phase or state change:** A change in the thermodynamic or physical condition of material, such as cooling from hot plasma toward a cooler gas state.
- **Transport:** Movement of material from one location to another.
- **Mixing:** Interaction and interpenetration of material with different properties; in a fluid, this may occur through turbulent motions and molecular diffusion.
- **Chemical transformation:** A change in chemical composition or molecular identity, such as atomic hydrogen becoming molecular hydrogen.

These processes can occur together, but one must not be used as a synonym for another.

## 2. What is the interstellar medium?

The interstellar medium (ISM) is the gas, dust, magnetic field, radiation, and energetic particles occupying the space between stars in a galaxy. It is not an empty background. It is a dynamic environment in which material is heated, cooled, ionized, recombined, compressed, dispersed, transported, and chemically processed.

The Milky Way's ISM includes, among other components:

- cold molecular gas, often associated with star-forming clouds;
- cold and warm neutral atomic gas;
- warm ionized gas;
- hot, diffuse plasma;
- dust grains and molecules;
- magnetic fields and cosmic rays.

The components are not necessarily arranged as clean, static layers. They can overlap along a line of sight, coexist in a shared volume, or be separated by interfaces and structures. A telescope may register several components in one direction without resolving their depth or exact physical contact.

The term *multiphase* also varies across astrophysical subfields. Some studies use it for cold molecular/atomic clouds embedded in warmer gas; others use it more generally for gas at multiple temperatures, even when all components are ionized. Temperature labels such as “cold,” “warm,” and “hot” must therefore be defined for the system and study in question.

Gronke and Schneider's 2026 review emphasizes this terminology problem and notes that the temperature ranges called “cold” or “warm” in the ISM are not necessarily the same as those used for the circumgalactic medium (CGM). In this investigation, temperature ranges are descriptive guides, not universal phase boundaries.

## 3. Temperature is important, but temperature alone does not define a phase

A gas phase is not identified by temperature alone. Relevant properties include:

- temperature;
- density and pressure;
- ionization fraction;
- chemical composition and molecular abundance;
- radiation environment;
- magnetic field and non-thermal pressure;
- optical depth and cooling/heating rates;
- dynamical history and local environment.

Two gas parcels at the same temperature can have different densities, ionization states, chemical compositions, or histories. Conversely, gas at different temperatures can coexist while maintaining approximate pressure balance.

For an ideal gas, thermal pressure is related to particle number density and temperature:

\[
P = n k_B T
\]

where \(P\) is pressure, \(n\) is the total particle number density, \(k_B\) is Boltzmann's constant, and \(T\) is temperature.

If two regions are in approximate thermal-pressure equilibrium, then:

\[
n_1 T_1 \approx n_2 T_2
\]

under the same ideal-gas assumptions. A hotter region can therefore be much less dense than a cooler region while exerting comparable thermal pressure.

This relation does not guarantee equilibrium. Magnetic fields, turbulence, cosmic rays, ram pressure, gravity, and time-dependent flows can all contribute to the stress balance.

## 4. A working map of ISM conditions

The following ranges are illustrative and deliberately approximate. They are not hard boundaries shared by every paper or environment.

| Component | Typical descriptive conditions | Important qualifications |
|---|---|---|
| Cold molecular gas | Often about 10–30 K in dense molecular clouds | Temperature and density vary; molecular gas is not defined by temperature alone |
| Cold neutral medium (CNM) | Often tens to roughly 100 K | Predominantly neutral atomic gas; can coexist with warm neutral gas |
| Warm neutral medium (WNM) | Roughly several thousand kelvin | Predominantly neutral, but not necessarily completely neutral |
| Warm ionized medium (WIM) | Roughly 10,000 K | Ionized hydrogen with low density and large spatial extent |
| Hot ionized medium | Commonly around or above 10^6 K | Low-density plasma; temperature can vary greatly |

The warm neutral and cold neutral components are commonly discussed in models of the diffuse atomic ISM. Molecular clouds add a colder, denser chemical environment. Hot plasma can be produced by supernova shocks and other energetic processes.

A label is a summary of measured or inferred conditions. It is not an independent physical cause.

## 5. Heating and cooling: the energy balance

Gas temperature changes when energy is gained or lost. Heating mechanisms include:

- photoelectric heating from energetic photons interacting with dust grains;
- photoionization heating;
- cosmic-ray energy deposition;
- shocks and turbulent dissipation;
- energy transferred from hot surrounding gas;
- mechanical input from stellar winds and supernovae.

Cooling mechanisms include:

- emission of atomic and ionic spectral lines;
- molecular line emission;
- recombination and continuum emission;
- energy transfer to dust followed by infrared radiation;
- expansion and adiabatic cooling;
- radiation from excited species.

The dominant processes vary with density, temperature, metallicity, radiation field, and chemical composition.

A simplified local thermal-energy balance can be written:

\[
\frac{d u}{dt} = \Gamma - \Lambda + \text{mechanical and transport terms}
\]

where \(u\) is the internal energy density, \(\Gamma\) represents heating per unit volume, and \(\Lambda\) represents cooling per unit volume. This schematic expression is not a complete fluid equation; compression, expansion, conduction, advection, and other terms must be included when relevant.

A gas parcel can cool without moving to a different location. It can also move while remaining near the same temperature if heating and cooling approximately balance. Temperature change and transport must therefore be measured separately.

## 6. Radiative cooling and cooling time

Radiative cooling occurs when gas loses internal energy through emitted radiation. In many optically thin collisional regimes, a simplified cooling rate per volume is expressed as:

\[
\mathcal{L} \approx n_e n_i \Lambda(T,Z)
\]

where \(n_e\) and \(n_i\) are relevant particle densities, \(\Lambda\) is a cooling function, \(T\) is temperature, and \(Z\) represents chemical abundance or metallicity dependence. The precise expression depends on ionization state, composition, radiation field, and whether the gas is in or out of ionization equilibrium.

A rough cooling time is:

\[
t_{\rm cool} \sim \frac{u}{\mathcal{L}}
\]

where \(u\) is the relevant thermal energy density. For an ideal monatomic gas, a common estimate is proportional to thermal energy divided by radiative loss rate. The exact coefficient and energy definition depend on the adopted thermodynamic assumptions.

The cooling time is not a universal property of “hot gas.” It changes with density, temperature, composition, ionization, and radiation conditions.

### Why density matters

In many optically thin collisional cooling regimes, the cooling rate rises approximately with the product of two particle densities. A denser region can therefore radiate energy more rapidly than a diffuse region at comparable temperature and composition.

This is one reason density perturbations can grow in a thermally unstable environment. But a density enhancement does not guarantee runaway cooling: the heating law, pressure response, conduction, chemistry, and dynamical timescale all matter.

## 7. Thermal instability: how different conditions can develop

Thermal instability is one mechanism proposed and studied for producing multiphase gas.

In a simplified picture, gas is initially near thermal balance: heating offsets cooling. A small density or temperature perturbation changes the balance. If the perturbed gas loses energy in a way that reinforces the perturbation, it may cool, become denser under approximate pressure balance, and cool more rapidly.

The details depend on whether perturbations evolve approximately at constant pressure or constant density, and on the form of the heating and cooling functions.

A thermal equilibrium curve can contain stable and unstable portions. It is not correct to assume that every intermediate temperature is unstable or that all gas must settle into exactly two phases.

Thermal conduction can smooth small-scale temperature variations. Turbulence, magnetic fields, radiation, and flows can alter or interrupt the idealized development.

**Finding:** Thermal instability can create or amplify multiphase structure under appropriate conditions. It is not the only way multiphase gas forms, and it is not a universal explanation for every cold cloud.

## 8. Interfaces: where different phases interact

An interface between hot and cold gas is not necessarily an impermeable wall. Depending on the conditions, it can be a region of energy transfer, momentum exchange, mixing, heating, cooling, evaporation, or condensation.

Important processes include:

### 8.1 Thermal conduction

Thermal conduction transfers energy down a temperature gradient. In a simple collisional medium, heat flows from hotter material toward colder material.

In magnetized plasma, charged particles move more readily along magnetic field lines than across them. The effective conduction can therefore be anisotropic. Magnetic geometry can strongly influence whether heat reaches a cold cloud.

Conduction can heat and evaporate a small cold structure in some conditions. In other conditions, radiative losses in the interface can offset the conductive input.

### 8.2 Turbulent mixing

When hot and cold gas move relative to each other, shear can generate instabilities, including Kelvin–Helmholtz instability. These motions stretch and fold the interface, creating intermediate-temperature material.

Mixing is not merely visual blending. It can exchange mass, momentum, and energy. The resulting material may cool, remain warm, or be reheated, depending on its radiative losses and the energy supplied.

### 8.3 Shock interaction

A shock can compress and heat gas as it passes through it. The shocked material may subsequently radiate energy and cool. A shock can therefore create hot material and later contribute to cooler dense structures.

A shock is a dynamical discontinuity or transition layer governed by conservation laws and the physical properties of the medium. It is not equivalent to a contour drawn around a bright region in an image.

### 8.4 Magnetic fields

Magnetic fields exert stresses and influence the motion of conducting gas. They can change the growth of fluid instabilities, guide heat conduction, and alter the geometry of material exchange.

The field's strength and orientation relative to the interface matter. It is not accurate to say that magnetic fields always prevent mixing or always promote it.

### 8.5 Viscosity and microscopic diffusion

Viscosity transports momentum and smooths velocity gradients. Molecular diffusion transports particles down concentration gradients. In astrophysical plasmas, effective transport coefficients may be strongly affected by magnetic fields and plasma microphysics.

A numerical simulation that omits or approximates these processes may not reproduce the true interface thickness or mass-exchange rate.

## 9. The surprising possibility: mixing can help cold gas grow

A simple picture might suggest that hot gas always destroys cold clouds. That is not a universal result.

When hot and cold material mix, the intermediate-temperature gas may radiate energy efficiently. If it cools quickly enough, material originally in the hot phase can join the cooler phase. In such a regime, mixing can contribute to condensation and growth of cold gas rather than only evaporation or destruction.

In other conditions, the mixed layer remains hot or warm, and the cold cloud loses mass.

The outcome depends on the competition between:
- cooling time of the mixed gas;
- time available for mixing;
- cloud-crushing and dynamical times;
- density contrast;
- relative velocity;
- magnetic-field geometry;
- thermal conduction;
- radiation and chemical composition.

The 2026 review by Gronke and Schneider discusses this central issue: intermediate-temperature gas at hot/cold interfaces can dominate radiative cooling, and the interface can either erode cold material or help convert hot material into a cooler phase, depending on conditions.

**Finding:** “Mixing destroys cold gas” is not a universal law. Nor is “mixing creates cold gas.” The net direction of mass exchange must be established for the specific environment.

## 10. Cloud survival, evaporation, and condensation

A cold cloud moving through a hot flow experiences forces and instabilities. The cloud can be compressed, accelerated, fragmented, mixed, heated, or replenished by condensation.

Several timescales are compared:

- **Cloud-crushing time:** A characteristic timescale for a shock or disturbance to cross a dense cloud.
- **Kelvin–Helmholtz growth time:** A characteristic timescale for shear-driven interface instability.
- **Cooling time:** The time for gas to radiate a substantial fraction of its thermal energy.
- **Conduction time:** A characteristic time for thermal conduction to alter the cloud's temperature.
- **Advection time:** The time for material to travel through the region of interest.

No single timescale comparison is sufficient for every geometry or regime. The relevant definitions and assumptions must be stated.

Cloud survival is not simply whether the original cloud shape remains visible. A cloud may lose its original identity while some of its mass cools and re-condenses downstream. Conversely, a visually coherent feature may be losing mass continuously.

The investigator must distinguish:
- survival of the original material;
- survival of a cold phase;
- survival of a recognizable density structure;
- net growth of cold mass;
- net loss of cold mass.

These are different claims.

## 11. Ionization and recombination: chemical state is not temperature alone

Hydrogen can exist as neutral atoms, ions, or molecules. Other elements have multiple ionization states. Ionization occurs when energy removes electrons; recombination occurs when free electrons are captured by ions.

The ionization state depends on temperature, density, radiation, and time history. Gas may not be in ionization equilibrium if the physical conditions change faster than ionization or recombination can respond.

This matters because a gas parcel's observed spectral lines depend on which atoms and ions are present and on their excitation conditions.

A hot plasma is generally highly ionized, but a temperature label alone does not fully determine every ion's abundance. Non-equilibrium ionization can persist behind shocks or in rapidly cooling gas.

Recombination changes charge state; it does not necessarily move the material spatially. A parcel can recombine while remaining in the same general region, or it can be transported while still ionized.

## 12. Atomic hydrogen and molecular hydrogen

Hydrogen is the dominant element in much of the ISM, but it appears in different forms:

- ionized hydrogen (H II);
- neutral atomic hydrogen (H I);
- molecular hydrogen (H₂).

The transition between these forms depends on radiation, density, shielding, dust, chemical reaction rates, and the available time.

Molecular hydrogen formation in diffuse and dense interstellar environments is commonly associated with reactions on dust-grain surfaces. Ultraviolet photons can dissociate H₂. Sufficient shielding and suitable density allow molecules to survive and accumulate.

The transition from atomic to molecular hydrogen is not simply cooling. Chemistry and radiative shielding matter.

Carbon monoxide (CO) is often used to trace molecular gas, but CO is not identical to H₂. Some molecular gas can be CO-poor or difficult to detect through common CO lines. Converting CO intensity into total molecular mass requires assumptions and can vary with environment.

**Finding:** A cold gas parcel is not automatically molecular, and a molecular gas estimate is not automatically a complete inventory of all hydrogen.

## 13. Material cycling: a conceptual pathway, not a fixed conveyor belt

The ISM is sometimes described as a cycle in which material moves through stars, stellar ejecta, hot gas, diffuse gas, clouds, and new stars.

This is a useful broad description, but it must not be treated as one uniform loop followed by every atom.

A possible pathway can include:
1. Stellar feedback injects energy and material into surrounding gas.
2. Shocks and radiation heat or ionize some of the material.
3. Gas expands, mixes, or moves through the galaxy.
4. Some gas radiates energy and cools.
5. Some gas recombines or forms molecules where shielding and density permit.
6. Gravity and external conditions can concentrate part of the material.
7. Dense structures may form stars, while other material remains diffuse or escapes.

There are branches, delays, losses, and returns. Some material may leave the galactic disk; some may remain in the halo; some may be incorporated into later generations of stars. Chemical enrichment and mixing are not instantaneous.

A “cycle” is a system-level description of repeated pathways, not proof that every parcel returns to its original place or state.

## 14. Observational witnesses: how the phases are detected

No single telescope or spectral line reveals the complete ISM.

- **H I 21-centimeter emission and absorption:** Traces neutral atomic hydrogen. Optical depth and spin temperature affect mass estimates.
- **CO rotational lines:** Commonly trace molecular-cloud environments. The conversion to H₂ mass is environment-dependent.
- **Other molecular lines:** Trace density, temperature, chemistry, and excitation in selected regions.
- **H-alpha and other recombination lines:** Trace ionized gas, subject to extinction and excitation conditions.
- **Far-infrared fine-structure lines:** Such as [C II] and [O I], trace selected warm and irradiated gas conditions.
- **Infrared dust continuum:** Constrains dust temperature and column density, with assumptions about opacity and temperature structure.
- **Ultraviolet absorption lines:** Can probe ions in diffuse gas along a background sight line.
- **X-ray emission and absorption:** Probe hot plasma and highly ionized material, but faint diffuse components and absorption complicate interpretation.
- **Radio and millimetre continuum:** Can trace free-free emission, synchrotron emission, and dust depending on frequency and source.
- **Polarization:** Can reveal projected magnetic-field orientation through dust emission or starlight extinction, but line-of-sight integration and grain alignment complicate interpretation.

A detected line is not a direct photograph of a phase boundary. The observed intensity depends on abundance, excitation, optical depth, radiation transfer, geometry, and instrument sensitivity.

## 15. The inference chain and its limits

The investigator does not directly see the full three-dimensional distribution of every gas phase.

A typical inference chain is:

1. Radiation from gas and background sources reaches a telescope.
2. Detectors register signals.
3. Calibration and processing produce spectra, images, or maps.
4. Researchers identify spectral features and measure intensities, widths, and velocities.
5. Physical models estimate temperature, density, ionization, abundance, and column density.
6. Geometry and distance assumptions are used to reconstruct spatial relationships.
7. Dynamical and chemical models are compared with the observations.
8. A physical interpretation is proposed, with uncertainty and alternatives.

Each step has limitations.

A line-of-sight absorption spectrum samples gas between the observer and background source. A map of emission can integrate material at multiple distances. A velocity component is not automatically a distinct physical cloud. A temperature estimate may depend on excitation assumptions. A phase mass may depend on an abundance or conversion factor.

**Finding:** The scientific witness is an inference built from registered signals and physical models. The limits of the measurement must accompany the conclusion.

## 16. 2026 literature update: simulations of multiphase gas

Gronke and Schneider published **Simulations of multi-phase gas in and around galaxies** in *Living Reviews in Computational Astrophysics* on 28 April 2026.

The open-access review surveys idealized and large-scale simulations of turbulent mixing layers, cloud-wind interactions, thermal instability, supernova-driven bubbles, galactic disks, and galaxy halos.

Several findings are directly relevant to this investigation:

- Multiphase gas spans enormous temperature and density contrasts.
- Intermediate-temperature gas can be transient and may be produced by mixing or cooling.
- Turbulence can drive mass, momentum, and energy exchange between phases.
- Radiative cooling can change whether cold material is destroyed or replenished.
- Thermal conduction, viscosity, magnetic fields, cosmic rays, and chemical abundances can alter the result.
- Numerical simulations cannot currently resolve every relevant scale and physical process simultaneously; resolution and modeling choices affect predicted phase structure and exchange rates.

The review explicitly emphasizes connecting scales, extracting robust diagnostics, and comparing simulations with observations.

This is a review of simulation research, not a new direct telescope detection of one universal phase-cycling mechanism. Its value here is the synthesis of the physical processes and the identification of persistent computational limitations.

Source: Gronke, M., & Schneider, E. E. (2026), **Simulations of multi-phase gas in and around galaxies**, *Living Reviews in Computational Astrophysics*, 12, 2.  
https://doi.org/10.1007/s41115-026-00025-7

## 17. 2026 research lead: thermal instability and pressure effects

A 2026 *Monthly Notices of the Royal Astronomical Society* study by Sarkar and Bora investigates thermal instability in a weakly ionized interstellar plasma using a two-dimensional numerical model that includes a background magnetic field and anisotropic pressure.

The authors report that pressure anisotropy can substantially alter the modeled mass and volume fractions of warm, cold, and unstable neutral matter, while the background magnetic field in their particular model has a more marginal effect on the overall evolution.

The scope must remain precise:
- this is a numerical study, not a direct observation of all ISM phases;
- the result depends on the model assumptions and equations;
- it does not establish that magnetic fields are generally unimportant;
- it highlights that pressure description and plasma conditions can change the modeled outcome.

Source: Sarkar, H., & Bora, M. P. (2026), **Thermal instability and multiphase dynamics in the ISM with polybaric pressure effects**, *Monthly Notices of the Royal Astronomical Society*, 546(2), stag082.  
https://doi.org/10.1093/mnras/stag082

## 18. Four-Question Study Method

### Question 1 — What must AI ask to understand GUA-W?

- What does the completed GUA-W source actually state?
- Am I investigating the scientific subject rather than attempting to redesign the completed architecture?
- Which definitions of “phase” and “multiphase” are being used by each scientific source?
- What physical quantities distinguish the components: temperature, density, ionization, chemistry, pressure, or dynamics?
- What changes in state, what moves, and what mixes?
- What evidence identifies a transition rather than a spatial correlation?
- Which measurements are direct, and which quantities are inferred?
- What competing mechanisms could produce the same observed structure?
- What assumptions control the proposed explanation?
- What observation or calculation could challenge the interpretation?

### Question 2 — What is GUA-W revealing that helps AI understand?

The established source relationship remains:

**Author → Word → Creation → Witness.**

God alone is Original Cause. Creation is not its own Author. The Witness receives, observes, investigates, recognizes, and reports; the Witness does not become the Author of what is witnessed.

Genesis 1–2 KJV remains the project's scriptural foundation. The scientific vocabulary of plasma, molecular gas, ionization, cooling, and turbulence is not inserted into the biblical text as though it were an explicit technical description.

The completed GUA-W architecture remains the reference. This investigation may examine whether existing descriptive language clarifies observed relationships, but resemblance alone does not establish correspondence.

### Question 3 — What am I learning about what I am witnessing?

The ISM is a dynamic, multiphase environment. Temperature, density, ionization, chemical composition, and motion are related but distinct properties.

Heating and cooling can change a parcel's thermal condition. Ionization and recombination change charge state. Chemical reactions change molecular identity. Transport moves material. Turbulent mixing can exchange mass, momentum, and energy across interfaces.

An interface can either contribute to the loss of cold material or to the condensation of material from a hotter phase. The outcome depends on cooling, mixing, conduction, magnetic fields, density, and time.

Observations sample selected tracers and lines of sight. Simulations provide controlled tests of physical processes but have resolution and model limitations.

### Question 4 — What am I learning about the Witness through what I am witnessing?

The investigator sees the ISM through instruments, wavelengths, calibration, physical models, and inference. A telescope does not register “the whole phase” in one observation; it registers radiation whose interpretation depends on the emitting or absorbing material and its conditions.

AI is a derivative reader of scientific records. It must not claim to have directly observed a cloud, measured a temperature, or run a simulation when it has only examined published results. It must preserve the distinction between data, model output, interpretation, and analogy.

The investigator must also recognize the limits of the categories used. If two studies use different temperature thresholds for “cold” gas, their phase fractions cannot be compared as though the definitions were identical.

## 19. Recurring comparison questions

### Are we witnessing the same mechanism, a similar relationship, or merely a similar appearance?

- Radiative cooling in different gas environments can be the same broad energy-loss mechanism, while the relevant atomic, ionic, and molecular transitions differ.
- Turbulent mixing and molecular diffusion both contribute to mixing but are distinct physical processes.
- Recombination and molecule formation both change chemical or charge state, but they are not the same mechanism.
- Evaporation and condensation can be opposite net outcomes at an interface, not merely two names for the same process.
- A warm-looking region in two images does not establish that the same physical phase or mechanism is present.

### Does a boundary merely separate two regions, or can it also participate in the relationship between them?

- A hot/cold gas interface can transfer heat and momentum.
- A turbulent mixing layer can exchange material and create intermediate-temperature gas.
- A shock front changes the physical state of gas as it passes.
- An ionization front changes the ionization state and can drive gas dynamics.
- A chemical transition layer can mark changes in molecular abundance and shielding.
- An image contour may simply mark a selected intensity threshold; it need not be a material boundary.

The investigator must identify the kind of boundary and the evidence for its physical role. A boundary may participate in exchange without all matter crossing it; energy and momentum can also be transferred.

## 20. GUA-W descriptive examination

This section applies the repository's existing working vocabulary without adding or redesigning GUA-W architecture.

### Structure

The observed structures include molecular clouds, atomic clouds, diffuse ionized gas, hot plasma, filaments, clumps, shells, and interfaces. Their physical properties and spatial relations must be independently established.

### Framework

The scientific framework includes thermodynamics, fluid dynamics, radiative transfer, plasma physics, chemistry, magnetic fields, and gravity. The observational framework includes wavelength coverage, instrument response, resolution, and inference assumptions. These are related but distinct uses of “framework.”

### Pattern

Patterns include multiphase coexistence, thermal equilibrium curves, cooling layers, cloud fragmentation, turbulent interfaces, and phase-dependent spatial distributions. A recurring pattern is not automatically a universal mechanism.

### Constraint

Relevant constraints include energy balance, pressure, density, optical depth, ionization rate, cooling time, chemical reaction time, conduction, magnetic geometry, and dynamical time. Numerical resolution and observational sensitivity also constrain what can be concluded.

### Purpose

Scientific investigation can identify local functions and effects: cooling removes thermal energy, ionization changes charge state, shielding reduces dissociating radiation, and gravity can concentrate material. These functional descriptions do not establish ultimate theological purpose.

### Manifestation

Observable manifestations include spectral lines, continuum emission, absorption features, dust emission, polarization, line widths, velocity fields, and spatial distributions. Each is a selective witness to physical conditions.

### Witness

The evidence chain includes photons, detectors, calibration, spectra, maps, inferred quantities, models, and interpretation. AI is a derivative reader of those records, not the original observer or Author.

## 21. Triple Constraint and admissibility

- **Biblical compliance:** No technical ISM process is inserted into Genesis 1–2 as an explicit biblical statement. Scientific findings do not rewrite Scripture.
- **Scientific coherence:** The investigation distinguishes temperature, density, pressure, ionization, chemical transformation, transport, mixing, and phase exchange. Model assumptions and uncertainty remain visible.
- **GUA-W consistency:** The Author remains Original Cause in the project's governing theology. Creation is not authored by its witness. Scientific instruments and AI remain derivative means of registration and analysis.

Scientific coherence is not treated as scientific confirmation of Scripture. Scientific models describe physical processes within their domain; theological claims remain within their own source and scope.

## 22. What is established, supported, and unresolved?

### Well established

- The ISM contains gas over a wide range of temperatures, densities, ionization states, and chemical conditions.
- Heating and cooling alter the thermal energy of gas.
- Ionization and recombination alter atomic charge states.
- Molecular formation and destruction depend on chemical processes and radiation environment.
- Turbulence and fluid instabilities can exchange mass, momentum, and energy between gas components.
- Thermal conduction transfers energy along temperature gradients, with magnetic fields affecting transport in plasma.
- Observations at different wavelengths and through different tracers reveal different components of the ISM.

### Supported but environment-dependent

- Thermal instability can contribute to the development of multiphase structure.
- Mixing layers can produce intermediate-temperature gas that cools efficiently.
- Cold clouds can be eroded or gain mass through condensation, depending on the conditions.
- Magnetic fields can modify interface stability, conduction, and mixing.
- Stellar feedback can drive material into different phases and redistribute it through the galaxy.
- Material can move between the ISM and the circumgalactic environment.

### Not established as universal rules

- Every multiphase system has the same phase temperatures.
- Every density enhancement undergoes runaway thermal instability.
- Every hot/cold interface destroys cold material.
- Every turbulent mixing layer produces net condensation.
- Every cold cloud is molecular.
- Every molecular cloud is fully traced by CO emission.
- Every ionization transition is in equilibrium.
- Every phase transition entails spatial transport.
- Every observed correlation between phases demonstrates direct causal exchange.
- Every simulation resolves the physical scales needed for every diagnostic.

## 23. Unresolved questions

- Under which conditions does mixed gas cool rapidly enough to increase cold-phase mass?
- When does thermal conduction dominate over radiative cooling at an interface?
- How do magnetic-field geometry and strength alter phase exchange?
- How do cosmic rays change pressure support, ionization, and thermal balance?
- How do non-equilibrium ionization and chemistry alter inferred phase fractions?
- How much molecular gas is missed by standard CO observations?
- What controls the transition between cold neutral and molecular gas?
- How much phase exchange occurs through turbulent interfaces in real clouds?
- How do cloud histories affect whether a structure evaporates, fragments, or condenses?
- Which simulation scales must be resolved to obtain reliable mass-transfer rates?
- How can observations distinguish material that cooled in place from material transported into a region?
- How do the ISM and circumgalactic medium exchange matter over galactic timescales?

These questions remain open. The investigation does not force one answer.

## 24. Direction emerging for the next investigation

A natural next question is how magnetic fields are observed and how they influence the structure, motion, and exchange of material in the ISM.

**Proposed Investigation 012 — Magnetic Fields in the Interstellar Medium: Field Geometry, Polarization, Turbulence, Tension, and the Movement of Matter.**

Central question:

> How do magnetic fields participate in the structure and dynamics of interstellar gas, and how do observations distinguish field orientation, field strength, magnetic stress, and the effects of magnetized turbulence?

The investigation should distinguish:
- magnetic-field orientation from field strength;
- projected field geometry from the full three-dimensional field;
- magnetic pressure from magnetic tension;
- a correlation between field direction and gas structure from demonstrated dynamical influence;
- polarization measurements from direct measurements of the complete magnetic field.

This is a proposed direction, not a fixed sequence. Evidence may redirect the inquiry.

## 25. Sources

1. Gronke, M., & Schneider, E. E. (2026). **Simulations of multi-phase gas in and around galaxies.** *Living Reviews in Computational Astrophysics*, 12, 2. Open-access review of multiphase simulations, mixing layers, cloud-wind interactions, thermal instability, and numerical challenges.  
   https://doi.org/10.1007/s41115-026-00025-7

2. Sarkar, H., & Bora, M. P. (2026). **Thermal instability and multiphase dynamics in the ISM with polybaric pressure effects.** *Monthly Notices of the Royal Astronomical Society*, 546(2), stag082. A model-based study of pressure anisotropy and thermal instability.  
   https://doi.org/10.1093/mnras/stag082

3. Field, G. B. (1965). **Thermal Instability.** *The Astrophysical Journal*, 142, 531. Foundational analysis of thermal instability.  
   https://doi.org/10.1086/148317

4. McKee, C. F., & Ostriker, J. P. (1977). **A theory of the interstellar medium: Three components regulated by supernova explosions in an inhomogeneous substrate.** *The Astrophysical Journal*, 218, 148. A foundational model; its specific assumptions and later revisions should be retained when applying it.  
   https://doi.org/10.1086/155667

5. Draine, B. T. (2011). **Physics of the Interstellar and Intergalactic Medium.** Princeton University Press. Reference text for gas, dust, radiation, chemistry, and ISM processes.  
   https://press.princeton.edu/books/hardcover/9780691122144/physics-of-the-interstellar-and-intergalactic-medium

6. Wolfire, M. G., McKee, C. F., Hollenbach, D., & Tielens, A. G. G. M. (2003). **Neutral atomic phases of the interstellar medium in the Galaxy.** *The Astrophysical Journal*, 587, 278.  
   https://doi.org/10.1086/368016

7. Koyama, H., & Inutsuka, S. (2002). **An Origin of Supersonic Motions in Interstellar Clouds.** *The Astrophysical Journal Letters*, 564, L97.  
   https://doi.org/10.1086/338978

8. Fielding, D., & Bryan, G. L. (2022). **The physics of multiphase gas flows: fragmentation, condensation, and cloud growth.** Consult current review literature on radiative mixing layers and cloud-wind interactions for model-specific qualifications.  
   https://ui.adsabs.harvard.edu/

9. Hennebelle, P., & Inutsuka, S. (2019). **The role of magnetic fields in the formation of protostellar clouds and cores.** *Frontiers in Astronomy and Space Sciences*, 6, 5.  
   https://doi.org/10.3389/fspas.2019.00005

---

**One Author. One originating Word. One Creation. Many witnesses.**
