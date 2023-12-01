### Scenarios
*  Are designed to control the query parameters variability.
*  Manage the complexity of the generated query
*  Sometimes they are also associated with particular SQL dialects (e.g., SparSQL)

### Main parameters which define a scenario, by the query clause/section
* FROM:
    - The minimum number of join paths included in a query 
    - The maximum number of join paths included in a query 
    - How the join paths may be joined with the linking table:
      * pklt - only by the primary key of the linking table (rjjp - restricted join of the join paths)
      * aalt - by any attribute of the linking table (ujjp - unrestricted join of the join paths)
* GROUP BY: whether this clause may appear 
* HAVING:
    - The minimal number of predicates using scalar subqueries
    - The maximal number of predicates using scalar subqueries
    - The minimal number of predicates using non-scalar subqueries
    - The maximal number of predicates using non-scalar subqueries


### List of scenarios with generated queries

<table style="width:100%">
  <tr>
    <th>         scenario_code         </th>
    <th>        FROM       </th>
    <th>min_n_of_join_paths</th>
    <th>max_n_of_join_paths</th>
    <th>    how_join_paths_are_joined   </th>
    <th>aggregation</th>
    <th>      group_by_and_having      </th>
  </tr>
  <tr>
    <td><a href="https://github.com/marinfotache/SQL-Queries-for-TPC-H/tree/main/FROM%20has%201-1%20JPs/no%20groups">1-1jp__ng</a></td>
    <th>FROM has 1-1 JPs</th>
    <th>1</th>
    <th>1</th>
    <th> </th>
    <th>no groups</th>
    <th>no groups</th>
  </tr>
  <tr>
    <td><a href="https://github.com/marinfotache/SQL-Queries-for-TPC-H/tree/main/FROM%20has%201-1%20JPs/HAVING-no%20scalar%20s-q%2C%20no%20non-scalar%20s-q">1-1jp__g__h0ss_h0nss</a></td>
    <th>FROM has 1-1 JPs</th>
    <th>1</th>
    <th>1</th>
    <th> </th>
    <th>groups may appear</th>
    <th>HAVING-no scalar subqueries, no non-scalar subqueries</th>
  </tr>
  <tr>
    <td><a href="https://github.com/marinfotache/SQL-Queries-for-TPC-H/tree/main/FROM%20has%201-1%20JPs/HAVING-max%203%20scalar%20s-q%2C%20max%203%20non-scalar%20s-q">1-1jp__g__h0-3ss_h0-3nss</a></td>
    <th>FROM has 1-1 JPs</th>
    <th>1</th>
    <th>1</th>
    <th> </th>
    <th>groups may appear</th>
    <th>HAVING-max 3 scalar subqueries, max 3 non-scalar subqueries</th>
  </tr>
  <tr>
    <td><a href="https://github.com/marinfotache/SQL-Queries-for-TPC-H/tree/main/FROM%20has%201-3%20JPs-aalt/HAVING-no%20scalar%20s-q%2C%20no%20non-scalar%20s-q">1-3jp_ujjp__g__h0ss_h0nss</a></td>
    <th>FROM has 1-3 JPs-aalt</th>
    <th>1</th>
    <th>3</th>
    <th>the join paths are joined by any attribute(s) of the linking table</th>
    <th>groups may appear</th>
    <th>HAVING-no scalar subqueries, no non-scalar subqueries</th>
  </tr>
    
</table>




