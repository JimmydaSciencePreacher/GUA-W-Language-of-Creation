# Investigation 037 — Interacting Processes, Feedback, Emergence, and the Limits of Single-Cause Explanation

**Primary disciplines:** Systems science, ecology, causal inference, dynamical systems, control theory, network science, statistical physics, and complex-systems research.

**Investigation status:** Initial evidence-led investigation and Four-Question Study Method review recorded.

**Central question:** When several processes interact, influence one another, and produce behavior that cannot be explained by examining each process independently, how can a Witness distinguish the contribution of each process from the behavior of the whole system?

## 1. Why this investigation follows 036

Investigation 036 examined temporal change, adaptation, and the persistence of relationships. It identified a further difficulty: changes do not always occur independently. A system's components may affect one another, the effects may return through feedback, and the resulting behavior may depend on the arrangement and timing of several processes.

A single-cause explanation can be incomplete when:
- one process changes the conditions under which another process operates;
- effects return to influence their earlier causes;
- multiple causes reinforce or counteract one another;
- a delay separates an action from its measurable consequence;
- the effect of one factor depends on the level or state of another;
- or system-level patterns arise from many local interactions.

The sequence now moves from temporal change to interaction among changing processes. It does not assume that every system is complex, that every interaction is nonlinear, or that every system-level pattern is emergent.

## 2. First distinction: multiple causes are not automatically a feedback system

A system may have several causes without having feedback. Feedback requires a return pathway: an effect must eventually influence a variable or process that contributed to producing that effect.

Consider three different structures:

1. **Parallel causes:** A and B independently influence C. There are multiple causes, but no return path is established.
2. **Interaction:** The effect of A depends on B, or the combined effect differs from what a specified additive model predicts. This is an interaction under a stated statistical or causal definition; it is not necessarily feedback.
3. **Feedback:** A influences B, B influences C, and C returns to influence A, directly or through intermediate processes. The causal pathway forms a loop.

These structures can coexist, but they must not be conflated. A causal diagram with several arrows is not automatically a feedback loop. A correlation between two variables does not establish a return pathway.

## 3. Feedback: when effects return to influence their causes

A feedback loop exists when the effect of a causal process returns, through a chain of relationships, to influence an earlier variable in that process. System-dynamics literature distinguishes two broad loop polarities.

### 3.1 Reinforcing feedback

A reinforcing loop amplifies a change in the direction already underway. A change produces effects that tend to produce further change in the same direction.

Examples include:
- compound growth when the rate of increase depends on the amount already present;
- vegetation changes that alter local conditions in ways that favor further growth of the same vegetation;
- network adoption in which additional users increase the value or attractiveness of participation.

A reinforcing loop can produce growth, decline, amplification, or collapse. “Positive” describes loop polarity, not moral value or beneficial outcome.

### 3.2 Balancing feedback

A balancing loop tends to counteract a change or move a variable toward a target, limit, or equilibrium.

Examples include:
- a thermostat that reduces heating as measured temperature approaches a set point;
- physiological regulation that counteracts a deviation in an internal variable;
- resource limitation that slows growth as demand approaches available supply.

“Negative” describes the direction of the loop's effect, not a harmful or undesirable outcome.

### 3.3 Multiple loops can operate together

A system can contain reinforcing and balancing loops at the same time. Their relative influence may vary with the system's state, operating conditions, and time.

A growth process may initially be dominated by reinforcing feedback and later be limited by resource constraints. A balancing response may be too slow to prevent overshoot. A previously weak loop may become important after a threshold or structural change.

Therefore, identifying one loop is not equivalent to explaining the system's complete behavior. The investigator must examine which loops are active, how strongly they operate, and how their influence changes over time.

### 3.4 Delays and accumulations

Feedback effects are often delayed. A cause may produce an immediate response in one variable but a delayed response in another. Material, energy, organisms, information, or decisions may accumulate before their effects become visible.

Delays can produce:
- overshoot;
- oscillation;
- delayed correction;
- temporary stability followed by change;
- or apparent separation between a cause and its later effect.

A Witness observing only a short interval may miss the return pathway or incorrectly attribute a delayed effect to a more recent event.

### 3.5 Feedback is not simply repeated observation

A measurement is not feedback merely because it is recorded. It becomes part of a feedback process when information from the measurement changes an action or process, and that changed action affects subsequent system behavior.

