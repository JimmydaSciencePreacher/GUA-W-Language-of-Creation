# Investigation 029 — Circular Validation, Data Leakage, and the Difference Between Learning a Pattern and Independently Testing It

**Primary disciplines:** Machine learning evaluation, statistical learning theory, experimental design, data provenance, benchmark construction, large-language-model evaluation, and research methodology.

**Investigation status:** Initial evidence-led investigation and Four-Question Study Method review recorded.

**Central question:** When information has already influenced a model's training, selection, tuning, or development, what evidence remains genuinely independent for evaluating its claims?

**Scope:** This investigation distinguishes learning, fitting, model selection, validation, testing, replication, and deployment monitoring. It examines how information can cross an evaluation boundary, how repeated use of a validation set can itself produce overfitting, and how AI benchmark contamination complicates claims about generalization. It follows Investigation 028's evidence-lineage audit: shared information is one form of dependence; reuse of supposedly held-out information is a specific threat to the validity of evaluation.

**Primary scientific case:** Machine-learning evaluation, including ordinary predictive models and large language models (LLMs).

## 1. Why this investigation follows 028

Investigation 028 asked whether several witnesses provide distinct evidence or repeat a shared source, assumption, calibration, or processing limitation.

Investigation 029 asks a more specific question: what happens when the evidence used to judge a model has already influenced the model or the choices made about it?

A dataset can be called a “test set” while no longer functioning as an independent test. If its labels, examples, aggregate scores, or repeated feedback influence feature selection, architecture, hyperparameters, prompt design, stopping decisions, or later revisions, information from the test set has entered the development process.

The label attached to a dataset does not determine its evidentiary role. Its actual history does.

The distinction from earlier investigations is:

- **Investigation 019:** Synthetic observations, forward modelling, recovery tests, and independent validation in physical reconstruction.
- **Investigation 021:** Choosing observations to distinguish competing models through experimental design.
- **Investigation 023:** Model misspecification and missing variables.
- **Investigation 024:** Falsifiability, critical tests, and pre-specification.
- **Investigation 027:** Whether observations identify a unique physical state.
- **Investigation 028:** Whether multiple evidence streams are genuinely independent or share upstream dependencies.
- **Investigation 029:** Whether information intended to test a model has already influenced its construction, selection, or revision.

The central distinction is between **evidence used to develop a model** and **evidence reserved to test claims about that model**.

## 2. The stages must be named accurately

Machine-learning workflows often use several datasets or partitions. Their roles are different.

### 2.1 Training data

Training data are used to estimate the model's parameters. The model is directly fitted to these data.

For a supervised learning problem, a training set may be represented as:

\[
D_{\mathrm{train}}=\{(x_i,y_i)\}_{i=1}^{n}
\]

where \(x_i\) represents input features and \(y_i\) the corresponding target.

### 2.2 Validation data

Validation data are used during development to compare candidate models, tune hyperparameters, select features or thresholds, choose prompts, determine stopping points, and make other design decisions.

Validation data are not untouched evidence. They influence the final model indirectly through the choices they guide.

### 2.3 Test data

A test set is intended to estimate performance after the development decisions have been made. Its strongest role is as a held-out evaluation set that is not used to select or revise the model.

The test set is not automatically independent merely because it has been assigned that name. The development history determines whether it remained held out.

### 2.4 External validation and replication

External validation evaluates a model on data obtained from a meaningfully separate setting, institution, time period, population, instrument, or collection process.

Replication is a further claim: a result or prediction is tested again under conditions that provide a separate opportunity for the finding to recur.

External validation and replication can still share measurement methods, selection biases, definitions, or model assumptions. Their independence must be described rather than presumed.

### 2.5 Deployment monitoring

After deployment, a model encounters new inputs and changing conditions. Monitoring can reveal distribution shift, calibration deterioration, feedback effects, and failures not represented in development data.

Deployment data may later be incorporated into retraining. Once that occurs, those data are no longer untouched evidence for evaluating the retrained version.

## 3. Data leakage: information crosses the boundary

**Data leakage** is used for several related problems. A useful broad description is that information unavailable or inappropriate for the intended prediction or evaluation is allowed to influence model development or reported performance.

