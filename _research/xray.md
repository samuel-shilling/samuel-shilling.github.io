---
title: "X-ray afterglow correlation analysis"
layout: single-portfolio
excerpt: ""
collection: research
order_number: 12
header:
  teaser: xray_2.png
  og_image: /images/xray_2.png
---
## Does brighter mean faster-fading in all cases? 

**The context.** Gamma-ray bursts (GRBs) are among the most energetic explosions in the universe, and their X-ray afterglows fade over hours to days. Earlier studies suggested that brighter afterglows tend to fade faster. I tested how that relationship holds up in a much larger dataset by applying rigorous statistical techniques.

**The method.** I wrote a Python pipeline to retrieve X-ray light curves for ~1900 GRBs observed by NASA's Swift satellite since 2004, then cleaned the data and selected those which have a measured distance (this is an important requirement which not all sources have). This resulted in 427 events with usable data. For each one, I measured the intrinsic brightness 200 s after the burst and the average rate of fading from that point.

**What I found.**
- Across all 427 afterglows there is a clear correlation (Spearman's rank $0.54 \pm 0.04$ at a statistical significance of $\geq 3 \sigma$). I quantified the uncertainty by bootstrapping over 100,000 trials.
- In a subset of 102 well-sampled long GRBs (a particular type of GRB) the correlation significantly increases in strength to $0.80 \pm 0.04$ and the scatter drops sharply. This suggests much of the noise comes from patchy observations, not from the physics.

**Bias testing.** Because I identified scatter was attributed to poor datasets, I selected this subset on data quality which potentially invites selection biases. I tested whether the selection itself could create the improved results. The two groups have consistent intrinsic brightness distributions, and the other differences I found (energy, redshift) are small or explained by observing conditions.

<div class="center-image">
<img src="/images/xray_2.png" width="450" alt="Scatter plot of afterglow decay rate against luminosity, showing a positive correlation">
</div>
*Decay rate against luminosity for the full sample. Brighter afterglows tend to fade faster.*

