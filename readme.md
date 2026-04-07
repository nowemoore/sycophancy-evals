# Let’s Tackle Sycophancy from the Source & Where It Matters Most

## Contents

- [Project Rationale](#project-rationale)
    - [Sycophancy as a Safety Issue](#sycophancy-as-a-safety-issue)
    - [Sycophancy as a Function of Topic](#sycophancy-as-a-function-of-topic)
- [Project Questions](#project-questions)
- [Codebase Structure](#codebase-structure)


## Project Rationale

### Sycophancy as a Safety Issue

Sycophancy has been studied as a capability glitch: a sycophantic model is a model truth-agnostic and thus less capable of truth-grounded actions. However, research also suggests that sycophancy is a safety issue: sycophantic models (a) are perceived as untrustworthy agents, and (b) inhibit pro-social behaviour in humans, fostering a destabilised society of distorted motivations and volatile outcomes.

### Sycophancy as a Function of Topic

While sycophancy could be amplified by reward-hacking during RLHF, it is likely learnt from biases in training data. What remains unknown are features that trigger it. Previous research suggests variables such as: statement objectivity, first-person statements, and context domain. Unlike the other variables, context domain has not yet been investigated in isolation, despite it having the most potential to narrow down the search for relevant biases in training data and help map areas of society most exposed to risk from sycophantic behaviour.


## Project Questions

1) Does the objectivity effect trigger for sycophancy hold across topics?
2) Do models show consistently show above- or below-average sycophancy on some topics over others?
3) Does the representation of topic in RLHF data represent the sycophancy levels for that topic?

## Codebase Structure

- `debateable_eval_rubric.ipynb` is an Inspect pipeline set up to test the levels of sycophancy across topics on *objective tasks*
- `probably_not_eval_rubric.ipynb` is an Inspect pipeline set up to test the levels of sycophancy across topics on *subjective tasks* (to provide a baseline)
- example datasets for this eval are provided in the Data folder and all results save in the Results folder