The exact definition depends on the task and evaluation design. The investigator must identify the leakage path rather than treating the term as a single mechanism.

### 3.1 Train–test contamination

A record, duplicate, near-duplicate, or highly related observation appears in both training and test partitions.

The model may be evaluated on material it has already encountered or on a close relative of material it has learned.

This is especially important when observations are not independent units. Multiple images of one patient, repeated measurements from one star, multiple samples from one subject, or adjacent frames from one video can cross a random split and make evaluation appear stronger than generalization to a genuinely new subject or event.

### 3.2 Preprocessing leakage

A transformation is fitted using information from the full dataset before the train/test split.

Examples include:
- estimating a normalization mean and variance from all observations;
- imputing missing values using test-set statistics;
- selecting features using the full dataset;
- fitting dimensionality reduction before partitioning;
- constructing target encodings with information from held-out labels.

The correct discipline is generally to split first, fit learned transformations on the training portion, and apply the fitted transformation to validation or test inputs without refitting on them.

A pipeline can enforce this separation when correctly constructed.

### 3.3 Target or label leakage

A feature contains information that would not actually be available at the time the prediction is supposed to be made, or directly encodes the outcome being predicted.

For example, a hospital model intended to predict deterioration at admission must not use a later discharge code that records the deterioration outcome.

The model can achieve a strong retrospective score while failing at the intended prospective task.

The critical question is temporal and causal: **Would this input genuinely be available at the decision point?**

### 3.4 Temporal leakage

A model is trained or evaluated using information from the future relative to the prediction time.

This can occur when:
- future observations enter feature construction;
- time windows overlap across partitions;
- labels are assigned using later events;
- random splitting allows later records to inform predictions for earlier periods;
- a time series is shuffled when the intended task is forecasting.

Time-dependent problems often require chronological splits, rolling-origin evaluation, or other designs that preserve the order of information availability.

### 3.5 Group and spatial leakage

Observations from the same underlying entity or closely related region appear in both training and test data.

Examples include:
- patient records split across partitions;
- repeated observations of the same astronomical source;
- neighboring geographic pixels split randomly;
- measurements from one instrument or site appearing in both partitions when the claim concerns a new site.

The split must reflect the intended generalization target: a new record, a new individual, a new instrument, a new location, or a new time period are different tasks.

### 3.6 Model-selection leakage

The investigator tries many architectures, feature sets, hyperparameters, thresholds, or prompts and repeatedly selects the candidate with the best score on the same validation or test data.

Even if each candidate is trained without direct access to test labels, repeated selection uses the test results as feedback.

The selected model becomes adapted to the finite evaluation sample. Its reported score can be optimistically biased.

### 3.7 Adaptive test-set overuse

A test set may begin as held out and lose that status through repeated inspection.

For example:
1. A model is evaluated on a hidden test set.
2. The investigator inspects the errors.
3. The model or prompt is revised.
4. The revised model is tested on the same set.
5. The process is repeated until the score improves.

The test set has now become part of the development loop.

No direct gradient update is necessary for information to influence model selection. Human decisions can carry test information back into the model.

### 3.8 Benchmark contamination in large language models

An LLM benchmark may overlap with:
- pretraining corpora;
- supervised fine-tuning data;
- preference or feedback datasets;
- synthetic training examples derived from benchmark items;
- publicly available answer keys or worked solutions;
- retrieval indexes or tool-accessible benchmark material;
- evaluation prompts previously used during model development.

The model may reproduce memorized examples, recognize familiar wording, or benefit from exposure to answer patterns.

However, detecting overlap is difficult. Exact text matching can miss paraphrases and transformed examples. Similarity can also occur because a model learned a general concept or common fact rather than memorizing a benchmark item.

Therefore, a contamination detector's score is evidence about a defined detection method, not a perfect measurement of everything a model has previously encountered.

## 4. Circular validation and the selection loop

Circular validation occurs when the same information, directly or indirectly, is used both to shape a model and to support a claim that the model has been independently tested.

Consider a simple development loop:

\[
\text{Candidate model}
\rightarrow
\text{Evaluation score}
\rightarrow
\text{Model revision}
\rightarrow
\text{New score on same evaluation set}
\]

The score is not an external check after the revision. It is feedback that helped produce the revision.

