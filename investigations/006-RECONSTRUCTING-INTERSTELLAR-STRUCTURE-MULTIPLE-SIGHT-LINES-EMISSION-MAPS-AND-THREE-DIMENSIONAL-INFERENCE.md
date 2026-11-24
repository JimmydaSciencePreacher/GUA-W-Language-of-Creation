# Investigation 006
# Reconstructing Interstellar Structure: Multiple Sight Lines, Emission Maps, and Three-Dimensional Inference

**Disciplines:** Galactic astronomy, interstellar-medium physics, observational astrophysics, radio astronomy, astrometry, statistical inference, computational imaging  
**Status:** Initial investigation with Four-Question Study Method applied  
**Primary subject:** How astronomers infer the three-dimensional distribution and motions of interstellar matter from observations that are incomplete projections of space

## 1. Starting question

Investigation 005 established that gas and dust between a star and an observer can modify the received spectrum. It also showed that multiple clouds may contribute along one line of sight.

The next question is:

> How can astronomers reconstruct the three-dimensional arrangement of interstellar matter when the available observations are separate lines of sight, projected emission maps, and measurements with different distance and velocity information?

This is an inverse problem. Instruments record radiation arriving from particular directions and wavelengths. They do not directly deliver a complete three-dimensional inventory of every gas cloud and dust grain. Astronomers combine different observations with distance estimates, physical models, and statistical methods to infer a spatial distribution.

The distinction between observation and reconstruction is central. A three-dimensional map can be a scientifically useful inference without being a direct photograph or a unique solution.

## 2. Scientific terminology

- **Astrometry:** Measurement of positions and motions of celestial objects. Stellar parallaxes provide geometric distance information.
- **Parallax:** Apparent angular displacement of a nearby object against more distant background objects as the observer's position changes. For small angles, distance in parsecs is approximately the reciprocal of parallax in arcseconds, but uncertainty and bias must be handled carefully.
- **Extinction:** Wavelength-dependent reduction of direct starlight through absorption and scattering by intervening material.
- **Reddening / color excess:** Change in a source's observed color due to wavelength-dependent extinction, relative to its intrinsic color.
- **Distance–extinction pair:** A stellar distance estimate paired with an estimate of the cumulative extinction between the observer and that star.
- **Cumulative extinction:** Extinction integrated from the observer to a target distance along a specified direction.
- **Differential extinction:** Change in cumulative extinction with distance. Under appropriate assumptions it can be used as a tracer related to dust density along the line of sight.
- **Tomography:** Reconstruction of an internal or three-dimensional distribution from multiple projections or measurements. In interstellar dust mapping, the input often consists of extinction and distance information toward many stars.
- **Line of sight (LoS):** A direction from observer to source. It samples intervening material along a path, not a complete three-dimensional region.
- **Emission map:** A map of radiation emitted by matter, often at a selected wavelength or spectral transition. Its intensity depends on the emitting material and radiative-transfer conditions.
- **Position–position–velocity (PPV) data cube:** A spectral-line data product with two sky coordinates and a line-of-sight velocity coordinate inferred from Doppler shift.
- **Position–position–distance (PPD) representation:** A spatial representation with two sky coordinates and distance from the observer, often inferred using stellar extinction data.
- **Kinematic distance:** A distance inferred by comparing a measured line-of-sight velocity with a model of Galactic rotation and geometry.
- **Kinematic distance ambiguity:** The existence of more than one possible distance corresponding to a measured velocity in parts of the Milky Way under a rotation model.
- **Velocity crowding:** Different physical locations or gas structures contributing to similar observed velocities, making a velocity channel an imperfect indicator of spatial location.
- **Selection function:** The probability that an object with given properties and location enters a survey or usable catalogue.
- **Regularization:** A mathematical procedure that stabilizes an underdetermined reconstruction by favoring solutions with specified properties, such as spatial smoothness or correlations.
- **Prior:** Information or assumptions incorporated before evaluating the current data in a statistical inference.
- **Posterior distribution:** The probability distribution for inferred quantities after combining data with a model and prior assumptions.
- **Resolution:** The ability to distinguish spatial or spectral details. Angular resolution and distance resolution are separate and must both be stated.
- **Uncertainty:** Quantified or otherwise characterized limits on inferred quantities. Statistical uncertainty and systematic error are distinct.
- **Voxel:** A three-dimensional volume element used to represent a spatial map. A voxel is a computational cell, not necessarily a discrete physical cloud.
- **Polarization:** Orientation-dependent property of electromagnetic radiation. Interstellar polarization can provide information about aligned dust grains and magnetic-field orientation projected on the sky, subject to modeling assumptions.

