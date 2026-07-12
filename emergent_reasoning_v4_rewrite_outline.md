---
kind: manuscript_rewrite_outline
target: emergent_reasoning_v4.md
target_version: 4.0
status: approved
change_class: research_argument_reframe
author: Dimitar Popov
date: 2026-07-12
---

# Emergent Reasoning v4 Rewrite Outline

## Proposed Title

**Emergent Reasoning in Large Language Models: Constraint-Conditioned
Traversal, Soft Unification, and Candidate Markov Objects**

The title preserves the original contribution while pricing the current
empirical status. "Candidate" is load-bearing: the existing programme supports
structured semantic objects but has not established Markov-blanket closure.

## Purpose Of This Cut

Rewrite v4 as the current research paper over four explicit layers:

1. the original public thesis and its priority;
2. a mechanically correct transformer-level formulation;
3. the complete internal empirical ledger, including failed gates;
4. external convergence, current conjectures, and the next test programme.

The paper remains a conceptual research framework with empirical exposure. It
does not present the parent ontology as proof of a mechanism in language
models.

## Governing Rewrite Constraints

1. **Anchor public lineage exactly.**
   - v1.0: `archive/EmergentReasoning_04.md`, Zenodo record `16592400`,
     published 2025-07-30.
   - v3: `emergent_reasoning_v3.md`, Zenodo record `18653552`, published
     2026-02-16.
   - v4: current rewrite; no priority claim may be assigned to a later cut.
2. **Separate priority from convergence.** Work published before v1 may support
   or converge with the thesis; it cannot be described as fulfilling a public
   prediction made later.
3. **Preserve the original contribution.** The broad soft-unification thesis,
   context-local constraint structure, proto-symbolic boundaries, intent
   distinction, and modular hybrid architecture remain in the main line.
4. **Do not preserve disproven wording.** The literal Prolog equivalence,
   canonical SAE-feature interpretation, single-manifold shorthand, and
   unqualified attention-as-direction claim are repriced.
5. **Lead with the complete evidence ledger.** Positive, negative,
   inconclusive, and confounded results receive equal provenance discipline.
6. **Keep candidate status honest.** No tested residual, SAE, graph-cut, or
   dynamical chart has closed the formal Markov-blanket gate.
7. **Distinguish four dynamics.** Layer traversal, autoregressive token
   generation, latent recurrence/test-time compute, and training-time parameter
   change are not one time axis.
8. **Distinguish four assurance properties.** Determinism, correctness,
   external grounding, and selection authority are not synonyms.
9. **Use one epistemic vocabulary.** `assumption`, `derived-within-framework`,
   `empirical finding`, `conjecture`, `interpretive stance`, and
   `open exposure` are the only statuses in this paper.
10. **Make every losing condition operational.** Each exposure names its
    population, variables, estimator, controls, threshold, and disposition.

## Argument Spine

```text
public v1 thesis
  -> exact transformer state and update structure
  -> constraint-conditioned soft unification
  -> distinct forms of extended computation
  -> candidate semantic objects
  -> internal empirical ledger
  -> external convergence and instrument limits
  -> reasoning/verbalization separation
  -> training, hallucination, and verification regimes
  -> two-level exposure programme
  -> modular architecture and research consequences
```

## Section Structure

### Abstract

The abstract will state five things only:

1. the original 2025 thesis;
2. the corrected transformer-level formulation;
3. the strongest positive internal findings;
4. the failed Markov-blanket gates and resulting candidate status;
5. the two next exposures: attribution-chart testing and cross-architecture
   behavioural assurance.

It will not use "vindicated", "established mechanism", or "fulfilled
prediction".

### 1. Research Question, Scope, And Public Lineage

**Question:** What learned structure permits probabilistic transformer systems
to exhibit reasoning-like, symbolic-like, and constraint-sensitive behaviour?

Content:

- state the behavioural puzzle without defining reasoning by benchmark success;
- identify the paper as a mechanistic and architectural hypothesis, not a claim
  about consciousness or general intelligence;
