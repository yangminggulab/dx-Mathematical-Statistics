## Overall Roadmap

Following the MIT OpenCourseWare statistics framing, mathematical statistics is organized around estimation, confidence intervals, hypothesis testing, chi-square tests, decision theory, and Bayesian methods. This tree matches the repository's notes on statistics, sampling distributions, point estimation, estimator evaluation, interval estimation, and hypothesis testing.

```text
Mathematical Statistics = using samples to infer populations
|
+-- 0. Foundation layer, not the goal but the ammunition
|   +-- Statistics and sufficiency
|   |   +-- Compress n data points into a few numbers without losing relevant information.
|   +-- Order statistics
|   |   +-- Study extrema and ranges as building blocks for intervals and tests.
|   +-- Sampling distributions: chi-square, t, F, and normal-population theorems
|       +-- Tell us what distributions common statistics follow.
|
+-- Ability 1: guess parameter values -> point estimation
|   +-- Method of moments  set sample moments equal to population moments
|   +-- MLE                choose parameters that make the observed data most likely
|   +-- Bayes              prior + data -> posterior, then extract an estimate
|
+-- Ability 2: judge whether an estimator is good -> evaluation theory
|   +-- Unbiasedness             average estimate equals the parameter
|   +-- UMVUE                    minimum-variance unbiased estimator
|   +-- Fisher information / C-R theoretical lower bound on variance
|   +-- Consistency / asymptotic normality large-sample behavior
|
+-- Ability 3: give a parameter range -> interval estimation
|   +-- Pivotal quantity method  find a known-distribution function and invert it
|
+-- Ability 4: decide whether a claim should be rejected -> hypothesis testing
    +-- Test statistics: Z, t, chi-square, F
    +-- Neyman-Pearson lemma and UMP tests
    +-- Goodness-of-fit tests for whether data come from a specified distribution
```

# dx's Mathematical Statistics

## Preface

If probability theory asks what happens when a distribution is already known, mathematical statistics asks the reverse question: when only a sample is available, how much can we infer about the population behind it?

The key shift is that probability often begins with a population model, while statistics begins with finite, noisy, accidental observations. The subject is about inference under limited evidence.

## Why This Book Is Written This Way

Mathematical statistics can easily become a course full of formulas and names that appear unrelated: skewness, sampling distributions, method of moments, maximum likelihood, intervals, tests, chi-square, t distributions, and Neyman-Pearson theory.

This book tries to keep each formula attached to the problem it answers. A statistic is not only an expression to memorize. It has a role: extracting sample information, standardizing uncertainty, controlling distributional shape, or supporting a decision.

## What This Book Keeps

The notes begin with population, sample, sampling, statistics, sampling distributions, and parameter spaces. They then move into parameter estimation, including method of moments, maximum likelihood, M-estimation, and Bayesian estimation. The later chapters develop interval estimation and hypothesis testing, where inference becomes decision-making.

The core thinking order is: identify the available information, identify what must be inferred, and then ask why the chosen statistic is reasonable.

## Intended Readers

This book is for readers who have studied probability but feel unstable when entering statistical inference. It tries to connect each new statistical action back to familiar probability ideas, and then show what extra step statistics adds.

## Repository Notes

- The main entry is `main.tex`.
- The body covers foundations, parameter estimation, interval estimation, and hypothesis testing.
- Exercises and pure homework notes are kept separately.
- For local compilation, running `xelatex main.tex` twice is usually enough.