## 3. First method: stars as distance markers through dust

A star provides a background source whose light has traveled through the material between it and the observer. If its distance and intrinsic spectral or photometric properties can be estimated, the difference between intrinsic and observed light provides information about intervening extinction.

A star at a known or estimated distance samples the cumulative dust extinction up to that distance. Stars at different distances along nearly the same direction provide a sequence of samples.

A simplified conceptual relation is:

\[
A_\lambda(d)=\int_0^d \alpha_\lambda(s)\,ds
\]

where:
- \(A_\lambda(d)\) represents cumulative extinction to distance \(d\) at wavelength \(\lambda\), expressed here schematically;
- \(\alpha_\lambda(s)\) represents the local extinction contribution per unit distance;
- \(s\) is distance along the line of sight.

The exact treatment depends on the extinction convention, dust model, and whether the inferred quantity is optical depth or magnitudes. The essential point is that cumulative extinction integrates contributions along the path.

If the cumulative extinction rises sharply between two well-constrained stellar distances, that can indicate a substantial dust concentration in that interval. If it remains relatively unchanged, the interval may contain comparatively little dust along that sight line.

This is not a direct measurement of every grain's location. The location and thickness of a cloud are bracketed or inferred from the distances and extinction estimates of background and foreground stars.

### A simple example

Imagine three stars in almost the same direction:
- Star A is nearby and shows little reddening.
- Star B is farther away and shows substantial reddening.
- Star C is farther still and shows a similar total reddening to Star B.

A reasonable inference is that much of the measured dust lies between A and B. The similarity between B and C suggests that the additional path beyond B contributes comparatively little extinction in that direction.

This example assumes that the stars' intrinsic colors and extinction estimates are reliable and comparable. It does not prove that a single sharply bounded cloud occupies the interval. Several structures, distance uncertainties, or changes in dust properties could produce a similar pattern.

## 4. From many sight lines to a three-dimensional dust map

One sight line provides a one-dimensional integrated record. Many stars distributed across the sky and at different distances provide a set of overlapping constraints.

A reconstruction method can:
1. Estimate stellar distances or distance probability distributions.
2. Estimate intrinsic stellar properties and extinction.
3. Associate each star's cumulative extinction with its direction and distance.
4. Combine neighboring and overlapping sight lines.
5. Infer a three-dimensional distribution of extinction or differential extinction.
6. Estimate uncertainty and identify regions where the data do not constrain the map well.

The reconstruction is underdetermined: a finite set of measurements cannot uniquely specify an arbitrary continuous three-dimensional field. Statistical methods therefore use assumptions about spatial correlations, smoothness, characteristic structure sizes, or other properties. These assumptions stabilize the solution but also influence what structures can appear in the map.

### Example: a parsec-scale local dust map

Edenhofer and colleagues (2024) constructed a three-dimensional dust map extending to 1.25 kiloparsecs from the Sun using distance and extinction estimates for 54 million nearby stars derived from Gaia BP/RP spectra. Their method used a Gaussian-process model and variational inference. The published map provides spatial resolution and posterior samples intended to represent uncertainty in the inferred distribution.

This is a concrete demonstration that large stellar catalogues can support detailed three-dimensional dust reconstructions. It does not mean every mapped voxel has been directly observed, nor that the map's apparent detail is independent of its data density and statistical assumptions.