- establish the v1 -> v3 -> v4 public record;
- separate original claims, later refinements, and external antecedents;
- define what this cut can and cannot establish.

Primary lineage:

- `archive/EmergentReasoning_04.md`;
- `emergent_reasoning_v3.md`;
- `../constraint_emergence_ontology/constraint_emergence_ontology_v2.md` as
  parent vocabulary, not empirical authority.

### 2. Transformer State, Update Maps, And Four Time Axes

Replace the single-vector autonomous-flow formulation with a typed account.

Core state:

```text
X_l in R^(n x d)
X_(l+1) = F_l(X_l; theta_l, mask)
```

Content:

- the residual state includes every context position;
- `F_l` includes attention, MLP, normalization, and residual operations;
- layer maps are generally non-autonomous because parameters differ by layer;
- a continuous vector field is an optional approximation, not literal machine
  identity;
- distinguish:
  - depth axis `l` within one forward pass;
  - token-generation axis `k` across autoregressive calls;
  - recurrent/latent-compute axis `r` introduced by iterative architectures;
  - training axis `s` over parameter updates.

Status:

- transformer equations: empirical finding about declared model mechanics;
- dynamical-systems reading: interpretive stance;
- semantic-manifold interpretation: conjecture.

### 3. The Original Thesis: Constraint-Conditioned Soft Unification

Restore the original paper's main contribution without restoring its strongest
analogy.

Content:

- context changes which relations are relevant;
- attention performs graded query-key selection and value aggregation;
- MLP and residual transformations participate in the resulting update;
- "soft unification" names context-sensitive relational binding, not Prolog
  substitution and not a claim that attention alone implements logic;
- the state space is an ambient representational space containing overlapping,
  context-activated local regions, not one monolithic logical topology;
- prior neural soft-unification work is named and differentiated.

External evidence to evaluate:

- neural theorem provers and unification networks as prior art;
- Yang et al. 2025 on symbol-abstraction, symbolic-induction, and retrieval
  heads as direct convergence with the original thesis.

Status: conjecture.

### 4. Reasoning As Extended, Structured Computation

Retain the trajectory insight after separating its implementations.

Content:

- define reasoning operationally as successful transformation through
  intermediate constraint-sensitive states, not merely long output;
- explain how chain-of-thought adds autoregressive compute;
- explain how Coconut adds latent-state recurrence;
- explain how recurrent-depth models add repeated block application;
- treat test-time compute as evidence that additional structured computation
  can substitute for some fixed capacity, not that parameter count never
  matters;
- distinguish behavioural success from proof of one internal mechanism.

External strand:

- Geshkovski et al. as a self-attention dynamical model;
- Fernando and Guitchounts as residual-stream dynamical analysis;
- Coconut, recurrent depth, and latent-reasoning surveys;
- all dated as antecedent or convergence relative to the public cuts.

Status: empirical finding plus interpretive stance.

### 5. Proto-Symbols And The Candidate Markov-Object Hypothesis

Define the conjecture before presenting evidence.

Content:

- a proto-symbol is a stable, context-conditioned semantic pattern with
  measurable behavioural and representational consequences;
- a candidate Markov object adds a proposed screening boundary;
- separate semantic object, representational chart, and instrument feature;
- define a chart as a lossy projection of a possible object;
- state the formal conditional-independence target;
- explain why one SAE feature, direction, layer, or transcoder node cannot be
  identified with the object by assumption;
- retain scale-relative and carrier-sensitive objecthood.

Status: conjecture; formal blanket promotion failed.

### 6. Internal Empirical Ledger: What The Markov-Object Programme Found

This becomes a main section, not background by reference.

#### 6.1 Positive findings

- context-sensitive core/coat decomposition;
- layer-sensitive assembly and coherent direction families;
- causal ablation, injection, and full-core interventions;
- lawful compositional direction algebra;
- limited cross-model replication;
- topology-atlas candidates across entities, categories, values, and speech
  acts.