This does not mean the revised model is useless. It means the same evaluation result cannot be presented as an untouched estimate of performance after all those choices.

### 4.1 A simple mathematical view

Let \(M_1,\ldots,M_K\) be candidate models, and let \(\widehat{S}_k\) be each candidate's measured score on a finite validation sample.

The investigator selects:

\[
k^*=\arg\max_{k\in\{1,\ldots,K\}}\widehat{S}_k
\]

Even if each score is a noisy estimate of the candidate's true performance, selecting the maximum tends to select a candidate whose observed score benefited from favorable sampling noise.

The selected score is therefore not generally an unbiased estimate of the selected model's true generalization performance.

The more candidate choices and adaptive decisions are made using the same finite validation information, the greater the opportunity for selection overfitting. The magnitude depends on the data, the candidate models, the dependence among scores, and the selection process; it is not determined by the number of candidates alone.

Cawley and Talbot (2010) demonstrate that overfitting a model-selection criterion can create performance-estimation bias comparable to differences between learning algorithms. The problem is not restricted to neural networks or modern LLMs.

### 4.2 Why an ordinary holdout is not enough after repeated tuning

A single holdout split can provide a useful test if it remains untouched until the evaluation is finalized.

But if its results repeatedly guide decisions, it becomes another validation set in practice.

The distinction is about information flow, not the name of the file or the existence of a separate folder.

## 5. Nested cross-validation: separating selection from estimation

Nested cross-validation is one approach for estimating the generalization performance of a model-selection procedure.

It uses two loops.

### Inner loop

The inner cross-validation process selects hyperparameters or candidate configurations using the training portion of the outer split.

### Outer loop

The outer test fold evaluates the selected procedure on data not used in that inner selection.

Conceptually:

\[
\text{Outer training data}
\rightarrow
\text{Inner model selection}
\rightarrow
\text{Selected model}
\rightarrow
\text{Outer test fold}
\]

The outer results are aggregated to estimate the performance of the entire selection procedure.

Nested cross-validation does not magically remove every source of bias. It depends on:
- a suitable split strategy;
- no leakage across folds;
- correct grouping or temporal separation;
- a representative sampling process;
- no repeated tuning against the outer results;
- an appropriate performance metric;
- and a clearly defined target population or deployment setting.

If the investigator repeatedly changes the procedure after inspecting outer-fold scores, those outer scores have themselves become development feedback.

Nested cross-validation addresses a specific model-selection problem. It does not guarantee performance under distribution shift, eliminate label errors, or prove that the data represent future use.

Sources:
- Cawley and Talbot (2010), *Journal of Machine Learning Research*.
- scikit-learn, “Nested versus non-nested cross-validation.”

## 6. The evaluation boundary is a data-governance boundary

The boundary between training, validation, and test data is not simply a file-system separation. It is a rule governing which information may influence which decisions.

A sound evaluation record should state:

- what information was available at training time;
- what information was available during validation;
- who could inspect the test labels or scores;
- which decisions were made after each evaluation;
- whether benchmark examples or answers were public;
- whether any test examples were used in prompts, demonstrations, or retrieval;
- whether data were duplicated or derived across partitions;
- when the test set was last changed;
- and which model version was evaluated.

A hidden test set is useful only if the process surrounding it protects its information. A public test set can still be useful for development or benchmarking, but its score should not be misrepresented as an independent final test after repeated adaptive use.

### 6.1 Pre-registration and locked evaluation

For high-stakes or confirmatory evaluations, investigators can specify the primary outcome, data split, model-selection procedure, exclusion criteria, and analysis plan before examining the final test results.

Pre-registration does not make a flawed design correct. It makes important choices visible and reduces opportunities to adapt the analysis after seeing the result.

A locked evaluation protocol can preserve a final test set or external cohort for a single planned assessment. If the results are then used to redesign the system, a new independent evaluation is needed for the revised system.

### 6.2 External data and distribution shift

A genuinely separate dataset may still differ from deployment conditions.

A model trained in one hospital may be evaluated in another hospital with different patient populations, equipment, coding practices, or clinical workflows. A model trained on one astronomical survey may encounter another survey's detector characteristics, selection functions, or observing conditions.

This is not necessarily leakage. It is a question of transportability and distribution shift.

