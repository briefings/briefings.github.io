---
layout: default
title: Spark Dataset & Spark SQL
nav_order: 3
has_children: true
permalink: /docs/Spark-dataset-and-spark-sql
---

# Spark Dataset & Spark SQL

Spark Dataset or Spark SQL
{: .fs-6 .fw-300 }


## Introduction

Within Apache Spark engineers & scientists may query data
  [programmatically via SQL](http://spark.apache.org/docs/2.4.7/sql-getting-started.html#running-sql-queries-programmatically) or [via Dataset objects](https://databricks.com/glossary/what-are-datasets).  A valid question is, why Dataset objects?  Amongst other characteristics, Dataset objects are strongly typed and

<p style="margin-left: 25px; margin-right: 25px; font-size: 95%">
  <span style="color: #555555">&ldquo;... are "lazy", i.e. computations are only triggered when an action is invoked. Internally, a Dataset represents a
  logical plan that describes the computation required to produce the data. When an action is invoked, Spark's query
  optimizer optimizes the logical plan and generates a physical plan for efficient execution in a parallel and distributed manner.&rdquo;</span>
  [<a href="https://spark.apache.org/docs/latest/api/scala/org/apache/spark/sql/Dataset.html">Dataset</a>]
</p>

<p>
  In addition to the ScalaDoc definition of a <a href="https://spark.apache.org/docs/latest/api/scala/org/apache/spark/sql/Dataset.html">Dataset</a>, the
  Databricks articles <a href="https://databricks.com/glossary/what-are-datasets">What are Datasets?</a> &
  <a href="https://docs.databricks.com/spark/latest/dataframes-datasets/introduction-to-datasets.html">Introduction to Datasets</a>
  are also helpful references.
</p>

<br>

The **Examples** section outlines parallel Dataset & SQL queries.