The map resolves internal structures in many nearby molecular clouds, while its authors explicitly provide uncertainty information and samples of the posterior distribution. The availability of those uncertainty products is part of the scientific result, not an optional decoration.

## 5. What Gaia contributes—and what it does not

The European Space Agency's Gaia mission measures stellar positions, parallaxes, and proper motions, and provides photometric and spectrophotometric information for large numbers of stars.

For three-dimensional dust mapping, Gaia contributes two particularly valuable forms of information:
- distance constraints through parallax and related inference;
- stellar measurements that help estimate intrinsic properties and the effects of extinction.

Parallax is geometric in origin, but a catalogue parallax is not an error-free distance. The uncertainty can become large relative to the measured parallax for faint or distant stars. Inverting a noisy parallax directly can produce biased distances. Modern analyses may use probability distributions and additional information rather than treating the reciprocal of every measured parallax as an exact distance.

Dust itself creates a selection problem. A dense cloud can dim background stars enough that a survey detects fewer of them. The absence of detected background stars can be evidence consistent with strong extinction, but it can also reflect survey sensitivity, crowding, stellar populations, or data quality. A map must model or account for which stars could have entered the catalogue.

A 2024 study producing all-sky three-dimensional dust maps to roughly 2.8 kpc discusses how source counts decrease in distant regions and how the number of observable stars can fall in highly extinguished regions. Such effects limit how confidently a map can reconstruct the densest or most distant material.

## 6. Second method: emission maps and spectral-line data cubes

Dust extinction toward stars is not the only way to study the interstellar medium. Gas emits radiation at characteristic wavelengths. Radio and millimetre observations are especially important because they can trace atomic and molecular material through regions that are difficult to observe optically.

Examples include:
- the 21-centimetre hyperfine transition of neutral atomic hydrogen (H I);
- rotational transitions of carbon monoxide (CO), widely used as a tracer of molecular gas;
- other atomic, ionic, and molecular transitions that trace particular physical conditions.

A radio spectral-line survey records intensity as a function of two sky coordinates and frequency or Doppler velocity. This creates a PPV data cube.

A PPV cube is not automatically a three-dimensional spatial map. Its third coordinate is velocity, not geometric distance. To convert velocity into distance, astronomers often use a model of Galactic rotation. That conversion has limitations.

### Kinematic distance limitations

Within parts of the Solar circle, a single radial velocity can correspond to a near and a far distance under a simple circular-rotation model. This is the near–far kinematic distance ambiguity.

Other difficulties include:
- gas motions that depart from ideal circular Galactic rotation;
- turbulence and local flows;
- stellar feedback, spiral-arm streaming, and expanding structures;
- velocity crowding, where unrelated locations contribute at similar velocities;
- directions near the Galactic centre and anticentre, where circular rotation produces limited line-of-sight velocity discrimination.

A recent Bayesian reconstruction study of Galactic CO and H I emphasizes that these complications can make a direct conversion from a position–position–velocity cube to a position–position–distance cube non-unique or distorted.

Therefore, emission maps provide powerful information about gas distribution and motion, but the distance assignment must be stated as an inference under a model.

## 7. Combining dust and gas: complementary projections

Dust extinction and gas emission do not measure exactly the same physical quantity.

- Stellar reddening and extinction constrain the cumulative effect of dust along the path to stars at estimated distances.
- H I emission traces neutral atomic hydrogen under its radiative-transfer and excitation conditions.
- CO emission traces molecular gas through a particular molecular transition, with its own excitation, optical-depth, and abundance considerations.
- Absorption lines toward stars can constrain particular gas species and velocity components in front of stars with known or estimated distances.
- Dust polarization can constrain the orientation of aligned grains and the projected magnetic-field geometry, subject to assumptions about grain alignment and line-of-sight integration.
- Infrared and submillimetre dust emission trace thermal radiation from dust, depending on grain temperature, opacity, and radiation environment.