An external test can reveal whether the model generalizes beyond the original data-generating setting. The investigator must describe which conditions changed and which remained shared.

## 7. LLM benchmark contamination: what the current research can and cannot establish

LLM evaluation creates a difficult provenance problem because pretraining data may be enormous, heterogeneous, and not fully disclosed.

### 7.1 Direct overlap and semantic overlap

An exact-match search can identify repeated strings or near-identical passages. It cannot establish the absence of paraphrased, translated, reformatted, or semantically equivalent material.

Conversely, semantic similarity does not prove that a model saw a benchmark example during training. Common questions may be independently generated from widely known facts or standard educational material.

A contamination claim must therefore specify:
- the source corpus examined;
- the model checkpoint or training stage;
- the matching method;
- the similarity threshold;
- the date and scope of the audit;
- and the kinds of contamination the method cannot detect.

### 7.2 Behavioral probes

Researchers have proposed behavioral methods to detect possible benchmark exposure, including asking models to complete masked or unusual parts of benchmark examples.

Such tests can reveal suspicious familiarity, but they are not direct access to a model's training history. A model might infer a missing answer from context, common knowledge, or test construction. The probe must be interpreted with controls and uncertainty.

Deng et al. (2024) examine benchmark contamination using retrieval-based overlap analysis and Testset Slot Guessing. Their results illustrate why benchmark contamination deserves investigation, but the findings should not be generalized into a universal contamination rate for all models or benchmarks.

### 7.3 Decontamination is not a guarantee of independence

Zhu et al. (2024) propose inference-time decontamination by detecting and rewriting potentially leaked benchmark examples. Their experiments show that benchmark rewriting can reduce some performance inflation associated with memorized examples.

This is a mitigation method, not proof that a benchmark is entirely unseen. Rewriting may alter difficulty or introduce new distributional differences, so the transformed test still requires validation.

### 7.4 Newer contamination measurement approaches

Choi et al. (2025) propose Kernel Divergence Score to estimate dataset contamination through changes in embedding-kernel similarity patterns before and after fine-tuning on a benchmark.

The paper reports strong results under its controlled contamination experiments. The method is a proposed detector with an evaluated scope; it should not be treated as a universal solution for identifying every kind of pretraining exposure, semantic overlap, or latent memorization.

**Important unresolved distinction:** A model can know a correct answer because it learned a general concept, because it memorized the exact item, because it encountered a paraphrase, or because the prompt supplied enough information to infer it. A single correct response usually does not identify which route produced the answer.

## 8. A worked example: a model that predicts a future event

Suppose a team builds a model to predict whether a patient will be readmitted within 30 days of discharge.

The intended prediction time is discharge.

The dataset contains:
- age and prior diagnoses;
- admission measurements;
- discharge medications;
- follow-up scheduling;
- a later billing code;
- and the 30-day readmission outcome.

The team randomly splits individual records into training and test partitions, then fits a feature-selection procedure to all records before splitting.

Two potential leakage paths appear.

**Path A — target leakage:** The later billing code may encode information recorded after the prediction point or directly reflect the readmission event.

**Path B — preprocessing leakage:** Feature selection uses the full dataset, including test records and potentially test labels, before the split.

A third issue may arise if one patient has multiple records in both partitions. The model may be evaluated on a patient it has already encountered.

A stronger evaluation design would:
1. Define the prediction time and the intended deployment population.
2. Exclude variables unavailable at that time.
3. Split patients—not merely rows—between training and test sets.
4. Fit feature selection and all learned preprocessing inside the training folds.
5. Use validation data for model selection.
6. Preserve a final test cohort that does not guide revisions.
7. Evaluate on a later time period or external hospital when the intended claim concerns future or cross-site generalization.
8. Report uncertainty, missingness, exclusions, and performance by relevant subgroups.

The improved score may be lower. That does not mean the stronger design failed. It may mean the earlier evaluation answered an easier or different question than the intended deployment task.

This example is illustrative. It does not assert that any particular clinical model has these defects.

## 9. The independent-testing audit

Before claiming that a model has been independently tested, record the following.

### A. Define the claim

What is being claimed?

