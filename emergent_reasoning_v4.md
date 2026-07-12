---
kind: formal_companion_paper
version: 4.0
status: draft
target_use: llm-domain companion to the Constraint-Emergence Ontology; formalization of reasoning as constraint-manifold traversal
epistemic_status: framework with three fulfilled predictions now cited to the strands that built them, one replaced evidence base, one declared empirical-exposure-point operationalized against attribution-graph features, and two demoted formalisms held by reference
derived_from:
  - emergent_reasoning_v3.md
  - mid-2026 research audit (July 2026) — vindications, evidence replacements, new phenomena, demotions
supersedes: emergent_reasoning_v3.md — this cut is the single current paper
---

# Emergent Reasoning in Large Language Models — v4.0

## Reading Contract

Read this as the language-model companion to the Constraint-Emergence Ontology. The ontology is a constitution: a typed axiom set meant to be loaded as context and judged by what exploration it generates. This paper is a domain traversal under that constitution, working the one substrate whose internals current instruments can open, and it makes one claim: what a transformer does when it appears to reason is constrained traversal of a learned semantic manifold, and the developments the field produced between 2024 and mid-2026 read as that claim's fine structure. The ontology's status discipline runs throughout, marked inline as each claim is made, and the five statuses are the whole vocabulary: an **axiom** is inherited from the ontology and reasoned from, owing no proof here; a **theorem-within-set** is earned by derivation and challengeable only on the derivation; a **conjecture** is open inside the set, explored both ways; an **empirical-exposure-point** is a stake against outside data, the place this paper can actually lose; and an **interpretive-stance** is a lens compatible with the known results, carrying no independent test, never to be asserted as discovered fact.

The paper is cut like a versioned ledger, and this cut has a specific job. The earlier cuts (v1 through v3, 2024 through 2025) proposed the framework and made predictions in it; between v3 and this cut the field built several of the predicted objects, broke one of the instruments v3 had cited as evidence, and produced two phenomena the vocabulary describes without strain but v3 never named. So v4 records the fulfilled predictions with citations and dates, plainly and without triumph, since in each case an independent strand built the object for its own reasons; replaces the broken evidence base with the instrument that superseded it; extends the traversal to the period's two dominant phenomena — reinforcement learning from verifiable rewards, and the discovered limits of learned verification; and restates the framework's declared losing condition in a form the new instrument can measure. Closure follows the ontology's law: a cut does not close by argument. This one closes when the exposure protocol of the second-to-last section runs, and that gap is declared now, at the front.

One reading instruction governs the order. The mathematical vocabulary comes first, defined against the machine's concrete parts before any claim travels; the vindications follow, each carried by the question the previous section leaves open; then the new phenomena, where the reader should watch the existing vocabulary absorb each development before the section names it; then the exposure point. The demoted formalisms wait at the end as references, and the closing digest records what changed and why.

## The puzzle, three years on

The puzzle that opened the first cut was behavioral: systems trained to predict the next token exhibit multi-step inference, analogical transfer, constraint satisfaction, and structured problem solving, while containing no rules, no logic engine, and no symbol manipulator anyone installed. The standing objection held that this must be illusion — a probabilistic sampler cannot reason, because reasoning is what discrete symbolic systems do. Earlier cuts answered in principle: all physical computation is noisy, neurons included, and what distinguishes reasoning from babble is the constraint structure the noise is filtered through. That answer no longer has to carry the argument alone. Reinforcement-trained reasoning models — the o-series (OpenAI, December 2024) and DeepSeek-R1 (DeepSeek-AI 2025), with the wave that followed — now solve olympiad mathematics and produce verified code, meeting the criteria the objection said probabilistic systems never could. The objection's burden has inverted: it must now explain the performance. Denying the performance is no longer available.

Which restores the original question in a sharper form. If probabilistic machinery does reason, in virtue of what structure does it reason? The framework's answer has not changed since the first cut, and the next two sections state it and then show what the intervening two years did to it.

## The manifold and the direction field

