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


## In focus

### Fundamentals

&nbsp; |buildings |stocks |comment
:--- |:--- |:--- |:---
**fundamentals** | | |
filtering |[$\checkmark$](https://github.com/briefings/buildings/blob/master/src/main/scala/com/grey/queries/FilteringOperators.scala) | |where, filter
 |[$\checkmark$](https://github.com/briefings/buildings/blob/master/src/main/scala/com/grey/queries/FundamentalClauses.scala) | |limit
 | | |distinct, fetch
logical operators |[$\checkmark$](https://github.com/briefings/buildings/blob/master/src/main/scala/com/grey/queries/LogicalOperators.scala) | |like, in, between, is null, etc. [not, or, and]
relational operators |[$\checkmark$](https://github.com/briefings/buildings/blob/master/src/main/scala/com/grey/queries/RelationalOperators.scala) | |$=$, $\\neq$, $\\gt$, $\\lt$, $\\ge$, $\\le$

<br>

### Aggregating, Ordering

&nbsp; |buildings |stocks |comment
:--- |:--- |:--- |:---
**fundamentals** | | |
aggregating | |[$\checkmark$](https://github.com/briefings/stocks/blob/master/src/main/scala/com/grey/queries/Aggregating.scala) |count(), sum(), avg(), min(), max()
ordering|[$\checkmark$](https://github.com/briefings/buildings/blob/master/src/main/scala/com/grey/queries/FundamentalClauses.scala) | |order by

<br>

### Conditionals

&nbsp; |stocks |comment
:--- |:--- |:---
**fundamentals** | |
case statements |[$\checkmark$](https://github.com/briefings/stocks/blob/master/src/main/scala/com/grey/queries/Conditionals.scala) |case statements include a sequence of if-then rules, and an else.

<br>

### Grouping

&nbsp; |buildings |bikeshare |comment
:--- |:--- |:--- |:---
**fundamentals** | | |
group by, having |[$\checkmark$](https://github.com/briefings/stocks/blob/master/src/main/scala/com/grey/queries/Grouping.scala) | |Dataset[Row] does not have a having function, instead there are effective proxy functions. Beware of the SQL query structure w.r.t. using Spark SQL having
hierarchical arithmetic | |[$\checkmark$](https://github.com/briefings/bikeshare/blob/master/src/main/scala/com/grey/queries/HierarchicalArithmetic.scala) |rollup()

Note:
* $^{1}$Dataset[Row] does not have a having function, instead there are effective proxy functions. Beware of the SQL query structure w.r.t. using Spark SQL having

<br>

### Window Operations

&nbsp; |bikeshare |comment
:--- |:--- |:---
**aggregate** | |
sum |[$\checkmark$](https://github.com/briefings/bikeshare/blob/master/src/main/scala/com/grey/queries/ContinuousArithmetic.scala) |
**ranking** | |
rank, dense rank |[$\checkmark$](https://github.com/briefings/bikeshare/blob/master/src/main/scala/com/grey/queries/RankingArithmetic.scala) |Per window, if there are multiple equivalent values the dense rank function will ...
row number |[$\checkmark$](https://github.com/briefings/bikeshare/blob/master/src/main/scala/com/grey/queries/NumberingArithmetic.scala) |

<br>

## Upcoming

<p>The examples will illustrate</p>
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