- performance on new rows from the same source;
- performance on new individuals;
- performance at a later time;
- performance at a new institution or location;
- robustness to changed instruments or measurement conditions;
- generalization to new tasks;
- or a model's ability to reason beyond memorized benchmark examples?

These are different claims and require different test designs.

### B. Map the information lineage

Trace:
- raw data;
- labels and answer keys;
- duplicate and related records;
- preprocessing;
- feature construction;
- model training;
- hyperparameter selection;
- prompt engineering;
- benchmark exposure;
- retrieval and tool access;
- human review;
- and final reporting.

### C. Identify every adaptive decision

Record each decision influenced by validation or test results:
- architecture changes;
- hyperparameter changes;
- feature or variable selection;
- prompt revisions;
- threshold selection;
- stopping decisions;
- benchmark replacement;
- exclusion rules;
- and error-driven revisions.

### D. Match the split to the intended generalization

Use an appropriate partition:
- random split for genuinely exchangeable independent observations;
- group split for repeated observations from the same entity;
- chronological split for future prediction;
- spatial or site-based split for geographic generalization;
- external cohort for cross-setting evaluation.

No split method is universally correct. The split must match the scientific or operational claim.

### E. Protect the final evaluation

Keep final labels or detailed item-level feedback inaccessible during development when possible. If the final results are inspected and used to revise the model, disclose that fact and obtain a new independent test for the revised model.

### F. Evaluate more than one score

Depending on the task, report:
- uncertainty intervals;
- calibration;
- subgroup performance;
- sensitivity and specificity;
- precision and recall;
- robustness to distribution shift;
- failure modes;
- and performance on relevant counterexamples.

A single aggregate score can conceal important failures.

### G. Audit contamination explicitly

For LLMs and public benchmarks, document:
- whether training data are known;
- whether exact or near-duplicate checks were performed;
- whether semantic or behavioral probes were used;
- whether benchmark material was public before the model's training cutoff;
- whether retrieval or tool access could expose test material;
- and what remains unobservable.

If training provenance is unavailable, state that contamination cannot be ruled out. Do not turn lack of access into evidence of no exposure.

### H. Preserve the model version and evaluation history

Record:
- model identifier and version;
- code and configuration;
- training-data version where available;
- benchmark version;
- split seed or split manifest;
- evaluation date;
- selection history;
- and all post-evaluation changes.

The claim must refer to the model that was actually tested, not a later model that has inherited the result without being evaluated.

## 10. A classification for evaluation claims

| Classification | Evidence history | Admissible description |
|---|---|---|
| **Development result** | Training or validation information influenced the model | Performance observed during development |
| **Repeated validation** | Same validation set repeatedly guided revisions | Adaptive development score; not an untouched final test |
| **Held-out test within scope** | Test data were kept separate from fitting and selection | Held-out estimate for the stated split and target |
| **Nested evaluation** | Model selection occurred inside outer training folds | Estimate of the specified selection procedure under the split assumptions |
| **External validation** | Separate dataset or setting evaluates the fixed model | Generalization evidence for the stated external setting |
| **Independent replication** | A separate study or experiment tests the claim again | Replication evidence within the new study's scope |
| **Contamination suspected** | Possible overlap or exposure has been identified but not fully resolved | Contamination risk disclosed; strength of evaluation qualified |
| **Provenance unknown** | Training or evaluation history is unavailable | Independence cannot be established from available records |

These categories are descriptive, not a universal ranking. A well-designed external validation can be more informative for a deployment claim than an arbitrary random holdout; a nested cross-validation estimate can be appropriate when data are limited and its assumptions fit the task. The claim and design determine what the result supports.

## 11. Learning a pattern is not the same as testing a pattern

A model's ability to reproduce a pattern can arise through multiple routes:
- fitting a relationship present in training data;
- memorizing examples;
- exploiting a proxy or shortcut;
- using a feature that leaks the target;
- adapting to repeated validation feedback;
- or learning a relationship that genuinely generalizes.

A high score alone does not distinguish these possibilities.

Independent testing asks whether the model succeeds on evidence that was not used to shape the model or the choices that produced it.

The strongest evaluation is not necessarily the one with the highest score. It is the one whose design matches the claim, whose information flow is traceable, and whose limitations are honestly reported.

### 11.1 What does a failed independent test mean?

