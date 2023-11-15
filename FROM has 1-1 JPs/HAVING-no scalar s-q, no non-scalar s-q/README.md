
#### Parameters defininig the current scenario are:
    * FROM has 1-1 JPs
    * groups may appear
    * HAVING-no scalar s-q, no non-scalar s-q

#### Here is an "average" query of this scenario:<br>



 SELECT RTRIM(nation.n_comment) AS RTRIM__nation__n_comment<br>&emsp; ,COUNT(DISTINCT nation.n_name) AS COUNT__DISTINCT__nation__n_name<br>FROM<br>&emsp; nation <br>WHERE<br>&emsp; nation.n_nationkey <=  18 <br>GROUP BY<br>&emsp;  RTRIM(nation.n_comment)  <br>HAVING<br>&emsp;  COUNT(DISTINCT nation.n_name) not between  5<br>&emsp; AND 7  <br>ORDER BY<br>&emsp; RTRIM(nation.n_comment) DESC <br>OFFSET 269 ROWS <br>FETCH NEXt 857 ROWS ONLY


<br><br>#### ... and a "lengthier" one:
<br>


 SELECT supplier.s_nationkey AS supplier__s_nationkey<br>&emsp; ,MIN(supplier.s_comment) AS MIN__supplier__s_comment<br>&emsp; ,MIN(RTRIM(supplier.s_name)) AS MIN__RTRIM__supplier__s_name<br>&emsp; ,COUNT(supplier.s_acctbal) AS COUNT__supplier__s_acctbal<br>FROM<br>&emsp; partsupp<br>&emsp;INNER JOIN supplier ON partsupp.ps_suppkey = supplier.s_suppkey <br>WHERE<br>&emsp; supplier.s_phone NOT IN  ( '10-470-144-1330', '11-555-705-5922', '14-563-538-1657', '19-475-537-1368', '31-267-327-4328', '31-758-894-4436')  <br>&emsp; AND supplier.s_comment IN  ( ' even theodolites wake against the blithely fluffy packages', 'blithely pending dolphins. quickly regular theodolites haggle slyly', 'd. instructions integrate sometimes slyly pending instructions. accounts nag among the ', 'even depths. regular foxes use slyly. theod', 'ffily along the even decoys. final instructions abov', 'ias. carefully silent accounts cajole blithely. pending<br>&emsp; ,special accounts cajole quickly above the f', 'n<br>&emsp; ,ironic ideas would nag blithely about the slyly regular accounts. silent<br>&emsp; ,expr', 'ously express ideas haggle quickly dugouts? fu')  <br>&emsp; AND supplier.s_address NOT BETWEEN  'gfeKpYw3400L0SDywXA6Ya1Qmq1w6YB9f3R'<br>&emsp; AND 'YFo8an7P6wi Q' <br>GROUP BY<br>&emsp; supplier.s_nationkey  <br>HAVING<br>&emsp;  MIN(supplier.s_comment) >=  'l accounts boost. fluffily bold warhorses wake'   or MIN(RTRIM(supplier.s_name)) <  'Supplier#000000061'   or COUNT(supplier.s_acctbal) <>  4  <br>OFFSET 952 ROWS <br>FETCH NEXt 455 ROWS ONLY

