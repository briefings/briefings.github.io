---
layout: default
title: Impending Outbreaks
parent: SARS-CoV-2 Trends & Metrics
nav_order: 2
custom_css:
- generic
- tabs
- tooltips
custom_js:
- tabs
- latex
---

# Background
{: .no_toc }

<br>

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---


## Anticipating Outbreaks

<p>This exploration is focused on <b>anticipating outbreaks via running percentage changes</b> of <b>cumulative observations per $\mathbf{\small{100K}}$ people</b> <span class="tooltip">w.r.t.<span class="tooltiptext">with respect to</span></span> a set of time periods.  Why such an approach?  Foremost, a mathematical outline which will make it easier to understand the discussion herein.</p>

<p><b>Let</b></p>

<div class="equation">$\mathcal{C}_{\tau} = \small{100K} \times \Large{\frac{\theta_{\tau}}{(\text{population of the area in question})} }$</div>

<p>wherein</p>
<table>
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

<p><b>Then</b> a percentage change on date $\:\tau\:$ w.r.t. $\:\Delta\:$ days ago is</p>

<div class="equation">$\text{pc}_{\tau, \Delta} = 100 * \Large{ \frac{C_{\tau} \; - \; C_{\tau - \Delta}}{C_{\tau - \Delta}} }$</div>

<p>noting that</p>

<table>
  <tr>
    <th style="width:20%"></th><th>Description</th>
  </tr>
  <tr>
    <td>$\Delta$</td><td>Days</td>
  </tr>
  <tr>
    <td>$C_{\tau - \Delta}$</td><td>The cumulative [observations per 100K] value on date $\tau - \Delta$</td>
  </tr>
</table>

<p><b>Now</b>, consider the  graph of curves below.  Each point on the 14 days curve, for example, is the percentage change relative to 14 days ago; the same logic applies to other "days ago", each having its own curve.</p>

<br>
<figure>
  <img src="../assets/images/delta.png" alt="stick" style="width:95%" />
  <figcaption>Running percentage changes</figcaption>
</figure>

<br>
<p>It is <b>the accumulative behaviour of these curves</b> that is of interest due to the
  following observations/hypotheses</p>

<dl>
  <dt>Observations: Positives</dt>
  <dd><ul>
      <li>A divergence point, i.e., an x-axis point from whence curves start diverging, is probably a warning of an impending
        outbreak.  And the probability of the outbreak occurring increases if there weren't any mitigating measures
        [coincidentally] in place around the same time.</li>
      <li>converging curves that are approaching zero suggests an improving state of affairs.</li>
  </ul></dd>
  <dt>Observations: Hospitalizations</dt>
  <dd><ul>
      <li>A divergence point is probably a warning that there might be a substantial increase
        in required hospitalizations.  Such a point should set off a contingency planning alert.</li>
  </ul></dd>
</dl>

<p>I will write more about percentage change curves.  Meanwhile, a few graphs are illustrated below.</p>



### Graphs
<p>Note, the most consistently available data sets are the tests, positives, and deaths data sets.</p>