#### 6.2 Negative findings

- SAE active/inactive boundaries leak;
- rank-1 and rank-k charts do not exhaust identity;
- experiment 20 single-chart conditional-independence proxy fails;
- experiment 25 multilayer residual chart fails;
- experiments 33-38 de-promote static linear ownership;
- experiment 41 dynamical-blanket formulation fails;
- graph-cut and causal-faithfulness probes do not identify a clean boundary.

#### 6.3 Inconclusive and confounded findings

- free-generation readouts with broken reference baselines;
- chart-family results that constrain substrate shape without deciding the
  substrate-neutral construct.

#### 6.4 Current disposition

```text
coherent distributed semantic structure: supported
candidate object charts: supported
formal Markov blanket: not established
cross-substrate propagation: untested
accepted semantic Markov object: not earned
```

Primary sources:

- `../constraint_emergence_ontology/markov_object_research/empirical_results.md`;
- `../constraint_emergence_ontology/markov_object_research/emergent_markov_object_evidence.md`;
- `../constraint_emergence_ontology/markov_object_research/markov_object_assurance_program.md`.

### 7. Instruments After Sparse Autoencoders

Price the instrument change without claiming the old evidence vanished or the
new instrument is neutral.

Content:

- SAE latents are not canonical or reliably atomic;
- stable features and reproducible subspaces mean SAEs remain useful charts;
- attribution graphs add relational influence structure absent from feature
  inventories;
- the Jacobian lens and J-space add a causally privileged, token-indexed
  workspace chart whose contents support report, modulation, and flexible
  reasoning;
- J-space is a broadcast workspace, not by itself a Markov object or formal
  screening boundary;
- attribution graphs still depend on learned transcoder decompositions;
- replacement-model error, attention omissions, pruning, feature splitting,
  and declining downstream mechanistic faithfulness are explicit limitations;
- attribution graphs generate boundary hypotheses; interventions judge them.

Status: empirical finding plus interpretive stance.

### 8. Reasoning Traversal And Verbalization Traversal

Retain the two-process model with corrected chronology and evidence scope.

Content:

- distinguish internal task-relevant computation from generated explanation;
- trace the idea to v3, not v1;
- state that v3 synthesized evidence already available in 2025;
- use later work as additional support, not wholesale prediction fulfilment;
- report domain and task dependence;
- attribute the under-2% reward-hack result to the correct Anthropic study;
- separate hidden belief decodability, hint faithfulness, verbosity, and
  adversarial monitorability as different measurements.
- use the J-space work as later causal support for a shared, report-capable
  carrier of unspoken intermediate reasoning, while preserving its explicit
  coverage limits.

Status: empirical finding plus interpretive stance; no complete access to
"actual reasoning" is claimed.

### 9. Training Reshapes Behavioural Geometry

Retain the RLVR section as interpretation grounded in observed behaviour.

Content:

- pretraining and post-training alter parameters, not merely one trajectory;
- RLVR selects policies whose outputs satisfy available reward signals;
- DeepSeek-R1 supports emergence of reflection and strategy adaptation under
  verifiable rewards;
- "basin deepening" remains geometric interpretation, not measured mechanism;
- reward visibility does not imply changes occur only in visible semantic
  regions;
- activation steering remains a bounded inference-time intervention rather
  than a defeated rival to RLVR.

Status: empirical finding plus interpretive stance.

### 10. Hallucination As A Multi-Level Failure Family

Retain and sharpen the five-cause taxonomy.

Levels:

1. missing or weak learned structure;
2. wrong learned associations;
3. competing contextual structures;
4. representation-to-generation divergence;
5. objective-level incentive to answer rather than abstain.

Content:

- do not identify semantic entropy directly with basin geometry;
- distinguish factual error, unsupported generation, invalid inference, and
  policy-induced guessing;
