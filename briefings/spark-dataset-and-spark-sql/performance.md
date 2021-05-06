---
layout: default
title: Performance
parent: Spark Dataset & Spark SQL
nav_order: 3
custom_js:
- latex
---

<br>

# Performance
{: .no_toc }

<br>

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Boosting Performance

<p>The programs herein include performance aiding aspects, e.g.,</p>
<ul>
  <li>Reading data files via their schemata, e.g.,
    <a href="https://github.com/briefings/firms/blob/develop/src/main/resources/schemata/crunchbase/schemaOfCompanies.json">schemaOfCompanies.json</a></li>
  <li>Selectively, judiciously, <a href="https://spark.apache.org/docs/2.4.7/rdd-programming-guide.html#rdd-persistence">persisting in-memory</a>.</li>
  <li>Using persisted temporary views; if a Dataset or DataFrame can be [feasibly] persisted, temporary views are created via such persisted objects.</li>
</ul>

Parallelism is implicit & explicit throughout; wherever applicable and effective.