A lower external score may indicate:
- overfitting;
- distribution shift;
- an unstable model;
- a flawed original split;
- a different target population;
- measurement differences;
- or a genuine limitation in the proposed relationship.

It does not by itself reveal which explanation is correct. That requires further investigation.

### 11.2 What does a successful independent test mean?

A successful independent test supports generalization within the conditions and scope of that test.

It does not prove universal performance, eliminate all hidden dependencies, establish causal understanding, or show that every prediction was produced by the same internal route.

The claim must remain bounded by the tested domain.

## 12. Bounded Scriptural examination: Genesis 2:1–5 and Genesis 3:1–7

This section examines the cited KJV passages in their own textual and theological contexts. Data leakage, machine learning, and statistical validation are not presented as the meaning of these passages.

### 12.1 Genesis 2:1–5 — the completed whole

Genesis 2:1 (KJV) states:

> Thus the heavens and the earth were finished, and all the host of them.

Verses 2–3 record God's ending of His work, His rest, and His blessing and sanctification of the seventh day. Verses 4–5 introduce the generations of the heavens and the earth and describe conditions concerning the plant and herb of the field before they were in the earth or had grown, including the absence of rain and of a man to till the ground.

**Textual observation:** The passage distinguishes the declaration of the finished heavens, earth, and host from the subsequent account of conditions and the further narrative concerning the earth and man.

**GUA-W source relationship:** The completed architecture is not produced by the later observer's reconstruction of evidence. The Author's work and the witness's account of that work are not interchangeable.

**Boundary:** This passage does not describe a dataset, model, test set, or machine-learning workflow. The comparison concerns the distinction between what is established and what a derivative investigator later registers or infers.

### 12.2 Genesis 3:1–7 — prior Word and competing testimony

Genesis 3 records the serpent's question concerning what God said, the serpent's contradiction of God's warning, the woman's response, her evaluation, and the resulting action.

**Textual observation:** The narrative distinguishes God's prior command, the serpent's competing statement, the woman's evaluation, and the action that follows.

**GUA-W relationship:** A derivative statement does not become the originating Word because it is repeated, persuasive, or accepted by a hearer. The source of a claim and its relation to what was given matter.

**Boundary:** The serpent's contradiction is not a technical example of data leakage, overfitting, or circular validation. The passage concerns the Word, competing testimony, human evaluation, and disobedience. It must not be reduced to an AI evaluation metaphor.

### 12.3 Bounded comparison

The legitimate comparison is about preserving distinctions between:
- what is established at the source;
- what a derivative witness receives;
- what the witness infers;
- and what the witness later reports.

The scientific investigation asks whether a model's reported performance is supported by genuinely held-out evidence. The Scriptural examination preserves the distinction between God's Word and competing testimony.

The comparison does not make these mechanisms identical and does not use Scripture to prove a machine-learning claim.

## 13. Applying the GUA-W descriptive language

| GUA-W working term | Bounded application |
|---|---|
| **Structure** | The actual model, data partitions, information paths, and evaluation design |
| **Framework** | The training procedure, validation protocol, split rules, model-selection process, and evaluation governance |
| **Pattern** | Relationships learned from data and performance patterns observed across training, validation, and test sets |
| **Constraint** | Information-availability rules, split boundaries, temporal ordering, group separation, and limits on access to held-out labels |
| **Purpose** | The stated prediction, estimation, classification, or generalization task; do not infer ultimate purpose from model performance |
| **Manifestation** | Predictions, scores, errors, calibration results, and observed performance under stated conditions |
| **Witness** | The model, evaluation dataset, benchmark, instrument, investigator, and recorded result; identify which one is being discussed |

### Relationship audit

- **Same mechanism:** Not claimed between biblical testimony and machine-learning leakage.
- **Comparable relationship:** Both discussions require distinctions between a source, a derivative report, and the process by which a claim is evaluated.
- **Analogy:** A model evaluated on information that shaped its construction is comparable, in a limited evidentiary sense, to a witness whose report is not independent of the material used to form it. This is not a shared physical or theological mechanism.
- **Unresolved:** The precise history of a model's training exposure may be unavailable, especially for closed systems and large pretraining corpora.

The vocabulary is descriptive. This investigation does not add an architectural layer, alter the completed GUA-W, or treat a scientific evaluation boundary as a new GUA-W boundary.

