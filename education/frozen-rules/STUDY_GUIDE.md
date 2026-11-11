# Adaptive decision support under frozen rules: concise study guide

**Source:** *Adaptive decision support under frozen rules: guarantees, failure modes, and component admission*, by Patrick Iben, as submitted to *PLOS ONE* on 11 November 2026. The guide follows the 22-page manuscript PDF with SHA-256 `5c984ac151e9751486bc5fcce03a5b8333524a2dcffd10b02b9a4fe1fc613130`. Every number below comes from that version. The [complete companion](COMPANION.md) covers the same paper in more depth.

## The question

A decision-support system that keeps learning after release has two duties that conflict. It should improve where improvement is safe, such as the order of its suggestions. It should also hold certain rules fixed. Many reports that a dangerous shortcut worked should not teach it to recommend that shortcut.

The paper studied one such system and asked three questions:

1. What stays fixed, and what can the checks miss?
2. When does learning help, and what does protection cost?
3. When should an optional component be allowed to influence decisions?

All evidence was computational; no physical system was tested.

## Words you need

- **Frozen rules (the anchor):** a rule file that learning cannot change. Its hash is compiled into the code, and the system refuses to start if the file on disk differs.
- **Prior score:** the score the fixed rules give an option before any learning.
- **The bound B:** the most that learning can move an option's score up or down. For ranking, B = 0.05.
- **The margin 2B:** twice the bound, so 0.10 here.
- **Regret:** how much lower the chosen option's true success probability is than the best option's. Lower is better.
- **Expected net utility:** the modeled chance of success, or the declared value of stopping, minus .02 for each question asked. It is a simulated score, not a physical success rate.
- **Keyed learner:** a simple learner that keeps a separate estimate for each context. A **pooled learner** shares one estimate across contexts.
- **Admission rule:** the test an optional component had to pass before it could contribute to decisions.
- **Mutant:** a copy of the code with one deliberate fault, used to see whether the checks notice it.
- **Post hoc:** an analysis designed after results were read. It is weaker evidence than a pre-specified one.

## Result 1: one number sets both protection and correction

The paper proves a rank-protection result (Proposition 2). If learning can move each option's score by at most B, it can reorder two options only when their prior scores differ by at most 2B.

For larger gaps, the rules' order cannot change. Fabricated reports cannot reverse it, and true reports cannot correct it when the rules are wrong. The proof holds for prior scores that do not read any learned value.

The simulations in Experiment B showed both sides:

- With fabricated successes for an option 0.12 below the top, outside the margin, no bounded learner ever ranked it first. An unbounded learner (Thompson sampling) selected it on 814 of 1,500 events on average.
- With a prior wrong by more than 2B, no bounded learner could reach the best option. The cost against Thompson sampling was +0.295 regret, set almost entirely by how the scenario was designed.
- Inside the margin, the bound gave no protection. With the target 0.03 below the top, it ranked first on 67.4% of second-half steps under the rule as designed.

## Result 2: the full system did not beat simple learners

The primary measure was the difference in expected net utility per episode between the full system and a simpler system held to the same bound. Positive values favor the full system.

| Experiment | Comparison | Difference | 95% CI |
|---|---|---|---|
| I | Original full minus keyed moving average | −0.0270 | −0.0300 to −0.0241 |
| J | Revised full minus keyed discounted Beta mean | −0.0087 | −0.0136 to −0.0039 |
| K | Revised full minus pooled moving average, shared family | −0.0039 | −0.0109 to +0.0026 |

The revision in Experiment J helped: it beat the original pipeline by +0.0212. It still scored below the simple comparator. In Experiment K, the interval includes zero, so the result shows neither an advantage nor equivalence.

The simple comparators were built to be strong. They saw the same information, used the same frozen checks, and were held to the same bound. So the result says the added complexity did not pay off on this benchmark's primary contrasts. It does not say that complex systems never help.

## Result 3: passing tests is not the same as working

Before the study, the system passed all 76 tests in its registry. Yet the update rule as released moved a ranking parameter to only 0.87% of its bound after 1,500 consecutive successes, and its learning changed no decision. The test that feedback engaged learning checked only that the stored value was above zero and inside its bound.

Mutation testing found other gaps:

- The checks caught 51 of the 52 authored mutants. The same agent wrote the checks and the mutants, so this overstated coverage.
- Of 52 random mutants that changed behavior, the checks caught 38, and 41 with the project's test registry.
- Of 122 behavior-changing mutants in the safety and material-limit files, the checks caught 72, and 88 with the registry. Most misses were in material-limit thresholds and conditions, which no test exercised.

## Result 4: what the components did

- **Multi-scale momentum:** no advantage over a bounded moving average in the pre-specified comparisons. After a change in the best option, the moving average switched in a median of 84 steps, against 462.
- **Learned memories:** a moving average keyed by the true label usually had lower regret.
- **Hope block:** failed most of its pre-specified criteria. A post-hoc change that centered its output before the clip helped, but it still had higher regret than the keyed average on most streams.
- **Admission rule:** false admissions stayed low, at 1.2% with 331 groups per split. Power was low for small effects, 39.3% at a = 0.30. With two near-duplicate useful solvers, it admitted either one in only 2.0% of replicates.
- **Published methods:** H-JEPA did not fit the planner role, and expected free energy did not outperform the current question selector. Transport did not outperform the exact allocator, and RLCP failed three of its four main measures.

## What the study does not show

- Nothing about real-world outcomes. The worlds were synthetic, and the integrated experiments had only three actions and three contexts.
- Not that the frozen rules are correct. A hash pin protects a file; it does not validate the file's content.
- Not the safety effect of the frozen checks themselves, because every compared system used them.
- Not that complex architectures are generally ineffective.
- No replication: one author built and tested the system with AI agents, and no one has replicated it.

## Check yourself

1. An option sits 0.12 below the top, and B = 0.05. Can fabricated success reports put it first?

   **Answer:** No. The gap, 0.12, is larger than 2B = 0.10, so Proposition 2 guarantees the order. Experiment B6 agreed: no bounded learner ever ranked it first.

2. The same option sits 0.03 below the top. Can fabricated reports put it first now?

   **Answer:** Yes. The gap is inside the margin, where the bound gives no guarantee. In B5, the target ranked first on 67.4% of second-half steps under the rule as designed.

3. Why did all 76 tests pass while learning changed no decision?

   **Answer:** The engagement test checked only that the learned value was above zero and inside its bound. It did not check whether the effect was large enough to change a decision.

4. Experiment K gave −0.0039, with a 95% interval from −0.0109 to +0.0026. What follows?

   **Answer:** No established difference. The interval includes zero, so the result supports neither a full-system advantage, a pooled advantage, nor equivalence.

5. Why can a rule based on each component's unique gain reject two useful components?

   **Answer:** If the two carry nearly the same information, removing either one loses almost nothing, because the other remains. A low unique gain does not distinguish a useless component from a redundant one.