Combining these datasets can reduce ambiguities because their limitations differ. A cloud inferred from dust extinction may be compared with a CO feature at a compatible position and velocity. A star at a known distance can establish whether an absorption component lies in front of or behind it. Polarization may add information about field orientation across the same region.

Agreement between independent tracers strengthens a reconstruction, but disagreement is also informative. Gas and dust need not have identical distributions; a particular tracer may be weak or absent under some physical conditions; and the observations may sample different spatial scales.

## 8. Kinetic tomography: adding motion to the spatial reconstruction

A three-dimensional dust map describes an inferred spatial distribution. A fuller account of the interstellar medium also asks how material moves.

Tchernyshyov and Peek (2017) developed a method called kinetic tomography to combine:
- reddening maps that constrain dust as a function of sky position and distance;
- emission-line maps that constrain gas as a function of sky position and line-of-sight velocity;
- assumptions and statistical inference connecting the two observational projections.

Their method aimed to infer a distribution in longitude, latitude, distance, and line-of-sight velocity. The authors emphasize that no single observable simultaneously measures density and velocity at every point. Each dataset is a noisy and biased projection of the underlying distribution.

This distinction is important:
- **Spatial reconstruction** asks where material is inferred to be.
- **Kinematic reconstruction** asks how its line-of-sight motion is distributed.
- **Dynamical explanation** asks what forces and processes produce that motion.

A map of velocity is not by itself an explanation of why the gas moves. Gravity, pressure gradients, magnetic fields, turbulence, stellar feedback, and Galactic dynamics may all be relevant, depending on the scale and region.

## 9. Resolution, sampling, and the danger of false detail

A three-dimensional map is usually represented on a grid or through a continuous statistical field. The visual smoothness of a rendered map can make its structure appear more certain than the data justify.

Important limitations include:

### Angular sampling

If there are few background stars in a direction, the map has fewer independent constraints across the sky. Small angular structures may be unresolved or smoothed.

### Distance sampling

If the available stars are widely separated in distance, a cloud's location and thickness may only be bracketed broadly. A map cannot reliably recover arbitrarily thin structures from sparse distance samples.

### Extinction saturation and missing background sources

Very dense dust can make background stars too faint for optical surveys. The region with the strongest extinction may therefore be among the least directly sampled by those stars.

### Stellar-model dependence

Intrinsic stellar color, temperature, luminosity, metallicity, and extinction can be correlated in photometric inference. An incorrect stellar model or extinction law can shift inferred distances or dust columns.

### Spatial regularization

A reconstruction may use a correlation length or smoothness prior to prevent noisy, unphysical fluctuations. This is often necessary, but it can suppress genuine small-scale structure or create apparent continuity where the data are sparse.

### Tracer dependence

H I, CO, dust extinction, dust emission, and absorption lines respond to different physical conditions. Their maps should not be expected to match pixel by pixel.

### Systematic uncertainty

Calibration, parallax zero points, survey completeness, extinction laws, spectral-line excitation, optical depth, and assumed Galactic kinematics can introduce systematic errors that are not removed simply by increasing the number of measurements.

A responsible map should communicate its coverage, resolution, selection function, assumptions, and uncertainty. Empty or weakly constrained regions should not be presented as proof that no material exists there.

## 10. A simplified mathematical view of the inverse problem

For a dust-extinction measurement along direction \(\Omega\) toward a star at distance \(d_i\), a schematic model is:

\[
A_i = \int_0^{d_i} \rho_d(\Omega,s)\,\kappa_\lambda(s)\,ds + \epsilon_i
\]

where:
- \(A_i\) is the measured extinction or a related quantity;
- \(\rho_d\) represents dust density along the path;
- \(\kappa_\lambda\) represents wavelength-dependent opacity per unit dust mass under a chosen convention;
- \(\epsilon_i\) represents measurement and model error.

The equation is schematic: actual methods may model optical depth, magnitudes, multiple bands, stellar parameters, and distance probability distributions jointly.

