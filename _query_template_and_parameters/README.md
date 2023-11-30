### Here is a typical SQL query
![A PostgreSQL Query](https://github.com/marinfotache/SQL-Queries-for-TPC-H/blob/main/_query_template/Q2311052230000015.pdf)


### Query parameters stored in the metadata (.xlsx) files

* _query_id_ - unique identifier of the query                                      
* _scale_factor_ - the database size, expressed in GB                                
* _scenario_ - see `_scenarios_for_query_generation` section                                     

* _SELECT_n_of_columns_ - number of columns declared in main SELECT (number of columns in the query result)                     
* _SELECT_n_of_non_aggr_func__UPPER_ - number of times the (non-aggregate) function `UPPER` appears in the main SELECT clause
* _SELECT_n_of_non_aggr_func__LOWER_ - number of times function `LOWER` appears in main SELECT                
* _SELECT_n_of_non_aggr_func__LTRIM_ - number of times function `LTRIM` appears in main SELECT                 
* _SELECT_n_of_non_aggr_func__SUBSTR_ - number of times function `SUBSTR` appears in main SELECT    
* _SELECT_n_of_non_aggr_func__DAY_ - number of times function `EXTRACT DAY FROM...` appears in main SELECT   
* _SELECT_n_of_non_aggr_func__LOG_ - number of times function `LOG` appears in main SELECT   
* _SELECT_n_of_non_aggr_func__MONTH_ - number of times function `EXTRACT MONTH FROM...`  appears in main SELECT   
* _SELECT_n_of_non_aggr_func__RTRIM_ - number of times function RTRIM appears in main SELECT    
* _SELECT_n_of_non_aggr_func__YEAR_ - number of times function `EXTRACT YEAR FROM...`  appears in main SELECT    
* _SELECT_n_of_non_aggr_func__ABS_ - number of times function `ABS` appears in main SELECT   
* _SELECT_n_of_non_aggr_func__SQRT_ - number of times function `SQRT` appears in main SELECT   
* _SELECT_n_of_non_aggr_func__FLOOR_ - number of times function `FLOOR` appears in main SELECT   
* _SELECT_n_of_non_aggr_func__ROUND_ - number of times function `ROUND` appears in main SELECT    
* _SELECT_n_of_non_aggr_func__DOW_ - number of times function `EXTRACT DOW FROM...` (`DOW` stands for Day of the Week) appears in main SELECT   
* _SELECT_n_of_non_aggr_func__TRUNC_ - number of times function `TRUNC` appears in main SELECT   
* _SELECT_n_of_all_non_aggr_func_ - number of all non-aggregate functions (from `UPPER` to `TRUNC`) appearing in main SELECT   
* _SELECT_n_of_aggr_func__MIN_ - number of times the aggregate function `MIN` appears in main SELECT   
* _SELECT_n_of_aggr_func__COUNT_ - number of times the aggregate function `COUNT` appears in main SELECT   
* _SELECT_n_of_aggr_func__AVG_ - number of times the aggregate function `AVG` appears in main SELECT    
* _SELECT_n_of_aggr_func__MAX_ - number of times the aggregate function `MAX` appears in main SELECT  
* _SELECT_n_of_aggr_func__SUM_  - number of times the aggregate function `SUM` appears in main SELECT 
* _SELECT_n_of_aggr_func__COUNT_DISTINCT_ - number of times the aggregate function `COUNT DISTINCT` appears in main SELECT  
* _SELECT_n_of_all_aggr_func_ - total number of aggregate functions appearing in the main SELECT

* _FROM_n_of_join_paths_ - number of join paths included in the main FROM clause
* _FROM_n_of_super_joins__FULL_ - number of times the join paths are FULL OUTER JOIN-ed in the main FROM clause
* _FROM_n_of_super_joins__LEFT_ - number of times the join paths are LEFT OUTER JOIN-ed in the main FROM clause
* _FROM_n_of_super_joins__RIGHT_ - number of times the join paths are RIGHT OUTER JOIN-ed in the main FROM clause
* _FROM_n_of_joins__INNER_ - number of INNER JOINs in the main FROM clause
* _FROM_n_of_joins__RIGHT_ - number of RIGHT OUTER JOINs in the main FROM clause
* _FROM_n_of_processed_rows_ - total number of records for all tables appearing in the main FROM clause
  
* _WHERE_n_of_predicates_ - number of all predicates declared in the main WHERE clause
* _WHERE_n_of_attribs_of_type__character_varying_ - number of attributes of type string with variable length appearing in all predicates in the main WHERE clause
* _WHERE_n_of_attribs_of_type__integer_ - number of attributes of type integer appearing in all predicates declared in main WHERE 
* _WHERE_n_of_attribs_of_type__numeric_ - number of attributes of type decimal appearing in all predicates declared in main WHERE
* _WHERE_n_of_attribs_of_type__character_ - number of attributes of type string with fixed length appearing in all predicates declared in main WHERE
* _WHERE_n_of_attribs_of_type__date_ - number of attributes of type date appearing in all predicates declared in main WHERE
* _WHERE_n_of_pkey_attribs_ - number of primary key attributes appearing in all predicates declared in main WHERE
* _WHERE_n_of_connect_OR_ - number of times the connector `OR` appears in main WHERE
* _WHERE_n_of_operators__between_ - number of times the operator `BETWEEN` appears in main WHERE
* _WHERE_n_of_operators__greater_or_less_ - number of comparison operators appearing in main WHERE
* _WHERE_n_of_operators__in_ - number of times the operator `IN` appears in main WHERE
* _WHERE_n_of_operators__like_ - number of times the operator `LIKE` appears in main WHERE
* _WHERE_n_of_non_aggr_func__ABS_ - number of times the (non-aggregate) function `ABS` appears in main WHERE
* _WHERE_n_of_non_aggr_func__LOG_ - number of times function `LOG` appears in main WHERE
* _WHERE_n_of_non_aggr_func__YEAR_ - number of times function `EXTRACT YEAR FROM` appears in main WHERE
* _WHERE_n_of_non_aggr_func__FLOOR_ - number of times function `FLOOR` appears in main WHERE
* _WHERE_n_of_non_aggr_func__DOW_ - number of times function `EXTRACT DOW FROM...` appears in main WHERE
* _WHERE_n_of_non_aggr_func__SQRT_ - number of times function `SQRT` appears in main WHERE
* _WHERE_n_of_non_aggr_func__DAY_ - number of times function `EXTRACT DAY FROM...` appears in main WHERE
* _WHERE_n_of_non_aggr_func__ROUND_ - number of times function `ROUND` appears in main WHERE
* _WHERE_n_of_non_aggr_func__MONTH_ - number of times function `EXTRACT MONTH FROM...` appears in main WHERE
* _WHERE_n_of_non_aggr_func__TRUNC_ - number of times function `TRUNC` appears in main WHERE
* _WHERE_n_of_all_non_aggr_func_ - total number of non-aggregate functions appearing in the main WHERE
  
* _GROUP_BY_n_of_columns_ - number of columns appearing in the main GROUP BY clause

* _HAVING_n_of_main_predicates_ - number of predicates appearing in the HAVING clause
* _HAVING_n_of_main_predicates__non_scalar_subquery_ - number of predicates in HAVING which use as arguments one or more non-scalar subqueries
* _HAVING_n_of_main_predicates__scalar_subquery_ - number of predicates in HAVING which use as arguments one or more scalar subqueries
* _HAVING_n_of_subqueries__non_scalar_subquery_ - number of all non-scalar subqueries appearing in HAVING
* _HAVING_n_of_subqueries__scalar_subquery_ - number of all scalar subqueries appearing in HAVING

* _ORDER_BY_n_of_columns_ - number of columns appearing in the ORDER BY clause
* _offset_ - number of records to be skipped at the beginning of the query results
* _limit_ - number of records to be included in the query result
