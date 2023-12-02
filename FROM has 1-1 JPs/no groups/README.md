
### Parameters defining the current scenario are:
    * FROM has 1-1 JPs
    * no groups
    

### Here is a typical query of this scenario:<br>



 SELECT MAX(nation.n_name) AS MAX__nation__n_name<br>FROM<br>&emsp; nation <br>FETCH NEXt 590 ROWS ONLY


<br><br>

### ... and a "lengthier" one:
<br>


 SELECT distinct SQRT(customer.c_custkey) AS SQRT__customer__c_custkey<br>&emsp; ,TRUNC(lineitem.l_discount, 0) AS TRUNC__lineitem__l_discount__0<br>&emsp; ,orders.o_orderpriority AS orders__o_orderpriority<br>&emsp; ,customer.c_mktsegment AS customer__c_mktsegment<br>&emsp; ,orders.o_totalprice AS orders__o_totalprice<br>&emsp; ,lineitem.l_quantity AS lineitem__l_quantity<br>&emsp; ,region.r_regionkey AS region__r_regionkey<br>&emsp; ,nation.n_nationkey AS nation__n_nationkey<br>&emsp; ,EXTRACT (MONTH FROM lineitem.l_shipdate) AS EXTRACT____MONTH__FROM__lineitem__l_shipdate<br>&emsp; ,EXTRACT (DAY FROM lineitem.l_shipdate) AS EXTRACT____DAY__FROM__lineitem__l_shipdate<br>&emsp; ,lineitem.l_tax AS lineitem__l_tax<br>&emsp; ,FLOOR(lineitem.l_extendedprice) AS FLOOR__lineitem__l_extendedprice<br>&emsp; ,customer.c_comment AS customer__c_comment<br>&emsp; ,orders.o_orderdate AS orders__o_orderdate<br>&emsp; ,RTRIM(lineitem.l_shipinstruct) AS RTRIM__lineitem__l_shipinstruct<br>&emsp; ,lineitem.l_partkey AS lineitem__l_partkey<br>&emsp; ,SUBSTR(customer.c_address, 8, 52) AS SUBSTR__customer__c_address__8__52<br>&emsp; ,EXTRACT (YEAR FROM lineitem.l_receiptdate) AS EXTRACT____YEAR__FROM__lineitem__l_receiptdate<br>&emsp; ,nation.n_comment AS nation__n_comment<br>&emsp; ,LOWER(lineitem.l_linestatus) AS LOWER__lineitem__l_linestatus<br>&emsp; ,customer.c_acctbal AS customer__c_acctbal<br>&emsp; ,EXTRACT (YEAR FROM lineitem.l_commitdate) AS EXTRACT____YEAR__FROM__lineitem__l_commitdate<br>&emsp; ,EXTRACT (MONTH FROM lineitem.l_commitdate) AS EXTRACT____MONTH__FROM__lineitem__l_commitdate<br>&emsp; ,EXTRACT (DOW<br>FROM<br>&emsp; lineitem.l_commitdate) AS EXTRACT____DOW__FROM__lineitem__l_commitdate<br>&emsp; ,SQRT(orders.o_shippriority) AS SQRT__orders__o_shippriority<br>&emsp; ,lineitem.l_orderkey AS lineitem__l_orderkey<br>&emsp; ,lineitem.l_shipmode AS lineitem__l_shipmode<br>&emsp; ,customer.c_name AS customer__c_name<br>&emsp; ,UPPER(orders.o_clerk) AS UPPER__orders__o_clerk<br>&emsp; ,LOWER(orders.o_comment) AS LOWER__orders__o_comment<br>&emsp; ,lineitem.l_linenumber AS lineitem__l_linenumber<br>&emsp; ,LOG(2<br>&emsp; ,lineitem.l_suppkey) AS LOG__2__lineitem__l_suppkey<br>&emsp; ,customer.c_nationkey AS customer__c_nationkey<br>&emsp; ,LOWER(nation.n_name) AS LOWER__nation__n_name<br>&emsp; ,nation.n_regionkey AS nation__n_regionkey<br>FROM<br>&emsp; lineitem<br>&emsp;INNER JOIN orders ON lineitem.l_orderkey = orders.o_orderkey<br>&emsp;INNER JOIN customer ON orders.o_custkey = customer.c_custkey<br>&emsp;INNER JOIN nation ON customer.c_nationkey = nation.n_nationkey<br>&emsp;INNER JOIN region ON nation.n_regionkey = region.r_regionkey <br>WHERE<br>&emsp; customer.c_custkey <>  83 <br>&emsp; OR nation.n_name <  'JORDAN                   ' <br>&emsp; OR customer.c_name >  'Customer#000000107' <br>ORDER BY<br>&emsp; EXTRACT (DOW<br>FROM<br>&emsp; lineitem.l_commitdate) DESC<br>&emsp; ,LOG(2<br>&emsp; ,lineitem.l_suppkey) DESC<br>&emsp; ,SQRT(orders.o_shippriority) DESC  <br>OFFSET 931 <br>LIMIT 662

