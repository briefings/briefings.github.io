---
layout: default
title: A note about candle sticks
parent: Daily Distributions
grand_parent: SARS-CoV-2 Trends & Metrics
nav_order: 1
custom_css:
- tooltips
- generic
custom_js:
- latex
---

# A note about candle sticks
{: .no_toc }

<br>

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

<h3>The Candlestick Graphs</h3>

<p>The <a href='https://www.highcharts.com/demo/stock/candlestick'>Japanese candlestick graph</a> is an excellent exploratory analysis tool for illustrating variation within a data set, and between data sets.  If a median line curve is superimposed, the graph will also portray <a href="https://www.itl.nist.gov/div898/handbook/eda/section3/eda351.htm">location</a> (median) and <a href="https://www.itl.nist.gov/div898/handbook/eda/section3/eda35b.htm">symmetry/asymmetry</a> (skewness) measures.  Succinct.<p>

<p>A few years ago I started re-purposing <a href='https://www.highcharts.com/demo/stock/candlestick'>HighCharts' Candlestick graphs</a> for data types other than stocks.  The core difference between a re-purposed graph, and an original, is what a candlestick wick represents.  In the case stock candlesticks, the ends of a wick denote the highest and lowest stock prices w.r.t. (with respect to) a time interval in question, whereas the wick ends of a re-purposed candlestick denote the 25th & 75th percentiles; as illustrated below, but also w.r.t. a time interval in question.  The candlestick graphs within any <a href='https://github.com/greyhypotheses#organisations'>greyhypotheses organisation</a> are annotated as illustrated below.</p>

<figure>
  <img src="/assets/images/sars/stick.png" alt="stick" style="float: middle;width:55%" />
  <figcaption>A candlestick with a superimposed median line.  Take note of the alternative names for the percentiles, e.g., the 90th percentile is also
    known as the upper whisker.  Altogether, this is akin to a <a href="https://www.itl.nist.gov/div898/handbook/eda/section3/boxplot.htm">box
      plot.</a></figcaption>
</figure>
