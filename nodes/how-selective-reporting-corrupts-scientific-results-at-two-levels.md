---
slug: how-selective-reporting-corrupts-scientific-results-at-two-levels
title: "How Selective Reporting Corrupts Scientific Results at Two Levels"
subtitle: "We called the fishing trip a hypothesis test."
observer: "Brian Nosek"
observer_slug: brian-nosek
source_title: "EP12 Brian Nosek – Open Science and Reproducibility"
source_url: "https://www.youtube.com/watch?v=6eKvI0QhKFI"
source_author: "The Jim Rutt Show"
tags: [Epistemology, Information Theory, Sensemaking]
edges:
  - target: why-sciences-reward-system-undermines-its-own-values
    type: grounds
  - target: registered-reports-peer-review-before-data-collection-fixes-publication-bias
    type: applies
  - target: psychologys-three-layer-crisis-fragmentation-misidentity-and-self-concealment
    type: exemplifies
created_at: "2026-04-01"
---

# How Selective Reporting Corrupts Scientific Results at Two Levels

We called the fishing trip a hypothesis test.

---

> The replication crisis stems not from bad actors but from a predictable collision between two layers of selective reporting — choosing which studies to publish and which analyses to run — compounded by scientists never being taught the distinction between exploration and confirmation.

The replication crisis is best understood not as a problem of fraud or incompetence, but as the predictable output of selective reporting operating at two levels simultaneously. The first is study-level selection: researchers run many experiments but report only a subset, and the subset is systematically skewed toward positive outcomes. The second, more subtle, and arguably more damaging level is analysis-level selection: once a researcher is inside a dataset, the data itself begins to inform which analyses get run and reported. This iterative, data-informed analysis process is cognitively natural and scientifically generative for exploration — but it is catastrophic for the diagnosticity of statistical inference when it gets mislabeled as confirmation. Any high-dimensional dataset contains spurious correlations by mathematical necessity; giving yourself the freedom to hunt for them guarantees you'll find some. The solution is not to ban exploration — exploratory research is essential and valuable — but to make the distinction between exploration and confirmation legible and honest. Pre-registration serves exactly this function: it doesn't privilege confirmatory over exploratory research, it simply marks which is which, so that readers can calibrate their confidence appropriately. The tragedy is that this distinction is essentially statistics 102, yet training programs in the life sciences routinely have no formal coursework in experimental design, leaving scientists to absorb methodology from their labs, which may themselves be perpetuating flawed intuitions about what p-values mean and what the .05 threshold actually signifies.

## Apprentice

Science has a well-known problem: many published findings fail to hold up when other researchers try to repeat them. The usual suspects — fraud, sloppiness — explain only a small fraction of this. The deeper cause is selective reporting, and it operates on two levels. First, researchers tend to share only the experiments that "worked," burying the rest. Second, and more insidiously, once inside a dataset, researchers naturally try different ways of analyzing it until something interesting emerges. This is perfectly fine as exploration, but it becomes misleading when it's presented as though the result was predicted all along.

Any sufficiently rich dataset will contain patterns that look meaningful but are actually coincidental. If you give yourself permission to search freely, you will inevitably find such patterns. The problem isn't the searching — it's pretending you weren't searching. Pre-registration, the practice of publicly declaring your hypothesis and analysis plan before looking at the data, exists to draw a clear line between exploring and confirming.

The deeper tragedy is that this distinction is not conceptually difficult. It is basic statistics. Yet many scientists in biology and medicine complete their training without a single formal course in experimental design, instead absorbing research habits from mentors who may themselves misunderstand what their statistical tests actually tell them.

## Adept

The replication crisis is most productively understood as the predictable consequence of selective reporting operating at two distinct levels. Study-level selection — the file-drawer problem — is well recognized: researchers conduct many studies but disproportionately publish those yielding positive results, inflating the literature's apparent effect sizes. The second level, analysis-level selection, is subtler and arguably more corrosive. Within a single dataset, the data themselves begin to shape which comparisons get tested, which covariates get included, and which subgroups get examined. This iterative, data-informed process is cognitively natural and genuinely useful for hypothesis generation, but it is catastrophic for inferential validity when its outputs are presented as confirmatory. High-dimensional datasets contain spurious correlations by mathematical necessity; unconstrained analytic flexibility guarantees their discovery.

Pre-registration addresses this problem not by privileging confirmatory over exploratory work, but by making the boundary between them legible. It is a labeling device, not a hierarchy. Readers can then calibrate their evidential confidence accordingly — treating pre-registered confirmations as stronger evidence and exploratory findings as promising leads requiring independent replication.

What makes this situation genuinely tragic is that the exploration-confirmation distinction is elementary — it belongs in any introductory course on experimental design. Yet training programs across the life sciences routinely lack formal coursework in methodology and statistical reasoning. Scientists absorb their inferential habits through apprenticeship in labs that may themselves perpetuate deep misunderstandings about what p-values represent, what the .05 threshold actually controls for, and how researcher degrees of freedom interact with nominal error rates.

## Magus

The replication crisis resolves into sharper focus when reframed as the inevitable output of a two-tiered selective reporting process rather than an indictment of individual integrity. The first tier — study-level selection — is the familiar file-drawer effect, systematically enriching the published literature with positive results and inflating meta-analytic effect size estimates. The second tier — analysis-level selection — is epistemically more dangerous precisely because it is less visible and more cognitively seamless. Once a researcher enters a high-dimensional dataset, the data begin to condition the analytic path: variable transformations, covariate adjustments, subgroup definitions, and outcome operationalizations are iteratively refined in light of emerging patterns. This process is indistinguishable, from the inside, from good scientific reasoning. Yet it converts what is functionally an exploratory search through a vast analytic space into something that gets reported — and read — as a single confirmatory test, with all the inferential weight that framing implies.

The mathematical point is straightforward: in any sufficiently high-dimensional space, spurious correlations exceeding conventional thresholds exist with probability approaching unity. Researcher degrees of freedom function as a search algorithm over this space, and the nominal alpha level ceases to bound the actual false-positive rate. Pre-registration intervenes at precisely the right joint — not by constraining scientific creativity, but by enforcing an honest partition between the hypothesis-generating and hypothesis-testing phases of inquiry, thereby preserving the diagnosticity of statistical inference for the latter.

The institutional failure is that this partition — conceptually no more demanding than the distinction between training and test sets in machine learning — remains absent from the methodological formation of most life scientists. Inferential reasoning is acquired through lab-based apprenticeship, propagating misapprehensions about the ontological status of p-values, the meaning of the Neyman-Pearson framework, and the relationship between analytic flexibility and error-rate control across generations of otherwise rigorous researchers.
