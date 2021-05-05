---
layout: default
title: Parallel Examples
parent: Spark Dataset & Spark SQL
nav_order: 2
custom_js:
- latex
custom_css:
- lists
---

<br>

# Parallel Examples
{: .no_toc }

<br>

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---


## In focus

### Implicit & Explicit Filtering Operators

Thus far, the examples include **(a)** explicit filtering operators [where, filter](https://github.com/briefings/buildings/blob/master/src/main/scala/com/grey/queries/FilteringOperators.scala) and [limit](https://github.com/briefings/buildings/blob/master/src/main/scala/com/grey/queries/FundamentalClauses.scala), **(b)** logical operators [like, in, between, is null](https://github.com/briefings/buildings/blob/master/src/main/scala/com/grey/queries/LogicalOperators.scala), and **(c)** relational operators [$=$, $\\neq$, $\\gt$, $\\lt$, $\\ge$, $\\le$](https://github.com/briefings/buildings/blob/master/src/main/scala/com/grey/queries/RelationalOperators.scala)  [Logical operators: not, or, and.  Filtering operators: distinct, fetch.]

<br>

### Aggregating, Ordering

A set of aggregation examples - [count(), sum(), avg(), min(), max()](https://github.com/briefings/stocks/blob/master/src/main/scala/com/grey/queries/Aggregating.scala) - is illustrated via a stock price series.  And, [order by](https://github.com/briefings/buildings/blob/master/src/main/scala/com/grey/queries/FundamentalClauses.scala) is illustrated via a buildings data set.

<br>

### Conditionals

The focus herein is the [case statement](https://github.com/briefings/stocks/blob/master/src/main/scala/com/grey/queries/Conditionals.scala).  As usual, the case statement is a sequence of *if-then* rules, and an *else*.


<br>

### Grouping

&nbsp; |comment
:--- |:---
[group by, having](https://github.com/briefings/stocks/blob/master/src/main/scala/com/grey/queries/Grouping.scala) | Dataset[Row] does not have a having function, instead there are effective proxy functions. Beware of the SQL query structure w.r.t. using Spark SQL having<br>
[roll up](https://github.com/briefings/bikeshare/blob/master/src/main/scala/com/grey/queries/HierarchicalArithmetic.scala) | For hierarchical arithmetic.


<br>

### Window Operations

&nbsp; |comment
:--- |:---
[sum](https://github.com/briefings/bikeshare/blob/master/src/main/scala/com/grey/queries/ContinuousArithmetic.scala) | additions by window
[rank, dense rank](https://github.com/briefings/bikeshare/blob/master/src/main/scala/com/grey/queries/RankingArithmetic.scala) |assigning ranks per window, Per window, if there are multiple equivalent values the dense rank function will ...
[row number](https://github.com/briefings/bikeshare/blob/master/src/main/scala/com/grey/queries/NumberingArithmetic.scala) | numbering data rows per window

<br>

## Upcoming

<ul>
  <li><b>Combinatorial queries.</b> Via $cube()$</li>
  <li><b>Joins.</b>  More join examples, e.g., right outer join, full outer join,  <span class="tooltip">left semi join
    <span class="tooltiptext" style="font-size: small">filters the left table w.r.t. keys present in the right table</span></span>,
    <span class="tooltip">left anti join <span class="tooltiptext" style="font-size: small">filters the left table for records
      that are NOT present in the right table</span> </span></li>
  <li><b>Pivoting.</b>  Pivoting via Dataset objects is explicit and elegant.  The
    <a href="https://github.com/briefings/buildings/blob/master/src/main/scala/com/grey/sources/DataReconfiguration.scala">DataReconfiguration</a>
    class, which reconfigures the data used by the <a href="https://github.com/briefings/buildings">buildings project/module</a>,
    uses the Dataset pivot function for a reconfiguration step.</li>
</ul>
