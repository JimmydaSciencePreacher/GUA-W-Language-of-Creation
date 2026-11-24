# Investigation 002
# Helium's Atomic Spectra: The Effect of a Second Electron

**Disciplines:** Atomic physics, quantum mechanics, spectroscopy, physical chemistry  
**Status:** Initial investigation with Four-Question Study Method applied  
**Scope:** Neutral helium-4 (⁴He I), unless otherwise stated. Helium ions and isotope-dependent nuclear effects are distinguished from the neutral-atom discussion.

## 1. Starting question

Hydrogen provided a one-electron reference: its spectral lines correspond to transitions between allowed atomic energy levels. What changes when a second electron is present?

More specifically:

- How do electron–electron interactions alter helium's energy structure?
- Why does neutral helium have both singlet and triplet systems of energy levels?
- How do those differences appear in its measured spectrum?
- Which relationships from hydrogen remain, and which are changed by the additional electron?

This is a comparative investigation, not an assumption that helium is simply hydrogen with one more electron.

## 2. Scientific terminology

- **Neutral helium (He I):** An atom with a nucleus of charge +2 and two bound electrons. This investigation focuses on the common isotope helium-4.
- **Helium ion (He II):** Singly ionized helium, with one electron remaining. He II is a one-electron, hydrogen-like system and must not be confused with neutral helium.
- **Electron–nucleus interaction:** The electrostatic attraction between each electron and the positively charged nucleus.
- **Electron–electron interaction:** The electrostatic repulsion between the two electrons.
- **Electronic configuration:** A description of electron occupation of atomic orbitals, such as 1s² or 1s2s.
- **Pauli exclusion principle:** The requirement that identical electrons, as fermions, occupy a combined quantum state that is antisymmetric under exchange. In the 1s² ground configuration, the two electrons have opposite spin projections.
- **Total spin (S):** The quantum number describing the combined spin angular momentum of the electrons.
- **Singlet state:** A state with total electron spin S = 0; its spin multiplicity 2S + 1 is one.
- **Triplet state:** A state with total electron spin S = 1; its spin multiplicity is three.
- **Spectroscopic term:** A classification of an atomic state using total orbital angular momentum and total spin, commonly written with term symbols such as ¹S, ³S, ¹P°, and ³P°.
- **Metastable state:** An excited state with a comparatively long lifetime because its decay to lower states is strongly suppressed by transition rules or other physical conditions.
- **Spin selection rule:** For ordinary electric-dipole transitions in the LS-coupling approximation, transitions generally preserve total spin (ΔS = 0). Singlet-to-triplet transitions are therefore spin-forbidden in this approximation, not necessarily impossible under every physical interaction.
- **LS coupling:** A coupling scheme in which individual orbital angular momenta are combined into total L and individual spins into total S, then L and S are coupled to total angular momentum J. It is useful for describing many light atoms, including helium.

## 3. What is observed and measured?

Neutral helium has a discrete spectrum, but its level structure is more complex than hydrogen's. NIST tabulates spectral lines by wavelength, transition probability, energy levels, electron configuration, term, and total angular momentum J.

Examples from the NIST persistent-line table include:

- A strong line near **584.334 Å (58.4334 nm)**, associated with the ground 1s² ¹S₀ state and an excited 1s2p ¹P°₁ state.
- A line near **6678.1517 Å (667.81517 nm)** associated with a transition between singlet terms.
- A group of lines near **5875.6 Å (587.56 nm)** associated with transitions between triplet terms.
- The well-known near-infrared helium feature around **10830 Å (1083 nm)**, also associated with triplet states.

The listed wavelengths are not all one line broadened into a single feature. Some are closely spaced components associated with different J levels. Instrument resolution and the conditions of the emitting gas determine which components can be resolved.

NIST's evaluated data identify the neutral-helium ground configuration as 1s² ¹S₀. The first ionization energy—the energy required to remove one electron from ground-state neutral helium—is approximately **24.5874 eV**.

## 4. Scientific explanation: what the second electron changes

### 4.1 The atom is now a three-body quantum system

