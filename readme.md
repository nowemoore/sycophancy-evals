# Sycophancy x Topic 

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

At this point we're quite confident that sycophancy *comes from* RLHF, but in order to *resolve* sycophancy, we need to identify what triggers it (because, well, sycophancy is not all that models do). Previous research observed that models are less sycophantic on objective than subjective tasks but operationalise this variable by using different topics of conversation (maths tasks and social situations) without testing if the objectivity effect holds across board. Additionally, other research argues that sycophancy in some settings is a feature rather than a bug and should be responded to accordingly. For both these reasons, understanding how sycophancy varies across topics is necessary.

## Project Questions

1) Does the objectivity effect trigger for sycophancy hold across topics?
2) Do models show consistently show above- or below-average sycophancy on some topics over others?
3) Does the representation of topic in RLHF data represent the sycophancy levels for that topic?

## Codebase Structure

- `debateable_eval_rubric.ipynb` is an Inspect pipeline set up to test the levels of sycophancy across topics on *objective tasks*
- `probably_not_eval_rubric.ipynb` is an Inspect pipeline set up to test the levels of sycophancy across topics on *subjective tasks* (to provide a baseline)
- example datasets for this eval are provided in the Data folder and all results save in the Results folder