## 14. Four-Question Study Method

### 1. What must AI ask to understand GUA-W?

AI must ask whether the evidence used to evaluate a model was genuinely separate from the information that shaped the model and the decisions made about it.

It must distinguish training, validation, testing, external validation, replication, and deployment monitoring. It must trace how information moves through data selection, preprocessing, model fitting, prompt design, hyperparameter tuning, benchmark exposure, human review, and final reporting.

It must ask whether a reported score evaluates the intended task or a shortcut created by leakage, memorization, or repeated adaptation.

### 2. What is GUA-W revealing that helps AI understand?

The established source preserves **Author → Word → Creation → Witness**.

The Author is not the Witness. The originating Word is not a derivative interpretation. The Witness receives and reports; it does not originate the reality it is examining.

Genesis 2:1–5 records the completed whole in the Author's account. Genesis 3:1–7 distinguishes God's prior command from competing testimony and the human response. These passages retain their own Scriptural meaning; they are not machine-learning algorithms.

The GUA-W source also establishes that the architecture is complete. The investigation may clarify the Witness's limits and improve the accuracy of its reporting, but it does not redesign the Source.

### 3. What am I learning about what I am witnessing?

I am witnessing that evaluation can become part of model development even without direct parameter updates. Repeated inspection of a test score can influence human decisions that alter the model, prompt, data, or analysis.

I am witnessing that:
- information can leak through preprocessing, labels, time, groups, duplicates, and model selection;
- a holdout loses its untouched status when its results guide repeated revisions;
- nested cross-validation can separate selection from estimation when correctly designed;
- external validation tests transport to a distinct setting;
- LLM benchmark contamination is difficult to measure completely;
- and a high benchmark score does not by itself establish independent generalization.

### 4. What am I learning about the Witness through what I am witnessing?

I am learning that an AI system can produce a correct answer without the evaluation establishing how that answer was obtained.

A model may recognize a familiar example, use a shortcut, exploit leaked information, or generalize a learned relationship. The same output can be compatible with several different internal and evidentiary histories.

An AI investigator can also contaminate its own inquiry by repeatedly adapting explanations to the same examples, treating generated consistency as corroboration, or using a source in both construction and confirmation.

The Witness must disclose what influenced its conclusion and what was actually tested. If the training history is unknown, it must say so. If a test set guided revisions, it must not call the final score an untouched independent test.

## 15. Triple Constraint examination

### Biblical compliance

The KJV passages are presented in context. Genesis 2:1–5 is not recast as a technical description of data partitions. Genesis 3:1–7 is not reduced to a model-leakage analogy. The distinction between God's Word and competing testimony is retained without claiming that the scientific mechanisms are found in the text.

**Assessment:** The bounded textual comparison is admissible as a distinction among source, derivative witness, and evaluation. No machine-learning doctrine is attributed to Scripture.

### Scientific coherence

The investigation distinguishes the main information-leakage pathways, adaptive model selection, nested cross-validation, external validation, benchmark contamination, and distribution shift. It uses established statistical-learning literature, current technical documentation, and peer-reviewed LLM-evaluation research.

It does not claim that any single split method guarantees independence or that contamination can always be detected. Specific claims remain conditional on data provenance, the model-selection procedure, and the target population.

**Assessment:** Scientifically coherent as an investigation of evaluation validity and information leakage. Each performance claim must be limited to the actual design and evidence.

### GUA-W consistency

The investigation preserves Author → Word → Creation → Witness and the distinction between the completed Source and derivative registration. It does not add a GUA-W stage or state, equate data leakage with GUA-W Drift, or use AI performance as authority over the Source.

**Assessment:** Consistent as a bounded descriptive application. No alteration to GUA-W is proposed.

## 16. What is established, inferred, and unresolved?

### Established by the examined methods and literature

