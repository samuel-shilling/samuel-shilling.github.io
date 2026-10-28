---
title: "Radio afterglow correlation analysis"
layout: single-portfolio
excerpt: ""
collection: research
order_number: 13
header: 
  teaser: radio.png
  og_image: <img src="/images/radio.png" width="400">

---

## Does an empirical correlation hold up at the lowest possible energy? 

**The context.** Earlier studies found that brighter gamma-ray burst afterglows fade faster, in optical, X-ray and GeV light. Does the same hold in a new untested data-domain, the radio?

**The method.** I filtered a catalogue of radio observations from 480 GRBs down to the 16 with well-constrained 8.5 GHz light curves, then measured each afterglow's luminosity at 10 days and its average rate of fading after that. I found a clear correlation (Spearman's rank of $-0.70 \pm 0.13$ at a statistical significance of $\geq 3 \sigma$). Uncertainties were quantified by bootstrapping. Together they show the effect spans 15 orders of magnitude in frequency, which points to a cause that doesn't depend on the type of light. I also conducted a linear regression analysis to quantify the relationship.

**Extensive bias testing.** With only 16 events, a chance result was a real risk, so I tested it directly. A Monte Carlo simulation of 1,000,000 trials, with my selection criteria applied, produced a correlation this strong only 0.17% of the time. 

**What I found.**
- The correlation holds up even at the lowest end of the electromagnetic spectrum, placing important constraints on the physical underlying mechanism.


<!-- ![Radio figure](/images/radio.png)
Figure -->
<div class="center-image">
    <img src="/images/radio.png" width="450">
</div>
*Decay rate against luminosity for the final sample. Brighter afterglows tend to fade faster.*