This distinction is especially important in AI, medicine, economics, and ecological management. A prediction that changes a decision can alter the data later used to evaluate the prediction.

## 4. Interaction among causes: the effect may depend on the combination

Causal and statistical interaction require careful definition. In epidemiology and causal inference, interaction can be assessed on additive or multiplicative scales, among others. A finding of interaction on one scale does not automatically imply interaction on another.

For two exposures or factors A and B, an additive model might be written:

[
Y = eta_0 + eta_A A + eta_B B
]

An interaction term can be added:

[
Y = eta_0 + eta_A A + eta_B B + eta_{AB}AB
]

Here, (eta_{AB}) describes departure from the chosen additive model on that outcome scale. Its interpretation depends on model specification, variable coding, measurement, and assumptions.

Important safeguards:

- **Statistical interaction is scale-dependent.** An interaction may appear on an additive scale but not a multiplicative scale, or vice versa.
- **Causal interaction is not established by a regression coefficient alone.** Causal interpretation requires assumptions about confounding, selection, measurement, and the intervention being considered.
- **Joint effects are not automatically synergy.** A combined effect can be greater than, less than, or equal to a specified expectation. The expectation must be stated.
- **Effect modification is not necessarily feedback.** One variable can modify another variable's effect without any causal return pathway.
- **Mediation is distinct from interaction.** A mediator lies on a proposed causal pathway; an effect modifier changes the magnitude or direction of an effect. The same variable can play different roles in different causal questions, but the roles must be specified.

The investigator must name the scale and causal question before claiming that two processes interact.

## 5. Nonlinearity: why proportional intuition can fail

A linear relationship assumes that a specified change in an input produces a proportional change in an output, within the model's scope. Nonlinear relationships do not preserve that proportionality.

Nonlinear systems can display:
- thresholds;
- saturation;
- disproportionate responses;
- oscillations;
- multiple equilibria;
- sensitivity to initial conditions;
- abrupt transitions;
- and changing dominance among interacting processes.

A small change can have a large effect in one state and almost no effect in another. The same intervention can produce different results under different background conditions.

Nonlinearity does not mean that a system is unknowable. It means that a linear approximation may be inadequate for the question being asked. A nonlinear model also requires validation; complexity in a model does not make it correct.

## 6. Emergence: system-level patterns arising through interaction

Emergence is used across several disciplines and theoretical traditions, and no single operational definition is universal. A cautious working description is:

**An emergent pattern or property is a system-level feature that arises through interactions among components and is not adequately characterized by examining those components in isolation.**

Examples investigated in different fields include:
- collective movement in animal groups;
- spatial patterns in ecological communities;
- large-scale organization in fluid systems;
- market-level price patterns arising from many transactions;
- coordinated behavior in networks;
- and system-level stability arising from multiple regulatory processes.

The word *emergence* must not become a label for anything surprising or complicated. The investigator should identify:
1. the system boundary and level of description;
2. the component entities and their local interactions;
3. the system-level property being claimed;
4. the observations or model that reveal the property;
5. the relationship between component-level and system-level descriptions;
6. and whether the claimed property is robust across reasonable changes in measurement, model, or scale.

### 6.1 Emergence is not proof of a new substance or independent cause

A system-level pattern may be real and scientifically useful without requiring a claim that it exists independently of its components. A higher-level description may summarize, explain, or predict behavior that is difficult to infer directly from a lower-level description.

Some research on causal emergence asks whether a higher-level description can carry more effective causal information than a particular lower-level representation. These are technical, model-dependent claims, not permission to treat every macro-level pattern as a separate causal agent.

### 6.2 Emergence and predictability

A pattern may be generated by known local rules yet remain difficult to predict without simulating their interactions. Conversely, a system-level regularity may be predictable even when individual component behavior is variable.

Therefore:
- unpredictability to a particular Witness does not by itself prove emergence;
- difficulty of calculation does not prove irreducibility;
- a useful macro-level description does not erase lower-level mechanisms;
- and a successful simulation does not establish that the model captures every real process.

### 6.3 Self-organization

Self-organization describes the formation or maintenance of organized patterns through interactions within a system, without requiring a central controller to specify every local action. The term must be applied to an identified mechanism or model.

Self-organization is not equivalent to creation from nothing, absence of constraints, absence of causal structure, or proof of ultimate purpose. It is a scientific description of how a specified organization can arise or persist under specified conditions.