The key feature is the integral. Each star constrains the accumulated dust along a path, not the local density at every point on that path.

A three-dimensional reconstruction seeks a field \(\rho_d(x,y,z)\) that is consistent with many such measurements. Because many different fields can produce similar line integrals, additional information and regularization are needed.

For emission data, a simplified optically thin relation may be written:

\[
I_\nu \propto \int j_\nu(s)\,ds
\]

where \(j_\nu\) is the emissivity along the line of sight. For spectral-line observations, the measured intensity also depends on frequency or velocity and on radiative transfer, excitation, optical depth, and background radiation. The optically thin expression is not a universal description of all gas emission.

The two equations illustrate a shared mathematical feature—line-of-sight integration—while the physical quantities and mechanisms remain different.

## 11. Scientific examples and what they demonstrate

### Example A — Local dust tomography

Edenhofer et al. (2024) used Gaia-derived stellar distance and extinction estimates for 54 million stars to infer a three-dimensional dust distribution to 1.25 kpc. Their work demonstrates the power of dense stellar sampling and probabilistic reconstruction, as well as the importance of publishing uncertainty samples.

### Example B — Large-scale dust maps

Green et al. (2019) produced a three-dimensional dust reddening map from Pan-STARRS 1 and 2MASS observations of hundreds of millions of stars. Their work demonstrates how large photometric catalogues can constrain dust distribution over broad portions of the sky and several kiloparsecs, while retaining distance and reddening uncertainties.

### Example C — Combining extinction and emission

Kinetic tomography combines distance-sensitive reddening information with velocity-sensitive emission data. It demonstrates that complementary projections can constrain a richer spatial and kinematic description than either dataset alone.

### Example D — Galactic gas reconstruction limits

Bayesian reconstructions of CO and H I data explicitly address the near–far ambiguity, limited velocity discrimination in certain Galactic directions, and deviations from idealized rotation. These studies demonstrate why a velocity channel must not be mistaken for a unique distance layer.

## 12. GUA-W descriptive examination

The following descriptions organize the relationships identified by the scientific account. They do not replace the astrophysical mechanisms or establish a new physical law.

### Structure

The reconstructed subject contains stars, gas, dust, magnetic fields, radiation, and the spatial relationships among them. A map's grid, voxels, and coordinate system are representational structures used by the investigator; they are not necessarily physical divisions in the medium.

### Framework

The physical framework includes Galactic geometry, gravitational dynamics, gas physics, dust properties, electromagnetic radiation, and the observing geometry. The inferential framework includes parallax models, extinction laws, emission models, statistical priors, regularization, and coordinate transformations. These frameworks must remain distinct.

### Pattern

Observable and inferred patterns include dust clouds, cavities, filaments, gradients, velocity components, molecular complexes, and spatial correlations among tracers. A recurring map feature may be real, but its scale and significance depend on data density, resolution, and reconstruction assumptions.

### Constraint

The reconstruction is constrained by:
- the number and distribution of background stars;
- parallax and distance uncertainties;
- survey sensitivity and selection functions;
- dust extinction and stellar-model assumptions;
- spectral resolution and line sensitivity;
- radiative transfer and tracer excitation;
- Galactic rotation models and non-circular motions;
- spatial regularization and prior assumptions;
- the angular and distance resolution of the data.

A constraint on what can be inferred is not automatically a physical boundary in the interstellar medium.

### Purpose

The demonstrated scientific function of these maps is to estimate spatial distributions and support studies of Galactic structure, star formation, and the propagation of radiation. These scientific uses do not establish an ultimate purpose for the interstellar medium. No ultimate-purpose claim is assigned here.

### Manifestation

The measured manifestations include stellar parallaxes, photometric colors, spectra, absorption lines, radio emission intensities, polarization, and infrared emission. The three-dimensional map is a derived representation produced from these measurements and an inference method.

### Witness