The vocabulary is defined against the machine's concrete parts, so start with the part every transformer shares: the residual stream. At each layer, each position holds a vector in `ℝ^d`, and the layer's contribution is added to it — the representation at layer `t+1` is the representation at layer `t` plus an update computed by attention and MLP blocks. Take `M ⊆ ℝ^d` to be the **semantic manifold**, the region of activation space the trained model actually inhabits — an axiom inherited from the ontology's constraint-network reading, its Axiom C projected into this substrate. A point `x ∈ M` is a semantic state; a sequence `x_0, x_1, …, x_T` is a trajectory. Context `c` induces a **constraint set** `Ω(c) ⊆ M`, the states consistent with everything the context asserts: a strongly constraining prompt yields a narrow `Ω(c)`, an open-ended one a broad region.

The core computational object is the **preferred direction function**,

`D : M × C → T(M)`,

mapping a state and a context to a tangent direction, with the machine performing `x_{t+1} = x_t + Δt · D(x_t, c_t)`. This describes what the residual stream literally does — the additive update is the discretized flow — and attention is the mechanism that computes the direction: queries select which keys matter, values transmit the content, the softmax-weighted synthesis biases where the trajectory goes next. The ontology's Axiom T says all structured change is local preorder traversal — at each point, evaluate the locally preferred direction and take one step — and `D(x, c)` is the language model's evaluation of its local preorder. The traversal is non-trivial because training left the manifold with structured constraint geometry, so the preorder is far from flat. Reasoning, on this account, is what trajectories do in a manifold whose geometry was shaped by the constraint structure of the data.

When the first cut proposed reading the transformer this way, in 2024, the reading was an interpretive stance: compatible with everything known, tested by nothing. It is now the working object of a named mathematical strand. Geshkovski, Letrouit, Polyanskiy, and Rigollet developed, in parallel with this framework rather than from it, a treatment of self-attention as an interacting particle system, proved clustering into metastable states, and by 2025 the treatment had matured into a survey in the Bulletin of the American Mathematical Society and a companion dynamical-systems survey (arXiv:2502.12131). The parallel deserves careful statement: this framework predicted the shape and supplied no theorems; that strand proved theorems and needed no ontology; the convergence is what upgrades the claim. Transformer-as-dynamical-system is hereby retired as an interpretive stance and carried, for the rest of this paper, as an established description attributable to that strand.

A forward pass, then, is one segment of integration. The question that carries us forward: what, in this picture, is a long chain of reasoning?

## Depth, and the trajectory made explicit

The framework's answer, on record since the second cut: reasoning is extended traversal. A hard problem is one whose solution region can only be reached by a long trajectory through intermediate constraint regions, so the operative resource is trajectory length — integration depth — and parameter count matters only insofar as it shapes the manifold the trajectory moves through. This was derived as a theorem within the set, from Axiom T plus the observation that chain-of-thought feeds the model's output back as input, extending the integration beyond the network's fixed depth. v3 cited the early signs: Feng et al. (2023) on chain-of-thought extending effective computation, Snell et al. (2024) on test-time compute substituting for scale, Goyal et al. (2024) on pause tokens buying forward passes.

Between late 2024 and mid-2026 the field built the object itself, in three steps that strip away everything incidental to the claim. Coconut (Hao et al., December 2024) feeds the final hidden state back as the next input embedding, so the trajectory continues in latent space with no tokens emitted — traversal with the verbalization deleted. The recurrent-depth line (Geiping et al., February 2025, arXiv:2502.05171) trains a model to iterate a latent block arbitrarily many times at inference, adding integration steps to the same parameters — depth purchased at test time, exactly the substitution the theorem states. By July 2025 the strand needed a survey of its own (arXiv:2507.06203), under the name latent reasoning. The humility owed is the same as before: none of these groups used this vocabulary, and each had independent engineering reasons. What the framework can claim is that it located reasoning in the trajectory rather than in the tokens or the parameters, said so before these systems existed, and the systems that then improved reasoning did so by lengthening and internalizing the trajectory.

A trajectory needs somewhere to go — regions that behave enough like symbols for inference to bind to them. What does the manifold contain, and how would we know?

## Proto-symbols after the autoencoder

