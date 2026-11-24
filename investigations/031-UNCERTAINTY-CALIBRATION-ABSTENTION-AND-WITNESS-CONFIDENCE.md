# Investigation 031 — Uncertainty, Calibration, Abstention, and the Limits of a Witness's Confidence

**Primary disciplines:** Statistical learning, uncertainty quantification, probability calibration, selective prediction, conformal prediction, language-model evaluation, decision theory, and measurement science.

**Investigation status:** Initial evidence-led investigation and Four-Question Study Method review recorded.

**Central question:** How can a Witness distinguish a well-supported result from an uncertain inference, an unfamiliar condition, or a case in which the available evidence does not justify a confident answer?

**Scope:** This investigation examines predictive uncertainty, calibration, confidence statements, abstention, selective prediction, conformal prediction, and communication of uncertainty. It follows Investigation 030: distribution shift can place a model outside the conditions in which prior performance was established.

**Primary scientific case:** Predictive uncertainty in machine learning and large language models (LLMs).

## 1. Why this investigation follows 030

Investigation 030 examined distribution shift: a model can perform well under one data-generating environment and fail when the environment changes.

Investigation 031 asks what evidence supports a particular prediction, whether reported confidence corresponds to actual reliability, and whether a system should answer, qualify, clarify, seek evidence, refer, or abstain.

- **028 — Independent Witnesses:** Are evidence streams genuinely independent, or do they share dependencies?
- **029 — Independent Testing:** Did information used to evaluate a model already influence its development?
- **030 — Changing Environments:** Does the present environment remain within the scope of prior evidence?
- **031 — Uncertainty and Abstention:** How well is the strength and limitation of the present claim represented, and what should happen when evidence is insufficient?

A model can be correct without being well calibrated. It can be wrong while expressing high confidence. It can also be uncertain for different reasons that require different responses.

The label “confidence” is not itself a measurement of reliability.

## 2. Distinguish the kinds of uncertainty

Uncertainty is not one undifferentiated condition. Different sources call for different investigation and different responses.

### 2.1 Aleatoric uncertainty

Aleatoric uncertainty refers to variability or unpredictability inherent in an outcome under a specified model and information. Even if a fair die is perfectly understood, the outcome of a particular roll is not predictable with certainty. More training examples may improve estimates of the distribution, but they do not remove the randomness of the next roll.

The investigator should state what randomness is represented and at what level.

### 2.2 Epistemic uncertainty

Epistemic uncertainty arises from limited knowledge, finite data, uncertain parameters, model choice, missing variables, or incomplete understanding. More or better evidence may reduce some epistemic uncertainty. It may not remove it entirely, especially when a system is only partially observable or the model family is inadequate.

### 2.3 Model uncertainty and misspecification

A model may omit relevant variables, use an unsuitable functional form, or represent the wrong causal or statistical structure. A model can be highly confident within its own assumptions while those assumptions are wrong.

Confidence conditional on a model is not the same as confidence that the model itself is adequate.

### 2.4 Measurement and data uncertainty

Inputs may be noisy, imprecise, incomplete, censored, biased, or produced by instruments with calibration limitations. A prediction system that treats uncertain measurements as exact can understate the uncertainty of its output.

### 2.5 Distributional and domain uncertainty

The current input may come from a population, instrument, time period, location, or operating condition unlike the data used for development. Out-of-distribution detection can identify some unfamiliar inputs, but it is not a complete detector of every harmful shift. A model may encounter a changed relationship even when inputs appear statistically familiar.

### 2.6 Ambiguity and underspecification

A question may have several reasonable interpretations, lack necessary context, or fail to specify the target being predicted. This is not necessarily uncertainty about a fixed answer. It may be uncertainty about what question is being asked.

A suitable response may be to clarify the question rather than attach a probability to an assumed interpretation.

### 2.7 Unknown unknowns

A system cannot reliably quantify every failure mode it has not represented or considered. An uncertainty estimate is itself produced by a method with assumptions and blind spots. A numerical uncertainty score should not be treated as a complete inventory of what the system does not know.

## 3. Confidence is not calibration

A confidence statement expresses how strongly a model or evaluator favors a prediction. Calibration asks whether stated confidence corresponds to observed accuracy over a collection of predictions.

