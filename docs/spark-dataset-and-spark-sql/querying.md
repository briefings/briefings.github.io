---
layout: default
title: Querying
parent: Spark Dataset & Spark SQL
nav_order: 1
custom_js:
- latex
---

# Querying
{: .no_toc }

<br>

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Why Datasets?

Within Apache Spark engineers & scientists may query data [programmatically via SQL](http://spark.apache.org/docs/2.4.7/sql-getting-started.html#running-sql-queries-programmatically) or [via Dataset objects](https://databricks.com/glossary/what-are-datasets).  A valid question is, why Dataset objects?  Amongst other characteristics, Dataset objects are strongly typed and

<p style="margin-left: 25px; margin-right: 25px; font-size: 95%">
  <span style="color: #555555">&ldquo;... are "lazy", i.e. computations are only triggered when an action is invoked. Internally, a Dataset represents a
  logical plan that describes the computation required to produce the data. When an action is invoked, Spark's query
  optimizer optimizes the logical plan and generates a physical plan for efficient execution in a parallel and distributed manner.&rdquo;</span>
  [<a href="https://spark.apache.org/docs/latest/api/scala/org/apache/spark/sql/Dataset.html">Dataset</a>]
</p>

In addition to this ScalaDoc definition, the Databricks articles <a href="https://databricks.com/glossary/what-are-datasets">What are Datasets?</a> &
<a href="https://docs.databricks.com/spark/latest/dataframes-datasets/introduction-to-datasets.html">Introduction to Datasets</a>
are also helpful references.

<br>

The **Examples** section outlines parallel Dataset & SQL queries.


<br>

## Parallel Examples


fundamentals |buildings |stocks |comment
:--- |:--- |:--- |:---
filtering |[$\checkmark$](https://github.com/briefings/buildings/blob/master/src/main/scala/com/grey/queries/FilteringOperators.scala) | |where, filter
logical operators |[$\checkmark$](https://github.com/briefings/buildings/blob/master/src/main/scala/com/grey/queries/LogicalOperators.scala) | |like, in, between, is null, etc.
relational operators |[$\checkmark$](https://github.com/briefings/buildings/blob/master/src/main/scala/com/grey/queries/RelationalOperators.scala) | |$=$, $\\neq$, $\\gt$, $\\lt$, $\\ge$, $\\le$
fundamental clauses |[$\checkmark$](https://github.com/briefings/buildings/blob/master/src/main/scala/com/grey/queries/FundamentalClauses.scala) | |limit, order by
arithmetic |[$\checkmark$](https://github.com/briefings/buildings/blob/master/src/main/scala/com/grey/queries/ArithmeticExpressions.scala) | |
aggregating | |[$\checkmark$](https://github.com/briefings/stocks/blob/master/src/main/scala/com/grey/queries/Aggregating.scala) |count(), sum(), avg(), min(), max()
conditions | |[$\checkmark$](https://github.com/briefings/stocks/blob/master/src/main/scala/com/grey/queries/Conditionals.scala) |via CASE Statement
grouping | |[$\checkmark$](https://github.com/briefings/stocks/blob/master/src/main/scala/com/grey/queries/Grouping.scala) |group by, having$^{1}$