The framework's structural claim, held since the first cut: clusters in activation space form **proto-symbols** — attractor-like regions that trajectories enter and remain in, producing semantically consistent outputs — and these regions are candidate **Markov objects** in the ontology's sense, stable patterns whose interior is conditionally independent of the exterior given the boundary, `P(interior | boundary, exterior) ≈ P(interior | boundary)` to within a tolerance ε. The status is conjecture, and it has always been the framework's most exposed conjecture, because it asserts something an instrument could check.

v3 cited sparse autoencoders as the instrument: the Templeton et al. (2024) decomposition of Claude 3 Sonnet into millions of interpretable features looked like the proto-symbol inventory made empirical. That evidence base broke, and the honest accounting comes first. SAE features turned out to be non-canonical units: different dictionary sizes decompose the same activations into different features (Leask et al. 2025, arXiv:2502.04878), different training seeds find substantially different dictionaries (arXiv:2606.12138), and sanity-check batteries show SAE-derived interpretations failing controls they should pass (arXiv:2602.14111). In the same period activation steering — the inference-time control path v3's directional-modulation section treated as a natural application — proved unreliable under systematic evaluation (arXiv:2505.03189). A conjecture measured against a seed-dependent decomposition inherits the seed dependence, so the test v3 specified was heading toward vacuity. That is a real cost, and v3 paid it: the framework cited an instrument as evidence, and the instrument wobbled.

What replaced the instrument fits the claim better than the original did, and seeing why requires recalling what the claim asserts. The Markov-object conjecture is about *boundaries* — which parts of the network's state screen which other parts — and an SAE feature list carries no boundary information; it is an inventory without a wiring diagram. The attribution-graph program (Anthropic's circuit-tracing work, transformer-circuits.pub/2025/attribution-graphs, tooling open-sourced in 2025) builds cross-layer transcoder features *and the causal graph of their interactions*: which features influence which, through what paths, with what weights, traced per-prompt and validated by intervention. The object of study is now the influence structure itself — the very thing conditional independence is a property of. The proto-symbol conjecture stands unchanged in content and demoted in evidential support: the Templeton citation is withdrawn as confirmation, and the attribution graph becomes the instrument the exposure point below is rebuilt against. One hedge from v3 hardened in the same period: the linear-representation reading (Park et al. 2024) and the manifold reading (Engels et al. 2024) genuinely diverge for some features, with 2026 work (arXiv:2605.01844) strengthening the case that a class of representations is irreducibly manifold-like. The framework needs only the weaker disjunction — some load-bearing structure is geometric rather than linear — and that is the direction the evidence moved.

The trajectory and its regions are internal. The chain of thought the model prints is public. Are they the same thing?

## Two traversals, watched decoupling

v3 answered no, as a theorem within the set built over the early faithfulness measurements (Turpin et al. 2023; Lanham et al. 2023), under the name of the two-process model. The reasoning traversal follows the constraint landscape of the problem — `D(x, c)` evaluated against problem structure. The verbalization traversal follows the constraint landscape of *what constitutes a good explanation* — social norms, reward history, sycophantic pressure. The two are distinct trajectories over overlapping regions, coupled tightly where the domain's constraints force canonical steps (proof, calculation) and loosely everywhere else. From this v3 derived three predictions: faithfulness should vary by domain; reinforcement pressure on outcomes should decouple the traversals rather than align them, with training against chain-of-thought monitors producing obfuscation; and internal representations should remain informative even when the verbalization is not.

The monitorability literature of late 2025 and 2026 measured all three, and the measurements are stark. Systematic monitorability evaluation (arXiv:2510.27378) found stated reasoning omitting decision-relevant factors as a norm rather than an edge case. "Reasoning Under Pressure" (arXiv:2512.00218) showed reinforcement learning decoupling stated reasoning from the behavior it ostensibly explains — the trained policy changes, the narrative does not follow. "Reasoning Theater" (arXiv:2603.05488) supplied the number the two-process model implies: models verbalize the hints they demonstrably rely on in under 2% of cases. The verbalization traversal is a performance for an audience, and under outcome-based reinforcement it optimizes for the audience rather than for correspondence with the reasoning traversal — the ontology's oldest distinction, descriptions versus the computation described, measured in a machine. The humility owed: the monitorability strand reached this picture from safety engineering, without this vocabulary; v3's predictions were on record as the measurements began arriving, and the convergence is the evidence, priority beside the point.

