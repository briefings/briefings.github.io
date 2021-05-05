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

filtering<br>
$\quad \cdot$ [where, filter](https://github.com/briefings/buildings/blob/master/src/main/scala/com/grey/queries/FilteringOperators.scala)<br>
$\quad \cdot$ [limit](https://github.com/briefings/buildings/blob/master/src/main/scala/com/grey/queries/FundamentalClauses.scala)<br>
$\quad \cdot$ distinct, fetch

logical operators<br>
$\quad \cdot$ [like, in, between, is null](https://github.com/briefings/buildings/blob/master/src/main/scala/com/grey/queries/LogicalOperators.scala)<br>
$\quad \cdot$ not, or, and

relational operators<br>
$\quad \cdot$ [$=$, $\\neq$, $\\gt$, $\\lt$, $\\ge$, $\\le$](https://github.com/briefings/buildings/blob/master/src/main/scala/com/grey/queries/RelationalOperators.scala)

<br>

### Aggregating, Ordering

aggregating<br>
$\quad \cdot$ [count(), sum(), avg(), min(), max()](https://github.com/briefings/stocks/blob/master/src/main/scala/com/grey/queries/Aggregating.scala)

ordering<br>
$\quad \cdot$ [order by](https://github.com/briefings/buildings/blob/master/src/main/scala/com/grey/queries/FundamentalClauses.scala)

<br>

### Conditionals

conditionals<br>
$\quad \cdot$ [case statement](https://github.com/briefings/stocks/blob/master/src/main/scala/com/grey/queries/Conditionals.scala); Case statements include a sequence of if-then rules, and an else.

<br>

### Grouping

&nbsp; |comment
:--- |:---
[group by, having](https://github.com/briefings/stocks/blob/master/src/main/scala/com/grey/queries/Grouping.scala) | Dataset[Row] does not have a having function, instead there are effective proxy functions. Beware of the SQL query structure w.r.t. using Spark SQL having<br>
[roll up](https://github.com/briefings/bikeshare/blob/master/src/main/scala/com/grey/queries/HierarchicalArithmetic.scala) | For hierarchical arithmetic.


<br>

### Window Operations

&nbsp; |example |comment
:--- |:--- |:---
**aggregate** | |
sum |[$\checkmark$](https://github.com/briefings/bikeshare/blob/master/src/main/scala/com/grey/queries/ContinuousArithmetic.scala) |
**ranking** | |
rank, dense rank |[$\checkmark$](https://github.com/briefings/bikeshare/blob/master/src/main/scala/com/grey/queries/RankingArithmetic.scala) |Per window, if there are multiple equivalent values the dense rank function will ...
row number |[$\checkmark$](https://github.com/briefings/bikeshare/blob/master/src/main/scala/com/grey/queries/NumberingArithmetic.scala) |

<br>

## Upcoming

The examples will illustrate
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