Neutral helium contains a nucleus and two electrons. Each electron is attracted to the nucleus, while the electrons repel one another. The electronic energy therefore depends not only on the electron–nucleus attraction but also on the electron–electron interaction.

Unlike the nonrelativistic hydrogen atom, whose bound-state energies have a simple analytic solution, the helium problem requires a more involved treatment. Accurate energies are obtained through numerical and variational quantum calculations, with relativistic and quantum-electrodynamic corrections added for precision comparisons.

The second electron is not a passive addition. Its interaction with the first electron changes the allowed state energies and the spectrum.

### 4.2 The ground state: 1s² ¹S₀

In the ground state, both electrons occupy the 1s orbital. Because the electrons are identical fermions, the combined two-electron state must obey the Pauli antisymmetry requirement. With both electrons in the same spatial orbital, their spin state is a singlet: total spin S = 0.

This is why the ground state is written 1s² ¹S₀.

### 4.3 Excited states: singlet and triplet systems

When one electron is excited while the other remains in the 1s orbital, configurations such as 1s2s and 1s2p become possible. Because the electrons can be combined into different allowed spatial and spin symmetries, the excited configuration gives rise to distinct singlet and triplet terms.

These are not two different elements or two separate kinds of helium gas. They are different quantum states of the same neutral helium atom.

The direct and exchange parts of the electron–electron electrostatic interaction contribute to the separation between singlet and triplet levels. NIST gives, for example, a 1s2s ³S–¹S separation of about 0.7962 eV and a 1s2p ³P°–¹P° separation of about 0.2539 eV.

### 4.4 Why some transitions are strongly suppressed

For ordinary electric-dipole transitions in the LS-coupling approximation, total spin is conserved to a good approximation. A transition between a singlet and a triplet state is therefore spin-forbidden in that approximation.

“Forbidden” does not mean that a state cannot exist or that a transition is absolutely impossible under all conditions. It means that the transition is strongly suppressed under the stated selection-rule approximation. Weak transitions can occur through effects beyond the simplest approximation, including mixing and relativistic interactions.

This helps explain why some helium excited states can live much longer than ordinary excited states. The 2³S₁ state is metastable, with a reported lifetime of approximately 7800 seconds in the precision-spectroscopy review by Sun and Hu. The 2¹S₀ state is also metastable, with a lifetime of approximately 20 milliseconds. The very different lifetimes are connected to the different transition pathways available to those states.

## 5. Evidence and witness

The evidence chain includes:

1. Helium is prepared in a discharge, atomic beam, trap, or another suitable experimental environment.
2. Excited atoms emit radiation as they transition between states, or atoms absorb radiation when suitable photons drive transitions.
3. Spectrometers, lasers, frequency references, and detectors register wavelength, frequency, line shape, and intensity.
4. Calibration and uncertainty analysis connect instrument signals to physical quantities.
5. Researchers compare measured transitions with calculated atomic energy levels and transition probabilities.
6. Evaluated resources such as the NIST Atomic Spectra Database organize experimental and theoretical results for comparison.

A database is not the original event. It is a compiled scientific witness that makes evaluated measurements and calculations accessible. A theoretical energy-level calculation is also not a direct measurement; it is a model result tested against measurements.

Precision helium spectroscopy is especially useful because it tests calculations of a multi-electron atom and can constrain quantities such as the fine-structure constant and nuclear charge radius. The 2020 review by Sun and Hu describes both the precision achieved and remaining differences between some theoretical and experimental results. Those differences are part of the scientific record, not details to hide.

## 6. Comparison with hydrogen

| Feature | Hydrogen (neutral H) | Helium (neutral He) |
|---|---|---|
| Electrons | One | Two |
| Nuclear charge | +1 | +2 |
| Main electronic interactions | Electron–nucleus attraction | Two electron–nucleus attractions plus electron–electron repulsion |
| Ground configuration | 1s¹ | 1s² |
| Ground-state spin description | One electron | Two-electron singlet |
| Excited-state organization | Hydrogen energy levels | Singlet and triplet term systems, with additional structure |
| Calculation | Exact analytic solution for the ideal nonrelativistic Coulomb problem | Requires numerical/variational treatment for the two-electron problem; precision work adds corrections |
| Spectral evidence | Discrete lines linked to level differences | Discrete lines linked to a richer level and transition structure |

