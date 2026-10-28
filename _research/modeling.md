---
title: "Using Bayesian inference to model GRB afterglows"
layout: single-portfolio
excerpt: ""
collection: research
order_number: 11
header: 
  teaser: inference_example.png
  og_image: <img src="/images/inference_example.png" width="375">
---

## What physics can we learn from observing these cosmic explosions?

**The context.** The jets of material launched by gamma-ray bursts can't be observed directly, but leaves clues in the form of `fingerprints' in the observed data, specifically in how the afterglow brightens and fades. It is very difficult to disentangle the data to find this imprinting, but not impossible.

**The method.** I developed a Python pipeline which uses Bayesian inference to model 316 GRB X-ray afterglows (these were selected from my other [X-ray project](/research/xray/)) for three different physical scenarios. Each fit was computationally heavy, so I parallelised the runs across multiple machines and cores and rebinned the data to cut runtime, after checking this didn't change the results. From these fits I can extract the Bayesian evidence for each model, infer estimates for the physical parameter values, and quantify parameter uncertainties.

**Robustness testing.** I simulated 100 synthetic light curves with known parameters and ran my pipeline on them. The parameters were recovered reliably, and I constrained an expected false-positive rate in the model selection. I adapted a means of classifying model selections based on their Bayesian evidence.

**What I found.**
- Most gamma-ray bursts are produced by a uniform jet (rather than a more complex structured jet)
- Inferred gamma-ray efficiencies are mostly low (median 0.17), consistent with theory.
- Expected jet-break times suggest that about 78% of "missing" jet breaks can be explained by observations ending too early or being too sparse.

<!-- ![Modeling figure](/images/modeling.png) -->
<div class="center-image">
    <img src="/images/inference_example.png" width="375">
</div>
*Corner plot and light curve showing the posterior and the model fit. Estimated parameter values were inferred from the posterior density at a confidence interval of $1\sigma$*