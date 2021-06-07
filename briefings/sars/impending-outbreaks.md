---
layout: default
title: Impending Outbreaks
parent: SARS-CoV-2 Trends & Metrics
nav_order: 2
has_children: true
custom_css:
- tooltips
- generic
custom_js:
- latex
---

# Impending Outbreaks
{: .no_toc }

<br>

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---


### Anticipating Outbreaks

<p>This exploration is focused on "anticipating outbreaks via running percentage changes" of "cumulative observations per $\mathbf{\small{100K}}$ people" <span class="tooltip">w.r.t.<span class="tooltiptext">with respect to</span></span> a set of time periods.  Why such an approach?  Foremost, a mathematical outline which will make it easier to understand the discussion herein.</p>

<p><b>Let</b></p>

<div class="equation">$\mathcal{C}_{\tau} = \small{100K} \times \Large{\frac{\theta_{\tau}}{\mathcal{P}} }$</div>

<p>wherein</p>
<table>
  <tr>
    <th style="width: 13%;"></th><th style="text-align: left;">Description</th>
  </tr>
  <tr>
    <td>$\tau$</td><td>Date</td>
  </tr>
  <tr>
    <td>$\theta$</td><td>Observations;  $\theta$ is <b>either</b> deaths, positives, tests, or hospitalizations</td>
  </tr>
  <tr>
    <td>$\theta_{\tau}$</td><td>The number of observations by date $\tau$</td>
  </tr>
  <tr>
    <td>$\mathcal{P}$</td><td>The population of the area in question</td>
  </tr>
</table>

<br>

<p><b>Then</b> a percentage change on date $\:\tau\:$ w.r.t. $\:\Delta\:$ days ago is</p>

<div class="equation">$\text{pc}_{\tau, \Delta} = 100 * \Large{ \frac{C_{\tau} \; - \; C_{\tau - \Delta}}{C_{\tau - \Delta}} }$</div>

<p>noting that</p>

<table>
  <tr>
    <th style="width:13%"></th><th style="text-align: left;">Description</th>
  </tr>
  <tr>
    <td>$\Delta$</td><td>Days</td>
  </tr>
  <tr>
    <td>$C_{\tau - \Delta}$</td><td>The cumulative [observations per 100K] value on date $\tau - \Delta$</td>
  </tr>
</table>

<br>

<p><b>Now</b>, consider the  graph of curves below.  Each point on the 14 days curve, for example, is the
percentage change relative to 14 days ago; the same logic applies to other "days ago", each having
its own curve.</p>

<br>

<figure>
  <img src="/assets/images/sars/delta.png" alt="stick" style="width:65%" />
  <figcaption>Running percentage changes</figcaption>
</figure>

<br>

<p>It is the accumulative behaviour of these curves that is of interest due to the following observations/hypotheses</p>

<div style="margin-left: 35px;margin-right: 55px">
  <b>Positives</b>
  <ul>
    <li>A divergence point, i.e., an x-axis point from whence curves start diverging, is probably a warning of an impending
      outbreak.  And the probability of the outbreak occurring increases if there weren't any mitigating measures
      [coincidentally] in place around the same time.</li>
    <li>Converging curves that are approaching zero suggests an improving state of affairs.</li>
  </ul>

  <b>Hospitalizations</b>
  <ul>
    <li>A divergence point is probably a warning that there might be a substantial increase
      in required hospitalizations.  Such a point should set off a contingency planning alert.</li>
  </ul>
</div>

<p>I will write more about percentage change curves in future.  Meanwhile, a few graphs are illustrated below.</p>

<br>

### Graphs

<p>Note, the most consistently available data sets are the tests, positives, and deaths data sets.</p>