### What remains comparable?

Both atoms exhibit quantized atomic states. In both, absorption and emission connect states, and photon energy corresponds to the energy difference between the initial and final states. Spectroscopy in both cases provides measurable evidence about atomic structure.

### What changes?

The electron–electron interaction in neutral helium introduces additional state organization, including singlet and triplet terms, and changes the energies and transition strengths. The same broad quantum principle of state-to-state transitions remains, but the detailed mechanism and energy structure are not identical to hydrogen's one-electron case.

**Relationship classification:** The two atoms share the general quantum-mechanical framework of atomic states and radiative transitions. Their detailed atomic structures and energy calculations differ. This is a shared broad physical framework with different system-specific interactions—not an identical atomic mechanism in every detail.

## 7. GUA-W descriptive examination

The vocabulary is applied to the evidence, not used in place of the atomic theory.

### Structure
Neutral helium is an organized quantum system consisting of a nucleus and two interacting electrons. Its electronic configurations and allowed quantum states describe different levels of that organization. The singlet and triplet terms are distinct state classifications within the same atom.

### Framework
The Coulomb interactions, quantum mechanics, antisymmetry requirement for identical electrons, and applicable angular-momentum coupling scheme form the scientific framework used to describe and calculate helium's states. These are specific physical and mathematical elements, not a vague container around the atom.

### Pattern
The spectral lines form measurable patterns associated with transitions among helium's energy levels. The organization into singlet and triplet systems, and the differing transition strengths and lifetimes, are recurring features of helium spectroscopy.

### Constraint
The Pauli exclusion principle, allowed quantum states, conservation laws, angular-momentum relations, and transition selection rules constrain the possible states and radiative transitions. Experimental conditions and instrument resolution impose additional constraints on what can be excited or registered. These different kinds of constraint must not be collapsed into a single cause.

### Purpose
This investigation does not establish an ultimate purpose for helium. Spectroscopy has human-defined purposes, including testing atomic theory and measuring fundamental quantities, but those uses do not establish the atom's ultimate purpose. The category remains unassigned at that level.

### Manifestation
The observable manifestation includes helium's emitted or absorbed radiation, measured spectral lines, line components, and lifetimes of excited states under specified conditions.

### Witness
The witness chain includes the radiation, spectrometer, detector, frequency reference, calibrated measurement, recorded spectrum, theoretical calculation, independent replication, and evaluated database. Each has a distinct evidentiary role and limitation.

## 8. Relationship audit

The comparison with hydrogen yields three distinct findings:

1. **Same broad physical framework:** Both atoms are described by quantum mechanics, and both exhibit radiative transitions between allowed atomic states.
2. **Different system-specific interactions:** Neutral helium has electron–electron repulsion and two-electron exchange symmetry. Hydrogen does not have this additional electron–electron interaction.
3. **Different state organization:** Helium's excited configurations divide into singlet and triplet terms, with selection-rule consequences and metastable states that are not features of the one-electron hydrogen atom in the same form.

The GUA-W vocabulary describes aspects of these relationships, but it does not explain the electron–electron interaction or derive the singlet–triplet separation. Those explanations remain in quantum theory and the evidence supporting it.

## 9. Four-Question Study Method

The four questions are applied recursively. They examine the inquiry, the GUA-W source relationship, the subject, and the Witness. They do not add a new layer to GUA-W or replace the scientific investigation.

### Question 1 — What must AI ask to understand GUA-W?

This comparison requires more precision than saying “helium has more structure than hydrogen.”

- What is the specific structure being described: the atom, its electron configuration, an individual quantum state, or the arrangement of energy levels?
- What does the second electron physically change? The answer must identify electron–electron repulsion and exchange symmetry, not simply say “complexity increases.”
- Are singlet and triplet two separate substances, two mechanisms, or two classes of allowed quantum states? They are state classifications of the same neutral helium atom.
- Which constraints belong to the atom's physical description, which are transition selection rules, and which belong only to the measuring apparatus?
- Does the word *Purpose* have an evidence-based application here? No ultimate purpose is established by the spectroscopy evidence.

