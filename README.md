## SQL-Queries-for-TPC-H
Public Repository containing SQL Queries for the TPC-H Benchmark.<br><br>

### Files containing the SQL query text and their metadata
For a given scenario and scale factor, packs of 1000 queries are generated as `.csv` files ready to be executed with jMeter (for automatically collecting the query completion/success and the query duration) in PostgreSQL, Oracle, or Microsoft SQL Server.<br>
Separated files (`.xlsx`) provide the query's metadata (e.g., number of joins, predicates in WHERE, GROUP BY attributes, etc.) for more granular analyses of query performance (e.g., assessing the association between query completion or query duration and the query parameters in various physical setups).

### Supported SQL dialects
Currently: PostgreSQL, Oracle, and MS-SQL Server (.csv files prepared for jMeter). <br>
In progress: Apache Spark (separate text file for each query).

### Database size (scale factors)
Each query set (in a .csv file) contains 1000 queries for one of the following scale factors: 0.01GB, 1GB, 2GB, 5GB, 10GB, 50GB, 100GB, 200GB, 1000GB, 2000GB 

### Query structure and parameters
For the query structure and the main vocabulary (used for defining the scenarios for query generation), see section [_query_template_and_parameters](https://github.com/marinfotache/SQL-Queries-for-TPC-H/tree/main/_query_template_and_parameters)

### Main scenarios for query generation
Each query set is generated following a specific scenario which basically controls the query complexity.<br>
For details, see section [_scenarios_for_query_generation](https://github.com/marinfotache/SQL-Queries-for-TPC-H/tree/main/_scenarios_for_query_generation)

### Resources:
  * [TPC-H Benchmark specification:](https://www.tpc.org/TPC_Documents_Current_Versions/pdf/TPC-H_v3.0.1.pdf)
  * [jMeter home page:](https://jmeter.apache.org)

  
### Other papers using the previous and the current versions of the query generator:
    -
    -
    -

### Acknowledgement:
Physical resources for deploying the query generator of this repository were provided by the Competitiveness Operational Program Romania, under project SMIS 124759 - RaaS-IS (Research as a Service Iasi).
  
