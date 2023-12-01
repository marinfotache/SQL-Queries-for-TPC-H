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

<table style="width:50%">
  <tr>
    <th>scenario_code</th>
    <th>FROM</th>
    <th>min_n_of_join_paths</th>
    <th>max_n_of_join_paths</th>
    <th>how_join_paths_are_joined</th>
    <th>aggregation</th>
    <th>group_by_and_having</th>
  </tr>
  <tr>
    <th>1-1jp__ng</th>
    <th>FROM has 1-1 JPs</th>
    <th>1</th>
    <th>1</th>
    <th> </th>
    <th>no groups</th>
    <th>no groups</th>
  </tr>
    
</table>


<table style="width:100%">
  <tr>
    <th>Company</th>
    <th>Contact</th>
    <th>Country</th>
  </tr>
  <tr>
    <td>Alfreds Futterkiste</td>
    <td>Maria Anders</td>
    <td>Germany</td>
  </tr>
  <tr>
    <td>Centro comercial Moctezuma</td>
    <td>Francisco Chang</td>
    <td>[Mexico]([htttp://wwww.uaic.ro](https://www.uaic.ro))</td>
  </tr>
</table>



 