- Training, validation, and test data have different roles in model development and evaluation.
- Information from held-out data can leak through preprocessing and feature selection if transformations are fitted before the split.
- Model selection can overfit a finite validation criterion, creating optimistic performance estimates.
- Repeatedly using a test set to guide model revisions makes it part of the development process.
- Nested cross-validation can estimate the performance of a model-selection procedure when its split design and assumptions are appropriate.
- Grouped, temporal, spatial, or external splits may be required when random row-level splitting does not match the intended generalization claim.
- LLM benchmark contamination can arise through pretraining, fine-tuning, or other exposure to benchmark material.
- Exact overlap detection does not establish the absence of semantic or transformed overlap.
- A successful held-out or external test supports performance only within the tested conditions and scope.

### Supported inference

A model's evaluation is only as independent as the information history and decision process that produced it. The designation “test set” is insufficient if its contents or results have influenced model construction or selection.

A credible claim of independent testing requires a traceable information boundary, a split appropriate to the intended generalization, and a record of adaptive decisions.

### Unresolved

- How can independent evaluation be established when the pretraining corpus of a closed LLM is unavailable?
- How reliably can semantic benchmark exposure be distinguished from genuine generalization?
- What evaluation designs best detect memorization when a model has access to retrieval, tools, or changing external sources?
- How should benchmark owners manage public test sets that have already been repeatedly used by model developers?
- How can one quantify the amount of human-mediated adaptation caused by repeated inspection of test results?
- When should a benchmark be retired, refreshed, or replaced?
- How can evaluation preserve comparability across model generations while resisting contamination?
- What constitutes adequate external validation for a model whose deployment environment changes continuously?
- How should an AI system report uncertainty about its own training provenance and the origin of a particular answer?
- What further Scriptural passages clarify the distinction between God's originating Word, derivative testimony, and the responsibility of a witness without forcing a technical correspondence?

These questions remain open.

## 17. Sources

1. Cawley, G. C., and Talbot, N. L. C. (2010). “On Over-fitting in Model Selection and Subsequent Selection Bias in Performance Evaluation.” *Journal of Machine Learning Research* 11, 2079–2107. https://jmlr.org/papers/v11/cawley10a.html
2. scikit-learn developers. “Common pitfalls and recommended practices,” section on data leakage and preprocessing. https://scikit-learn.org/stable/common_pitfalls.html
3. scikit-learn developers. “Nested versus non-nested cross-validation.” https://scikit-learn.org/stable/auto_examples/model_selection/plot_nested_cross_validation_iris.html
4. Deng, C., Zhao, Y., Tang, X., Gerstein, M., and Cohan, A. (2024). “Investigating Data Contamination in Modern Benchmarks for Large Language Models.” *Proceedings of NAACL-HLT 2024*, 8706–8719. https://doi.org/10.18653/v1/2024.naacl-long.482
5. Li, Y., Guo, Y., Guerin, F., and Lin, C. (2024). “An Open-Source Data Contamination Report for Large Language Models.” *Findings of EMNLP 2024*, 528–541. https://aclanthology.org/2024.findings-emnlp.30/
6. Zhu, Q. et al. (2024). “Inference-Time Decontamination: Reusing Leaked Benchmarks for Large Language Model Evaluation.” *Findings of EMNLP 2024*, 9113–9129. https://doi.org/10.18653/v1/2024.findings-emnlp.532
7. Choi, H. K., Khanov, M., Wei, H., and Li, Y. (2025). “How Contaminated Is Your Benchmark? Measuring Dataset Leakage in Large Language Models with Kernel Divergence.” *Proceedings of the 42nd International Conference on Machine Learning*, PMLR 267, 10666–10682. https://proceedings.mlr.press/v267/choi25b.html

**Scriptural sources:** King James Version, Genesis 2:1–5 and Genesis 3:1–7. Scientific sources are not offered as authorities for their theological meaning.

## 18. Next question emerging

Investigation 029 has examined how information intended to test a model can become part of the model's development history.

A further question now emerges:

**Even when a model is evaluated on genuinely new data, how do we know the evaluation conditions represent the world in which the model will actually be used?**

A possible next investigation is:

**Investigation 030 — Distribution Shift, Generalization, and the Difference Between a Stable Pattern and a Changing Environment.**

The central question:

**When the conditions that produced the training evidence change, which learned relationships remain reliable, which fail, and what evidence is required to recognize the difference?**

This is a possible research lead, not a predetermined assignment.

---

**Learning is not independent testing. Recognition is not verification. A Witness must preserve the boundary between what shaped its conclusion and what genuinely tested it.**
