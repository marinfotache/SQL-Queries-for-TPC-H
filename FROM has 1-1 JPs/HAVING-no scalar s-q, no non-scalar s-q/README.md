## Here is an "average" query of this type:
SELECT
     nation.n_regionkey AS nation__n_regionkey
    ,nation.n_name AS nation__n_name
    ,COUNT(nation.n_nationkey) AS COUNT__nation__n_nationkey 
FROM
     nation 
WHERE
     nation.n_regionkey NOT BETWEEN  1
    AND 3 
GROUP BY
     nation.n_regionkey 
    ,nation.n_name  
HAVING
      COUNT(nation.n_nationkey) >=  4  
ORDER BY
     COUNT(nation.n_nationkey) ASC 
FETCH NEXt 717 ROWS ONLY


## ... and a "lenghtier" one:
SELECT
     lineitem.l_suppkey AS lineitem__l_suppkey
    ,MIN(SUBSTR(lineitem.l_returnflag, 1, 0)) AS MIN__SUBSTR__lineitem__l_returnflag__1__0
    ,MAX(lineitem.l_extendedprice) AS MAX__lineitem__l_extendedprice 
FROM
     lineitem 
WHERE
     lineitem.l_shipmode NOT LIKE  'RA%' 
    OR lineitem.l_commitdate NOT IN  ( DATE'1992-04-22'
    ,DATE'1992-12-15'
    ,DATE'1993-10-08'
    ,DATE'1993-10-20'
    ,DATE'1993-11-20'
    ,DATE'1994-02-12'
    ,DATE'1994-05-08'
    ,DATE'1994-09-07'
    ,DATE'1994-09-25'
    ,DATE'1995-06-03'
    ,DATE'1995-12-06'
    ,DATE'1996-01-03'
    ,DATE'1996-01-30'
    ,DATE'1996-02-12'
    ,DATE'1996-03-28'
    ,DATE'1996-10-14'
    ,DATE'1997-07-12'
    ,DATE'1997-12-01'
    ,DATE'1998-06-27'
    ,DATE'1998-09-06')  
    OR lineitem.l_shipinstruct NOT LIKE  '%           ' 
    AND lineitem.l_returnflag >  'N' 
GROUP BY
     lineitem.l_suppkey  
ORDER BY
     MIN(SUBSTR(lineitem.l_returnflag, 1, 0)) DESC 
FETCH NEXt 792 ROWS ONLY