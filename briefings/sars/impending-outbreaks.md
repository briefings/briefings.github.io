---
layout: default
title: Impending Outbreaks
parent: SARS-CoV-2 Trends & Metrics
nav_order: 2
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


## Anticipating Outbreaks

<p>This exploration is focused on --anticipating outbreaks via running percentage changes-- of --cumulative observations per $\mathbf{\small{100K}}$ people-- <span class="tooltip">w.r.t.<span class="tooltiptext">with respect to</span></span> a set of time periods.  Why such an approach?  Foremost, a mathematical outline which will make it easier to understand the discussion herein.</p>

<p><b>Let</b></p>

<div class="equation">$\mathcal{C}_{\tau} = \small{100K} \times \Large{\frac{\theta_{\tau}}{(\text{population of the area in question})} }$</div>

<p>wherein</p>
<table style="width:55%">
  <tr>
    <th style="width:20%"></th><th>Description</th>
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
</table>
