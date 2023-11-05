## SQL-Queries-for-TPC-H
Public Repository containing SQL Queries for the TPC-H Benchmark.

### Files Containing the SQL Queries and the metadata
Packs of 1000 queries are generated as `.csv` files ready to be executed with jMeter (for automatically collecting the query completion/success and the query duration.<br>
Separated files (`.xlsx`) provide the query's metadata (e.g., number of joins, of predicates, of grouping attributes, etc.)

### Supported SQL dialects
Currently: PostgreSQL, Oracle, and MS-SQL Server (.csv files prepared for jMeter). <br>
In progress: Apache Spark (each individual query generated as a text file).

### Database Size (Scale Factors)
Each query set (in a .csv file) contains 1000 queries for one of the following scale factors: 0.01GB, 1GB, 2GB, 5GB, 10GB, 50GB, 100GB, 200GB, 1000GB, 2000GB 

### Vocabulary
For query structure and main vocabulary, see `_query_template` section

### Main scenarios for query generation


### Resources:

* TPC-H Benchmark home page:
* 
* Other papers using the previous and the current versions of the query generator:
  -
  -
  -
  
