
#### Parameters defininig the current scenario are:
    * FROM has 1-1 JPs
    * no groups
    

#### Here is an "average" query of this scenario:<br>



 SELECT distinct nation.n_nationkey AS nation__n_nationkey<br>FROM<br>&emsp; nation <br>WHERE<br>&emsp; nation.n_regionkey BETWEEN  0<br>&emsp; AND 1 <br>&emsp; OR nation.n_comment >  'ular asymptotes are about the furious multipliers. express dependencies nag above the ironically ironic account' <br>ORDER BY<br>&emsp; nation.n_nationkey DESC <br>FETCH NEXt 967 ROWS ONLY


<br><br>#### ... and a "lengthier" one:
<br>


 SELECT distinct lineitem.l_extendedprice AS lineitem__l_extendedprice<br>&emsp; ,supplier.s_acctbal AS supplier__s_acctbal<br>&emsp; ,EXTRACT (YEAR FROM lineitem.l_receiptdate) AS EXTRACT____YEAR__FROM__lineitem__l_receiptdate<br>&emsp; ,EXTRACT (MONTH FROM lineitem.l_receiptdate) AS EXTRACT____MONTH__FROM__lineitem__l_receiptdate<br>&emsp; ,lineitem.l_suppkey AS lineitem__l_suppkey<br>&emsp; ,RTRIM(lineitem.l_comment) AS RTRIM__lineitem__l_comment<br>&emsp; ,partsupp.ps_partkey AS partsupp__ps_partkey<br>&emsp; ,LOWER(supplier.s_comment) AS LOWER__supplier__s_comment<br>&emsp; ,LTRIM(supplier.s_address) AS LTRIM__supplier__s_address<br>&emsp; ,lineitem.l_partkey AS lineitem__l_partkey<br>&emsp; ,lineitem.l_shipmode AS lineitem__l_shipmode<br>&emsp; ,RTRIM(supplier.s_name) AS RTRIM__supplier__s_name<br>&emsp; ,FLOOR(lineitem.l_tax) AS FLOOR__lineitem__l_tax<br>&emsp; ,supplier.s_phone AS supplier__s_phone<br>&emsp; ,lineitem.l_returnflag AS lineitem__l_returnflag<br>&emsp; ,lineitem.l_quantity AS lineitem__l_quantity<br>&emsp; ,lineitem.l_orderkey AS lineitem__l_orderkey<br>&emsp; ,supplier.s_nationkey AS supplier__s_nationkey<br>&emsp; ,partsupp.ps_availqty AS partsupp__ps_availqty<br>&emsp; ,FLOOR(partsupp.ps_supplycost) AS FLOOR__partsupp__ps_supplycost<br>&emsp; ,EXTRACT (DAY FROM lineitem.l_commitdate) AS EXTRACT____DAY__FROM__lineitem__l_commitdate<br>&emsp; ,supplier.s_suppkey AS supplier__s_suppkey<br>&emsp; ,UPPER(lineitem.l_shipinstruct) AS UPPER__lineitem__l_shipinstruct<br>&emsp; ,partsupp.ps_comment AS partsupp__ps_comment<br>&emsp; ,partsupp.ps_suppkey AS partsupp__ps_suppkey<br>&emsp; ,lineitem.l_discount AS lineitem__l_discount<br>&emsp; ,lineitem.l_linenumber AS lineitem__l_linenumber<br>FROM<br>&emsp; lineitem<br>&emsp;INNER JOIN partsupp ON lineitem.l_suppkey = partsupp.ps_suppkey<br>&emsp; AND lineitem.l_partkey = partsupp.ps_partkey<br>&emsp;INNER JOIN supplier ON partsupp.ps_suppkey = supplier.s_suppkey <br>WHERE<br>&emsp; partsupp.ps_suppkey <  48 <br>&emsp; AND lineitem.l_orderkey >  17795 <br>&emsp; AND EXTRACT (MONTH FROM lineitem.l_shipdate)  >=  12 <br>&emsp; OR lineitem.l_quantity NOT BETWEEN  3<br>&emsp; AND 14 <br>&emsp; OR ABS(partsupp.ps_supplycost)  <>  53.6 <br>ORDER BY<br>&emsp; LOWER(supplier.s_comment) ASC<br>&emsp; ,supplier.s_phone DESC<br>&emsp; ,UPPER(lineitem.l_shipinstruct) DESC <br>OFFSET 805 ROWS <br>FETCH NEXt 538 ROWS ONLY