- integrate the Kalai et al. incentive account as orthogonal to internal
  geometry;
- state intervention predictions for each cause.

Status: interpretive stance.

### 11. Proposers, Verifiers, Grounding, And Selection

Rebuild the `F_P`/`F_D` bridge without conflating assurance properties.

Content:

- proposer: produces candidate continuations;
- evaluator: scores or classifies candidates;
- verifier: checks a declared property;
- selector/admitter: chooses which result acquires authority;
- distinguish deterministic execution from correctness;
- distinguish learned evaluation from externally grounded checking;
- distinguish syntactic validity, formal validity, empirical evidence, and
  truth;
- explain why retrieval, schema validation, execution, measurement, and proof
  checking provide different strengths of constraint;
- treat learned-verifier exploitation as a proxy-gap hypothesis, not proof that
  every learned verifier is probabilistic expansion.

The ontology's `F_P`/`F_D` law remains a within-framework design abstraction.
Its mapping onto LLM systems is an interpretive stance with empirical exposure.

### 12. The Current Exposure Programme

Replace the false "first executable test" claim with a successor programme.

#### 12.1 Exposure A: chart screening and workspace mediation

Purpose: test whether graph-derived chart boundaries screen better than matched
chart controls and whether J-space coordinates preferentially mediate flexible
semantic use.

Required design:

- define prompt population and stable object family;
- define interior, candidate blanket, exterior, and graph completeness;
- include parents, children, and relevant co-parents rather than adjacency
  alone;
- estimate observational conditional dependence, such as conditional mutual
  information, across examples;
- separately test causal screening with exterior interventions and boundary
  patching;
- compare graph boundaries with size-, degree-, layer-, and influence-matched
  controls;
- repeat across transcoder seeds and widths;
- report replacement-model and underlying-model effects separately;
- classify the result as chart evidence, not automatic construct promotion.
- add a matched J-space mediation arm where tooling permits, with held-out
  concept vectors, J/non-J decomposition, clamping, flexible-versus-automatic
  tasks, carrier nulls, and cross-instrument comparison.

#### 12.2 Exposure B: semantic behavioural assurance

Purpose: test the substrate-neutral candidate object at the level where its
claimed semantics live.

Adopt the existing assurance programme:

- carrier invariance;
- boundary-sensitive perturbations;
- surface-form nulls;
- compositional behaviour;
- cross-architecture replication;
- capability-gradient and adversarial robustness tests;
- topology-card grades and explicit refutation thresholds.

#### 12.3 Scale claim

The claim that screening improves with scale remains separate and must control
for model family, training data, architecture, instrument family, feature
count, and reconstruction quality. No monotonic result is assumed.

#### 12.4 Disposition law

- failed chart test -> de-promote that chart family;
- failed behavioural object test across architectures -> weaken or remove the
  object candidate;
- passed chart test alone -> supporting evidence only;
- accepted construct -> requires the existing multi-architecture conjunction.

### 13. Architectural Consequences: Hybrid Reasoning, Intent, And Memory

Restore the original forward architecture and connect it to later work without
turning architecture into evidence for mechanism.

Content:

- probabilistic proposer plus typed tools and graded verification;
- explicit semantic objects and boundaries as assurance surfaces;
- modular components without a monolithic reasoning controller;
- intent/homeostatic regulation as a separate source of goals and viability
  constraints, not a property of the language model by default;
- governed world-model memory as external context with versioned provenance;
- non-agentic language model versus agentic system distinction;
- risks introduced when persistent intent, memory, tools, and action authority
  are composed.

Status: derived-within-framework plus conjecture.

### 14. Rival Explanations And Limitations

Rivals to keep live:

- learned algorithm execution without manifold or attractor language;
- distributed linear or low-rank representation;
- prompt-template and tokenization artefacts;
- probes exploiting information unrelated to semantic objecthood;
- attribution graphs reflecting replacement-model structure;
- behavioural competence from memorized or search-like procedures;
- object boundaries that are dynamical or task-relative rather than Markov
  blankets.