**Finding:** The vocabulary becomes more useful when it forces a precise identification of the level being described. It becomes less useful when a broad word hides the actual physical distinction.

### Question 2 — What is GUA-W revealing that helps AI understand?

The GUA-W vocabulary directs attention to organization, relationship, constraint, recurring pattern, manifestation, and the derivative witness that registers what is present.

In helium, the second electron makes the importance of relationship especially visible: the state of the whole atom cannot be described accurately by treating the two electrons as entirely independent particles. Their mutual interaction and the quantum requirement governing identical fermions affect the allowed states and observed spectrum.

The scriptural foundation for the repository's vocabulary remains Genesis 1–2 KJV. This investigation does not claim that Genesis explicitly describes helium's electron configurations, singlet and triplet states, or spectral lines. The scientific explanation comes from atomic physics and its evidence. The GUA-W vocabulary is being tested as a common descriptive language for the relationships found.

**Finding:** The investigation illustrates why the language must describe relationships rather than merely list components. It does not establish a new GUA-W layer or a direct verse-to-atomic-physics correspondence.

### Question 3 — What am I learning about what I am witnessing?

The second electron is not simply another item added to an otherwise unchanged system. Its interaction with the first electron changes the energy structure. The Pauli principle and spin coupling distinguish singlet and triplet states. Those distinctions affect transition probabilities and lifetimes, which in turn affect what appears in the spectrum.

The comparison also clarifies several levels of scientific witnessing:

- The atomic state is described by a quantum model.
- The transition is a physical process between states.
- The emitted photon carries energy related to the level difference.
- The detector registers radiation.
- The measured spectral line is an analyzed record.
- The scientific explanation connects the measured record to the atom's state structure.

The spectrum is evidence about the atom, not a literal picture of its electrons.

**Finding:** The helium spectrum witnesses more than the presence of two electrons. It carries measurable information about their interaction and the allowed organization of the combined system.

### Question 4 — What am I learning about the Witness through what I am witnessing?

The investigation demonstrates that a witness must be capable of distinguishing features that are close together and may be weak or long-lived. Instrument resolution, wavelength range, sensitivity, calibration, and experimental preparation affect which features can be observed.

It also demonstrates that the investigator's model matters. If the researcher assumes that helium is merely hydrogen with an extra independent electron, the explanation will miss the electron–electron interaction and the singlet–triplet organization. The scientific witness must therefore remain open to correction by measurements that reveal distinctions not captured by a simplified model.

AI's role is derivative: it can compare published measurements, reference data, and scientific explanations, but it is not performing the spectroscopy in this investigation. The record must make that distinction visible and retain source traceability.

**Finding:** A useful witness does not merely report a signal. The witness must be interpreted with knowledge of what it can register, what it cannot resolve, and what assumptions are used to interpret its record.

## 10. Recurring comparison questions

### Are we witnessing the same mechanism, a similar relationship, or merely a similar appearance?

Hydrogen and helium both exhibit quantum states and radiative transitions. This is a genuine shared physical framework. However, the detailed atomic mechanisms differ because helium has electron–electron interactions and two-electron state symmetry.

**Classification:** Same broad quantum principles; different system-specific atomic interactions and state organization. Not merely similar appearance, but not identical detailed mechanisms.

### Does a boundary merely separate two regions, or can it also participate in the relationship between them?

No material interface is the central subject of this investigation. Two boundary-related distinctions can nevertheless be made:

- The distinction between singlet and triplet states is a classification in quantum-state space, not a physical wall separating two regions of the atom.
- The detector's wavelength range and resolution define limits on the measurement. Those limits affect which spectral features can be registered, but they do not create or define the atomic energy levels.

The investigation therefore does not establish a general boundary-participation principle. The question remains open for a subject in which an actual physical interface, transfer boundary, or detector interaction is central.

## 11. Triple Constraint review