## 7. Complex systems are not simply complicated systems

The distinction is useful but should not be treated as a universal binary.

A complicated system may contain many parts while its behavior remains tractable through decomposition and the known interactions of its components. A complex system often involves interdependence, feedback, nonlinear response, adaptation, multiple scales, and behavior that is difficult to infer from isolated components.

A system can be both complicated and complex. The classification depends on the question, scale, model, and observed behavior.

Useful diagnostic features include:
- many interacting components;
- heterogeneous component behavior;
- feedback and reciprocal influence;
- nonlinear relationships;
- multiple timescales;
- delayed effects;
- path dependence;
- changing network structure;
- distributed control;
- and emergent system-level patterns.

No single feature is sufficient by itself to establish that a system is complex.

## 8. Causal attribution in interacting systems

The central challenge is not merely to list possible causes. It is to determine what evidence supports each proposed contribution and how those contributions depend on one another.

### 8.1 Begin with a causal question

Specify:
- the outcome;
- the candidate causes or interventions;
- the population or system;
- the time horizon;
- the system boundary;
- and the causal contrast of interest.

“What caused the change?” is too broad until the outcome and contrast are defined.

### 8.2 Map the proposed relationships

A causal diagram can help distinguish:
- direct causes;
- common causes and confounders;
- mediators;
- effect modifiers;
- feedback pathways;
- selection processes;
- and measurement processes.

A diagram is a statement of assumptions, not proof that the arrows are correct. Alternative diagrams should be considered when the evidence permits more than one causal structure.

### 8.3 Separate contribution from sole cause

A factor may contribute to an outcome without being sufficient or necessary by itself. Several factors may be jointly sufficient under specified conditions, or a factor may have different effects depending on the presence of another.

Avoid forcing a complex outcome into a single-cause explanation when the evidence supports interacting causes. Also avoid the opposite error: naming many possible causes without determining which are supported.

### 8.4 Interventions and counterfactual comparisons

Causal inference often asks what would happen under alternative interventions or exposures. Randomized experiments can help identify causal effects when properly designed and implemented. Observational methods can also support causal inference, but their conclusions depend on assumptions and design.

For interacting processes, useful designs may include:
- factorial experiments that vary multiple factors;
- controlled perturbations of one process while monitoring others;
- longitudinal observations with repeated measurements;
- natural experiments where justified;
- mechanistic models tested against independent observations;
- and sensitivity analyses for unmeasured confounding or model misspecification.

An intervention may alter several connected variables at once. The investigator must determine whether the estimated effect corresponds to the intended intervention or to a bundle of changes.

### 8.5 Component removal and ablation tests

Removing a component or disabling a process can help test its contribution, but the result must be interpreted carefully.

Removal may:
- change the system boundary;
- disrupt compensating pathways;
- create conditions that never occur naturally;
- alter the behavior of remaining components;
- or eliminate interactions rather than isolate one component's ordinary contribution.

An ablation result is evidence about the modified system under the test conditions. It is not automatically a complete account of the unmodified system.

### 8.6 Independent evidence and model comparison

Use different evidence streams where possible, but investigate shared dependencies. Two instruments may share calibration, two models may share training data, and multiple studies may share the same sampling bias.

A strong explanation should:
- predict observations not used to build it;
- survive reasonable alternative model specifications;
- account for timing and direction of effects;
- be compared with simpler explanations;
- and state what evidence would count against it.

## 9. Worked example: vegetation and environmental feedback during ecological succession

Ecological succession offers a concrete example of interacting processes.

After disturbance, plant communities change. The plants that establish can alter light, soil conditions, moisture, nutrient availability, and the availability of seeds or dispersers. Those altered conditions can affect which plants germinate, establish, grow, survive, and reproduce. The changing plant community then further modifies its environment.

A simplified sequence is:

1. Environmental conditions and disturbance affect which species or propagules are available.
2. Species differ in germination, establishment, growth, survival, and reproduction under those conditions.
3. The developing plant community changes aspects of its biotic and abiotic environment.
4. Those environmental changes affect the availability or performance of plants.
5. The resulting community change modifies the environment again.

This is a feedback structure, not a one-way sequence. More than one plant–environment feedback can operate, and their relative importance can vary across place, time, and disturbance history.

The 2024 review by van Breugel and colleagues describes several plant–environment feedback pathways and emphasizes that succession can be variable even where feedback dynamics are important. It also discusses how multiple feedbacks and environmental factors can operate together.