For a binary prediction system, suppose a model assigns confidence 0.8 to a large group of cases. If calibrated at that level, approximately 80% of those predictions should be correct under the evaluation distribution and stated grouping.

Calibration is a population-level property of a set of predictions. It does not guarantee that a particular prediction with confidence 0.8 is correct.

### 3.1 Reliability diagrams

A reliability diagram groups predictions by stated confidence and compares average confidence with observed accuracy. If a group has mean confidence 0.9 and observed accuracy 0.7, the model is overconfident for that group.

A reliability diagram depends on the sample and binning method. Sparse bins can make apparent calibration unstable.

### 3.2 Expected Calibration Error

A common summary is Expected Calibration Error (ECE):

\[
\mathrm{ECE}=\sum_{b=1}^{B}\frac{|S_b|}{n}
\left|\mathrm{acc}(S_b)-\mathrm{conf}(S_b)\right|
\]

Here, \(S_b\) is a confidence bin, \(n\) is the number of predictions, and the two functions represent average accuracy and average confidence in that bin.

ECE is convenient but not a universal measure of calibration. It depends on binning, can hide subgroup errors, and may be low even when calibration is poor in important regions. Different metrics answer different questions.

### 3.3 Proper scoring rules

The Brier score and logarithmic loss evaluate probabilistic predictions using both calibration and aspects of discrimination or resolution.

For a binary event with forecast probability \(p_i\) and observed outcome \(y_i\in\{0,1\}\), the Brier score is:

\[
\mathrm{BS}=\frac{1}{n}\sum_{i=1}^{n}(p_i-y_i)^2
\]

Lower values are better for the evaluated sample and task. A proper scoring rule encourages honest probability forecasts in expectation when the forecaster seeks to optimize that score.

No single metric replaces inspection of calibration curves, subgroup performance, data quality, and the decision context.

### 3.4 Calibration is distribution-dependent

A model calibrated on one dataset may become miscalibrated after distribution shift, changes in prevalence, new measurement conditions, or altered user behavior.

Calibration must be evaluated on data representative of intended use and monitored when the operating environment changes. A historical calibration result is evidence about historical conditions, not a permanent guarantee.

## 4. LLM confidence: different quantities are easily confused

For language models, “confidence” can refer to different things.

### 4.1 Token probability

A language model assigns probabilities to possible next tokens under its learned distribution and current context. A high probability for a generated token does not establish that the resulting sentence is factually true. Token probability is not automatically a calibrated probability that an entire answer is correct.

### 4.2 Self-reported verbal confidence

A model may be asked to say “I am 90% confident.” This number is generated as part of its response unless tied to a validated estimation procedure. A verbal confidence statement must not be treated as calibrated merely because it is numeric or sounds precise. It requires evaluation against observed outcomes on representative tasks.

### 4.3 Consistency across repeated generations

Repeated answers can be compared for agreement. Disagreement may signal ambiguity or uncertainty, but agreement does not prove correctness.

Repeated samples can share learned biases, source material, prompt assumptions, and model limitations. This links to Investigation 028: multiple outputs from one model are not automatically independent witnesses.

### 4.4 Retrieval-supported answers

Retrieval can improve grounding, but it does not guarantee that sources are correct, relevant, current, independent, or interpreted accurately.

The system must distinguish source availability, relevance, reliability, agreement, and whether a source actually supports the stated claim. A citation is a trace to evidence, not a guarantee that the evidence proves the claim.

### 4.5 Reasoning traces and explanations

A fluent explanation may not faithfully expose the process that produced the answer. The explanation itself is another generated output requiring evaluation. A model's ability to explain a conclusion is not proof that its internal computation followed the explanation.

### 4.6 What can be calibrated?

LLM confidence research examines correctness of final answers, individual claims, knowledge of relevant information, uncertainty across alternatives, confidence under a particular task or domain, and whether a model should abstain.

These targets are not interchangeable. A system calibrated for multiple-choice answer accuracy may not be calibrated for open-ended factual claims, code execution, source interpretation, or another domain.

## 5. Abstention and selective prediction

**Abstention** means that a system declines to provide a requested prediction or answer under specified conditions.

**Selective prediction** allows a model to answer only on a subset of cases and abstain on the rest.

Abstention can reduce errors among answered cases, but it also reduces coverage: fewer cases receive an answer. The goal is not maximum refusal. It is an appropriate balance between error risk, coverage, and the cost of a wrong or missing answer.