<div>

  <div class="tab">
    <button class="tablinks" onclick="tabs(event, 'delta')" id="defaultOpen">All</button>
    <button class="tablinks" onclick="tabs(event, 'deltaPR')">Postives</button>
    <button class="tablinks" onclick="tabs(event, 'deltaHR')">Hospitalized</button>
  </div>

  <div id="delta" class="tabcontent">
    <div class='tableauPlaceholder' id='viz1606317021717' style='position: relative'>
      <noscript><a href='#'><img alt=' ' src='https://public.tableau.com/static/images/pe/percentages_twb/percentages_twb/1_rss.png' style='border: none' /></a></noscript>
      <object class='tableauViz'  style='display:none;'>
        <param name='host_url' value='https://public.tableau.com/' /> <param name='embed_code_version' value='3' /> <param name='site_root' value='' />
        <param name='name' value='percentages_twb/percentages_twb' />
        <param name='tabs' value='no' /> <param name='toolbar' value='yes' />
        <param name='static_image' value='https://public.tableau.com/static/images/pe/percentages_twb/percentages_twb/1.png' />
        <param name='animate_transition' value='yes' />
        <param name='display_static_image' value='yes' /><param name='display_spinner' value='yes' />
        <param name='display_overlay' value='yes' /><param name='display_count' value='yes' />
        <param name='language' value='en' />
      </object>
    </div>
    <script type='text/javascript'>
        var divElement = document.getElementById('viz1606317021717');
        var vizElement = divElement.getElementsByTagName('object')[0];
        vizElement.style.width='500px';vizElement.style.height='1477px';
        var scriptElement = document.createElement('script');
        scriptElement.src = 'https://public.tableau.com/javascripts/api/viz_v1.js';
        vizElement.parentNode.insertBefore(scriptElement, vizElement);
    </script>
  </div>

  <div id="deltaPR" class="tabcontent">
    <div class='tableauPlaceholder' id='viz1606350521720' style='position: relative'>
      <noscript><a href='#'>
        <img alt=' ' src='https://public.tableau.com/static/images/Pe/PercentageChangeCumulativeValuesper100KSingleState/percentagesPRD_twb/1_rss.png' style='border: none' /></a>
      </noscript>
      <object class='tableauViz'  style='display:none;'>
        <param name='host_url' value='https://public.tableau.com/' />
        <param name='embed_code_version' value='3' /> <param name='site_root' value='' />
        <param name='name' value='PercentageChangeCumulativeValuesper100KSingleState/percentagesPRD_twb' />
        <param name='tabs' value='no' /><param name='toolbar' value='yes' />
        <param name='static_image' value='https://public.tableau.com/static/images/Pe/PercentageChangeCumulativeValuesper100KSingleState/percentagesPRD_twb/1.png' />
        <param name='animate_transition' value='yes' />
        <param name='display_static_image' value='yes' /><param name='display_spinner' value='yes' />
        <param name='display_overlay' value='yes' /><param name='display_count' value='yes' />
        <param name='language' value='en-GB' /></object></div>
    <script type='text/javascript'>
        var divElement = document.getElementById('viz1606350521720');
        var vizElement = divElement.getElementsByTagName('object')[0];
        vizElement.style.width='500px';vizElement.style.height='1477px';
        var scriptElement = document.createElement('script');
        scriptElement.src = 'https://public.tableau.com/javascripts/api/viz_v1.js';
        vizElement.parentNode.insertBefore(scriptElement, vizElement);
    </script>
  </div>

  <div id="deltaHR" class="tabcontent">
    <div class='tableauPlaceholder' id='viz1606388307733' style='position: relative'>
      <noscript><a href='#'><img alt=' ' src='https://public.tableau.com/static/images/pe/percentagesHRD_twb/percentagesHRD_twb/1_rss.png' style='border: none' /></a></noscript>
      <object class='tableauViz'  style='display:none;'>
        <param name='host_url' value='https://public.tableau.com/' />
        <param name='embed_code_version' value='3' /> <param name='site_root' value='' />
        <param name='name' value='percentagesHRD_twb/percentagesHRD_twb' />
        <param name='tabs' value='no' /><param name='toolbar' value='yes' />
        <param name='static_image' value='https://public.tableau.com/static/images/pe/percentagesHRD_twb/percentagesHRD_twb/1.png' />
        <param name='animate_transition' value='yes' />
        <param name='display_static_image' value='yes' /><param name='display_spinner' value='yes' />
        <param name='display_overlay' value='yes' /><param name='display_count' value='yes' /><param name='language' value='en-GB' />
      </object>
    </div>
    <script type='text/javascript'>
        var divElement = document.getElementById('viz1606388307733');
        var vizElement = divElement.getElementsByTagName('object')[0];
        vizElement.style.width='500px';vizElement.style.height='1477px';
        var scriptElement = document.createElement('script');
        scriptElement.src = 'https://public.tableau.com/javascripts/api/viz_v1.js';
        vizElement.parentNode.insertBefore(scriptElement, vizElement);
    </script>
  </div>

  <script>
      // Get the element with id="defaultOpen" and click on it
      document.getElementById("defaultOpen").click();
  </script>

</div>