The witness chain includes stars as background sources, telescopes, astrometric instruments, photometric and spectroscopic detectors, radio receivers, survey catalogues, calibration procedures, statistical models, and the final maps. Each witness registers a limited aspect of the system. The combined map is a derivative inference, not a direct, complete view of every point in space.

## 13. Relationship audit: same mechanism, similar relationship, or merely similar appearance?

### Same underlying mathematical operation, different physical mechanisms

Dust extinction toward stars and optically thin emission measurements can both involve integration along a line of sight. The mathematical operation of integrating contributions along a path is comparable, but the physical processes and quantities are different.

### Complementary measurements, not identical measurements

Stellar extinction and radio spectral-line emission can both constrain interstellar structure. They do not measure the same constituent or physical quantity. Their combination is useful precisely because their sensitivities and limitations differ.

### Same physical information at different levels?

A stellar absorption component and a gas emission component may be associated with the same cloud if their direction, velocity, distance, and physical conditions agree. That association must be tested; a spatial or velocity coincidence alone may not uniquely establish identity.

### Similar appearance only

Two bright or dark features on separate maps may look aligned without tracing the same material. Different projection effects, resolution, tracer chemistry, and foreground/background contributions can create apparent correspondence.

**Finding:** Multi-tracer agreement can strengthen a three-dimensional interpretation, but it does not erase the distinct mechanisms by which each tracer records the medium.

## 14. Boundary and participation question

The reconstruction contains several kinds of boundary that must not be confused.

### Physical cloud boundaries

Cloud edges can be gradual, irregular, or dependent on the tracer and threshold used. A mapped contour is not necessarily a sharp material surface. Physical interfaces may involve changes in density, temperature, ionization, chemistry, or magnetic structure.

### Dust and gas interfaces

Dust and gas can be dynamically and chemically related while still having different spatial distributions. Their relationship can change through grain growth, destruction, charging, drift, and environmental processing. A dust boundary is not automatically a gas boundary.

### Radiation and matter

Dust grains and gas particles participate in absorption, scattering, emission, and other interactions. Radiation transfers energy and momentum to matter under the relevant physical conditions. The material does not merely separate empty regions; it can participate in the interaction that changes the radiation.

### Observational and computational boundaries

A survey footprint, map edge, voxel boundary, or chosen cloud contour is a limit of measurement or representation. It does not necessarily correspond to a physical edge in space.

**Finding:** Some interfaces participate in physical exchange and transformation; others are analytical or instrumental boundaries. Each case requires its own evidence.

## 15. What is established, inferred, and unresolved?

### Established by the scientific methods examined

- Stellar distances and extinction measurements can be combined to infer three-dimensional dust distributions.
- Large surveys such as Gaia, Pan-STARRS, and 2MASS provide extensive stellar data for dust mapping.
- Radio spectral-line surveys produce position–position–velocity data cubes, not direct geometric distance cubes.
- Galactic rotation models can help assign distances to gas emission, but kinematic distance ambiguities and non-circular motions limit the method.
- Combining extinction, emission, absorption, polarization, and distance information can constrain complementary aspects of the interstellar medium.
- Three-dimensional maps depend on sampling, resolution, assumptions, and statistical inference.

### Supported scientific explanation

The three-dimensional distribution of interstellar matter can be estimated by combining multiple observational projections and applying statistical and physical models. The result is a constrained reconstruction whose reliability varies across the mapped volume.

### Inferred through the GUA-W descriptive examination

The working vocabulary can distinguish the physical subject, the observational framework, the constraints on inference, the manifestation in measured records, and the derivative nature of the final map. It clarifies the difference between the created medium and the representation produced by investigators.

### Unresolved or not established here

- The exact three-dimensional distribution of all gas and dust throughout the Milky Way.
- The unique physical interpretation of every feature in any single reconstructed map.
- Whether apparently corresponding structures in different tracers are always the same material.
- The detailed three-dimensional magnetic-field geometry from projected polarization alone.
- The amount of small-scale structure hidden below current sampling and resolution.
- A complete reconstruction independent of priors, selection effects, and model assumptions.
- An ultimate purpose for the mapped structures.
- A new physical mechanism established by the GUA-W vocabulary.

