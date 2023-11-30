### Here is a typical SQL query
![PostgreSQL](https://github.com/marinfotache/SQL-Queries-for-TPC-H/blob/main/_query_template/Q2311052230000015.pdf)


### Query parameters stored in the metadata (.xlsx) files
* _query_id_ - unique identifier of the query                                      
* _scale_factor_ - the database size                                 
* _scenario_ - see `scenarios` section                                     
* _SELECT_n_of_columns_ - number of columns declared in main SELECT (number of columns in the query result)                         
* _SELECT_n_of_non_aggr_func__UPPER_ - number of times function `UPPER` appears in the main SELECT clause               
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
* _SELECT_n_of_non_aggr_func__DOW_ - number of times function `DOW` (Day of the Wook) appears in main SELECT   
* _SELECT_n_of_non_aggr_func__TRUNC_ - number of times function `TRUNC` appears in main SELECT   
* _SELECT_n_of_all_non_aggr_func_ - number of all non-aggregate functions (from `UPPER` to `TRUNC`) appearing in main SELECT   
* _SELECT_n_of_aggr_func__MIN_ - number of times function UPPER appears in main SELECT   
* _SELECT_n_of_aggr_func__COUNT_ - number of times function UPPER appears in main SELECT   
* _SELECT_n_of_aggr_func__AVG_ - number of times function UPPER appears in main SELECT   
* _SELECT_n_of_aggr_func__MAX_ - number of times function UPPER appears in main SELECT   
* _SELECT_n_of_aggr_func__SUM_  - number of times function UPPER appears in main SELECT    
* _SELECT_n_of_aggr_func__COUNT_DISTINCT_ - number of times function UPPER appears in main SELECT   
* _SELECT_n_of_all_aggr_func_ - number of times function UPPER appears in main SELECT   
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
