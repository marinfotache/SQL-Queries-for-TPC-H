A scenario is a combination of the following query parameters:

- Join paths cardinality and join type: appears at the beginning of the scenario code and is defined by:
  * Minimum number of join paths included in a query. Values: [1, 2, 3]
  * Maximum number of join paths included in a query. Range: [1, 2, 3, 6]
  * How the join paths may be joined (of course, for queries containing at least two join paths):
    - only by the primary key (rjjp - restricted join of the join paths)
    - by any attribute, not only the primary keys (ujjp - unrestricted join of the join paths)

  Examples of scenarios:
* 1-1jp__g__h0-3ss_h0-3nss - queries may contain only one join path
* 1-3jp_rjjp__g__h0-3ss_h0-3nss - ...


- the query may contain GROUP BY (value g for GROPU

- the minimum number of scalar subqueries included in clause HAVING (between 0 and 6)

- the minimum number of non-scalar subqueries included in clause HAVING (between 0 and 6)


