
#### Parameters defininig the current scenario are:
    * FROM has 1-3 JPs-pklt
    * the join paths are joined only by the primary key of the linking tables
    * groups may appear
    * HAVING-max 3 scalar s-q, max 3 non-scalar s-q

#### Here is an "average" query of this scenario:<br>



 SELECT ROUND(t1.l_quantity, 0) AS ROUND__t1__l_quantity__0, EXTRACT (YEAR FROM t3.l_receiptdate) AS EXTRACT____YEAR__FROM__t3__l_receiptdate, EXTRACT (MONTH FROM t3.l_receiptdate) AS EXTRACT____MONTH__FROM__t3__l_receiptdate, t3.l_shipmode AS t3__l_shipmode, t3.ps_partkey AS t3__ps_partkey, t3.l_shipinstruct AS t3__l_shipinstruct, t3.l_extendedprice AS t3__l_extendedprice, LOG(2, t1.l_linenumber) AS LOG__2__t1__l_linenumber, SQRT(t3.s_suppkey) AS SQRT__t3__s_suppkey, t1.p_brand AS t1__p_brand, t3.ps_suppkey AS t3__ps_suppkey, t3.n_regionkey AS t3__n_regionkey, t2.ps_comment AS t2__ps_comment, LTRIM(t1.p_comment) AS LTRIM__t1__p_comment, EXTRACT (MONTH FROM t1.l_receiptdate) AS EXTRACT____MONTH__FROM__t1__l_receiptdate, UPPER(t3.ps_comment) AS UPPER__t3__ps_comment FROM<br>(SELECT \<br />FROM <br><space><space><space><space> lineitem lineitem1 RIGHT JOIN partsupp partsupp1 ON lineitem1.l_suppkey = partsupp1.ps_suppkey AND lineitem1.l_partkey = partsupp1.ps_partkey RIGHT JOIN part part1 ON partsupp1.ps_partkey = part1.p_partkey ) t1 FULL JOIN<br>(SELECT \<br />FROM <br><space><space><space><space> partsupp partsupp2 RIGHT JOIN supplier supplier2 ON partsupp2.ps_suppkey = supplier2.s_suppkey ) t2 ON t1.ps_partkey = t2.ps_partkey AND t1.ps_suppkey = t2.ps_suppkey  LEFT JOIN<br>(SELECT \<br />FROM <br><space><space><space><space> lineitem lineitem3 RIGHT JOIN partsupp partsupp3 ON lineitem3.l_suppkey = partsupp3.ps_suppkey AND lineitem3.l_partkey = partsupp3.ps_partkey RIGHT JOIN supplier supplier3 ON partsupp3.ps_suppkey = supplier3.s_suppkey INNER JOIN nation nation3 ON supplier3.s_nationkey = nation3.n_nationkey ) t3 ON t1.ps_partkey = t3.ps_partkey AND t1.ps_suppkey = t3.ps_suppkey  WHERE t2.s_comment IN  ( 'eposits. slyly final deposits toward the slyly regular dependencies sleep among the excu')   AND t2.s_address NOT BETWEEN  'n48Wy4QI3lml8T217rk' AND 'SLlacbhgpKmVa,gF3saYv12e0'  OR t3.l_returnflag NOT IN  ( 'A', 'A', 'N', 'N', 'N', 'N', 'R', 'R', 'R', 'R')   OR t1.ps_comment <=  'o beans boost carefully fluffily ironic accounts. express courts eat furiously. accounts boost carefull'  OR EXTRACT (DAY FROM t3.l_receiptdate)  <=  17 OFFSET 553 ROWS FETCH NEXT 845 ROWS ONLY