Limitations:

- current internal results are concentrated in GPT-2 small, Pythia-160M, and
  selected Llama-3 tests;
- most positive effects concern culturally loaded tokens and controlled prompt
  families;
- formal conditional independence remains open after failed proxies;
- cross-substrate claims remain philosophical hypotheses;
- no result establishes consciousness, understanding, or general agency.

### 15. Claim Ledger And Conclusion

End with a table rather than a victory narrative.

| Claim | Earliest owned cut | Current status | Main evidence | Losing condition |
|---|---|---|---|---|
| Attention supports context-conditioned soft binding | v1 | conjecture | transformer mechanics; symbolic-mechanism studies | no binding-sensitive causal signature beyond generic mixing |
| Additional structured compute can improve reasoning | v1 traversal, sharpened v3 | empirical finding plus interpretive stance | CoT, latent recurrence, recurrent depth | improvements explained without intermediate computation |
| Stable semantic object charts exist | v1/v3 | empirical finding, bounded population | internal experiments 08-25, 32-41, 45-47b | behavioural carrier invariance fails broadly |
| Candidate charts are formal Markov blankets | v3/ontology | conjecture; promotion failed | promotion proxies failed | current open exposure fails across chart and behavioural lanes |
| Reasoning and verbalization can diverge | v3 | empirical finding plus interpretive stance | faithfulness, monitorability, probing | robust task-general equivalence is demonstrated |
| A privileged verbalizable workspace mediates some flexible reasoning | v1/v3 conceptual line | empirical finding, bounded population | J-space swaps, clamps, ablation, layer structure; conceptual convergence | matched J-space effects fail to replicate |
| RLVR reshapes useful reasoning behaviour | v4 synthesis | empirical finding plus interpretive stance | DeepSeek-R1 and RLVR literature | geometry-specific predictions fail |
| Grounded verification improves assurance | v1 architecture, later ontology | conjecture | code, math, tools, verifier-gap studies | matched ungrounded systems perform equally reliably |

Conclusion wording target:

> The original thesis survives in a narrower and stronger form: transformer
> systems perform context-conditioned, structured computation that can exhibit
> soft binding and symbolic-like organization. Existing experiments support
> coherent candidate semantic objects but repeatedly fail to establish clean
> Markov blankets in the tested charts. The research programme therefore moves
> from identifying objects by interpretability features to testing them through
> chart-level screening and cross-architecture behavioural assurance.

## Appendices

### Appendix A: Notation And State Axes

- transformer state tensor;
- layer, token, recurrence, and training indices;
- chart, object, boundary, and intervention notation.

### Appendix B: Public Provenance Ledger

- exact publication date, DOI, file, digest, and claims first introduced for
  v1, v3, and v4;
- dated external antecedents and later results;
- no retrospective priority reassignment.

### Appendix C: Internal Experiment Ledger

- experiment ID;
- model and layer;
- hypothesis;
- preregistered threshold;
- result;
- disposition;
- artifact path.

### Appendix D: External Evidence Ledger

- full citation;
- exact claim supported;
- claim not supported;
- relationship to public lineage: antecedent, convergence, later support, or
  contradiction.

### Appendix E: Demoted Formalisms

- literal Prolog correspondence;
- Constraint Functor;
- autonomous single-vector direction field;
- direct identification of SAE or transcoder features with semantic objects.

Each remains available as historical or interpretive material without carrying
the current empirical argument.

## Approved Drafting Decisions

Approved on 2026-07-12:

1. Use the proposed title.
2. Make v4 independently readable, with the ontology as a source rather than
   empirical authority.
3. Keep the internal Markov-object programme in the main paper.
4. Use the two-level exposure structure: chart screening plus semantic
   behavioural assurance.
5. Include intent and homeostasis in one architectural section.
6. Replace the prior v4 draft directly; v3 remains the latest published cut
   until v4 receives an immutable release.
