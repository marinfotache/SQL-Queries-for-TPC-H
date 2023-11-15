
#### Parameters defininig the current scenario are:
    * FROM has 1-3 JPs
    * the join paths are joined by any attribute(s) of the linking table
    * groups may appear
    * HAVING-no scalar s-q, no non-scalar s-q

#### Here is an "average" query of this scenario:<br>



 SELECT supplier.s_name AS supplier__s_name<br>&emsp; ,supplier.s_suppkey AS supplier__s_suppkey<br>&emsp; ,MAX(supplier.s_nationkey) AS MAX__supplier__s_nationkey<br>&emsp; ,MAX(LOWER(supplier.s_address)) AS MAX__LOWER__supplier__s_address<br>FROM<br>&emsp; partsupp<br>&emsp;INNER JOIN supplier ON partsupp.ps_suppkey = supplier.s_suppkey <br>WHERE<br>&emsp; partsupp.ps_comment <=  're furiously final deposits. closely regular gifts wake carefully across the foxes; even accounts play slyly. carefully ironic courts sleep slyly fluffily' <br>&emsp; AND supplier.s_suppkey <  47 <br>GROUP BY<br>&emsp; supplier.s_name <br>&emsp; ,supplier.s_suppkey  <br>HAVING<br>&emsp;  MAX(LOWER(supplier.s_address)) =  '84nmc1rmqfo0fj3zkoblt'   or MAX(supplier.s_nationkey) <=  19  <br>OFFSET 648 ROWS <br>FETCH NEXt 467 ROWS ONLY


<br><br>#### ... and a "lengthier" one:
<br>


 SELECT t3.n_regionkey AS t3__n_regionkey<br>&emsp; ,LOWER(t3.n_comment) AS LOWER__t3__n_comment<br>&emsp; ,t1.c_nationkey AS t1__c_nationkey<br>&emsp; ,t1.c_comment AS t1__c_comment<br>&emsp; ,t2.c_name AS t2__c_name<br>&emsp; ,t3.c_address AS t3__c_address<br>&emsp; ,AVG(SQRT(t2.l_discount)) AS AVG__SQRT__t2__l_discount<br>&emsp; ,COUNT(t3.o_orderstatus) AS COUNT__t3__o_orderstatus<br>&emsp; ,COUNT(UPPER(t3.o_comment)) AS COUNT__UPPER__t3__o_comment<br>&emsp; ,COUNT(RTRIM(t2.c_phone)) AS COUNT__RTRIM__t2__c_phone<br>&emsp; ,COUNT(t1.c_custkey) AS COUNT__t1__c_custkey<br>&emsp; ,COUNT(LTRIM(t2.l_linestatus)) AS COUNT__LTRIM__t2__l_linestatus<br>&emsp; ,AVG(t1.o_totalprice) AS AVG__t1__o_totalprice<br>FROM<br>&emsp; (SELECT *<br>FROM<br>&emsp;  orders orders1<br>&emsp;INNER JOIN customer customer1 ON orders1.o_custkey = customer1.c_custkey ) t1<br>&emsp;RIGHT JOIN<br>(SELECT *<br>FROM<br>&emsp;  lineitem lineitem2<br>&emsp;RIGHT JOIN orders orders2 ON lineitem2.l_orderkey = orders2.o_orderkey<br>&emsp;INNER JOIN customer customer2 ON orders2.o_custkey = customer2.c_custkey<br>&emsp;RIGHT JOIN nation nation2 ON customer2.c_nationkey = nation2.n_nationkey ) t2 ON  t1.o_orderstatus = t2.o_orderstatus <br>&emsp;RIGHT JOIN<br>(SELECT *<br>FROM<br>&emsp;  orders orders3<br>&emsp;RIGHT JOIN customer customer3 ON orders3.o_custkey = customer3.c_custkey<br>&emsp;INNER JOIN nation nation3 ON customer3.c_nationkey = nation3.n_nationkey ) t3 ON t2.o_clerk = t3.o_clerk<br>&emsp; AND o_totalprice<br>&emsp; AND t2.o_custkey = t3.o_custkey  <br>WHERE<br>&emsp; t2.c_mktsegment >=  'FURNITURE ' <br>&emsp; OR t2.c_comment LIKE  '%ending packages cajole quickly furiously special ' <br>&emsp; OR t2.n_comment BETWEEN  'ss excuses cajole slyly across the packages. deposits print aroun'<br>&emsp; AND 'y above the carefully unusual theodolites. final dugouts are quickly across the furiously regular d' <br>GROUP BY<br>&emsp; t3.n_regionkey ,  LOWER(t3.n_comment) <br>&emsp; ,t1.c_nationkey <br>&emsp; ,t1.c_comment <br>&emsp; ,t2.c_name <br>&emsp; ,t3.c_address  <br>ORDER BY<br>&emsp; AVG(t1.o_totalprice) DESC<br>&emsp; ,t1.c_comment ASC<br>&emsp; ,LOWER(t3.n_comment) DESC <br>FETCH NEXt 648 ROWS ONLY