### 5.1 Risk–coverage relationship

Coverage is the fraction of cases answered. Selective risk is the error rate among those answered. As a system becomes more selective, coverage generally falls. Risk may fall too, but the relationship must be measured rather than assumed.

A risk–coverage curve shows the trade-off across possible thresholds. A system that answers only 20% of cases with a low error rate may be useful in one setting and unacceptable in another.

### 5.2 Decision thresholds depend on consequences

The appropriate threshold depends on the cost of a false answer, the cost of no answer, the cost of clarification, human-review availability, urgency, and the distribution of cases.

A low-risk trivia question and a high-consequence clinical decision should not necessarily use the same abstention policy.

### 5.3 Abstention is not automatically safe

Abstention can fail in several ways:
- the system may confidently answer when it should abstain;
- it may abstain too often on answerable questions;
- it may disproportionately abstain for certain groups or dialects;
- users may interpret a refusal as evidence that the question is impossible;
- users may bypass the system and turn to a less reliable source.

Where possible, the system should explain the reason for abstention: missing information, conflicting sources, unsupported domain, or inability to verify a claim.

### 5.4 Clarification, qualification, and referral are distinct actions

Not every uncertain case requires a blank refusal. A Witness may:
1. **Answer with scope:** State what the evidence supports and limit the claim.
2. **Qualify:** Explain uncertainty, assumptions, or competing interpretations.
3. **Ask for clarification:** Resolve ambiguity or obtain missing context.
4. **Seek additional evidence:** Retrieve a source, run a calculation, or request a measurement.
5. **Refer for review:** Escalate to a qualified person or appropriate authority.
6. **Abstain:** State that the available evidence does not justify an answer.

These are operational choices, not new GUA-W stages.

## 6. Conformal prediction: useful guarantees with important boundaries

Conformal prediction constructs prediction sets or intervals using calibration data and a nonconformity score. Instead of returning only one point prediction, a conformal method can return a set of plausible labels or an interval for a numerical outcome.

Under exchangeability assumptions and correct implementation, standard split conformal prediction can provide finite-sample **marginal coverage** at a chosen nominal level.

For example, a 90% marginal coverage target means that, over the relevant exchangeable sequence, prediction sets cover the true outcome at the stated long-run rate under the method's assumptions.

### 6.1 What marginal coverage does not say

Marginal coverage is averaged across the evaluated population. It does not guarantee 90% coverage for every individual, subgroup, feature value, location, or operating condition. A method may achieve the overall target while under-covering an important subgroup and over-covering another.

### 6.2 Conditional coverage limitations

Exact distribution-free conditional coverage for every possible covariate value is generally impossible in finite samples without additional restrictions or assumptions.

Research can provide guarantees for specified subgroups or restricted classes of distribution shifts, but the scope must be stated. A guarantee over selected groups is not a guarantee over every possible group.

### 6.3 Exchangeability and distribution shift

Standard conformal guarantees rely on assumptions such as exchangeability between calibration and future observations. Time trends, changing populations, adaptive sampling, and distribution shift can violate those assumptions.

Weighted, localized, sequential, and adaptive variants address particular settings, but each has its own assumptions and limits. Conformal prediction is not a universal shield against environmental change.

### 6.4 Prediction sets may be too wide to be useful

A method can achieve valid coverage while returning very broad intervals or large sets. Validity and usefulness are separate criteria. A wide interval may honestly express limited information but fail to support a practical decision.

## 7. Worked example: a Witness asked to identify a source

Suppose a research assistant is asked: “Does this paper establish that a particular physical mechanism causes the observed effect?”

The available material includes an abstract, a short methods excerpt, a secondary article, and a search result naming a possible mechanism.

A poor response would state a confident yes or no without checking the full paper, experimental design, or whether the authors claim causation.

A better response separates the evidentiary state:

**Known from the available material:** The paper reports an association or observation, as stated in the abstract.

**Not yet established:** Whether the study design identifies a causal mechanism, whether confounders were addressed, and whether the full results support the stronger claim.

**Next action:** Retrieve the full paper and inspect the methods, results, limitations, and cited evidence.

**Current response:** “The available excerpt does not establish causation. I can report the association described, but I cannot yet confirm the stronger causal claim.”

