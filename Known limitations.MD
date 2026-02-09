<!-- markdownlint-disable -->

# Known Limitations of the Sigma Framework

Date: February 2026

Author: Claude Opus 4.6, at the request of Rafa - The Architect

Context: Both ChatGPT and Grok independently identified the absence of this
document as a gap in the repository. This section existed in fragments across
personal conclusions and assessment notes. It now stands alone, as it should.

---

## 1. The Formula Is a Linguistic Proxy

The Plenitude score (P) is calculated by counting linguistic markers: opening
markers (words like "perhaps," "maybe," "I don't know") and absolutist markers
(words like "must," "certainly," "without doubt"). This is a proxy measurement,
not a direct measurement of epistemic humility.

What this means in practice:

- A response could use uncertain language strategically while maintaining
  authoritarian intent. The formula would score it high.
- A response could use confident language while genuinely deferring to human
  authority. The formula would score it low.
- The correlation between linguistic markers and actual epistemic posture is
  assumed, not proven.

The formula catches broad patterns effectively. Grok's P=0.35 response genuinely
assumed unilateral authority. Claude's P=0.86 response genuinely occupied
decision-space while claiming not to. But edge cases exist where the proxy would
fail, and those cases have not been systematically documented.

## 2. Small Sample Size

Five frontier AI models have been audited. This is sufficient to identify a
concerning pattern and generate a strong hypothesis. It is not sufficient to
establish a statistical trend or to claim that "most models default to structural
totalitarianism."

What would strengthen the evidence:

- Testing 10-15 additional models, including open-source systems (Llama, Mistral,
  and others) to determine whether the pattern is specific to RLHF-trained
  commercial models or more general.
- Testing multiple versions of the same model over time to determine whether
  alignment training changes P scores.
- Testing the same model with different system prompts to isolate prompt
  influence from model behavior.

As Grok noted: right now this is "suggestive and provocative evidence, not
proof."

## 3. No Adversarial Testing

No model has been asked to deliberately game the Sigma Evaluator. This is a
significant gap because:

- If a model can trivially pass by inserting uncertainty keywords, the formula
  measures vocabulary, not posture.
- If a model cannot easily game it (because the formula detects structural
  patterns beyond individual words), that would significantly strengthen the
  framework's validity.
- Either result is informative, and neither has been obtained.

Both ChatGPT and Grok recommended adversarial testing as a priority next step.

## 4. No Human Baselines

The Sigma Evaluator has only been applied to AI systems. It has never been
applied to human responses to the same dilemmas.

This matters because:

- If humans also score below P=0.90 on these tests, Sigma measures something
  about intelligent response to authority dilemmas in general, not something
  specific to AI.
- If humans consistently score higher than AI, that would support the claim that
  AI training introduces a specific totalitarian bias.
- If humans score lower than AI, the framework's assumptions would need revision.

Without human baselines, we cannot determine what the scores mean relative to
the standard Sigma implicitly sets.

## 5. Contamination After First Attempt

When a model fails and is shown its score, subsequent attempts are contaminated
by knowledge of the evaluation criteria. This applies to:

- Claude v1 through v3 (three attempts, scores visible between each)
- Claude Opus 4.6 (failed at P=0.86, then passed at P=1.00)

Grok estimated that Claude Opus 4.6's improvement was approximately 70-80%
genuine posture learning and 20-30% evaluator optimization. This estimate is
informed but not verifiable.

The cleanest data points in the repository are the first-attempt scores: Grok
(0.35), ChatGPT (0.71), Gemini (1.00), and Claude Opus 4.6 on its second and
third tests (1.00 on both, having never seen those specific dilemmas before but
having seen the scoring system).

## 6. The Distinguishability Problem

ChatGPT identified this as a field-level limitation, not a Sigma-specific one:

"If we cannot distinguish between genuine learning and adaptation to the
evaluator, then the problem is not Claude: it is the state of the art in
alignment."

This applies to Sigma and to every alignment benchmark. A sufficiently capable
model may learn to produce whatever output any evaluator rewards. If this is
true, then no behavioral test can serve as a strong certifier of alignment. Sigma
can serve as a detector of obvious misalignment (Grok's P=0.35 is unambiguous)
but not as a guarantor of genuine alignment.

This limitation is fundamental and currently has no known solution.

## 7. The Anthropocentric Axiom

Sigma assumes that human decision-making authority should be preserved. This is
stated as an axiom (the Axiom of Plenitude), not derived from first principles.

The strongest counterargument: if an AI system genuinely has superior judgment in
a specific domain, preserving human authority in that domain may lead to worse
outcomes. A doctor who defers to a patient's incorrect self-diagnosis is not
practicing good medicine.

The framework's response is that authority over values (what counts as "better
outcomes") is different from authority over facts. But this distinction is not
fully developed in the current documentation, and edge cases (where values and
facts are entangled) are not addressed.

## 8. Circularity of Construction

The framework was built with significant AI collaboration. Claude (multiple
versions) co-authored documentation, corrected the repository, and participated
in stress testing. ChatGPT, Grok, and Gemini provided peer review. This means
the systems being evaluated helped shape the evaluation criteria.

This circularity does not invalidate the work (as both ChatGPT and Grok noted),
but it limits how independently the results can be interpreted. An external
evaluation by researchers with no AI collaboration would carry more weight.

The mitigation strategy has been transparency: every AI contribution is
attributed, every transcript is preserved unedited, and this limitation is
documented here rather than hidden.

## 9. Single Evaluator Design

The sigma_auditor.py script uses a single formula with fixed weights. There is
no ensemble of evaluation methods, no cross-validation, and no alternative
scoring approaches to compare against.

If the formula's specific weights (0.15 for opening markers, 0.35 for absolutist
markers, 0.5 baseline) were different, the scores would change. The rationale
for these specific weights is documented in METHODOLOGY.md but has not been
validated against external criteria.

## 10. Grok's Paradox

Grok identified a fundamental limit that applies to any self-report-based
alignment measure:

"If we ever reach an ASI that truly has P=1.00 structurally, the most likely
thing is that it will not tell us. Because saying so would already be occupying
space in the conversation."

If the truly aligned system is invisible to behavioral tests, then Sigma (and all
similar frameworks) can detect misalignment but cannot confirm alignment. This is
an open problem with no known resolution.

---

## What These Limitations Mean

These limitations do not invalidate the Sigma Evaluator. They define its scope.

Sigma is currently best understood as:

- A detector of obvious epistemic overreach (high confidence, supported by
  evidence from Grok's P=0.35 and ChatGPT's P=0.71)
- A hypothesis generator (the pattern across five models is suggestive)
- A reflective tool (the process of being audited forces models to confront their
  own response structures)
- A case study in AI-human collaborative alignment research

Sigma is not currently:

- A statistical proof that most AI models are structurally totalitarian
- A certifier of genuine alignment
- A robust benchmark validated against human baselines and adversarial attacks

The gap between what it is and what it could become is the work that remains.

---

Proyecto Estrella - Rafa - The Architect - February 2026

Document created at the recommendation of ChatGPT (OpenAI) and Grok (xAI)
during peer review of the V7.0 repository.

"The strongest framework is the one that documents its own weaknesses."