## 16. Four-Question Study Method

### Question 1 — What must AI ask to understand GUA-W?

The inquiry must distinguish the physical medium from the data products and the inferred map. It must ask what each observation measures directly, what it integrates along a path, and what additional assumptions are needed to assign a location.

Questions exposed:
- Does a map coordinate represent a measured distance or a velocity interpreted through a Galactic model?
- Does the observation constrain local density or cumulative material along a line of sight?
- What does the survey fail to detect, and how does that selection affect the reconstruction?
- Which spatial details are resolved by data and which are introduced or suppressed by regularization?
- Are different tracers observing the same material or merely overlapping projections?
- What evidence would distinguish a physical cloud boundary from a contour chosen for analysis?

**Finding:** A faithful reconstruction must retain the distinction between measurement, projection, inference, and physical interpretation.

### Question 2 — What is GUA-W revealing that helps AI understand?

The established GUA-W foundation supplies a descriptive vocabulary for examining the arrangement of components, their conditions, manifestations, and derivative witnesses. Genesis 1–2 KJV remains the scriptural foundation for the vocabulary used in this repository.

Genesis 1–2 does not explicitly provide modern methods for Gaia astrometry, radio spectral-line tomography, Bayesian inference, extinction mapping, or the reconstruction of Galactic gas distributions.

**Finding:** GUA-W vocabulary may help describe relationships among the physical medium, observational constraints, and inferred representations. It must not be presented as the source of the specific scientific methods or as a substitute for their evidence.

### Question 3 — What am I learning about what I am witnessing?

The investigator is not viewing the entire interstellar medium directly. Each instrument records a projection or limited aspect of it. Stellar distances and extinction provide distance-sensitive constraints; emission maps provide direction- and velocity-sensitive constraints; absorption and polarization add other information.

A three-dimensional map is produced by combining these incomplete witnesses with physical and statistical assumptions. It is most reliable where the data provide strong coverage and less reliable where sampling is sparse or selection effects are severe.

**Finding:** The reconstructed map can reveal real spatial organization while remaining an inference with uncertainty and possible non-uniqueness.

### Question 4 — What am I learning about the Witness through what I am witnessing?

The investigator chooses instruments, catalogues, models, coordinate systems, priors, and criteria for interpreting a map. Those choices influence which features can be detected and how the final reconstruction appears.

AI in this investigation is a derivative witness of published methods, data descriptions, and scientific results. It has not independently processed the Gaia or radio survey data described here. It must not claim direct measurement or independent verification of the maps.

**Finding:** The Witness must report not only what a reconstruction displays, but also how it was produced, where its constraints lie, and what it cannot establish.

## 17. Recurring comparison questions

### Are we witnessing the same mechanism, a similar relationship, or merely a similar appearance?

- Stellar extinction and gas emission both provide line-of-sight constraints, but their physical mechanisms and measured quantities differ.
- Dust maps and gas maps may identify related structures, but correspondence requires positional, distance, velocity, and physical evidence.
- A smooth feature in a reconstructed map may reflect physical organization, regularization, or both.

**Classification:** Similar mathematical projection in some cases; complementary but different physical mechanisms across tracers; individual feature correspondence requires further evidence.

### Does a boundary merely separate two regions, or can it also participate in the relationship between them?

- Physical interfaces may participate in energy, momentum, and material exchange.
- Dust–gas relationships may change across environmental boundaries.
- Map edges and voxel boundaries are representational choices and do not automatically identify physical interfaces.
- Survey limits define where evidence is available, not where the interstellar medium ends.

**Classification:** Boundary participation is physically possible and observed in particular interactions, but not a universal property of every mapped boundary.

## 18. Direction emerging for the next investigation