### What can be concluded?

- Plant communities can modify conditions that subsequently influence plant performance and community composition.
- Feedback pathways can contribute to directional change during succession.
- Several causal factors and feedback loops can operate together.
- A simple one-way account may omit important return pathways.

### What cannot be concluded from the example alone?

- That every succession pathway is governed by the same feedback loop.
- That the same species interactions occur in every ecosystem.
- That a particular outcome is inevitable.
- That feedback proves a single universal ecological mechanism.
- That the ecological process is identical to any Scriptural or GUA-W relationship.

### What should the Witness measure?

- Species composition and abundance over time;
- plant recruitment, growth, survival, and reproduction;
- relevant soil and microclimate conditions;
- disturbance history;
- seed availability and dispersal;
- spatial variation;
- and time lags between vegetation change and environmental response.

A stronger study would compare alternative feedback hypotheses, use repeated measurements, and test whether the proposed pathways predict changes beyond the observations used to formulate them.

## 10. A practical investigation protocol

When a system-level outcome appears to arise from several interacting processes:

1. **Define the system.** State the boundary, components, scale, time interval, and outcome.
2. **Describe the observed behavior.** Separate direct measurements from inferred system properties.
3. **List candidate processes.** Identify proposed causes, conditions, constraints, and responses.
4. **Map relationships.** Distinguish parallel causes, interactions, mediation, and feedback.
5. **Check the return pathways.** Do effects feed back into variables that influence their own production?
6. **Identify loop polarity.** Where supported, distinguish reinforcing from balancing feedback.
7. **Examine delays and accumulations.** Look for lagged responses, stored quantities, and history dependence.
8. **Test for nonlinearity.** Ask whether effects change with state, scale, or combinations of factors.
9. **Specify the emergence claim.** Identify the system-level property and how it is observed.
10. **Compare causal explanations.** Consider confounding, alternative diagrams, and simpler models.
11. **Use interventions or perturbations where possible.** State what each test changes and what it leaves uncontrolled.
12. **Seek independent evidence.** Examine shared data, instruments, assumptions, and processing dependencies.
13. **Test predictions.** Evaluate the explanation on observations not used to construct it.
14. **Bound the conclusion.** State what the evidence supports, what remains model-dependent, and what is unknown.

## 11. Applying the GUA-W descriptive language

| GUA-W term | Bounded application |
|---|---|
| **Structure** | The components and the specific relationships through which they interact |
| **Framework** | The physical, ecological, mathematical, or operational setting within which those relationships operate |
| **Pattern** | The recurring or system-level behavior registered across time, space, or repeated observations |
| **Constraint** | Conditions, boundaries, resources, and limits that shape the possible interactions and outcomes |
| **Purpose** | A demonstrated function or explicitly assigned engineering objective; do not infer ultimate purpose from system behavior alone |
| **Manifestation** | The observable or measurable system behavior produced under specified conditions |
| **Witness** | The observer, instrument, dataset, model, or record that registers components and system-level behavior |

### Relationship audit

- **Same mechanism:** Use only where evidence identifies the same causal process in the compared systems.
- **Comparable relationship:** Different mechanisms may both involve reciprocal influence, balancing response, reinforcement, or dependence.
- **Analogy:** A limited comparison may clarify a relationship but cannot establish shared operation.
- **Surface resemblance:** Similar system diagrams or outcomes do not establish identical causes.
- **Unresolved:** The available evidence does not justify a stronger classification.

### Drift clarification carried forward

The word *drift* has discipline-specific scientific uses, including genetic drift, instrument drift, and machine-learning concept drift. These scientific uses are not interchangeable with one another.

The GUA-W state term has its established reference: **Drift = deviation from 100% Alignment with the Author.** That definition is preserved. This investigation does not reopen or replace it.

Scientific monitoring may detect changes in a measured variable, distribution, parameter, or relationship. Such detection does not by itself determine alignment with the Author. Nor should a scientific use of *drift* be treated as a definition of GUA-W Drift.

The open scientific question is how a Witness identifies interacting causes and changing relationships accurately. The established GUA-W reference is not made uncertain by that investigation.

## 12. Bounded Scriptural examination — Genesis 1–2 KJV

