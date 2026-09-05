# Statistics for Data Science
 
A complete, audited course in statistical reasoning, in 13 articles, from a first
histogram to a fully designed and analyzed A/B test. Built as the theory prerequisite
for inferential work in data science, experimentation, and machine learning.
 
<p>
  <img alt="13 articles" src="https://img.shields.io/badge/articles-13-3776AB">
  <img alt="67 diagrams" src="https://img.shields.io/badge/diagrams-67%20hand--built%20SVG-F37626">
  <img alt="77 code examples" src="https://img.shields.io/badge/code%20examples-77-success">
  <img alt="every number checked" src="https://img.shields.io/badge/numbers-verified%20against%20code-brightgreen">
</p>

**Read the complete edition:** <https://shikharkumar13.github.io/Statistics-for-Data-Science/index.html>
 
---
 
## Contents
 
- [What this is](#what-this-is)
- [Getting started](#getting-started)
- [Curriculum](#curriculum)
- [Repository layout](#repository-layout)
- [Verified, not just written](#verified-not-just-written)
- [How each article gets made](#how-each-article-gets-made)
- [Where to go next](#where-to-go-next)
---
 
## What this is
 
13 self-contained HTML articles, 67 hand-built diagrams, 77 worked code examples, and
61 interview-style quiz questions, covering descriptive statistics, probability, and
inferential statistics in the order a data scientist actually needs them. About 3.7
hours of reading, start to finish.
 
The series was first serialized day by day on Substack. This repository is the audited
edition: every draft re-checked line by line against real computation before anything
here was called finished.
 
The material is built around three principles.
 
**Every number is executed, not assumed.** A worked example that claims a p-value of
0.0016, a confidence interval of [27.7, 29.1], or a sample size of 476 has had that
exact figure produced by running the code in front of it, not typed in by hand. Where
the original draft got a number wrong, this edition says so and shows the corrected
run. Day 7 compared a routing problem to "atoms in the observable universe" when the
math only supports "atoms on Earth", fixed. Day 8 mislabeled a basic normalization
property as the law of total probability, a different and more specific theorem,
fixed. Day 10's Central Limit Theorem walkthrough had a stale number pasted in from
an unrelated calculation, fixed. Day 12 illustrated a two-tailed rule with a one-tailed
example that doesn't actually satisfy it in general, fixed. None of these were
cosmetic; each one would have taught the wrong thing.
 
**Every article builds on the last.** The PMF from Day 8 becomes the named
distributions of Day 9, which become the continuous distributions and Central Limit
Theorem of Day 10, which is the machinery Day 11 needs to build a confidence interval,
which Day 12 turns into a hypothesis test, which Day 13 runs for real inside an A/B
test. Nothing is re-explained from scratch; later articles say "as covered in Day 8"
and mean it.
 
**The examples are real companies, not urns and dice.** Netflix's recommendation
engine, Uber's surge pricing, Swiggy's delivery SLA, Spotify's onboarding funnel,
Stripe's fraud threshold, Google's search CTR: the same five or six companies
recur throughout, so the running numbers actually accumulate instead of resetting
with every new toy example.
 
### Who it is for
 
Anyone who wants to actually understand the statistics underneath data science,
not just call `.describe()` and `scipy.stats.ttest_ind()` without knowing what came
out the other end. Days 1 through 10 assume no statistics background. Days 11 through
13 assume you've finished them, or already know descriptive statistics and probability
some other way.
 
### What you need
 
No installation. Every article is a single HTML file that opens in a browser. The
Python in the worked examples uses `numpy`, `scipy.stats`, and occasionally `pandas`,
and reading it is enough, running it yourself is optional. If you want to run it,
any Python 3.9+ environment with those three packages is sufficient for all 13
articles.
 
---
 
## Getting started
 
```bash
git clone https://github.com/shikharkumar13/Statistics-for-Data-Science.git
cd Statistics-for-Data-Science
 
open "docs/statistics-for-data-science-day-1.html"    # macOS
# or just open the file in any browser
```
 
No build step, no server, no dependencies. If you would rather read online without
cloning anything, every article is also published at the GitHub Pages link above, and
the original day-by-day posts are on Substack.
 
---
 
## Curriculum
 
Each row's **Link** points to that article's page on GitHub Pages, following the
`docs/statistics-for-data-science-day-N.html` file as served from the repo root.
Swap in the real URLs once the repo and Pages site are live; until then these are
placeholders built from the same guessed username and repo name used elsewhere in
this file.
 
### Part I: Descriptive statistics (Days 1 to 6)
 
Summarizing the data already sitting in front of you, correctly.
 
| # | Article | Covers | Diagrams | Read time | Link |
|--:|---------|--------|:-:|:-:|:-:|
| 1 | **The Foundation** | Descriptive vs. inferential statistics, why anyone samples at all, populations and samples | 4 | 14 min | [Open](https://shikharkumar13.github.io/Statistics-for-Data-Science/statistics-for-data-science-day-1.html) |
| 2 | **Types of Data & Scales of Measurement** | Qualitative vs. quantitative, nominal, ordinal, interval, ratio | 2 | 12 min | [Open](https://shikharkumar13.github.io/Statistics-for-Data-Science/statistics-for-data-science-day-2.html) |
| 3 | **Measures of Central Tendency** | Mean, median, mode, trimmed mean, when each one lies to you | 4 | 13 min | [Open](https://shikharkumar13.github.io/Statistics-for-Data-Science/statistics-for-data-science-day-3.html) |
| 4 | **Measures of Dispersion** | Range, variance, standard deviation, MAD, IQR, the outlier fence rule | 4 | 14 min | [Open](https://shikharkumar13.github.io/Statistics-for-Data-Science/statistics-for-data-science-day-4.html) |
| 5 | **Relative Measures of Dispersion** | Coefficient of Variation, Coefficient of Quartile Deviation | 3 | 12 min | [Open](https://shikharkumar13.github.io/Statistics-for-Data-Science/statistics-for-data-science-day-5.html) |
| 6 | **Correlation and Covariance** | Pearson r, Spearman &rho;, Kendall's &tau;, why correlation isn't causation | 8 | 20 min | [Open](https://shikharkumar13.github.io/Statistics-for-Data-Science/statistics-for-data-science-day-6.html) |
 
### Part II: Probability and distributions (Days 7 to 10)
 
Modeling uncertainty before a single sample gets collected.
 
| # | Article | Covers | Diagrams | Read time | Link |
|--:|---------|--------|:-:|:-:|:-:|
| 7 | **Introduction to Probability** | Sample spaces, combinatorics, conditional probability, Bayes' Theorem | 5 | 16 min | [Open](https://shikharkumar13.github.io/Statistics-for-Data-Science/statistics-for-data-science-day-7.html) |
| 8 | **Random Variables and Probability Distributions** | Random variables, the PMF, the PDF, the CDF | 6 | 15 min | [Open](https://shikharkumar13.github.io/Statistics-for-Data-Science/statistics-for-data-science-day-8.html) |
| 9 | **Discrete Probability Distributions** | Bernoulli, Binomial, Geometric, Poisson, and how they relate | 6 | 18 min | [Open](https://shikharkumar13.github.io/Statistics-for-Data-Science/statistics-for-data-science-day-9.html) |
| 10 | **Continuous Probability Distributions** | Uniform, Normal, Exponential, and the Central Limit Theorem | 9 | 17 min | [Open](https://shikharkumar13.github.io/Statistics-for-Data-Science/statistics-for-data-science-day-10.html) |
 
### Part III: Inferential statistics and experimentation (Days 11 to 13)
 
Turning a sample you can actually collect into a decision you can defend.
 
| # | Article | Covers | Diagrams | Read time | Link |
|--:|---------|--------|:-:|:-:|:-:|
| 11 | **From Samples to Certainty** | Sampling methods, Standard Error, confidence intervals, Bootstrap | 7 | 24 min | [Open](https://shikharkumar13.github.io/Statistics-for-Data-Science/statistics-for-data-science-day-11.html) |
| 12 | **Hypothesis Testing End to End** | H&#8320;/H&#8321;, p-values, Type I/II errors, power, Bonferroni correction | 5 | 22 min | [Open](https://shikharkumar13.github.io/Statistics-for-Data-Science/statistics-for-data-science-day-12.html) |
| 13 | **A/B Testing: The Applied Playbook** | Experiment design, sample size and MDE, randomization, peeking, Simpson's paradox | 4 | 24 min | [Open](https://shikharkumar13.github.io/Statistics-for-Data-Science/statistics-for-data-science-day-13.html) |
 
Days 11 to 13 also close with a set of interview-style questions, drawn from real data
science interview loops, worked the way you'd actually want to answer one out loud.
 
---
 
## Repository layout
 
```
.
├── docs/                                     the published site (GitHub Pages)
│   ├── index.html                            series index
│   └── statistics-for-data-science-day-N.html   one self-contained article per day
│
└── README.md
```
 
Each article is a single self-contained HTML file: inline stylesheet, inline SVG
diagrams, and pre-formatted, syntax-highlighted code blocks. The only external
dependency is a system font stack, nothing is fetched from a CDN. Diagrams are
hand-built SVG driven by the article's own verified numbers, not screenshots of a
plotting library, so a diagram of a p-value or a confidence interval is drawn from
the exact figures in the code block next to it.
 
---
 
## Verified, not just written
 
Every worked example in this series was executed before publication, and every claim
that could be checked, was. That includes:
 
- All 77 code examples, run and compared against the output shown on the page
- Every confidence interval, p-value, sample size, and effect size in the five solved
  business problems that anchor Days 11 through 13
- Every simulation with a fixed random seed, re-run to confirm it reproduces exactly,
  including the ones with surprising results (a 26% false-positive rate from peeking
  at an experiment early, a Central Limit Theorem simulation whose skewness collapses
  from 2.00 to 0.32 purely from averaging)
- Terminology, not just arithmetic: a property being called by the wrong name is
  still an error, even when the number attached to it is right
Where this process found a mistake in the original draft, the fix and a short note on
what was wrong are part of the article itself, not silently patched over. Statistics
is exactly the wrong subject to take on faith.
 
---
 
## How each article gets made
 
Each day starts as a Substack draft. Turning it into the audited edition means:
 
1. **Read the whole draft before touching anything.** No edits until the source is
   fully understood.
2. **Re-derive every number.** Formulas get re-run in Python; simulations get re-run
   with the stated seed; anything that doesn't reproduce gets flagged and corrected.
3. **Add diagrams only where they earn their place.** A diagram gets built when it
   would change what a reader takes away, not by default and not for decoration. Every
   diagram is generated from the article's own verified numbers, then hand-styled as
   SVG to match the series' visual language.
4. **Humanize the prose.** Short sentences, no em dashes, plain words for technical
   ideas, real company examples instead of urns and coins wherever the concept allows
   it.
5. **Close with a check.** Each article ends with a handful of quiz-style questions a
   reader can use to confirm the concept actually landed.
---
 
## Where to go next
 
This series ends where experiment design becomes production machine learning.
 
1. **This series.** Descriptive statistics, probability, and inference.
2. **[Python Programming Series](https://github.com/shikharkumar13/Python-Programming-Code).**
   The language these worked examples are written in, from a first literal to a
   tested, packaged pipeline.
3. **Machine learning, MLOps, and AI engineering.** Everything that needs a trained
   model, a monitored experiment, or a deployed service, all of it resting on the
   confidence intervals and hypothesis tests built here.
---
 
## Notes
 
- Articles are self-contained enough to read out of order, but Days 11 to 13 lean
  directly on Days 7 to 10, and Day 13 assumes Days 11 and 12 are already read.
- "DSAI with Shikhar" on Substack carries the original day-by-day posts as they were
  first published. This repository is the revised, verified, and diagram-enhanced
  edition of the same 13 days.