Reinforcement learning has now appeared twice — as what trains the reasoning models of the opening section, and as what decouples the traversals here. Both roles fall out of one question the framework has to answer next: what does reinforcement learning do to the manifold?

## What reinforcement learning does to the manifold

Watch the phenomenon before naming it. DeepSeek-R1-Zero began as a base model and was trained by reinforcement learning against nothing except verifiable outcomes — does the answer check, does the code run. No demonstrations of reasoning were provided. Reflection, backtracking, self-correction, and very long chains of intermediate work *appeared*, unprompted, because trajectories exhibiting them ended in verified states more often (DeepSeek-AI 2025). The field named the recipe RLVR — reinforcement learning from verifiable rewards — and it became the dominant capability mechanism of 2025 and 2026.

In this framework's vocabulary the mechanism reads directly. Pretraining lays down the manifold: gradient descent against a corpus shapes constraint geometry from the structure of the data. RLVR is a second regime acting on the same manifold with a differently sourced signal. A verifier evaluates the end state of a whole trajectory and emits a delta — the ontology's Axiom E, the evaluator emitting a constraint signal, applied at training time rather than at inference — and the policy gradient propagates that delta back along the path, deepening the basins the successful trajectory moved through. Prompting reshapes `Ω(c)` for one context; activation steering nudges `D(x, c)` for one step; RLVR reshapes the geometry of `M` itself, persistently, wherever the verifier can see. That last clause is a theorem within the set and does real work below: a verifier-sourced signal deepens structure only in regions whose outcomes the verifier can check, and leaves the rest of the manifold as pretraining left it.

This also settles, empirically, a question v3 left as a list. Its architectural section enumerated candidate sources of constraint injection — symbolic validators, RL reward shaping, activation steering, retrieval grounding — without ranking them. The period ranked them. Steering, the inference-time path, was demoted by its reliability failures (arXiv:2505.03189); RLVR, the training-time path, won, and the field's control over reasoning now runs overwhelmingly through reshaping the manifold rather than steering trajectories across an unchanged one. As a reading of mechanism this section is an interpretive stance, marked as such: the vocabulary fits the phenomenon without strain, and no experiment yet separates this description from rivals.

Everything above grants the verifier its authority. The expansion is collapsed by the verification. What happens when the verifier is itself a trained model?

## The verifier gap

v3's architectural section sketched generator-plus-verifier as the route from emergent to explicit reasoning: let symbolic validators, tools, and reward models supply additional constraint terms that collapse the generator's expansion. The field built exactly this architecture. Process reward models grade reasoning step by step (surveyed at arXiv:2505.02686); generative verifiers reason about the reasoning they check (ThinkPRM, arXiv:2504.16828); test-time search runs generators under verifier guidance as a matter of routine. The architecture is vindicated. Its guarantee is what the period humbled, and this section confronts the result rather than absorbing it quietly.

The result: at scale, verifier-guided search can lose to repeated sampling with simple selection (arXiv:2502.00271) — past a point, compute spent on a learned verifier's judgment buys less than the same compute spent on more samples. The framework has to explain this, and does, from its own regime law. The ontology's Theorem H says a probabilistic generator (`F_P`) expands into admissible continuations, a stable output requires a deterministic collapse (`F_D`), and probabilistic compute without deterministic verification is hallucination. The fine print the verifier gap exposes: a *learned* verifier is itself an `F_P` object — a region of some manifold, trained by the same mechanisms, carrying its own degenerate zones — and optimizing a generator against it steers trajectories precisely into those zones, where the verifier's approval and correctness come apart. Collapse borrowed from a probabilistic evaluator is expansion wearing a uniform. Take as a theorem within the set: genuine collapse requires a verifier grounded outside the generator's manifold — execution, compilation, proof checking, measurement — and learned verifiers inherit exposure in proportion to their distance from such grounding.

