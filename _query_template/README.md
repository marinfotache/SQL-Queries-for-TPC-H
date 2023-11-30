### Here is a typical SQL query
![PostgreSQL](https://github.com/marinfotache/SQL-Queries-for-TPC-H/blob/main/_query_template/Q2311052230000015.pdf)


### Query parameters stored in metadata (.xlsx) files
* __query_id__ - unique identifier of the query                                      
* scale_factor - the database size                                 
* scenario - see `scenarios` section                                     
* SELECT_n_of_columns - number of columns declared in SELECT (number of columns in the query result)                         
* SELECT_n_of_non_aggr_func__UPPER              <dbl> 1, 0, 1, 0, 1, 2, 0, 0, 0, 0, 0, 0, 1, 0, 0, 2, 2, 0, 1, ~
* SELECT_n_of_non_aggr_func__LOWER              <dbl> 0, 1, 0, 0, 5, 2, 0, 0, 0, 0, 1, 0, 0, 0, 0, 0, 0, 2, 0, ~
* SELECT_n_of_non_aggr_func__LTRIM              <dbl> 0, 0, 1, 0, 3, 0, 1, 0, 0, 1, 0, 1, 0, 0, 0, 2, 1, 0, 0, ~
* SELECT_n_of_non_aggr_func__SUBSTR             <dbl> 0, 0, 1, 0, 2, 1, 4, 0, 0, 1, 0, 0, 1, 0, 1, 0, 1, 0, 0, ~
* SELECT_n_of_non_aggr_func__DAY                <dbl> 0, 0, 0, 0, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 1, 1, 0, 1, 0, ~
* SELECT_n_of_non_aggr_func__LOG                <dbl> 0, 0, 0, 0, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, ~
* SELECT_n_of_non_aggr_func__MONTH              <dbl> 0, 0, 0, 0, 2, 0, 0, 0, 0, 0, 0, 0, 0, 0, 1, 1, 0, 0, 0, ~
* SELECT_n_of_non_aggr_func__RTRIM              <dbl> 0, 0, 0, 0, 2, 2, 1, 2, 3, 0, 1, 1, 0, 0, 1, 2, 0, 0, 0, ~
* SELECT_n_of_non_aggr_func__YEAR               <dbl> 0, 0, 0, 0, 1, 1, 0, 0, 0, 0, 0, 0, 0, 0, 1, 0, 0, 0, 0, ~
* SELECT_n_of_non_aggr_func__ABS                <dbl> 0, 0, 0, 0, 0, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, ~
* SELECT_n_of_non_aggr_func__SQRT               <dbl> 0, 0, 0, 0, 0, 0, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, ~
* SELECT_n_of_non_aggr_func__FLOOR              <dbl> 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 1, 0, 0, 0, 0, 0, 0, 0, 0, ~
* SELECT_n_of_non_aggr_func__ROUND              <dbl> 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 1, 0, 0, 0, 0, 0, 0, 0, ~
* SELECT_n_of_non_aggr_func__DOW                <dbl> 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 1, 0, 0, 0, ~
* SELECT_n_of_non_aggr_func__TRUNC              <dbl> 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, ~
* SELECT_n_of_all_non_aggr_func                 <dbl> 1, 1, 3, 0, 18, 9, 7, 2, 3, 2, 3, 3, 2, 0, 5, 9, 4, 3, 1,~
* SELECT_n_of_aggr_func__MIN                    <dbl> 2, 1, 0, 0, 0, 0, 0, 1, 0, 0, 0, 0, 0, 0, 0, 0, 2, 0, 0, ~
* SELECT_n_of_aggr_func__COUNT                  <dbl> 0, 0, 3, 0, 0, 0, 0, 0, 2, 0, 0, 0, 1, 0, 0, 0, 1, 0, 0, ~
* SELECT_n_of_aggr_func__AVG                    <dbl> 0, 0, 0, 0, 0, 3, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, ~
* SELECT_n_of_aggr_func__MAX                    <dbl> 0, 0, 0, 0, 0, 3, 0, 0, 0, 0, 4, 0, 0, 0, 5, 0, 0, 0, 0, ~
* SELECT_n_of_aggr_func__SUM                    <dbl> 0, 0, 0, 0, 0, 0, 0, 0, 1, 0, 0, 1, 0, 0, 0, 0, 0, 0, 0, ~
* SELECT_n_of_aggr_func__COUNT_DISTINCT         <dbl> 0, 0, 0, 0, 0, 0, 0, 0, 0, 1, 0, 3, 0, 1, 0, 8, 0, 5, 2, ~
* SELECT_n_of_all_aggr_func                     <dbl> 2, 1, 3, 0, 0, 6, 0, 1, 3, 1, 4, 4, 1, 1, 5, 8, 3, 5, 2, ~
* FROM_n_of_join_paths                          <dbl> 6, 1, 3, 4, 4, 4, 2, 6, 3, 5, 1, 3, 1, 1, 3, 6, 5, 3, 1, ~
* FROM_n_of_super_joins__FULL                   <dbl> 1, 0, 0, 1, 1, 0, 1, 1, 1, 0, 0, 1, 0, 0, 0, 2, 1, 0, 0, ~
* FROM_n_of_super_joins__LEFT                   <dbl> 2, 0, 0, 0, 0, 1, 0, 1, 0, 0, 0, 1, 0, 0, 1, 1, 1, 1, 0, ~
* FROM_n_of_super_joins__RIGHT                  <dbl> 1, 0, 0, 1, 2, 1, 0, 0, 1, 4, 0, 0, 0, 0, 1, 1, 2, 0, 0, ~
* FROM_n_of_joins__INNER                        <dbl> 6, 2, 5, 6, 1, 4, 2, 5, 2, 3, 2, 3, 2, 0, 5, 7, 2, 2, 0, ~
* FROM_n_of_joins__RIGHT                        <dbl> 4, 1, 1, 2, 5, 7, 2, 6, 2, 5, 2, 6, 0, 2, 2, 8, 5, 3, 2, ~
* FROM_n_of_processed_rows                      <dbl> 15610113018, 825000030, 6880056539, 6225028302, 615002829~
* WHERE_n_of_predicates                         <dbl> 9, 1, 5, 7, 8, 7, 2, 7, 5, 4, 6, 3, 2, 1, 0, 7, 8, 8, 3, ~
* WHERE_n_of_attribs_of_type__character_varying <dbl> 3, 0, 0, 5, 2, 2, 2, 2, 2, 2, 2, 2, 0, 0, 0, 3, 3, 2, 2, ~
* WHERE_n_of_attribs_of_type__integer           <dbl> 4, 1, 1, 1, 3, 3, 0, 3, 1, 1, 2, 0, 1, 0, 0, 3, 3, 4, 1, ~
* WHERE_n_of_attribs_of_type__numeric           <dbl> 2, 0, 3, 1, 1, 0, 0, 1, 1, 0, 1, 1, 1, 0, 0, 1, 1, 1, 0, ~
* WHERE_n_of_attribs_of_type__character         <dbl> 0, 0, 1, 0, 1, 1, 0, 1, 1, 1, 0, 0, 0, 1, 0, 0, 1, 1, 0, ~
* WHERE_n_of_attribs_of_type__date              <dbl> 0, 0, 0, 0, 1, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 0, 0, 0, 0, ~
* WHERE_n_of_pkey_attribs                       <dbl> 2, 0, 0, 0, 1, 1, 0, 1, 0, 1, 2, 0, 0, 0, 0, 3, 1, 2, 0, ~
* WHERE_n_of_connect_OR                         <dbl> 7, 0, 2, 4, 7, 5, 0, 4, 2, 2, 3, 0, 0, 0, 0, 3, 5, 5, 1, ~
* WHERE_n_of_operators__between                 <dbl> 1, 1, 1, 3, 1, 4, 1, 1, 1, 0, 1, 1, 1, 0, 0, 1, 1, 2, 1, ~
* WHERE_n_of_operators__greater_or_less         <dbl> 3, 0, 1, 0, 6, 2, 1, 1, 3, 1, 3, 0, 0, 1, 0, 5, 6, 3, 0, ~
* WHERE_n_of_operators__in                      <dbl> 2, 0, 0, 1, 0, 1, 0, 2, 1, 1, 1, 0, 0, 0, 0, 0, 0, 0, 0, ~
* WHERE_n_of_operators__like                    <dbl> 1, 0, 0, 1, 1, 0, 0, 1, 0, 2, 0, 0, 0, 0, 0, 0, 0, 2, 2, ~
* WHERE_n_of_non_aggr_func__ABS                 <dbl> 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 1, 0, 0, ~
* WHERE_n_of_non_aggr_func__LOG                 <dbl> 2, 0, 0, 0, 0, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 1, 0, 0, 0, ~
* WHERE_n_of_non_aggr_func__YEAR                <dbl> 0, 0, 0, 0, 1, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, ~
* WHERE_n_of_non_aggr_func__FLOOR               <dbl> 0, 0, 0, 0, 0, 0, 0, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, ~
* WHERE_n_of_non_aggr_func__DOW                 <dbl> 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 1, 0, 0, 0, 0, 0, 0, 0, 0, ~
* WHERE_n_of_non_aggr_func__SQRT                <dbl> 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 1, 0, 0, 0, 0, 0, 1, 0, ~
* WHERE_n_of_non_aggr_func__DAY                 <dbl> 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, ~
* WHERE_n_of_non_aggr_func__ROUND               <dbl> 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, ~
* WHERE_n_of_non_aggr_func__MONTH               <dbl> 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, ~
* WHERE_n_of_non_aggr_func__TRUNC               <dbl> 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, ~
* WHERE_n_of_all_non_aggr_func                  <dbl> 3, 0, 0, 0, 1, 2, 0, 1, 0, 0, 1, 1, 0, 0, 0, 1, 1, 1, 0, ~
* GROUP_BY_n_of_columns                         <dbl> 5, 4, 6, 0, 0, 9, 0, 5, 2, 7, 1, 3, 1, 1, 3, 6, 3, 2, 1, ~
* HAVING_n_of_main_predicates                   <dbl> 1, 1, 3, 0, 0, 3, 0, 0, 2, 3, 2, 0, 3, 2, 1, 2, 2, 1, 1, ~
* ORDER_BY_n_of_columns                         <dbl> 1, 2, 0, 0, 0, 2, 1, 1, 1, 2, 1, 2, 1, 1, 1, 3, 1, 1, 1, ~
* limit                                         <dbl> 328, 983, 400, 541, 153, 89, 462, 967, 443, 57, 734, 207,~
* offset                                        <dbl> 0, 558, 561, 198, 0, 0, 0, 94, 826, 0, 0, 0, 378, 0, 45, ~