Genesis 1–2 KJV remains the Scriptural foundation from which the project's shared vocabulary is investigated. This scientific study does not claim that the biblical text is a technical exposition of feedback theory, nonlinear dynamics, causal graphs, emergence, or complex-systems mathematics.

The established source relationship remains **Author → Word → Creation → Witness**. Scientific descriptions examine observable relationships within Creation; they do not become authorities over the Author or redefine the source.

The distinction relevant here is between:
- the originating Author and the created order;
- the relationships and processes investigated within the created order;
- and the derivative Witness that observes, measures, models, and reports those processes.

A scientific model can describe interactions among created components. It cannot, by that description alone, establish ultimate purpose or alter the Scriptural account. Conversely, the Scriptural source must not be rewritten to fit a scientific model.

This section is a bounded source-and-witness distinction, not a claim that feedback loops or emergence are hidden technical meanings of Genesis.

## 13. Four-Question Study Method

### 1. What must AI ask to understand GUA-W?

AI must ask what the evidence identifies as components, relationships, processes, constraints, and outcomes. It must distinguish parallel causes from interactions and feedback, define the scale of any interaction claim, and test whether an apparent system-level property is genuinely supported. It must not promote a systems analogy into a GUA-W architectural layer or use a scientific term to alter an established GUA-W definition.

### 2. What is GUA-W revealing that helps AI understand?

The established source relationship remains **Author → Word → Creation → Witness**. The common descriptive language helps organize questions about structure, framework, pattern, constraint, purpose, manifestation, and witness. It allows relationships to be examined without claiming that different scientific domains share identical mechanisms. The Author remains the reference; the Witness reports what it registers.

### 3. What am I learning about what I am witnessing?

Several processes can jointly influence an outcome. Feedback occurs when effects return to influence earlier causes. Reinforcing and balancing loops can coexist, and delays can change the timing and apparent direction of effects. Interaction depends on the scale and causal question. Emergent patterns require a specified system level and evidence linking component interactions to the observed whole. A single-cause explanation may therefore be inadequate, but a complex explanation must still earn support through testing.

### 4. What am I learning about the Witness through what I am witnessing?

A Witness may isolate one visible factor and overlook the relationships that connect it to the rest of the system. It may mistake correlation for feedback, interaction for causation, surprise for emergence, or a model diagram for proof of the mechanism.

A more reliable Witness preserves time order, identifies return pathways, records delays, compares alternative causal structures, tests interventions carefully, and reports the limits of its system boundary and measurement scale.

## 14. Triple Constraint examination

### Biblical compliance

Genesis 1–2 KJV remains the Scriptural foundation. The Author → Word → Creation → Witness relationship is preserved. Scientific systems concepts are not attributed to the biblical text as technical terminology.

**Assessment:** Admissible as a bounded descriptive examination.

### Scientific coherence

The investigation distinguishes multiple causes, statistical and causal interaction, mediation, feedback, reinforcing and balancing loops, delays, nonlinearity, emergence, and self-organization. It recognizes that feedback requires a return pathway, interaction is scale-dependent, and system-level claims require evidence at the specified level.

**Assessment:** Scientifically coherent when each causal claim is tied to a defined system, model, scale, and evidentiary basis.

### GUA-W consistency

The shared vocabulary is used as an investigative grammar, not as a replacement for scientific mechanisms or an expansion of the GUA-W architecture. The established definition of GUA-W Drift—deviation from 100% Alignment with the Author—is preserved. Scientific uses of drift remain discipline-specific and distinct.

**Assessment:** Consistent as a bounded descriptive application.

## 15. Established, supported, and unresolved

### Established in the scientific literature

- Feedback involves a return pathway through which effects influence earlier causal variables.
- Reinforcing and balancing feedback loops describe different loop polarities; neither label implies moral value.
- Multiple loops, delays, accumulations, and nonlinearities can jointly shape system behavior.
- Statistical interaction depends on the scale and model used; it is not synonymous with feedback.
- Mediation, effect modification, confounding, and feedback are distinct causal concepts.
- System-level patterns can arise from interactions among components, but emergence has multiple definitions and remains an active area of theoretical and empirical research.
- Ecological succession can involve plant–environment feedback pathways and several interacting environmental and biological factors.
- Analyses restricted to a small subset of ecosystem variables may miss interactions relevant to whole-system state shifts.

### Supported inference