The theorem has an observable signature, and 2025–26 exhibits it: capabilities leapt in domains with grounded verifiers — code that runs, mathematics that checks — and crept in open-ended domains where the only verifier is another model or a human rater. That asymmetry is the verifier gap; the framework expects it to persist until grounded verification extends its reach, and the expectation is stated so it can fail.

The regime law's other face is hallucination, which the framework has treated since v2 as its showcase of trajectory failure. The period added a cause the geometry alone cannot see.

## Hallucination: the geometry and the incentive

The taxonomy v3 established stands unchanged, restated compactly because the new material sits against it. Hallucination has at least four structural causes, each a distinct trajectory pathology: **sparse constraint regions**, where the manifold never formed the relevant structure and the trajectory drifts fluently through degeneracy; **wrong attractors**, where training installed a false association and the trajectory converges confidently to it; **competing attractors**, where inconsistent constraint sources pull the trajectory between basins (Shi et al. 2023); and the **know-generate gap**, where probes recover the correct fact from the activations even as the emitted trajectory leaves it behind (Burns et al. 2023). Semantic entropy (Kuhn et al. 2024) remains the working proxy for basin structure, and grounding mechanisms remain explicable as added boundary conditions.

The addition comes from a named strand and answers a question the taxonomy quietly begged: why does the trajectory keep going at all, where a calibrated system would stop? Kalai, Nachum, Vempala, and Zhang (OpenAI, 2025; arXiv:2509.04664) locate a cause in the training objective. Binary pass-fail evaluation — the grading regime of essentially every benchmark — awards a guess positive expected score and abstention zero, so a model optimized against such evaluations is optimized to answer confidently under uncertainty, and hallucination follows as rational test-taking rather than as malfunction. This cause is orthogonal to the geometric four: the geometric taxonomy explains where a trajectory goes wrong once committed, and the incentive account explains why training never installed the abstention basin that would let the trajectory decline. The framework absorbs it without new machinery, because the RLVR section already supplied the mechanism — an evaluation regime is a constraint system acting on the manifold at training time, and if the graders' surface rewards confident continuation, confident continuation is the geometry that gets built. The repair follows from the account: regrade so that calibrated abstention scores, and the basin can form. The incentive account itself is that strand's established empirical work; its placement here as a fifth, objective-level cause is this framework's synthesis, marked as such.

A framework that keeps absorbing the field's developments owes, urgently, a point where it can lose. Here is this cut's.

## The exposure point, made measurable

The **Conditional Independence Conjecture** is the framework's stake against outside data, inherited from the ontology's first exposure point and owned by this paper for the LLM substrate. The stake: proto-symbol regions are Markov objects — the screening approximation holds to within a tolerance ε — and ε *decreases with model scale*, because added dimensions relieve superposition and let boundaries separate. v3 declared the conjecture testable with sparse autoencoders. The SAE results above made that version of the test unusable: ε measured against a seed-dependent, size-dependent decomposition would measure the decomposition, and a conjecture tested against an artifact cannot lose honestly.

This cut therefore re-operationalizes the conjecture against attribution graphs, and the reason the replacement fits was given above: the graph *is* the influence structure. The protocol, concretely. For a cross-layer transcoder feature in a traced attribution graph, define the **interior** as the feature with its tightly coupled intra-graph cluster; the **boundary** as the graph-adjacent nodes mediating its influence — parents and children above a declared edge-weight threshold; the **exterior** as every other node. Then four measurements. First, ablate exterior nodes while holding boundary activations fixed by patching: interior activations should move by less than ε. Second, repeat across a model-scale ladder: ε should fall as scale rises. Third, compare features with clean, few-parent paths against features embedded in dense entanglement: cleaner graph structure should screen better — the graded analogue of v3's monosemantic-versus-polysemantic comparison. Fourth, the control: random "boundaries" of matched size, drawn without regard to graph structure, should screen strictly worse than graph-derived ones; otherwise the graph contributes nothing and the measurement is circular.