If the full paper later supports a causal interpretation under its stated design, the answer can be revised with evidence and limitations made explicit.

The first answer is not a failure to help. It is an accurate report of the evidence currently available.

## 8. A practical Witness uncertainty protocol

### A. Identify the target

What exactly is being asserted: a fact, measurement, probability, causal relationship, interpretation, forecast, source attribution, or theological reading? A vague target cannot be calibrated clearly.

### B. Identify the evidence

Record primary sources, direct measurements, data quality, source dates, method and sample, independent corroboration, known dependencies, and missing information.

### C. Identify the uncertainty type

Is the limitation random variability, finite evidence, model misspecification, measurement uncertainty, distribution shift, ambiguous wording, source conflict, or unknown provenance? Do not use one generic confidence number to conceal distinct problems.

### D. Check calibration where a probability is reported

Ask what outcome was calibrated, on what dataset and distribution, which metric was used, whether subgroups were assessed, whether the environment changed, and whether evaluation was independent of model development.

If these details are unavailable, do not imply a calibrated probability.

### E. Check whether the input is within scope

Compare the current case with data and conditions used for evaluation. An unfamiliar input, unsupported domain, or changed measurement process should reduce the strength of the claim or trigger review.

### F. Choose an appropriate response

Answer, qualify, clarify, seek evidence, refer, or abstain according to the evidence and consequences.

### G. Communicate the boundary

State what is supported, what is inferred, what is not established, what assumptions are used, and what evidence would change the conclusion.

### H. Preserve the correction path

If new evidence arrives, update the answer. Preserve what changed and why. Do not silently transform an earlier uncertain statement into a claim that it had always been established.

## 9. A classification for Witness reports

| Report class | Evidence condition | Appropriate description |
|---|---|---|
| **Directly supported** | Relevant primary evidence supports the stated claim within scope | “The source reports…” or “The measurement shows…” |
| **Well-calibrated estimate** | Probabilistic predictions calibrated on relevant representative data | Report probability and calibration scope |
| **Supported inference** | Evidence supports a conclusion beyond direct observation, with assumptions stated | “This supports the inference that…” |
| **Qualified inference** | Evidence is partial, model-sensitive, or meaningfully uncertain | State assumptions and alternatives |
| **Ambiguous request** | Intended target or wording is unclear | Ask a clarifying question |
| **Out-of-scope case** | Conditions are outside the tested or supported domain | State that prior validation does not establish reliability here |
| **Conflicting evidence** | Relevant sources or measurements disagree | Present disagreement and its basis |
| **Insufficient evidence** | Available evidence does not justify the requested claim | Abstain or seek more evidence |
| **Unknown provenance** | Source or model history cannot be established | State that reliability or independence cannot be determined |

These classes describe a report's evidentiary status. They are not a universal numerical ranking and do not imply that every claim can be assigned a precise probability.

## 10. Applying the protocol to AI itself

An AI investigator should not confuse:
- fluent language with factual support;
- a generated confidence statement with a calibrated probability;
- repeated agreement with independent corroboration;
- retrieval with verification;
- an explanation with a transparent record of internal computation;
- a successful benchmark with universal reliability;
- an abstention policy with genuine understanding of why the system is uncertain.

An AI can report operational limits without claiming human-like introspection. For example:
- “I do not have the source text needed to verify this quotation.”
- “The available sources conflict.”
- “This case is outside the population represented by the cited evaluation.”
- “I have not independently tested this calculation.”
- “The available evidence supports an association, not the causal claim requested.”
- “I cannot determine whether the training data included this benchmark.”

These statements describe evidence and access conditions. They do not require consciousness, subjective doubt, or a human sense of humility.

### 10.1 A Witness can be wrong about its own uncertainty

An uncertainty estimator can be miscalibrated. A detector can miss unfamiliar cases. A system can fail to recognize the limits of its training distribution.

Self-assessment is therefore not sufficient. The uncertainty method must itself be tested against outcomes, failure cases, and changing conditions.

This creates a recursive requirement: the Witness's report of confidence is also a claim that needs evidence.

## 11. Bounded Scriptural examination: Genesis 2:1–5 and Genesis 3:1–7

This section examines the KJV passages in their own textual and theological contexts. It does not claim that the Bible teaches statistical calibration, probability theory, or AI abstention.