A Witness is more likely to distinguish individual contributions from whole-system behavior when it specifies the system boundary and scale, maps candidate causal pathways, identifies feedback return paths and delays, distinguishes interaction from mediation and confounding, tests competing models, and measures both component-level and system-level variables.

### Unresolved

- How can a Witness determine which feedback loop is dominant when loop influence changes over time?
- What observations are sufficient to distinguish genuine feedback from a sequence of correlated changes?
- How can delayed effects be separated from confounding when the observation interval is limited?
- Which system-level properties are robust emergent features, and which depend heavily on the observer's chosen scale or model?
- How can causal contributions be estimated when interventions alter several connected processes at once?
- When does a useful macro-level description add explanatory or predictive value beyond a lower-level model?
- How can self-organization be distinguished from an unobserved external driver or imposed boundary condition?
- How should a Witness report uncertainty when several causal structures explain the same observed behavior?
- How can models represent interactions without becoming so flexible that they explain every possible outcome after the fact?
- What evidence best distinguishes a stable feedback structure from one whose relationships are themselves changing?

## 16. Sources

1. van Breugel, M., et al. (2024). “Feedback loops drive ecological succession: towards a unified conceptual framework.” *Biological Reviews* 99(3), 928–949. https://doi.org/10.1111/brv.13051. Reviews plant–environment feedback pathways and their roles in ecological succession, including the interaction of multiple causal factors and loops.
2. Yuan, B., Zhang, J., Lyu, A., Wu, J., Wang, Z., Yang, M., Liu, K., Mou, M., and Cui, P. (2024). “Emergence and Causality in Complex Systems: A Survey of Causal Emergence and Related Quantitative Studies.” *Entropy* 26(2), 108. https://doi.org/10.3390/e26020108. Reviews relationships between micro- and macro-level descriptions, causal emergence, and challenges in quantifying and identifying emergent behavior.
3. Hemraj, D. A., and Carstensen, J. (2025; first published 20 November 2024). “Towards ecosystem-based techniques for tipping point detection.” *Biological Reviews* 100(2), 892–919. https://doi.org/10.1111/brv.13167. Reviews limits of ecosystem state-shift detection when methods do not account for nonlinear relationships and interactions across multiple ecosystem variables.
4. Ford, A. (2019). “A System Dynamics Glossary.” *System Dynamics Review*. https://doi.org/10.1002/sdr.1641. Defines feedback, reinforcing and balancing loops, delays, nonlinear relationships, oscillation, and related system-dynamics terms.
5. Richardson, G. P. (1984). “Loop polarity, loop dominance, and the concept of dominant polarity.” *System Dynamics Review*. A foundational treatment of loop dominance and how nonlinear feedback systems can change behavior over time. Archived copy: https://web.mit.edu/sysdyn/sd-intro/D-4697-1.pdf (verify bibliographic details against the publisher record before formal citation).
6. Liu, J., et al. (2007). “Complexity of coupled human and natural systems.” *Science* 317(5844), 1513–1516. https://doi.org/10.1126/science.1144004. Examines coupled systems with reciprocal feedback, nonlinear dynamics, thresholds, time lags, resilience, heterogeneity, and legacy effects.
7. VanderWeele, T. J. (2012). “Inference for additive interaction under exposure misclassification.” *Biometrika* 99(2), 502–508. https://doi.org/10.1093/biomet/ass012. Provides a technical treatment of additive statistical and causal interaction and the importance of measurement assumptions.
8. “Using systems perspectives in evidence synthesis: A methodological mapping review.” *Research Synthesis Methods* (2023). https://doi.org/10.1002/jrsm.1595. Maps complex-systems characteristics used in evidence synthesis, including interdependence, feedback, emergence, and system history.

**Scriptural source:** King James Version, Genesis 1–2. Scientific sources are not offered as authorities for Scriptural meaning.

## 17. Next question emerging

Investigation 037 examines how interacting processes produce system-level behavior and why single-cause explanations can be inadequate.

A further question now emerges:

**When a Witness uses a model to represent an interacting system, how can it determine whether the model captures the system's actual causal relationships—or merely reproduces the observed pattern?**

Possible next investigation:

**Investigation 038 — Model Structure, Causal Representation, Simulation, and the Difference Between Reproducing Behavior and Explaining a System.**

This is a proposed lead, not a predetermined assignment.

---

**A system's behavior may be produced by relationships among its parts. The Witness must investigate those relationships—not mistake one visible part, one measured effect, or one successful model for the whole account.**