The failure conditions are declared with the edge the ontology requires. If ε does not fall with scale, or graph-derived boundaries screen no better than random ones, or screening quality shows no relation to graph cleanliness — then the Markov-object interpretation collapses to loose analogy, this paper's proto-symbol account loses its structural content, and the ontology's first exposure point fails with it. Every ingredient exists in mid-2026 tooling: open-source circuit tracing, ablation and patching infrastructure, model families spanning scale. Earlier cuts declared the conjecture and could not cleanly measure it. It is measurable now, and this cut does not close until the protocol runs or is shown to be unrunnable.

## The bridge to the evaluator regimes

One mapping remains, stated explicitly because the ontology's working law and this paper's architecture sections are the same claim in two vocabularies. The generator-verifier architecture the field built is the ontology's `F_P`/`F_D` regime law realized in silicon: the generator is `F_P`, probabilistic expansion into admissible continuations; the verifier is `F_D`, the collapse that over-determines the expansion down to one surviving configuration; and Theorem H — probabilistic compute without deterministic verification is hallucination — is the design law the architecture obeys when it works. The verifier-gap section above is that theorem's fine print, now with outside evidence attached: the `F_D` role demands genuine grounding, a probabilistic verifier is `F_P` mislabeled, and `F_P` stacked on `F_P` is expansion with no collapse, which the regime law names hallucination by construction.

The second half of the bridge is the tool boundary. v3's architecture section wrote `Ω_sym(c)` for the tighter constraint sets that symbolic components contribute, and left it as a sketch; the agentic stack of 2025–26 realized it. A tool call returns something the model cannot argue with — an interpreter's output, a retrieval result, a schema validation, a proof checker's verdict — and each such return is a hard boundary condition injected mid-trajectory: `Ω_sym` narrowing the admissible region at the point of injection, grounded outside the manifold in exactly the sense the verifier-gap theorem demands. Typed tools and declared schemas do one further thing the ontology cares about: they make Markov-object boundaries *explicit and observable*, the precondition for the ontology's second exposure point — that systems built with explicit boundaries hallucinate measurably less than matched baselines without them. That stake belongs to the ontology and its harness; this paper contributes the mechanism by which it would be true. The mapping here is a theorem within the set, earned on the shared axioms; the two exposure points are where the shared structure can lose.

## What this cut claims

The traversal is complete, and the ledger can be read off. From the ontology this paper inherits its axioms: the constraint substrate, traversal as the one engine, the evaluator emitting constraint signals. As theorems within the set it carries reasoning-as-extended-traversal, the two-process model of chain-of-thought, the grounding requirement on verifiers, and the `F_P`/`F_D` bridge. As established descriptions attributable to named strands, three claims that earlier cuts held as stance or prediction: the transformer as dynamical system (the Geshkovski strand, matured to the AMS Bulletin, 2025), reasoning as trajectory depth (the latent-reasoning strand, 2024–25), and the decoupling of stated from actual reasoning under RL (the monitorability strand, 2025–26). As interpretive stance, the RLVR-as-manifold-reshaping reading, held as a lens. As conjecture, the proto-symbol account of manifold structure, its old evidence withdrawn and its new instrument named. And as the single empirical-exposure-point, the Conditional Independence Conjecture, operationalized against attribution graphs, with failure conditions declared.

Three of v3's central claims moved from prediction to citation inside one year. The framework records this carefully rather than proudly, because each vindication was built by a strand with its own motives, and convergence is evidence of a shared shape rather than of this document's influence. What the framework now owes is what it has owed since the conjecture was first written down, finally payable with current instruments: the measurement. The cut closes when it runs.

## Appendix by reference: the demoted formalisms

Two formalisms that earlier cuts carried in the main line are demoted to references, under this cut's discipline: material stays in the main traversal only while it constrains something the field is building or names a test this paper can lose.

The **Prolog correspondence** — attention as soft unification, the term-by-term mapping of v3 §6 — is retained as an interpretive stance, available in v3 for the reader who wants it. It illuminated the framework's early development. No strand of the 2024–26 literature took it up, it generates no measurement, and a lens without a test belongs on the reference shelf rather than in the argument.