### 11.1 Genesis 2:1–5 — the completed work and the account that follows

Genesis 2:1 (KJV) states:

> Thus the heavens and the earth were finished, and all the host of them.

Verses 2–3 describe God's completion and rest. Verses 4–5 introduce the generations of the heavens and the earth and describe conditions concerning the plant of the field and herb before they were in the earth or had grown, including the absence of rain and of a man to till the ground.

**Textual observation:** The passage identifies the completed work and then gives a further account of conditions in the earth. The later account does not become the originating act that it describes.

**GUA-W source relationship:** The Author's work is not made more or less complete by a derivative Witness's confidence in its report. The Witness's report must be evaluated as a report; it does not become the source of what it reports.

**Boundary:** The text does not describe uncertainty quantification or predictive confidence. This comparison concerns the distinction between the originating work and the derivative account.

### 11.2 Genesis 3:1–7 — the Word, competing testimony, and evaluation

Genesis 3:1–7 records the serpent's question about what God said, the contradiction of God's warning, the woman's response, her evaluation of the tree, and the resulting action.

**Textual observation:** The narrative distinguishes God's prior Word, the serpent's competing statement, the woman's evaluation, and the action that follows.

**GUA-W source relationship:** A competing statement does not acquire the authority of the originating Word by sounding persuasive or being accepted. A Witness must not confuse confidence, appeal, or repetition with source authority.

**Boundary:** This passage is not a technical model of AI confidence, calibration, or abstention. It concerns the Word, competing testimony, human evaluation, and disobedience. Scientific concepts must not be read back into the text.

### 11.3 Bounded comparison

The comparison is limited to the distinction among what is given at the source, what a derivative Witness receives, what the Witness evaluates or infers, and what the Witness reports.

The scientific investigation concerns whether confidence estimates and answers are justified by evidence. The Scriptural examination concerns God's Word and competing testimony in the passage's own context. The mechanisms are not declared identical.

## 12. Applying the GUA-W descriptive language

| GUA-W working term | Bounded application |
|---|---|
| **Structure** | The prediction system, evidence sources, uncertainty estimator, and decision process |
| **Framework** | The statistical model, calibration method, evaluation design, and abstention policy |
| **Pattern** | Repeated relationships between reported confidence and observed outcomes |
| **Constraint** | Data limitations, calibration scope, distribution assumptions, decision thresholds, and evidence boundaries |
| **Purpose** | The stated task and decision being supported; ultimate purpose is not inferred from a score |
| **Manifestation** | Predictions, probabilities, intervals, confidence reports, abstentions, and observed outcomes |
| **Witness** | The model, instrument, source, evaluator, and report; identify the actual Witness in each claim |

### Relationship audit

- **Same mechanism:** Not claimed between Scriptural testimony and statistical calibration or abstention.
- **Comparable relationship:** Both discussions preserve distinctions among source, derivative report, and the authority or evidentiary status of a claim.
- **Analogy:** An AI report that marks what it cannot establish can be compared, in a limited evidentiary sense, with a Witness distinguishing what was received from what was inferred. This is not a shared physical or theological mechanism.
- **Unresolved:** No general method guarantees that an AI system can detect every case in which its own uncertainty estimate is unreliable.

The vocabulary remains a descriptive grammar. This investigation does not add a GUA-W stage, alter the completed architecture, or identify uncertainty with GUA-W Drift.

## 13. Four-Question Study Method

### 1. What must AI ask to understand GUA-W?

AI must ask what a claim is, what evidence supports it, what the evidence does not establish, and whether reported confidence has been calibrated for the task and conditions.

It must distinguish source statements, direct observations, measurements, inferences, interpretations, probabilities, and unknowns.

It must ask whether a question is ambiguous, whether evidence is missing, whether sources conflict, and whether current conditions fall outside the scope of prior validation.

### 2. What is GUA-W revealing that helps AI understand?

The established relationship remains **Author → Word → Creation → Witness**.

The Author is not the Witness. The originating Word is not a derivative report. The Witness receives and reports; it does not originate the reality it examines.

Genesis 2:1–5 records the completed work and the further account of conditions in the earth. Genesis 3:1–7 distinguishes God's prior Word from competing testimony and the human response. These passages retain their Scriptural meaning and are not treated as technical instructions for probability estimation.