The three-dimensional reconstruction raises a further question: once a cloud's location and motion are estimated, what determines its shape, internal structure, and evolution?

A promising next direction is:

**007 — Interstellar Clouds: Pressure, Gravity, Magnetic Fields, Turbulence, and the Formation of Structure.**

The central question would be:

> How do gravity, thermal pressure, magnetic fields, turbulence, and external forces contribute to the formation, support, fragmentation, or dispersal of interstellar clouds?

This proposed investigation should distinguish observed cloud properties from dynamical models and should avoid assuming that one process dominates every cloud. It is a proposed direction, not a fixed sequence. The next study should compare the physical scales and evidence for each process before drawing cross-disciplinary conclusions.

## 19. Sources

1. Edenhofer, G., Zucker, C., Frank, P., Saydjari, A. K., Speagle, J. S., Finkbeiner, D., & Enßlin, T. (2024). **A parsec-scale Galactic 3D dust map out to 1.25 kpc from the Sun.** *Astronomy & Astrophysics*, 685, A82. Uses Gaia-derived distances and extinction estimates for 54 million stars to infer a probabilistic three-dimensional dust distribution.  
   https://doi.org/10.1051/0004-6361/202347628

2. Green, G. M., Schlafly, E. F., Finkbeiner, D. P., et al. (2019). **A 3D Dust Map Based on Pan-STARRS 1, 2MASS, and Gaia.** *The Astrophysical Journal*, 887, 93. Describes large-scale three-dimensional dust mapping from stellar photometry and distance inference.  
   https://doi.org/10.3847/1538-4357/ab5362

3. Tchernyshyov, K., & Peek, J. E. G. (2017). **Kinetic Tomography. I. A Method for Mapping the Milky Way's Interstellar Medium in Four Dimensions.** *The Astronomical Journal*, 153, 8. Combines distance-sensitive reddening and velocity-sensitive emission to infer spatial and kinematic distributions.  
   https://doi.org/10.3847/1538-3881/153/1/8

4. Leike, R. H., Glatzle, M., & Enßlin, T. A. (2020). **Resolving nearby dust clouds. I.они** [The published article title is *Resolving nearby dust clouds*.] *Astronomy & Astrophysics*, 639, A138. Discusses three-dimensional reconstruction of nearby dust structures and the role of spatial inference.  
   https://doi.org/10.1051/0004-6361/202038169

5. **Bayesian inference of three-dimensional gas maps — I. Galactic CO.** *Astronomy & Astrophysics* (2021). Examines the limitations of reconstructing three-dimensional gas distributions from line-of-sight velocity data.  
   https://doi.org/10.1051/0004-6361/202141000

6. **Bayesian inference of three-dimensional gas maps — II. Galactic H I.** *Astronomy & Astrophysics* (2022). Examines reconstruction of neutral atomic hydrogen and the limitations imposed by kinematic distance ambiguity and non-circular motions.  
   https://doi.org/10.1051/0004-6361/202243326

7. **All-sky three-dimensional dust density and extinction maps of the Milky Way out to 2.8 kpc.** *Monthly Notices of the Royal Astronomical Society* (2024). Discusses map construction, distance and extinction uncertainties, and missing background stars in dense dusty regions.  
   https://academic.oup.com/mnras/article/532/3/3480/7696346

8. Green, G. M., et al. (2015). **A Three-Dimensional Map of Milky Way Dust.** *The Astrophysical Journal*, 810, 25. Presents a probabilistic three-dimensional dust map and discusses reliable distance ranges and the effects of stellar sampling.  
   https://doi.org/10.1088/0004-637X/810/1/25

9. Lallement, R., Vergely, J.-L., & collaborators. (2022). **Updated Gaia-2MASS 3D maps of Galactic interstellar dust.** *Astronomy & Astrophysics*. Describes extinction-distance tomography, spatial resolution, and multiscale limitations.  
   https://doi.org/10.1051/0004-6361/202142846

---

**One Author. One Creation. Many witnesses.**