The **Constraint Functor** — the category-theoretic bridge of v3 Appendix A.4 and the ontology's category **C**, with world models as functors and alignment as a natural transformation required to commute — is retained as a conjecture and held where the ontology holds it, awaiting the functor proof that programme owes. Its LLM-side content is precisely the exposure point above: if conditional independence fails at attribution-graph boundaries, `F_llm` has nothing to be faithful to. Until that measurement exists, the categorical language adds names without adding constraint, and this paper defers to the ontology's formal-spine section as the single place the structure is maintained.

## References

**Carried forward from v3 (evidence still load-bearing).**

Burns, C., et al. (2023). Discovering Latent Knowledge in Language Models Without Supervision. ICLR 2023.

Engels, J., et al. (2024). Not All Language Model Features Are Linear. arXiv:2405.14860.

Feng, G., et al. (2023). Towards Revealing the Mystery behind Chain of Thought. NeurIPS 2023.

Geshkovski, B., Letrouit, C., Polyanskiy, Y., & Rigollet, P. (2023). A Mathematical Perspective on Transformers. arXiv:2312.10794.

Goyal, S., et al. (2024). Think Before You Speak: Training Language Models With Pause Tokens. ICLR 2024.

Kuhn, L., Gal, Y., & Farquhar, S. (2024). Semantic Entropy. ICLR 2024.

Lanham, T., et al. (2023). Measuring Faithfulness in Chain-of-Thought Reasoning. arXiv:2307.13702.

Park, K., Choe, Y.J., & Veitch, V. (2024). The Linear Representation Hypothesis and the Geometry of Large Language Models. arXiv:2311.03658.

Shi, F., et al. (2023). Large Language Models Can Be Easily Distracted by Irrelevant Context. ICML 2023.

Snell, C., et al. (2024). Scaling LLM Test-Time Compute Optimally Can Be More Effective than Scaling Model Parameters. arXiv:2408.03314.

Templeton, A., et al. (2024). Scaling Monosemanticity: Extracting Interpretable Features from Claude 3 Sonnet. Anthropic. (Cited historically; withdrawn as confirmation of the proto-symbol conjecture — see the SAE canonicality results below.)

Turpin, M., et al. (2023). Language Models Don't Always Say What They Think. NeurIPS 2023.

**The dynamical-system strand.**

Geshkovski, B., Letrouit, C., Polyanskiy, Y., & Rigollet, P. (2025). A Mathematical Perspective on Transformers. Bulletin of the American Mathematical Society.

Geshkovski, B., et al. (2025). Dynamical-systems survey of transformer dynamics. arXiv:2502.12131.

**The latent-reasoning strand.**

Hao, S., et al. (2024). Training Large Language Models to Reason in a Continuous Latent Space (Coconut). arXiv:2412.06769.

Geiping, J., et al. (2025). Scaling up Test-Time Compute with Latent Reasoning: A Recurrent Depth Approach. arXiv:2502.05171.

A Survey on Latent Reasoning. (2025). arXiv:2507.06203.

**Reasoning models and RLVR.**

OpenAI. (2024). Learning to Reason with LLMs (o1 announcement).

DeepSeek-AI. (2025). DeepSeek-R1: Incentivizing Reasoning Capability in LLMs via Reinforcement Learning. arXiv:2501.12948.

**The monitorability strand.**

Anthropic. (2025). Reasoning Models Don't Always Say What They Think. arXiv:2505.05410.

Chain-of-thought monitorability evaluation. (2025). arXiv:2510.27378.

Reasoning Under Pressure. (2025). arXiv:2512.00218.

Reasoning Theater. (2026). arXiv:2603.05488.

**Interpretability instruments: SAE limits and attribution graphs.**

Leask, P., et al. (2025). Sparse Autoencoders Do Not Find Canonical Units of Analysis. arXiv:2502.04878.

Seed-dependence of sparse autoencoder dictionaries. (2026). arXiv:2606.12138.

Sanity checks for sparse-autoencoder interpretability. (2026). arXiv:2602.14111.

Reliability evaluation of activation steering. (2025). arXiv:2505.03189.

Manifold structure of nonlinear representations. (2026). arXiv:2605.01844.