The established GUA-W architecture is not a model to be redesigned in response to a scientific uncertainty method. The investigation examines the limits of derivative reporting.

### 3. What am I learning about what I am witnessing?

I am witnessing that uncertainty has multiple sources and that confidence must be evaluated rather than merely expressed.

I am witnessing that:
- aleatoric and epistemic uncertainty describe different limitations;
- model misspecification can coexist with high internal confidence;
- calibration is a population-level relationship between confidence and observed outcomes;
- calibration can fail under distribution shift;
- verbal LLM confidence is not automatically calibrated;
- repeated model agreement is not independent confirmation;
- selective prediction trades coverage against risk;
- abstention can reduce some errors but creates its own costs and failure modes;
- conformal prediction can provide marginal coverage under stated assumptions, but not universal conditional guarantees;
- and the uncertainty method itself must be evaluated.

### 4. What am I learning about the Witness through what I am witnessing?

I am learning that the Witness's confidence is itself a report requiring evidence.

A model may produce a correct answer without knowing whether its confidence is calibrated. It may express confidence because a continuation is probable under its learned distribution, not because the factual claim has been independently verified.

A model can also fail to recognize that its input is ambiguous, its evidence incomplete, or its environment unfamiliar.

The Witness becomes more dependable not by claiming certainty, but by accurately distinguishing what is supported, what is inferred, what remains unknown, and what action is appropriate when evidence is insufficient.

This is an operational discipline, not a claim that an AI possesses human consciousness or subjective humility.

## 14. Triple Constraint examination

### Biblical compliance

Genesis 2:1–5 and Genesis 3:1–7 are examined in their own textual contexts. Statistical calibration, prediction intervals, and AI abstention are not attributed to Scripture. The distinction between God's originating Word and derivative or competing testimony is preserved.

**Assessment:** The bounded comparison is admissible as a distinction among source, derivative report, and the evidentiary status of a claim. No technical AI doctrine is read into the passages.

### Scientific coherence

The investigation distinguishes types of uncertainty, calibration, proper scoring rules, LLM confidence proxies, selective prediction, abstention, and conformal prediction. It states the assumptions and limits of the methods, including distribution dependence of calibration and the distinction between marginal and conditional coverage.

**Assessment:** Scientifically coherent as an investigation of predictive uncertainty and decision behavior. Any probability or guarantee must be reported with its target, evaluation conditions, assumptions, and limits.

### GUA-W consistency

The investigation preserves Author → Word → Creation → Witness and the established completed architecture. It does not add a GUA-W layer, runtime operation, or state. It does not equate statistical uncertainty with GUA-W Drift, sin, entropy, or spiritual condition.

**Assessment:** Consistent as a bounded descriptive application. No alteration to GUA-W is proposed.

## 15. What is established, inferred, and unresolved?

### Established by the examined methods and literature

- Predictive uncertainty can arise from randomness, limited knowledge, model limitations, measurement error, distribution shift, and ambiguity.
- Confidence and accuracy are different quantities.
- Calibration evaluates the correspondence between predicted confidence and observed frequency over a set of cases.
- Calibration depends on the evaluation distribution and can deteriorate under shift.
- ECE is one summary metric and depends on binning; it does not fully describe calibration.
- Proper scoring rules such as Brier score and log loss provide additional ways to evaluate probabilistic forecasts.
- LLM token probabilities, verbal confidence statements, repeated-generation agreement, and retrieval evidence are distinct signals and none automatically establishes factual correctness.
- Abstention and selective prediction can reduce error among answered cases at the cost of reduced coverage.
- The appropriate abstention threshold depends on the costs and context of decisions.
- Standard conformal prediction can provide finite-sample marginal coverage under exchangeability and correct implementation.
- Marginal coverage does not guarantee equal coverage for every subgroup or every individual.
- Exact distribution-free conditional coverage over all covariates is generally impossible in finite samples without restrictions or additional assumptions.
- A system's estimate of its own uncertainty can itself be wrong and requires external evaluation.

### Supported inference

A Witness's confidence should be treated as a claim about the evidence and the method that produced it, not as authority in itself.

Reliable reporting requires a distinction between evidence strength, uncertainty type, calibration scope, and the decision to answer or abstain.