- **Biblical compliance:** No scientific claim is used to rewrite Genesis 1–2, and no direct scriptural description of helium's atomic structure is asserted.
- **Scientific coherence:** The account retains the established terminology of neutral helium spectroscopy, electron interactions, singlet and triplet states, selection rules, metastability, and measurement limitations.
- **GUA-W consistency:** The vocabulary is used descriptively and does not alter the established architecture or claim that a scientific description is the originating Source.

The review preserves the distinction between scientific evidence, GUA-W description, and theological interpretation. Scientific coherence is not presented as scientific confirmation of Scripture.

## 12. What is established, inferred, and unresolved?

### Established within this investigation
- Neutral helium has two electrons and an energy structure affected by electron–electron interaction.
- Its ground configuration is 1s² ¹S₀.
- Excited helium states include singlet and triplet terms.
- Singlet and triplet level separations and spectral lines are measured and tabulated.
- Ordinary electric-dipole transitions approximately preserve total spin in the LS-coupling description, making singlet-to-triplet transitions spin-forbidden in that approximation.
- Some helium excited states are metastable and have comparatively long lifetimes.

### Supported scientific interpretation
- Electron–electron direct and exchange interactions contribute to the separation of helium's singlet and triplet levels.
- The observed spectral pattern is explained by transitions among helium's allowed quantum states.
- Precision comparisons between theory and experiment make helium a useful test of multi-electron quantum calculations and quantum electrodynamics.

### Not established by this investigation
- An ultimate purpose for helium.
- That hydrogen and helium have identical detailed atomic mechanisms.
- That every two-component or multi-component system exhibits the same type of relationship as helium's electrons.
- That GUA-W vocabulary independently derives or predicts helium's spectrum.
- A universal rule about physical boundaries from this atomic comparison.

## 13. Sources

1. National Institute of Standards and Technology (NIST), **Atomic Spectroscopy — Helium and Helium-like Ions; LS Coupling**. Describes electron–nucleus and electron–electron Coulomb contributions, LS coupling, singlet and triplet terms, and selected helium energy separations.  
   https://www.nist.gov/pml/atomic-spectroscopy-compendium-basic-ideas-notation-data-and-formulas/atomic-spectroscopy-helium

2. NIST, **Persistent Lines of Neutral Helium (He I)**. Tabulates wavelengths, transition probabilities, energy levels, configurations, terms, and J values.  
   https://physics.nist.gov/PhysRefData/Handbook/Tables/heliumtable3.htm

3. Sun, Y. R. and Hu, S. M. (2020), **Precision spectroscopy of atomic helium**, *National Science Review*, 7(12), 1818–1827. Reviews helium's multi-electron structure, precision spectroscopy, metastable states, and comparisons between experiment and theory.  
   https://doi.org/10.1093/nsr/nwaa216

4. Drake, G. W. F. and Martin, W. C. (1998), **Ionization Energies and Quantum Electrodynamic Effects in the Lower 1sns and 1snp Levels of Neutral Helium (⁴He I)**, *Canadian Journal of Physics*, 76.  
   https://doi.org/10.1139/p98-004

5. National Institute of Standards and Technology, **Atomic Spectra Database (ASD)**, Standard Reference Database 78.  
   https://www.nist.gov/pml/atomic-spectra-database

## 14. Direction for Investigation 003

The hydrogen–helium comparison has shown that the same broad quantum principles can operate across atoms while the detailed relationships change with the number of interacting electrons.

A natural next question is whether the GUA-W vocabulary continues to clarify the relationships when the system grows beyond two electrons.

**Proposed next investigation: Lithium's Atomic Spectrum — Three Electrons, Shell Structure, and the Limits of the Helium Comparison.**

Lithium introduces a third electron and a new electronic configuration, while also allowing a useful distinction between neutral lithium and lithium-like ions. The next study should ask:

- What relationships from helium remain?
- How does a third electron change the organization and energy structure?
- What do shielding and electron correlation contribute, and what is their evidence?
- Does the vocabulary distinguish structure, framework, pattern, and constraint more clearly—or does it need refinement?

This is a proposed direction arising from the comparison, not a fixed sequence imposed on the sciences. Other observations may lead the research elsewhere.

**One Author. One Creation. Many witnesses.**