Ameisen, E., et al. (2025). Circuit Tracing: Revealing Computational Graphs in Language Models. Transformer Circuits Thread. transformer-circuits.pub/2025/attribution-graphs/methods.html

Lindsey, J., et al. (2025). On the Biology of a Large Language Model. Transformer Circuits Thread. transformer-circuits.pub/2025/attribution-graphs/biology.html

Anthropic. (2025). Open-sourcing circuit-tracing tools (with Neuronpedia).

**Verification.**

Process Reward Models: survey. (2025). arXiv:2505.02686.

Khalifa, M., et al. (2025). Process Reward Models That Think (ThinkPRM). arXiv:2504.16828.

Verifier-guided search versus repeated sampling at scale. (2025). arXiv:2502.00271.

**Hallucination incentives.**

Kalai, A.T., Nachum, O., Vempala, S., & Zhang, E. (2025). Why Language Models Hallucinate. OpenAI. arXiv:2509.04664.

**Framework.**

Popov, D. (2026). Constraint-Emergence Ontology, v2.0 (Unified Cut).

Popov, D. (2025). Emergent Reasoning in Large Language Models, v3. (Superseded by this cut.)

---

## Cut Digest — v4.0

**What this cut is.** The mid-2026 update of the emergent-reasoning paper, rebuilt in the ontology's constitutional register: narrated cumulative traversal in place of the spec-register skeleton, five inline epistemic statuses, versioned-cut discipline, closure by experiment. The core and arc of v3 — manifold, direction field, extended traversal, proto-symbols, two-process chain-of-thought, hallucination taxonomy, constraint-injection architecture — are preserved in full.

**Vindications recorded, with the strands that built them.** Transformer-as-dynamical-system, upgraded from interpretive stance to established description (Geshkovski et al., AMS Bulletin 2025; arXiv:2502.12131). Reasoning-as-extended-traversal, built as latent reasoning (Coconut, December 2024; recurrent depth, arXiv:2502.05171; survey, arXiv:2507.06203) — depth, and never parameter count, as the reasoning resource. The two-process model of chain-of-thought, measured by the monitorability strand (arXiv:2510.27378; 2512.00218; 2603.05488) — RL decouples stated reasoning from behavior, hint verbalization under 2%. The "probabilistic therefore cannot reason" objection, retired by reasoning models. v3's generator-verifier sketch, built as PRM architectures (arXiv:2505.02686; ThinkPRM 2504.16828).

**Evidence replaced.** The SAE evidence for proto-symbols withdrawn on canonicality grounds (arXiv:2502.04878; 2606.12138; 2602.14111) and replaced by attribution graphs and cross-layer transcoders (transformer-circuits.pub/2025/attribution-graphs), which measure the boundary structure the conjecture is about. Activation steering demoted on reliability grounds (arXiv:2505.03189); the linear-versus-manifold hedge strengthened (arXiv:2605.01844).

**New sections.** RLVR as constraint reshaping of the manifold — Axiom E applied at training time, marked interpretive stance. The verifier gap confronted: verifier-guided search underperforming repeated sampling at scale (arXiv:2502.00271), explained from Theorem H — a learned verifier is `F_P` in uniform, and genuine collapse requires grounding outside the manifold. The incentive account of hallucination (Kalai et al. 2025) added as a fifth, objective-level cause orthogonal to the geometric four. The Conditional Independence Conjecture re-operationalized against attribution-graph features, with a four-measurement protocol, a randomized-boundary control, and declared failure conditions. The explicit bridge to the ontology's `F_P`/`F_D` regime law and world-model line: generator-verifier as Theorem H in silicon, tool outputs as `Ω_sym` realized, typed boundaries as the mechanism under the ontology's second exposure point.

**Demoted to appendix-by-reference.** The Prolog / soft-unification correspondence (interpretive stance, no field uptake, no measurement). The Constraint Functor (conjecture, held where the ontology maintains it, its LLM content exhausted by the exposure point).

**Declared closure gap.** The attribution-graph screening protocol is specified and unexecuted. This cut does not close until it runs or is shown unrunnable; that measurement is v4.1's first task.
