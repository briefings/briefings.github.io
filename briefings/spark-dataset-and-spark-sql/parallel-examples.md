---
layout: default
title: Parallel Examples
parent: Spark Dataset & Spark SQL
nav_order: 2
custom_js:
- latex
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


## Examples

The <span style="color: #722f37"><i>sample programs</i></span> of each table link to examples within Apache Spark programs.  The programs explore

<ul style="margin-left:35px">
  <li><a href="https://github.com/briefings/stocks" target="\_blank">Apple stock prices</a></li>
  <li><a href="https://github.com/briefings/firms" target="\_blank">A subset of CrunchBase companies data</a></li>
  <li><a href="https://github.com/briefings/bikeshare" target="\_blank">Washington D.C. Capital BikeShare data</a></li>
  <li><a href="https://github.com/briefings/buildings" target="\_blank">United States Census Bureau buildings data</a></li>
</ul>

<br>

### Filtering Operators

The examples do not yet include **(a)** the logical operators *not, or, and*, and **(b)** the filtering operators *distinct, fetch*.

<table>
  <tr>
      <th style="width:20%;text-align: left;">sample programs</th><th style="text-align: left;">comment</th>
  </tr>
  <tr>
    <td><a href="https://github.com/briefings/buildings/blob/master/src/main/scala/com/grey/queries/FilteringOperators.scala" target="\_blank">where, filter</a>, <a href="https://github.com/briefings/buildings/blob/master/src/main/scala/com/grey/queries/FundamentalClauses.scala" target="\_blank">limit</a> </td>
    <td>Explicit filtering operators.</td>
  </tr>
  <tr>    
    <td><a href="https://github.com/briefings/buildings/blob/master/src/main/scala/com/grey/queries/LogicalOperators.scala" target="\_blank">like, in, between,<br>is null</a></td>
    <td>Logical operators.</td>
  </tr>
  <tr>    
    <td><a href="https://github.com/briefings/buildings/blob/master/src/main/scala/com/grey/queries/RelationalOperators.scala" target="\_blank">$=$, $\neq$, $\gt$, $\lt$,<br>$\ge$, $\le$</a></td>
    <td>Relational operators.</td>
  </tr>
  <tr>
    <td></td>
    <td></td>
  </tr>
</table>

<br>

### Aggregating, Ordering

<table>
  <tr>
      <th style="width:20%;text-align: left;">sample programs</th><th style="text-align: left;">comment</th>
  </tr>
  <tr>    
    <td><a href="https://github.com/briefings/stocks/blob/master/src/main/scala/com/grey/queries/Aggregating.scala" target="\_blank">count(), sum(), avg(),<br>min(), max()</a></td>
    <td>For aggregating</td>
  </tr>
  <tr>    
    <td><a href="https://github.com/briefings/buildings/blob/master/src/main/scala/com/grey/queries/FundamentalClauses.scala" target="\_blank">order by</a></td>
    <td>&nbsp;</td>
  </tr>
  <tr>
    <td></td>
    <td></td>
  </tr>
</table>

<br>

### Conditionals

<table>
  <tr>
      <th style="width:20%;text-align: left;">sample programs</th><th style="text-align: left;">comment</th>
  </tr>
  <tr>
    <td><a href="https://github.com/briefings/stocks/blob/master/src/main/scala/com/grey/queries/Conditionals.scala" target="\_blank">case statement</a></td>
    <td>Read more about the <a href="https://spark.apache.org/docs/latest/api/sql/#when" target="\_blank">case statement</a></td>
  </tr>
  <tr>
    <td></td>
    <td></td>
  </tr>
</table>

<br>

### Grouping

<table>
  <tr>
      <th style="width:20%;text-align: left;">sample programs</th><th style="text-align: left;">comment</th>
  </tr>
  <tr>
    <td><a href="https://github.com/briefings/stocks/blob/master/src/main/scala/com/grey/queries/Grouping.scala" target="\_blank">group by, having</a></td>
    <td>Dataset[Row] does not have a having function, instead there are effective proxy functions. Beware of the SQL query structure w.r.t. using Spark SQL having</td>
  </tr>
  <tr>
    <td><a href="https://github.com/briefings/bikeshare/blob/master/src/main/scala/com/grey/queries/HierarchicalArithmetic.scala" target="\_blank">roll up</a></td>
    <td>For hierarchical arithmetic.</td>
  </tr>
  <tr>
    <td></td>
    <td></td>
  </tr>
</table>

<br>

### Window Operations

<table>
  <tr>
      <th style="width:20%;text-align: left;">sample programs</th><th style="text-align: left;">comment</th>
  </tr>
  <tr>
    <td><a href="https://github.com/briefings/bikeshare/blob/master/src/main/scala/com/grey/queries/ContinuousArithmetic.scala" target="\_blank">sum().over()</a></td>
    <td>&nbsp;</td>
  </tr>
  <tr>
    <td><a href="https://github.com/briefings/bikeshare/blob/master/src/main/scala/com/grey/queries/RankingArithmetic.scala" target="\_blank">rank(), dense_rank()</a></td>
    <td>Read more about <a href="https://spark.apache.org/docs/latest/api/sql/index.html#rank">rank()</a> and <a href="https://spark.apache.org/docs/latest/api/sql/index.html#dense_rank">dense_rank()</a></td>
  </tr>
  <tr>
    <td><a href="https://github.com/briefings/bikeshare/blob/master/src/main/scala/com/grey/queries/NumberingArithmetic.scala" target="\_blank">row_number()</a></td>
    <td>Read more about <a href="https://spark.apache.org/docs/latest/api/sql/index.html#row_number">row_number()</a></td>
  </tr>
  <tr>
    <td></td>
    <td></td>
  </tr>
</table>

<br>
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


<br>
<br>
<br>
<br>