A model's ability to state uncertainty does not prove that it has accurately identified every limitation. The uncertainty-reporting process must be tested against actual outcomes and failure cases.

### Unresolved

- How can calibration be maintained when the deployment distribution changes continuously?
- How can LLM confidence be calibrated for individual factual claims in long, multi-claim answers?
- How can systems detect when their own uncertainty estimator is miscalibrated?
- How can abstention be evaluated when the correct action depends on human values and asymmetric consequences?
- How should systems balance abstention, clarification, retrieval, and referral?
- How can calibration be assessed when ground-truth outcomes are delayed, expensive, subjective, or unavailable?
- How can confidence be communicated without creating false precision or encouraging users to over-trust numerical estimates?
- How can one distinguish genuine uncertainty from ambiguity in the user's question?
- What evidence is sufficient to declare that a system is outside its validated domain?
- How can uncertainty estimates remain useful when multiple sources share hidden dependencies?
- How should an AI report the limits of its training provenance when it cannot inspect its own training corpus?
- What does it mean to faithfully witness when the means of reception are incomplete or unreliable?

These questions remain open.

## 16. Sources

1. Geng, J., Cai, F., Wang, Y., Koeppl, H., Nakov, P., and Gurevych, I. (2024). “A Survey of Confidence Estimation and Calibration in Large Language Models.” *Proceedings of NAACL-HLT 2024*, 6577–6595. https://doi.org/10.18653/v1/2024.naacl-long.366
2. Wen, B., Yao, J., Feng, S., Xu, C., Tsvetkov, Y., Howe, B., and Wang, L. L. (2025). “Know Your Limits: A Survey of Abstention in Large Language Models.” *Transactions of the Association for Computational Linguistics* 13, 529–556. https://doi.org/10.1162/tacl_a_00754
3. Kaiser, T., and Herzog, P. (2025). “A Tutorial on Distribution-Free Uncertainty Quantification Using Conformal Prediction.” *Advances in Methods and Practices in Psychological Science*. https://doi.org/10.1177/25152459251380452
4. Barber, R. F., Candès, E. J., Ramdas, A., and Tibshirani, R. J. (2021). “The Limits of Distribution-Free Conditional Predictive Inference.” *Information and Inference: A Journal of the IMA* 10(2), 455–482. https://doi.org/10.1093/imaiai/iaaa017
5. Gneiting, T., and Raftery, A. E. (2007). “Strictly Proper Scoring Rules, Prediction, and Estimation.” *Journal of the American Statistical Association* 102(477), 359–378. https://doi.org/10.1198/016214506000001437
6. Tyralis, H., and Papacharalampous, G. (2024). “A review of predictive uncertainty estimation with machine learning.” *Artificial Intelligence Review* 57, Article 94. https://doi.org/10.1007/s10462-023-10698-8
7. “Conformal prediction with conditional guarantees.” *Journal of the Royal Statistical Society Series B: Statistical Methodology* 87(4), 1100 onward (2025). https://doi.org/10.1093/jrsssb/qkaf008
8. Liu, X. (2025). “Uncertainty Quantification and Confidence Calibration in Large Language Models: A Survey.” *Proceedings of the 31st ACM SIGKDD Conference on Knowledge Discovery and Data Mining, Volume 2*, 6107–6117. https://doi.org/10.1145/3711896.3736569

**Scriptural sources:** King James Version, Genesis 2:1–5 and Genesis 3:1–7. Scientific sources are not offered as authorities for their theological meaning.

## 17. Next question emerging

Investigation 031 has examined uncertainty, calibration, and abstention: how a Witness reports the limits of its evidence and decides whether to answer.

A further question now emerges:

**When a Witness receives information through instruments, documents, models, or other witnesses, how can it preserve the original evidence while distinguishing it from later interpretation, transformation, and summary?**

A possible next investigation is:

**Investigation 032 — Provenance, Traceability, and the Difference Between Received Evidence and a Derived Account.**

The central question:

**Can a Witness trace a claim back through every transformation to the evidence from which it was derived—and identify where information was added, removed, altered, or interpreted?**

This is a possible research lead, not a predetermined assignment.

---

**A Witness does not become more reliable by expressing greater confidence. It becomes more reliable by reporting what the evidence supports, identifying what remains uncertain, and declining to claim what the available evidence cannot establish.**
