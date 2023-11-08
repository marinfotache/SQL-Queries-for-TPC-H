
#### Parameters defininig the current scenario are:
    * FROM has 1-3 JPs-pklt
    * the join paths are joined only by the primary key of the linking tables
    * groups may appear
    * HAVING-max 3 scalar s-q, max 3 non-scalar s-q

#### Here is an "average" query of this scenario:<br>



 SELECT
     ROUND(t1.l_quantity, 0) AS ROUND__t1__l_quantity__0<br>    ,EXTRACT (YEAR FROM t3.l_receiptdate) AS EXTRACT____YEAR__FROM__t3__l_receiptdate<br>    ,EXTRACT (MONTH FROM t3.l_receiptdate) AS EXTRACT____MONTH__FROM__t3__l_receiptdate<br>    ,t3.l_shipmode AS t3__l_shipmode<br>    ,t3.ps_partkey AS t3__ps_partkey<br>    ,t3.l_shipinstruct AS t3__l_shipinstruct<br>    ,t3.l_extendedprice AS t3__l_extendedprice<br>    ,LOG(2<br>    ,t1.l_linenumber) AS LOG__2__t1__l_linenumber<br>    ,SQRT(t3.s_suppkey) AS SQRT__t3__s_suppkey<br>    ,t1.p_brand AS t1__p_brand<br>    ,t3.ps_suppkey AS t3__ps_suppkey<br>    ,t3.n_regionkey AS t3__n_regionkey<br>    ,t2.ps_comment AS t2__ps_comment<br>    ,LTRIM(t1.p_comment) AS LTRIM__t1__p_comment<br>    ,EXTRACT (MONTH FROM t1.l_receiptdate) AS EXTRACT____MONTH__FROM__t1__l_receiptdate<br>    ,UPPER(t3.ps_comment) AS UPPER__t3__ps_comment FROM (SELECT * FROM  lineitem lineitem1 <br>    RIGHT JOIN partsupp partsupp1 ON lineitem1.l_suppkey = partsupp1.ps_suppkey<br    /> AND lineitem1.l_partkey = partsupp1.ps_partkey <br>    RIGHT JOIN part part1 ON partsupp1.ps_partkey = part1.p_partkey ) t1 FULL JOIN (SELECT * FROM  partsupp partsupp2 <br>    RIGHT JOIN supplier supplier2 ON partsupp2.ps_suppkey = supplier2.s_suppkey ) t2 ON t1.ps_partkey = t2.ps_partkey<br    /> AND t1.ps_suppkey = t2.ps_suppkey  <br>    LEFT JOIN (SELECT * FROM  lineitem lineitem3 <br>    RIGHT JOIN partsupp partsupp3 ON lineitem3.l_suppkey = partsupp3.ps_suppkey<br    /> AND lineitem3.l_partkey = partsupp3.ps_partkey <br>    RIGHT JOIN supplier supplier3 ON partsupp3.ps_suppkey = supplier3.s_suppkey <br>    INNER JOIN nation nation3 ON supplier3.s_nationkey = nation3.n_nationkey ) t3 ON t1.ps_partkey = t3.ps_partkey<br    /> AND t1.ps_suppkey = t3.ps_suppkey  <br>WHERE<br>     t2.s_comment IN  ( 'eposits. slyly final deposits toward the slyly regular dependencies sleep among the excu')  <br    /> AND t2.s_address NOT BETWEEN  'n48Wy4QI3lml8T217rk'<br    /> AND 'SLlacbhgpKmVa,gF3saYv12e0' <br>    OR t3.l_returnflag NOT IN  ( 'A', 'A', 'N', 'N', 'N', 'N', 'R', 'R', 'R', 'R')  <br>    OR t1.ps_comment <=  'o beans boost carefully fluffily ironic accounts. express courts eat furiously. accounts boost carefull' <br>    OR EXTRACT (DAY FROM t3.l_receiptdate)  <=  17 <br>OFFSET 553 ROWS <br>FETCH NEXt 845 ROWS ONLY

